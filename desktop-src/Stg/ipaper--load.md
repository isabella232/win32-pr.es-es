---
title: Carga de IPaper
description: En el código de ejemplo de C++ siguiente se muestra cómo abrir la secuencia existente en el almacenamiento, leer nuevas propiedades de papel en y, a continuación, establecerlas como los valores actuales de las copapers.
ms.assetid: a1559d97-387f-4d1a-8a9d-fa5c27abd545
keywords:
- Carga de IPaper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b5f16b8fe649d08226b2cff5a4b1a5234bddb6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994464"
---
# <a name="ipaperload"></a>IPaper:: Load

En el código de ejemplo de C++ siguiente se muestra cómo abrir la secuencia existente en el almacenamiento, leer nuevas propiedades de papel en y, a continuación, establecerlas como los valores actuales de las copapers.

A continuación se explica el método **IPaper:: Load** de Paper. cpp.


```
STDMETHODIMP COPaper::CImpIPaper::Load(
                 SHORT nLockKey,
                 IStorage* pIStorage)
  {
    HRESULT hr = E_FAIL;
    IStream* pIStream;
    INKDATA* paInkData;
    ULONG ulToRead, ulReadIn;
    LONG lNewArraySize;
    PAPER_PROPERTIES NewProps;

    if (OwnThis())
    {
      if (m_bLocked && m_cLockKey == nLockKey && NULL != pIStorage)
      {
       // Open the "PAPERDATA" stream where the paper data is stored.
        hr = pIStorage->OpenStream(
               STREAM_PAPERDATA_USTR,
               0,
               STGM_READ | STGM_DIRECT | STGM_SHARE_EXCLUSIVE,
               0,
               &pIStream);
        if (SUCCEEDED(hr))
        {
          // Obtained paper data stream. Read the Paper Properties.
          ulToRead = sizeof(PAPER_PROPERTIES);
          hr = pIStream->Read(
                           &NewProps,
                           ulToRead,
                           &ulReadIn);
          if (SUCCEEDED(hr) && ulToRead != ulReadIn)
            hr = E_FAIL;
          if (SUCCEEDED(hr))
          {
            // Handle the different versions of ink data format.
            switch (NewProps.lInkDataVersion)
            {
              case INKDATA_VERSION10:
                // Allocate an ample-sized ink data array.
                lNewArraySize = NewProps.lInkArraySize + 
                                               INKDATA_ALLOC;
                paInkData = new INKDATA[(LONG) lNewArraySize];
                if (NULL != paInkData)
                {
                  // Delete the old ink data array.
                  delete [] m_paInkData;

                  // Assign the new array.
                  m_paInkData = paInkData;
                  m_lInkDataMax = lNewArraySize;

                  // Read the complete array of Ink Data.
                  ulToRead = NewProps.lInkArraySize * sizeof(INKDATA);
                  hr = pIStream->Read(m_paInkData, 
                                      ulToRead, &ulReadIn);
                  if (SUCCEEDED(hr) && ulToRead != ulReadIn)
                    hr = E_FAIL;
                  if (SUCCEEDED(hr))
                  {
                    // Set COPaper to use the new PAPER_PROPERTIES
                    // data.
                    m_lInkDataEnd = NewProps.lInkArraySize-1;
                    m_crWinColor = NewProps.crWinColor;
                    m_WinRect.right = NewProps.WinRect.right;
                    m_WinRect.bottom = NewProps.WinRect.bottom;

                    // Copy the new properties into current 
                    // properties.
                    memcpy(
                      &m_PaperProperties,
                      &NewProps,
                      sizeof(PAPER_PROPERTIES));
                  }
                }
                else
                  hr = E_OUTOFMEMORY;
                break;
              default:
                hr = E_FAIL;  // Bad version.
                break;
            }
          }

          // Release the stream.
          pIStream->Release();
        }
      }

      UnOwnThis();
    }

    // Notify other connected clients that Paper is now loaded.
    // If Paper not loaded, then erase to a safe, empty ink data 
    // array.
    if (SUCCEEDED(hr))
      m_pBackObj->NotifySinks(PAPER_EVENT_LOADED, 0, 0, 0, 0);
    else
      Erase(nLockKey);

    return hr;
  }
```



Ahora, se llama al método [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) para abrir la secuencia existente en el almacenamiento llamado "PAPERDATA". Las marcas de modo de acceso son para el acceso exclusivo de solo lectura, directo y no compartido. Cuando la secuencia está abierta, se llama al método [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) para leer la \_ estructura de las propiedades del papel. Si la cantidad realmente leída no es igual a la cantidad solicitada, se anula la operación de carga y \_ se devuelve e Fail. Si no se reconoce la versión de formato en las propiedades del papel que se acaba de leer \_ , la operación de carga se anula y la **carga** devuelve e \_ produce un error.

Con una versión de formato de datos de entrada de lápiz válida, el tamaño de la nueva matriz de datos de tinta de las propiedades de papel \_ leídas en se utiliza para asignar una nueva matriz de datos de tinta del tamaño requerido. Los datos de tinta existentes se eliminan y sus datos se pierden. Si estos datos eran valiosos, se deberían haber guardado antes de llamar a **Load** . Una vez asignada la nueva matriz, [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) se llama de nuevo para leer los datos en la matriz desde el flujo. Si la llamada se realiza correctamente, los valores de las propiedades del papel de lectura reciente se adoptan como los valores actuales para el copaper.

Durante esta operación de carga, \_ se usó una estructura de propiedades de papel temporal, NewProps, para contener las nuevas propiedades leídas en. Si todo se realiza correctamente con la carga, NewProps se copia en la \_ estructura de propiedades del papel, m \_ PaperProperties. Como antes, una vez finalizada la carga y la [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) ya no es necesaria, se libera el puntero **IStream** .

Si se produce un error al final de la **carga**, se borra la matriz de datos de tinta, ya que puede contener datos dañados.

Si no hay ningún error al final de la **carga**, se llama al método [**IPaperSink:: Loaded**](ipapersink-methods.md) del cliente, en el método NotifySinks interno copaper, para notificar al cliente que se ha completado la operación de carga. Se trata de una notificación importante para el cliente, ya que debe mostrar estos nuevos datos de tinta cargados. Esta notificación hace un uso significativo de las características de los objetos conectables en copapers.

 

 





---
title: Carga de IPaper
description: El siguiente código de ejemplo de C++ muestra cómo abrir la secuencia existente en el almacenamiento, leer nuevas propiedades de papel en y, a continuación, establecerlas como los valores actuales de COPaper.
ms.assetid: a1559d97-387f-4d1a-8a9d-fa5c27abd545
keywords:
- Carga de IPaper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b592573f016018d359b5e3e35911d92371892b98ebea70338844b7f8ef4b1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961385"
---
# <a name="ipaperload"></a>IPaper::Load

El siguiente código de ejemplo de C++ muestra cómo abrir la secuencia existente en el almacenamiento, leer nuevas propiedades de papel en y, a continuación, establecerlas como los valores actuales de COPaper.

A continuación se muestra **el método IPaper::Load** de Paper.cpp.


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



Ahora, se [**llama al método IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) para abrir la secuencia existente en el almacenamiento denominada "PAPERDATA". Las marcas de modo de acceso son para acceso exclusivo de solo lectura, directo y no compartido. Cuando la secuencia está abierta, se llama al [**método IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) para leer la estructura PAPER \_ PROPERTIES. Si la cantidad leida realmente no es igual a la cantidad solicitada, se anula la operación de carga y se devuelve E \_ FAIL. Si no se reconoce la versión de formato de LAS PROPIEDADES DE PAPEL recién leídas, se anula la operación de carga y \_ **Load** devuelve E \_ FAIL.

Con una versión de formato de datos de entrada de lápiz válida, el tamaño de la nueva matriz de datos ink de LAS PROPIEDADES DE PAPEL que se leyó en se usa para asignar una nueva matriz de datos de entrada de lápiz del \_ tamaño necesario. Los datos de entrada de lápiz existentes se eliminan y se pierden sus datos. Si estos datos son valiosos, se deberían haber guardado antes de **llamar a** Load. Una vez asignada la nueva matriz, se llama de nuevo a [**IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) para leer los datos en la matriz desde la secuencia. Si esta llamada se realiza correctamente, los valores de las propiedades de papel recién leídas se adoptan como los valores actuales de COPaper.

Durante esta operación de carga, se usó una estructura temporal PAPER \_ PROPERTIES, NewProps, para contener las nuevas propiedades leídas. Si todo se realiza correctamente con la carga, NewProps se copia en la estructura PAPER \_ PROPERTIES, m \_ PaperProperties. Como antes, después de realizar la carga y de que [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) ya no sea necesario, se libera el puntero **IStream.**

Si se produce un error al final de **Cargar**, se borra la matriz de datos ink, ya que puede contener datos dañados.

Si no hay ningún error al final de **Load**, se llama al método [**IPaperSink::Loaded**](ipapersink-methods.md) del cliente, en el método NotifySinks interno de COPaper, para notificar al cliente que se ha completado la operación de carga. Se trata de una notificación importante para el cliente, ya que debe mostrar estos nuevos datos de entrada de lápiz cargados. Esta notificación hace un uso significativo de las características de objetos conectables en COPaper.

 

 





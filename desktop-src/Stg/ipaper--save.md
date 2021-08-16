---
title: IPaper Save
description: El enfoque principal en este código de ejemplo es cómo COPaper puede cargar y guardar sus datos de papel en archivos compuestos. Las implementaciones del método IPaper, Load y Save se de abordan con detalle.
ms.assetid: 62154658-ff47-425f-94da-ee2806de5318
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52772002fe8f0ed234a4f430eaff4328f96f9d1ef151e83da3f4aa3e255dba09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961375"
---
# <a name="ipapersave"></a>IPaper::Save

El enfoque principal en este código de ejemplo es cómo COPaper puede cargar y guardar sus datos de papel en archivos compuestos. Las implementaciones de los métodos [**IPaper,**](ipaper-methods.md) [**Load**](ipaper--load.md)y **Save** se analizan en detalle.

A continuación se muestra **el método IPaper::Save** de Paper.cpp.


```C++
STDMETHODIMP COPaper::CImpIPaper::Save(
                 SHORT nLockKey,
                 IStorage* pIStorage)
  {
    HRESULT hr = E_FAIL;
    IStream* pIStream;
    ULONG ulToWrite, ulWritten;

    if (OwnThis())
    {
      if (m_bLocked && m_cLockKey == nLockKey && NULL != pIStorage)
      {
        // Use the COM service to mark this compound file as one 
        // that is handled by our server component, DllPaper.
        WriteClassStg(pIStorage, CLSID_DllPaper);

        // Use the COM Service to write user-readable clipboard 
        // format into the compound file.
        WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, 
                            TEXT(CLIPBDFMT_STR));

        // Create the stream to be used for the actual paper data.
        // Call it "PAPERDATA".
        hr = pIStorage->CreateStream(
               STREAM_PAPERDATA_USTR,
        STGM_CREATE | STGM_WRITE | STGM_DIRECT | STGM_SHARE_EXCLUSIVE,
               0,
               0,
               &pIStream);
        if (SUCCEEDED(hr))
        {
          // Obtained a stream. Write data to it.
          // First, write PAPER_PROPERTIES structure.
          m_PaperProperties.lInkArraySize = m_lInkDataEnd+1;
          m_PaperProperties.crWinColor = m_crWinColor;
          m_PaperProperties.WinRect.right = m_WinRect.right;
          m_PaperProperties.WinRect.bottom = m_WinRect.bottom;
          ulToWrite = sizeof(PAPER_PROPERTIES);
          hr = pIStream->Write(&m_Paper_Properties, ulToWrite, 
                               &ulWritten);
          if (SUCCEEDED(hr) && ulToWrite != ulWritten)
            hr = STG_E_CANTSAVE;
          if (SUCCEEDED(hr))
          {
            // Now, write the complete array of Ink Data.
            ulToWrite = m_PaperProperties.lInkArraySize * 
                                                     sizeof(INKDATA);
            hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
            if (SUCCEEDED(hr) && ulToWrite != ulWritten)
              hr = STG_E_CANTSAVE;
          }

          // Release the stream.
          pIStream->Release();
        }
      }

      UnOwnThis();
    }

    // Notify all other connected clients that Paper is now saved.
    if (SUCCEEDED(hr))
      m_pBackObj->NotifySinks(PAPER_EVENT_SAVED, 0, 0, 0, 0);

    return hr;
  }
```



En esta relación de cliente y servidor, COPaper no crea el archivo compuesto que se usa para almacenar datos de papel. Para los **métodos Save** [**y Load,**](ipaper--load.md) el cliente pasa un puntero de [**interfaz IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para un archivo compuesto existente. A continuación, usa **IStorage** para escribir y leer datos en ese archivo compuesto. En **IPaper::Save** anterior, se almacenan varios tipos de datos.

CLSID para DllPaper, CLSID DllPaper, se serializa y almacena en una secuencia especial controlada por COM dentro del objeto de almacenamiento denominado \_ \\ "001CompObj". La [**función de servicio WriteClassStg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) realiza este almacenamiento. Estos datos CLSID almacenados se pueden usar para asociar el contenido de almacenamiento con el componente DllPaper que creó y puede interpretarlo. En este ejemplo, **StoClien** pasa el almacenamiento raíz y, por tanto, todo el archivo compuesto está asociado al componente DllPaper. Estos datos CLSID se pueden recuperar más adelante con una llamada a la función [**de servicio ReadClassStg.**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg)

Dado que DllPaper trata con datos editables, también es adecuado registrar un formato del Portapapeles en el almacenamiento. Se llama a la función de servicio [**WriteFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) para almacenar una designación de formato del Portapapeles y un nombre legible por el usuario para el formato. El nombre legible por el usuario está pensado para mostrar la GUI en las listas de selección. El nombre pasado anteriormente usa una macro, CLIPBDFMT STR, que se define como \_ "DllPaper 1.0" en Paper.h. Estos datos almacenados del Portapapeles se pueden recuperar más adelante con una llamada a la función de servicio [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg). Esta función devuelve un valor de cadena que se asigna mediante el asignador de memoria de tareas. El autor de la llamada es responsable de liberar la cadena.

**Guardar** a continuación crea una secuencia en el almacenamiento para los datos de papel de COPaper. La secuencia se denomina "PAPERDATA" y se pasa mediante la macro STREAM \_ PAPERDATA \_ USTR. El [**método IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) requiere que esta cadena esté en Unicode. Dado que la cadena se fija en tiempo de compilación, la macro se define como Unicode en Paper.h.

``` syntax
#define STREAM_PAPERDATA_USTR L"PAPERDATA"
```

La "L" anterior a la cadena, que indica LONG, lo consigue.

El [**método CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) crea y abre una secuencia dentro del almacenamiento especificado. Se pasa un puntero de interfaz [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) para la nueva secuencia en una variable de puntero de interfaz de llamador. Se llama a AddRef en este puntero de interfaz dentro **de CreateStream** y el autor de la llamada debe liberar este puntero después de usarlo. Al **método CreateStream** se le pasan numerosas marcas de modo de acceso, como se muestra a continuación.

STGM \_ CREATE \| STGM \_ WRITE \| STGM \_ DIRECT \| STGM \_ SHARE \_ EXCLUSIVE

[**STGM \_ CREATE**](stgm-constants.md) crea una nueva secuencia o sobrescribe una existente con el mismo nombre. [**STGM \_ WRITE**](stgm-constants.md) abre la secuencia con permiso de escritura. [**STGM \_ DIRECT**](stgm-constants.md) abre la secuencia para el acceso directo, en lugar del acceso con transacciones. [**STGM \_ SHARE \_ EXCLUSIVE**](stgm-constants.md) abre el archivo para su uso exclusivo y no compartido por parte del autor de la llamada.

Una vez creada correctamente la secuencia PAPERDATA, se usa la [**interfaz IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) para escribir en la secuencia. El **método IStream::Write** se usa para almacenar primero el contenido de la estructura PAPER \_ PROPERTIES. Se trata básicamente de un encabezado de propiedades al frente de la secuencia. Dado que el número de versión es lo primero del archivo, se puede leer de forma independiente para determinar cómo tratar los datos siguientes. Si la cantidad de datos escritos realmente no es igual a la cantidad solicitada, se anula el método Save y devuelve STG \_ E \_ CANTSAVE.

Guardar toda la matriz de datos de entrada de lápiz en la secuencia es sencillo.


```C++
// Now write the complete array of Ink Data.
  ulToWrite = m_PaperProperties.lInkArraySize * sizeof(INKDATA);
  hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
  if (SUCCEEDED(hr) && ulToWrite != ulWritten)
    hr = STG_E_CANTSAVE;
```



Dado que [**el método IStream::Write**](/windows/desktop/api/Objidl/nn-objidl-istream) funciona en una matriz de bytes, se calcula el número de bytes de datos de entrada de lápiz almacenados en la matriz y la operación de escritura comienza al principio de la matriz. Si la cantidad de datos escritos realmente no es igual a la cantidad solicitada, el **método Save** devuelve STG \_ E \_ CANTSAVE.

Una vez escrita la secuencia, el **método IPaper::Save** libera el [**puntero IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) que estaba usando.

El **método Save** también llama al cliente [**IPaperSink**](ipapersink-methods.md) (en el método NotifySinks interno de COPaper) para notificar al cliente que la operación de guardado se ha completado. En este momento, **el método Save** vuelve al cliente que realiza la llamada, que normalmente liberará el puntero [**IStorage.**](/windows/desktop/api/Objidl/nn-objidl-istorage)

 

 





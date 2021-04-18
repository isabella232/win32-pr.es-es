---
title: IPaper guardar
description: El foco principal en este código de ejemplo es cómo puede cargar el copaper y guardar sus datos de papel en archivos compuestos. Las implementaciones de los métodos IPaper, Load y Save se describen en detalle.
ms.assetid: 62154658-ff47-425f-94da-ee2806de5318
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ea49f194e64ab3f0cfd78569b1e6ff9ddee577
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665713"
---
# <a name="ipapersave"></a>IPaper:: Save

El foco principal en este código de ejemplo es cómo puede cargar el copaper y guardar sus datos de papel en archivos compuestos. Las implementaciones de los métodos [**IPaper**](ipaper-methods.md), [**Load**](ipaper--load.md)y **Save** se describen en detalle.

A continuación se explica el método **IPaper:: Save** de Paper. cpp.


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



En esta relación entre cliente y servidor, el copaper no crea el archivo compuesto que se usa para almacenar los datos del papel. En el caso de los métodos **Save** y [**Load**](ipaper--load.md) , el cliente pasa un puntero de interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para un archivo compuesto existente. A continuación, usa el **IStorage** para escribir y leer datos en ese archivo compuesto. En **IPaper:: Save** anterior, se almacenan varios tipos de datos.

El CLSID de DllPaper, CLSID \_ DllPaper, se serializa y se almacena en un flujo especial controlado por com en el objeto de almacenamiento llamado " \\ 001CompObj". La función de servicio [**WriteClassStg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) realiza este almacenamiento. Estos datos de CLSID almacenados se pueden usar para asociar el contenido de almacenamiento al componente DllPaper que creó y puede interpretarlo. En este ejemplo, **StoClien** pasa el almacenamiento raíz y, por tanto, el archivo compuesto completo está asociado al componente DllPaper. Estos datos CLSID se pueden recuperar más adelante con una llamada a la función de servicio [**ReadClassStg**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) .

Dado que DllPaper se encarga de los datos editables, también es adecuado registrar un formato de Portapapeles en el almacenamiento. Se llama a la función de servicio [**WriteFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) para almacenar una designación de formato del portapapeles y un nombre legible por el usuario para el formato. El nombre legible para el usuario está pensado para la visualización de GUI en listas de selección. El nombre pasado usa una macro, CLIPBDFMT \_ Str, que se define como "DllPaper 1,0" en Paper. h. Estos datos almacenados del portapapeles se pueden recuperar más adelante con una llamada a la función de servicio [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg). Esta función devuelve un valor de cadena que se asigna mediante el asignador de memoria de la tarea. El autor de la llamada es responsable de liberar la cadena.

**Guardar** siguiente crea una secuencia en el almacenamiento para los datos de papel de los papeles. La secuencia se denomina "PAPERDATA" y se pasa mediante la \_ macro Stream PAPERDATA \_ USTR. El método [**IStorage:: CreateStream (**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) requiere que esta cadena esté en Unicode. Dado que la cadena se fija en tiempo de compilación, la macro se define como Unicode en Paper. h.

``` syntax
#define STREAM_PAPERDATA_USTR L"PAPERDATA"
```

La ' L ' antes de la cadena, que indica LONG, logra esto.

El método [**CreateStream (**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) crea y abre una secuencia dentro del almacenamiento especificado. Un puntero de interfaz [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) para la nueva secuencia se pasa en una variable de puntero de interfaz de autor de llamada. Se llama a AddRef en este puntero de interfaz dentro de **CreateStream (** y el llamador debe liberar este puntero después de usarlo. El método **CreateStream (** recibe varias marcas de modo de acceso, como se indica a continuación.

STGM \_ Create \| STGM \_ Write \| STGM \_ Direct \| STGM \_ share \_

[**STGM \_ CREAR**](stgm-constants.md) crea una nueva secuencia o sobrescribe una existente del mismo nombre. [**STGM \_ ESCRIBIR**](stgm-constants.md) abre el flujo con permiso de escritura. [**STGM \_ DIRECT**](stgm-constants.md) abre la secuencia para el acceso directo, en lugar del acceso con transacciones. [**STGM \_ Recurso compartido \_ exclusivo**](stgm-constants.md) abre el archivo para uso exclusivo y no compartido por parte del autor de la llamada.

Una vez creada correctamente la secuencia PAPERDATA, se usa la interfaz [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) para escribir en la secuencia. El método **IStream:: Write** se usa para almacenar primero el contenido de la estructura de propiedades del papel \_ . Es esencialmente un encabezado de propiedades al principio de la secuencia. Dado que el número de versión es lo primero en el archivo, se puede leer de forma independiente para determinar cómo tratar los datos que se indican a continuación. Si la cantidad de datos escritos realmente no es igual a la cantidad solicitada, se anula el método Save y se devuelve STG \_ E \_ CANTSAVE.

Guardar toda la matriz de datos de entrada de lápiz en el flujo es sencillo.


```C++
// Now write the complete array of Ink Data.
  ulToWrite = m_PaperProperties.lInkArraySize * sizeof(INKDATA);
  hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
  if (SUCCEEDED(hr) && ulToWrite != ulWritten)
    hr = STG_E_CANTSAVE;
```



Dado que el método [**IStream:: Write**](/windows/desktop/api/Objidl/nn-objidl-istream) funciona en una matriz de bytes, se calcula el número de bytes de los datos de tinta almacenados en la matriz y la operación de escritura comienza en el inicio de la matriz. Si la cantidad de datos escritos realmente no es igual a la cantidad solicitada, el método **Save** devuelve STG \_ E \_ CANTSAVE.

Una vez escrita la secuencia, el método **IPaper:: Save** libera el puntero [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) que estaba usando.

El método **Save** también llama al cliente [**IPaperSink**](ipapersink-methods.md) (en el método NotifySinks interno de copaper) para notificar al cliente que se ha completado la operación de guardar. En este momento, el método **Save** vuelve al cliente que realiza la llamada, que normalmente liberará el puntero [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .

 

 





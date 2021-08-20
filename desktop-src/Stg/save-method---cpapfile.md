---
title: 'Método Save: CPapFile'
description: Cuando se inicializa CPapFile, se puede usar para guardar los datos de dibujo actuales que se mantienen en el objeto COPaper.
ms.assetid: ceac32e5-7d47-480b-b1cd-5a17ac04dd0c
keywords:
- 'Método Save: CPapFile'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b465d5b275949b3cdfcea04a5023cd110a8600c59a706d2c2f1515e4225c757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960602"
---
# <a name="save-method---cpapfile"></a>Método Save: CPapFile

Cuando **se inicializa CPapFile,** se puede usar para guardar los datos de dibujo actuales que se mantienen en el objeto COPaper.

## <a name="save-method-papfilecpp"></a>Método Save (PAPFILE. CPP)

Este ejemplo es el **método CPapFile** [**Save**](ipaper--save.md) de Papfile.cpp.


```C++
HRESULT CPapFile::Save(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If a null file name is passed, then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Use the COM service to reopen, or create, the compound file.
    hr = StgCreateDocfile(
        pszFile,
    STGM_CREATE | STGM_DIRECT | STGM_READWRITE | STGM_SHARE_EXCLUSIVE,
        0,
        &m_pIStorage);
    if (SUCCEEDED(hr))
    {
      // Obtained the IStorage. The compound file is open.
      // Instruct the COPaper object on the server side to save its
      // paper data into the compound file using the IStorage of our
      // client-provided compound file.
      hr = m_pIPaper->Save(nLockKey, m_pIStorage);
      if (SUCCEEDED(hr))
      {
        // The paper data was saved and obtained a new current 
        // compound file name. Copy it for later use in saves 
        // and loads.
        if (bNewFile)
          StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
      }

      // Storage complete. Do not hold the file open.
      // Re-obtain the IStorage again later (and thus re-open
      // the compound file) when required for another save or load.
      RELEASE_INTERFACE(m_pIStorage);
    }

    return (hr);
  }
  
```



Si se pasa **NULL** para el *parámetro pszFileName,* se usa el contenido almacenado del miembro **m \_ szCurFileName** para el nombre de archivo. *nLockKey es* la clave de bloqueo de cliente obtenida en una llamada anterior al método COPaper [**Lock**](ipaper-methods.md) en la **interfaz IPaper.**

Se llama a la función de servicio [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) estándar com para crear el archivo compuesto en el que se guardarán los datos de dibujo.

El nombre del archivo compuesto que se va a crear se pasa como primer parámetro. [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) lo espera como una cadena Unicode. Cuando Se compila **StoClien** para cadenas ANSI (UNICODE no está definido, que es el valor predeterminado en el archivo make), esta llamada se reduce realmente a una llamada a una función APPUTIL interna, **\_ A StgCreateDocfile**. Esta función realiza la conversión adecuada del parámetro ANSI pszFile en una versión Unicode antes de llamar a **StgCreateDocfile**. Para obtener más información, vea Apputil.h y Stoserve.htm.

Las marcas de modo de acceso se pasan como segundo parámetro y determinan qué modos de acceso se permiten en el nuevo archivo. La marca de modo de acceso [ \_ STGM CREATE](stgm-constants.md) crea un nuevo archivo compuesto o sobrescribe uno existente con el mismo nombre. [STGM \_ READWRITE](stgm-constants.md) abre el archivo con permiso de lectura y escritura. [STGM \_ DIRECT](stgm-constants.md) abre el archivo para el acceso directo, en lugar del acceso con transacciones. [STGM \_ SHARE \_ EXCLUSIVE](stgm-constants.md) abre el archivo para que el autor de la llamada lo use de forma exclusiva y no compartida.

El tercer parámetro está reservado y debe ser cero.

La dirección de la variable de **puntero m \_ pIStorage** se pasa a [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) como cuarto parámetro. Cuando la llamada se devuelve correctamente, **m \_ pIStorage contiene** un puntero de interfaz a una interfaz [**IStorage.**](/windows/desktop/api/Objidl/nn-objidl-istorage) Esta es la interfaz que se usa para las operaciones posteriores en el archivo.

En este caso, la operación importante es hacer que el objeto COPaper almacene sus datos de dibujo en el archivo. Esto se hace anteriormente mediante [**el método Save**](ipaper--save.md) de la interfaz COPaper [**IPaper.**](ipaper-methods.md) Si COPaper guarda correctamente sus datos en el objeto de almacenamiento proporcionado, el nombre del archivo compuesto se copia en **m \_ szCurFileName** como el nuevo nombre de archivo actual.

 

 





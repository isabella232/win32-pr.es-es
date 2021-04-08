---
title: 'Método Save: CPapFile'
description: Cuando se inicializa CPapFile, se puede usar para guardar los datos de dibujo actuales contenidos en el objeto de copaper.
ms.assetid: ceac32e5-7d47-480b-b1cd-5a17ac04dd0c
keywords:
- 'Método Save: CPapFile'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3166b649f28cb1a8ddc37e9efc53465a6cb5d3e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994606"
---
# <a name="save-method---cpapfile"></a>Método Save: CPapFile

Cuando se inicializa **CPapFile** , se puede usar para guardar los datos de dibujo actuales contenidos en el objeto de copaper.

## <a name="save-method-papfilecpp"></a>Método Save (PAPFILE. CPP

Este ejemplo es el método  [**Save**](ipaper--save.md) de **CPapFile** de Papfile. cpp.


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



Si se pasa **null** para el parámetro *pszFileName* , se usa el contenido almacenado del miembro **m \_ szCurFileName** para el nombre de archivo. *NLockKey* es la clave de bloqueo de cliente obtenida en una llamada anterior al método de [**bloqueo**](ipaper-methods.md) de copapeles en la interfaz **IPaper** .

Se llama a la función de servicio [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) estándar com para crear el archivo compuesto en el que se guardarán los datos del dibujo.

El nombre del archivo compuesto que se va a crear se pasa como primer parámetro. Esto lo espera [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) como una cadena Unicode. Cuando se compila **StoClien** para cadenas ANSI (no se define Unicode, que es el valor predeterminado en el archivo make), esta llamada se reduce realmente a una llamada a una función APPUTIL interna, **\_ StgCreateDocfile**. Esta función realiza la conversión adecuada del parámetro pszFile de ANSI a una versión de Unicode antes de llamar a **StgCreateDocfile**. Para obtener más información, vea apputil. h y Stoserve.htm.

Las marcas de modo de acceso se pasan como el segundo parámetro y determinan qué modos de acceso se permiten en el nuevo archivo. La marca [STGM \_ Create](stgm-constants.md) Access Mode crea un nuevo archivo compuesto o sobrescribe uno existente del mismo nombre. [STGM \_ READWRITE](stgm-constants.md) abre el archivo con permiso de lectura y escritura. [STGM \_ DIRECT](stgm-constants.md) abre el archivo para el acceso directo, en lugar del acceso con transacciones. [STGM \_ Recurso compartido \_ exclusivo](stgm-constants.md) abre el archivo para uso exclusivo y no compartido por parte del autor de la llamada.

El tercer parámetro está reservado y debe ser cero.

La dirección de la variable de puntero **m \_ pIStorage** se pasa a [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) como el cuarto parámetro. Cuando la llamada devuelve correctamente, **m \_ pIStorage** contiene un puntero de interfaz a una interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Esta es la interfaz que se utiliza para las operaciones posteriores en el archivo.

La operación importante en este caso es que el objeto de copapeles almacene sus datos de dibujo en el archivo. Para ello, use el método [**Save**](ipaper--save.md) de la interfaz [**IPaper**](ipaper-methods.md) de copaper. Si el copapel es correcto al guardar sus datos en el objeto de almacenamiento proporcionado, el nombre del archivo compuesto se copia en **m \_ szCurFileName** como el nuevo nombre de archivo actual.

 

 





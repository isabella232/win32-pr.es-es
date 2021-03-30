---
title: 'Método de carga: CPapFile'
description: Cuando estas operaciones se realizan correctamente, se libera la interfaz IStorage obtenida. Esto cierra el archivo e indica que el archivo no se mantiene abierto durante otras operaciones de cliente. Se volverá a abrir cuando sea necesario.
ms.assetid: 40f79adb-87f3-4b0e-9cfe-927a4bc9ada5
keywords:
- 'Método de carga: CPapFile'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe70be7241fe1e1eaeb779317e11a76fb479f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903904"
---
# <a name="load-method---cpapfile"></a>Método de carga: CPapFile

Cuando estas operaciones se realizan correctamente, se libera la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) obtenida. Esto cierra el archivo e indica que el archivo no se mantiene abierto durante otras operaciones de cliente. Se volverá a abrir cuando sea necesario.

Este ejemplo es el método  **Load** de **CPapFile** de Papfile. cpp.


```C++
HRESULT CPapFile::Load(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If null file name passed then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Verify that the file is using the APPUTIL function.
    if (FileExist(pszFile))
    {
      // Use the COM service to verify that the file is actually a 
      // valid compound file.
      hr = StgIsStorageFile(pszFile);
      if (SUCCEEDED(hr))
      {
        // Use the COM service to open the compound file and
        // obtain an IStorage interface.
        hr = StgOpenStorage(
               pszFile,
               NULL,
               STGM_DIRECT | STGM_READ | STGM_SHARE_EXCLUSIVE,
               NULL,
               0,
               &m_pIStorage);
        if (SUCCEEDED(hr))
        {
          // An IStorage interface has been obtained. Now, request 
          // the COPaper object on the server side to load into  
          // itself the file's paper data using IStorage for our 
          // client-provided compound file.
          hr = m_pIPaper->Load(nLockKey, m_pIStorage);
          if (SUCCEEDED(hr))
          {
            // The paper data was loaded and a current compound
            // file name exists. Copy it for later use in a saves 
            // and loads.
            if (bNewFile)
              StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
          }

          // The Storage object is not required now. Do not hold the 
          // file open. Re-obtain the IStorage again later, when 
          // required (and thus re-open the compound file) for
          // another save or load.
          RELEASE_INTERFACE(m_pIStorage);
        }
      }
    }

    return (hr);
  }
  
```



### <a name="remarks"></a>Observaciones

Al igual que con el método [**Save**](save-method---cpapfile.md) , si se pasa **null** para el parámetro *pszFileName* , se usa el contenido almacenado del miembro **m \_ szCurFileName** para el nombre de archivo. Dado que se puede abrir un archivo existente, la función APPUTIL **FileExist** se usa en primer lugar para comprobar que el archivo existe. Si existe, se llama a la función estándar del servicio [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) para comprobar el formato del archivo y determinar si es un archivo compuesto válido.

Si el archivo es válido, se llama a la función de servicio [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) estándar para abrir el archivo y devolver un puntero a una interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para él.

El primer parámetro es el nombre del archivo compuesto que se va a abrir. Al igual que con la llamada a [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) , esta cadena se espera en el formato Unicode y durante la compilación ANSI se usa una macro APPUTIL para asegurarse de que el parámetro ANSI se convierte en el Unicode esperado.

El segundo parámetro de almacenamiento de prioridad es **null**, lo que indica que no se utiliza en este ejemplo.

Las marcas de modo de acceso se pasan como el tercer parámetro para especificar qué modos de acceso se permiten en el archivo abierto. [**STGM \_ LEER**](stgm-constants.md) abre el archivo con permiso de solo lectura. [**STGM \_ DIRECT**](stgm-constants.md) abre el archivo para el acceso directo, en lugar del acceso con transacciones. [**STGM \_ Recurso compartido \_ exclusivo**](stgm-constants.md) abre el archivo para uso exclusivo y no compartido por parte del autor de la llamada.

El cuarto parámetro de exclusión de elemento en **null**, que indica que no se utiliza en este ejemplo.

El quinto parámetro está reservado para un uso futuro y debe ser cero.

La dirección de la variable de puntero **m \_ pIStorage** se pasa como el sexto parámetro. Cuando la llamada devuelve correctamente, **m \_ pIStorage** contiene un puntero a una interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Esta es la interfaz que se utiliza para las operaciones posteriores en el archivo abierto.

La operación importante en este caso es que el objeto de copapeles cargue sus datos de dibujo del archivo. Para ello, se usa el método **Load** de la interfaz [**IPaper**](ipaper-methods.md) del copaper. Si el copapel se ejecuta correctamente al cargar sus datos mediante el [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) proporcionado, el nombre del archivo compuesto se copia en **m \_ szCurFileName** como el nuevo nombre de archivo actual.

Cuando estas operaciones se completan correctamente, se libera la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) obtenida. Esto cierra el archivo y significa que el archivo no se mantiene abierto durante otras operaciones de cliente. Se volverá a abrir cuando sea necesario.

 

 





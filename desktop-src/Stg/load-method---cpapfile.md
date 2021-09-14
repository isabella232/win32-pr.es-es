---
title: 'Método Load: CPapFile'
description: Cuando estas operaciones se realiza correctamente, se libera la interfaz IStorage obtenida. Esto cierra el archivo e indica que el archivo no se mantiene abierto durante otras operaciones de cliente. Se volverá a abrir cuando sea necesario.
ms.assetid: 40f79adb-87f3-4b0e-9cfe-927a4bc9ada5
keywords:
- 'Método Load: CPapFile'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe70be7241fe1e1eaeb779317e11a76fb479f76
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068917"
---
# <a name="load-method---cpapfile"></a>Método Load: CPapFile

Cuando estas operaciones se realiza correctamente, se libera [**la interfaz IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) obtenida. Esto cierra el archivo e indica que el archivo no se mantiene abierto durante otras operaciones de cliente. Se volverá a abrir cuando sea necesario.

Este ejemplo es el **método CPapFile** **Load** de Papfile.cpp.


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

Al igual que con [**el método Save,**](save-method---cpapfile.md) si se pasa **NULL** para el parámetro *pszFileName,* el contenido almacenado del miembro **m \_ szCurFileName** se usa para el nombre de archivo. Dado que se puede abrir un archivo existente, la función APPUTIL **FileExist** se usa primero para comprobar que el archivo existe. Si existe, se llama a la función de servicio [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) estándar para comprobar el formato del archivo a fin de determinar si es un archivo compuesto válido.

Si el archivo es válido, se llama a la función de servicio [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) estándar para abrir el archivo y devolver un puntero a una [**interfaz IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para él.

El primer parámetro es el nombre del archivo compuesto que se va a abrir. Al igual que con la llamada a [**StgCreateDocfile,**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) esta cadena se espera en el formato Unicode y, durante la compilación ANSI, se usa una macro APPUTIL para asegurarse de que el parámetro ANSI se convierte en el Unicode esperado.

El segundo parámetro de almacenamiento de prioridad **es NULL,** lo que indica que no se usa en este ejemplo.

Las marcas de modo de acceso se pasan como tercer parámetro para especificar qué modos de acceso se permiten en el archivo abierto. [**STGM \_ READ**](stgm-constants.md) abre el archivo con permiso de solo lectura. [**STGM \_ DIRECT**](stgm-constants.md) abre el archivo para el acceso directo, en lugar del acceso con transacciones. [**STGM \_ SHARE \_ EXCLUSIVE**](stgm-constants.md) abre el archivo para que el autor de la llamada lo use de forma exclusiva y no compartida.

Cuarto parámetro de exclusión de elemento **en NULL,** que indica que no se usa en este ejemplo.

El quinto parámetro está reservado para uso futuro y debe ser cero.

La dirección de la variable de **puntero m \_ pIStorage** se pasa como el sexto parámetro. Cuando la llamada se devuelve correctamente, **m \_ pIStorage** contiene un puntero a una [**interfaz IStorage.**](/windows/desktop/api/Objidl/nn-objidl-istorage) Esta es la interfaz que se usa para las operaciones posteriores en el archivo abierto.

En este caso, la operación importante es hacer que el objeto COPaper cargue sus datos de dibujo del archivo. Esto se hace anteriormente mediante **el método Load** de la interfaz [**IPaper de COPaper.**](ipaper-methods.md) Si COPaper carga correctamente sus datos mediante el valor de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) proporcionado, el nombre del archivo compuesto se copia en **m \_ szCurFileName** como el nuevo nombre de archivo actual.

Cuando estas operaciones se completan correctamente, se libera la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) que se obtuvo. Esto cierra el archivo y significa que el archivo no se mantiene abierto durante otras operaciones de cliente. Se volverá a abrir cuando sea necesario.

 

 





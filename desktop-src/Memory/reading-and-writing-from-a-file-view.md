---
description: Para leer desde una vista de archivo, desreferencia el puntero devuelto por la función MapViewOfFile tal como se muestra en los ejemplos siguientes.
ms.assetid: c2a3da09-d116-4c2c-9e6c-ec9e80c88b99
title: Leer y escribir en una vista de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98ec50dc6cd8b0224f2ba33a17ba80c7b0fc658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688683"
---
# <a name="reading-and-writing-from-a-file-view"></a>Leer y escribir en una vista de archivo

Para leer desde una vista de archivo, desreferencia el puntero devuelto por la función [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) tal como se muestra en los ejemplos siguientes.

Leer o escribir en una vista de archivo de un archivo que no sea el archivo de paginación puede producir una **excepción en la excepción \_ de \_ \_ error de página** . Por ejemplo, el acceso a un archivo asignado que se encuentra en un servidor remoto puede generar una excepción si se pierde la conexión al servidor. También se pueden producir excepciones debido a un disco completo, un error de dispositivo subyacente o un error de asignación de memoria. Al escribir en una vista de archivos, las excepciones también pueden producirse porque el archivo está compartido y un proceso diferente ha bloqueado un intervalo de bytes. Para protegerse frente a excepciones debido a errores de entrada y salida (e/s), todos los intentos de acceso a archivos asignados a memoria se deben encapsular en controladores de excepciones estructurados. Cuando reciba una **excepción \_ en \_ un \_ error de página** en el filtro **\_ \_ excepto** , asegúrese de que la dirección está dentro de la asignación a la que está accediendo actualmente. Si es así, recupere o produzca un error correctamente; de lo contrario, no controle la excepción.

En el ejemplo siguiente se usa el puntero devuelto por **MapViewOfFile** para leer desde la vista de archivo:


```C++
  DWORD dwLength;

  __try
  {
    dwLength = *((LPDWORD) lpMapAddress);
  }
  __except(GetExceptionCode()==EXCEPTION_IN_PAGE_ERROR ?
    EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
  {
    // Failed to read from the view.
  }
```



En el ejemplo siguiente se usa el puntero devuelto por **MapViewOfFile** para escribir en la vista de archivo:


```C++
  DWORD dwLength;

  __try
  {
    *((LPDWORD) lpMapAddress) = dwLength;
  }
  __except (GetExceptionCode() == EXCEPTION_IN_PAGE_ERROR ? 
    EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
  {
    // Failed to write to the view.
  }
```



La función [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) copia el número especificado de bytes de la vista de archivo en el archivo físico, sin esperar a que se produzca la operación de escritura almacenada en caché:


```C++
  if (!FlushViewOfFile(lpMapAddress, dwBytesToFlush)) 
  {
    printf("Could not flush memory to disk (%d).\n", GetLastError()); 
  }
```



Si está asignando un archivo comprimido o disperso en una partición NTFS, existe una posibilidad adicional de que se produzca un error de e/s al paginar en una parte del archivo. En este caso, es posible que el espacio de direcciones asignado por [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) no esté respaldado por el espacio en disco asignado. Esto se debe a que un archivo disperso puede tener regiones de ceros para los que NTFS no asigna espacio en disco, y un archivo comprimido puede ocupar menos espacio en disco que los datos reales que representa. Si lee o escribe en una parte de un archivo disperso o comprimido que no está respaldado por el espacio en disco, el sistema operativo puede intentar asignar espacio en disco. Si el disco está lleno, se puede producir una excepción que indica un error de e/s.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control estructurado de excepciones](../debug/structured-exception-handling.md)
</dt> </dl>

 

 

---
description: Para leer desde una vista de archivo, desreferencia el puntero devuelto por la función MapViewOfFile como se muestra en los ejemplos siguientes.
ms.assetid: c2a3da09-d116-4c2c-9e6c-ec9e80c88b99
title: Lectura y escritura desde una vista de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee56f1d06e53bdfd6f7571e4ec296da0270ce0a7050b253b5900c4640d6df0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067685"
---
# <a name="reading-and-writing-from-a-file-view"></a>Lectura y escritura desde una vista de archivo

Para leer desde una vista de archivo, desreferencia el puntero devuelto por la [**función MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) como se muestra en los ejemplos siguientes.

Leer o escribir en una vista de archivo de un archivo distinto del archivo de página puede provocar una **excepción EXCEPTION \_ IN PAGE \_ \_ ERROR.** Por ejemplo, el acceso a un archivo asignado que reside en un servidor remoto puede generar una excepción si se pierde la conexión al servidor. También pueden producirse excepciones debido a un disco completo, un error de dispositivo subyacente o un error de asignación de memoria. Al escribir en una vista de archivo, también pueden producirse excepciones porque el archivo se comparte y un proceso diferente ha bloqueado un intervalo de bytes. Para protegerse frente a excepciones debido a errores de entrada y salida (E/S), todos los intentos de acceso a los archivos asignados a memoria deben encapsularse en controladores de excepciones estructurados. Cuando reciba EXCEPTION **IN PAGE ERROR en \_ \_ \_ el** filtro **\_ \_ excepto** , asegúrese de que la dirección se encuentra dentro de la asignación a la que está accediendo actualmente. Si es así, recuperar o producir un error correctamente; De lo contrario, no controle la excepción.

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



La [**función FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) copia el número especificado de bytes de la vista de archivo en el archivo físico, sin tener que esperar a que se produzca la operación de escritura almacenada en caché:


```C++
  if (!FlushViewOfFile(lpMapAddress, dwBytesToFlush)) 
  {
    printf("Could not flush memory to disk (%d).\n", GetLastError()); 
  }
```



Si va a asignar un archivo comprimido o disperso en una partición NTFS, existe la posibilidad adicional de un error de E/S al paginar en una parte del archivo. En este caso, es posible que el espacio de direcciones asignado por [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) no tenga el respaldo del espacio en disco asignado. Esto se debe a que un archivo disperso puede tener regiones de ceros para las que NTFS no asigna espacio en disco y un archivo comprimido puede ocupar menos espacio en disco que los datos reales que representa. Si lee o escribe en una parte de un archivo disperso o comprimido que no está respaldo por el espacio en disco, el sistema operativo puede intentar asignar espacio en disco. Si el disco está lleno, puede producirse una excepción que indica un error de E/S.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control estructurado de excepciones](../debug/structured-exception-handling.md)
</dt> </dl>

 

 

---
description: Código de ejemplo que muestra cómo usar la función GetFileAttributesEx para recuperar atributos de archivo.
ms.assetid: f6eaea8a-0cc2-4fb6-bec5-7fb12b20c075
title: Recuperar y cambiar atributos de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d2609030d1657b78c266ed6b10841159e0df4d40a2e3b07b0fce42e98b45d54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015143"
---
# <a name="retrieving-and-changing-file-attributes"></a>Recuperar y cambiar atributos de archivo

Una aplicación puede recuperar los atributos de archivo mediante la [**función GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) o [**GetFileAttributesEx.**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) Las [**funciones CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) y [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) pueden establecer muchos de los atributos. Sin embargo, las aplicaciones no pueden establecer todos los atributos.

En el ejemplo de código de este tema se usa la función [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) para copiar todos los archivos de texto (.txt) del directorio actual en un nuevo directorio de archivos de solo lectura. Los archivos del nuevo directorio se cambian para que sean de solo lectura, si es necesario.

La aplicación crea el directorio especificado como parámetro mediante la [**función CreateDirectory.**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) El directorio no debe existir todavía.

La aplicación busca en el directorio actual todos los archivos de texto mediante las funciones [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) y [**FindNextFile.**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) Cada archivo de texto se copia en el \\ directorio TextRO. Después de copiar un archivo, la [**función GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) determina si un archivo es de solo lectura o no. Si el archivo no es de solo lectura, la aplicación cambia los directorios a TextRO y convierte el archivo copiado en solo lectura mediante la \\ [**función SetFileAttributes.**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)

Una vez copiados todos los archivos de texto del directorio actual, la aplicación cierra el identificador de búsqueda mediante la [**función FindClose.**](/windows/desktop/api/FileAPI/nf-fileapi-findclose)


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

void _tmain(int argc, TCHAR* argv[])
{
   WIN32_FIND_DATA FileData;
   HANDLE          hSearch;
   DWORD           dwAttrs;
   TCHAR           szNewPath[MAX_PATH];   
 
   BOOL            fFinished = FALSE; 

   if(argc != 2)
   {
      _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
      return;
   }
 
// Create a new directory. 
 
   if (!CreateDirectory(argv[1], NULL)) 
   { 
      printf("CreateDirectory failed (%d)\n", GetLastError()); 
      return;
   } 
 
// Start searching for text files in the current directory. 
 
   hSearch = FindFirstFile(TEXT("*.txt"), &FileData); 
   if (hSearch == INVALID_HANDLE_VALUE) 
   { 
      printf("No text files found.\n"); 
      return;
   } 
 
// Copy each .TXT file to the new directory 
// and change it to read only, if not already. 
 
   while (!fFinished) 
   { 
      StringCchPrintf(szNewPath, sizeof(szNewPath)/sizeof(szNewPath[0]), TEXT("%s\\%s"), argv[1], FileData.cFileName);

      if (CopyFile(FileData.cFileName, szNewPath, FALSE))
      { 
         dwAttrs = GetFileAttributes(FileData.cFileName); 
         if (dwAttrs==INVALID_FILE_ATTRIBUTES) return; 

         if (!(dwAttrs & FILE_ATTRIBUTE_READONLY)) 
         { 
            SetFileAttributes(szNewPath, 
                dwAttrs | FILE_ATTRIBUTE_READONLY); 
         } 
      } 
      else 
      { 
         printf("Could not copy file.\n"); 
         return;
      } 
 
      if (!FindNextFile(hSearch, &FileData)) 
      {
         if (GetLastError() == ERROR_NO_MORE_FILES) 
         { 
            _tprintf(TEXT("Copied *.txt to %s\n"), argv[1]); 
            fFinished = TRUE; 
         } 
         else 
         { 
            printf("Could not find next file.\n"); 
            return;
         } 
      }
   } 
 
// Close the search handle. 
 
   FindClose(hSearch);
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Constantes de atributo de archivo**](file-attribute-constants.md)
</dt> <dt>

[Nombres de archivo, rutas de acceso y espacios de nombres](naming-a-file.md)
</dt> </dl>

 

 




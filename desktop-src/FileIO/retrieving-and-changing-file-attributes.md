---
description: Código de ejemplo que muestra cómo usar la función GetFileAttributesEx para recuperar atributos de archivo.
ms.assetid: f6eaea8a-0cc2-4fb6-bec5-7fb12b20c075
title: Recuperar y cambiar atributos de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c980ddd6390f016b2057392f42f6bf645859307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688203"
---
# <a name="retrieving-and-changing-file-attributes"></a><span data-ttu-id="826b0-103">Recuperar y cambiar atributos de archivo</span><span class="sxs-lookup"><span data-stu-id="826b0-103">Retrieving and Changing File Attributes</span></span>

<span data-ttu-id="826b0-104">Una aplicación puede recuperar los atributos de archivo mediante la función [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) o [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) .</span><span class="sxs-lookup"><span data-stu-id="826b0-104">An application can retrieve the file attributes by using the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) or [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) function.</span></span> <span data-ttu-id="826b0-105">Las funciones [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) y [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) pueden establecer muchos de los atributos.</span><span class="sxs-lookup"><span data-stu-id="826b0-105">The [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) and [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) functions can set many of the attributes.</span></span> <span data-ttu-id="826b0-106">Sin embargo, las aplicaciones no pueden establecer todos los atributos.</span><span class="sxs-lookup"><span data-stu-id="826b0-106">However, applications cannot set all attributes.</span></span>

<span data-ttu-id="826b0-107">En el ejemplo de código de este tema se usa la función [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) para copiar todos los archivos de texto (. txt) del directorio actual en un nuevo directorio de archivos de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="826b0-107">The code example in this topic uses the [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) function to copy all text files (.txt) in the current directory to a new directory of read-only files.</span></span> <span data-ttu-id="826b0-108">Los archivos del nuevo directorio se cambian a solo lectura, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="826b0-108">Files in the new directory are changed to read only, if necessary.</span></span>

<span data-ttu-id="826b0-109">La aplicación crea el directorio especificado como un parámetro mediante la función [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) .</span><span class="sxs-lookup"><span data-stu-id="826b0-109">The application creates the directory specified as a parameter by using the [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) function.</span></span> <span data-ttu-id="826b0-110">El directorio no debe existir ya.</span><span class="sxs-lookup"><span data-stu-id="826b0-110">The directory must not exist already.</span></span>

<span data-ttu-id="826b0-111">La aplicación busca en el directorio actual todos los archivos de texto mediante las funciones [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) y [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) .</span><span class="sxs-lookup"><span data-stu-id="826b0-111">The application searches the current directory for all text files by using the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) functions.</span></span> <span data-ttu-id="826b0-112">Cada archivo de texto se copia en el \\ directorio TextRO</span><span class="sxs-lookup"><span data-stu-id="826b0-112">Each text file is copied to the \\TextRO directory.</span></span> <span data-ttu-id="826b0-113">Una vez copiado un archivo, la función [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) determina si un archivo es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="826b0-113">After a file is copied, the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) function determines whether or not a file is read only.</span></span> <span data-ttu-id="826b0-114">Si el archivo no es de solo lectura, la aplicación cambia los directorios a \\ TextRO y convierte el archivo copiado en solo lectura mediante la función [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) .</span><span class="sxs-lookup"><span data-stu-id="826b0-114">If the file is not read only, the application changes directories to \\TextRO and converts the copied file to read only by using the [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) function.</span></span>

<span data-ttu-id="826b0-115">Una vez copiados todos los archivos de texto del directorio actual, la aplicación cierra el identificador de búsqueda mediante la función [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .</span><span class="sxs-lookup"><span data-stu-id="826b0-115">After all text files in the current directory are copied, the application closes the search handle by using the [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) function.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="826b0-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="826b0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="826b0-117">**Constantes de atributo de archivo**</span><span class="sxs-lookup"><span data-stu-id="826b0-117">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> <dt>

[<span data-ttu-id="826b0-118">Nombres de archivo, rutas de acceso y espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="826b0-118">File Names, Paths, and Namespaces</span></span>](naming-a-file.md)
</dt> </dl>

 

 




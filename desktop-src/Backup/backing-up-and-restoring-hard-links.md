---
title: Copia de seguridad y restauración de vínculos duros
description: Para realizar copias de seguridad y restaurar vínculos duros, use las funciones CreateFile, CreateHardLink, FindFirstFileNameW, FindNextFileNameW, BackupRead, GetFileInformationByHandle y BackupWrite, como se muestra en los siguientes ejemplos de pseudocódigo.
ms.assetid: 129e9cf4-8ab1-45d2-8e1a-4bc85b9de668
keywords:
- copias de seguridad de vínculos duros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25e5cf5a114160456e83e39cb06f441554f998df65bed2ea8f0e63b036c33c94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702225"
---
# <a name="backing-up-and-restoring-hard-links"></a>Copia de seguridad y restauración de vínculos duros

Para realizar copias de seguridad y restaurar vínculos duros, use las funciones [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**CreateHardLink**](/windows/desktop/api/winbase/nf-winbase-createhardlinka), [**FindFirstFileNameW**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilenamew), [**FindNextFileNameW,**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilenamew) [**BackupRead,**](/windows/desktop/api/Winbase/nf-winbase-backupread) [**GetFileInformationByHandle**](/windows/desktop/api/fileapi/nf-fileapi-getfileinformationbyhandle)y [**BackupWrite,**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) como se muestra en los siguientes ejemplos de pseudocódigo.

## <a name="pseudocode-algorithm-for-backing-up-hard-links"></a>Algoritmo de seudocódigo para hacer una copia de seguridad de vínculos duros

``` syntax
1.  Initialize and empty a list of known links. 
2.  While there are more files to back up 
3.     Read the disk and get the next file. 
4.     Call CreateFile to open the file for read. 
5.     Call GetFileInformationByHandle to get the NumberOfLinks 
          and the FileIndex.
6.     If the NumberOfLinks is greater than 1 
7.        Search the list of known links, looking for the  
             same FileIndex.
8.        If a match is found 
9.           Skip this file; its link exists already on
                your backup media.
10.       Else
11.          Add the full path of the file and the FileIndex
                to the list of links.
12.          Call BackupRead to copy all data to your backup media.
13.          Call FindFirstFileNameW and FindNextFileNameW to 
                enumerate the hard links to the file.
14.          For each hard link
15.             Mark the data as a LINK on your backup media.
16.             Store the full path from the list to your backup media.
17.          Endfor
18.       Endif
19.    Else
20.       Call BackupRead to copy all data to your backup media.
21.    Endif
22. EndWhile
```

## <a name="pseudocode-algorithm-for-restoring-hard-links"></a>Algoritmo de pseudocódigo para restaurar vínculos duros

``` syntax
1.  While there are more files to restore 
2.     If there are hard links to the file
3.        Call CreateHardLink to recreate the links.
4.     Endif
5.     Call BackupWrite with the data stored on your backup media
6.  EndWhile
```

**Windows Server 2003 y Windows XP:** No se admiten las funciones [**FindFirstFileNameW**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilenamew) [**y FindNextFileNameW.**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilenamew) En su lugar, puede usar el procedimiento descrito en el siguiente ejemplo de pseudocódigo.

## <a name="alternate-pseudocode-algorithm-for-backing-up-hard-links"></a>Algoritmo de seudocódigo alternativo para hacer una copia de seguridad de vínculos duros

``` syntax
1.  Initialize and empty a list of known links. 
2.  While there are more files to back up 
3.     Read the disk and get the next file. 
4.     Call CreateFile to open the file for read. 
5.     Call GetFileInformationByHandle to get the NumberOfLinks and 
          the FileIndex. 
6.     If the NumberOfLinks is greater than 1 
7.        Search the list of known links looking for 
             the same FileIndex. 
8.           If a match is NOT found 
9.              Add the full path of the file and the FileIndex
                   to the list. 
10.             Call BackupRead to copy all data to 
                   your backup media. 
11.          Else 
12.             Mark the data as a LINK on your backup media 
13.             Store the full path from the list 
                   to your backup media. 
14.          Endif 
15.    Else 
16.       Call BackupRead to copy all data to your 
             backup media. 
17.    Endif 
18. EndWhile
```

 

 
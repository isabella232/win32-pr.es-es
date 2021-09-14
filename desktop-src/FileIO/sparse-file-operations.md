---
description: Determine si un sistema de archivos admite archivos dispersos llamando a la función GetVolumeInformation.
ms.assetid: a08f6bbc-c139-4396-8964-4aa63285f3f5
title: Operaciones de archivos dispersos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c23d26fc1c52db32ca7674aec2fc487a826e9a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069845"
---
# <a name="sparse-file-operations"></a>Operaciones de archivos dispersos

Para determinar si un sistema de archivos admite archivos dispersos, llame a la función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) y examine la marca de bits **FILE SUPPORTS \_ \_ SPARSE \_ FILES** devuelta a través del parámetro *lpFileSystemFlags.*

La mayoría de las aplicaciones no son conscientes de los archivos dispersos y no crearán archivos dispersos. El hecho de que una aplicación esté leyendo un archivo disperso es transparente para la aplicación. Una aplicación que sea consciente de los archivos dispersos debe determinar si su conjunto de datos es adecuado para mantenerse en un archivo disperso. Una vez realizada esa determinación, la aplicación debe declarar explícitamente un archivo como disperso, mediante el código de control [**FSCTL \_ SET \_ SPARSE.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse)

Una vez que una aplicación ha establecido un archivo para que sea disperso, la aplicación puede usar el código de control [**FSCTL \_ SET ZERO \_ \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) para establecer una región del archivo en cero. Además, la aplicación puede usar el código de control [**FSCTL \_ QUERY \_ ALLOCATED \_ RANGES**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges) para acelerar las búsquedas de datos distintos de cero en el archivo disperso.

Cuando se realiza una operación de escritura (con una función u otra operación que no sea [**FSCTL \_ SET ZERO \_ \_ DATA)**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)cuyos datos no constan de nada más que ceros, los ceros se escribirán en el disco durante toda la longitud de la escritura. Para poner a cero un intervalo del archivo y mantener la dispersa, use **FSCTL \_ SET ZERO \_ \_ DATA**.

Una aplicación que tenga en cuenta la dispersa también puede establecer un archivo existente para que sea disperso. Si una aplicación establece un archivo existente para que sea disperso, debe examinar el archivo en busca de regiones que contengan ceros y usar [**FSCTL \_ SET ZERO \_ \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) para restablecer esas regiones, lo que posiblemente desasigne algún almacenamiento en disco físico. Una aplicación actualizada a un reconocimiento de archivos dispersos debe realizar esta conversión.

Cuando se realiza una operación de lectura desde una parte con ceros de un archivo disperso, es posible que el sistema operativo no lea desde la unidad de disco duro. En su lugar, el sistema reconoce que la parte del archivo que se va a leer contiene ceros y devuelve un búfer lleno de ceros sin leer realmente del disco.

Al igual que con cualquier otro archivo, el sistema puede escribir o leer datos desde cualquier posición de un archivo disperso. Los datos distintos de cero que se escriben en una parte previamente cero del archivo pueden dar lugar a la asignación de espacio en disco. Los ceros que se escriben sobre datos distintos de cero (solo con [**FSCTL \_ SET ZERO \_ \_ DATA)**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)pueden dar lugar a una desasignación de espacio en disco.

> [!Note]  
> La aplicación debe mantener la dispersa escritura de ceros con [**FSCTL \_ SET ZERO \_ \_ DATA.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)

 

Las herramientas de desfragmentación que controlan archivos comprimidos en sistemas de archivos NTFS controlarán correctamente los archivos dispersos en volúmenes del sistema de archivos NTFS. Los archivos dispersos grandes y muy fragmentados pueden superar la limitación de NTFS en las extensiones de disco antes de usar el espacio disponible. Para obtener más información, vea Extender un archivo puede producir un [error de "Disco lleno" aunque el volumen tenga espacio libre.](https://support.microsoft.com/default.aspx/kb/957180)

 

 

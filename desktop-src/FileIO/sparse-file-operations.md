---
description: Determine si un sistema de archivos admite archivos dispersos mediante una llamada a la función GetVolumeInformation.
ms.assetid: a08f6bbc-c139-4396-8964-4aa63285f3f5
title: Operaciones de archivos dispersos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c23d26fc1c52db32ca7674aec2fc487a826e9a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666626"
---
# <a name="sparse-file-operations"></a>Operaciones de archivos dispersos

Para determinar si un sistema de archivos admite archivos dispersos, llame a la función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) y examine el archivo admite la marca de bits de **\_ \_ \_ archivos dispersos** devuelta mediante el parámetro *lpFileSystemFlags* .

La mayoría de las aplicaciones no tienen en cuenta los archivos dispersos y no crearán archivos dispersos. El hecho de que una aplicación lea un archivo disperso es transparente para la aplicación. Una aplicación que tenga en cuenta los archivos dispersos debe determinar si su conjunto de datos es adecuado para conservarse en un archivo disperso. Una vez realizada esa determinación, la aplicación debe declarar explícitamente un archivo como disperso, mediante el uso del código de control [**\_ \_ disperso de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse) .

Después de que una aplicación haya configurado un archivo para que sea disperso, la aplicación puede usar el código de control de [**datos de FSCTL \_ establecido en \_ cero \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) para establecer una región del archivo en cero. Además, la aplicación puede usar el código de control de [**\_ \_ \_ intervalos asignados de consulta FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges) para acelerar las búsquedas de datos distintos de cero en el archivo disperso.

Cuando se realiza una operación de escritura (con una función u operación distinta de [**FSCTL \_ establecida en \_ cero \_ datos**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)) cuyos datos se componen de nada pero ceros, se escribirán ceros en el disco para la longitud completa de la escritura. Para que un intervalo del archivo sea cero y mantener la dispersión, use **FSCTL \_ establecer \_ \_ datos cero**.

Una aplicación compatible con la dispersión también puede establecer un archivo existente para que sea disperso. Si una aplicación establece un archivo existente para que sea disperso, debe analizar el archivo en busca de regiones que contengan ceros y usar [**FSCTL \_ establecer \_ cero \_ datos**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) para restablecer esas regiones, lo que posiblemente desasignaría algún almacenamiento de disco físico. Una aplicación actualizada al reconocimiento de archivos dispersos debe realizar esta conversión.

Cuando se realiza una operación de lectura desde una parte con ceros de un archivo disperso, es posible que el sistema operativo no se lea desde la unidad de disco duro. En su lugar, el sistema reconoce que la parte del archivo que se va a leer contiene ceros y devuelve un búfer lleno de ceros sin leer realmente el disco.

Como con cualquier otro archivo, el sistema puede escribir o leer datos desde cualquier posición en un archivo disperso. Los datos distintos de cero que se escriben en una parte con ceros anterior del archivo pueden dar lugar a la asignación de espacio en disco. Los ceros que se escriben sobre datos distintos de cero (solo con [**\_ \_ \_ datos**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)de otro conjunto de FSCTL) pueden dar lugar a una desasignación de espacio en disco.

> [!Note]  
> Depende de la aplicación mantener la dispersión si escribe ceros con los [**\_ \_ \_ datos de FSCTL establecidos**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data).

 

Las herramientas de desfragmentación que controlan archivos comprimidos en sistemas de archivos NTFS administrarán correctamente los archivos dispersos en volúmenes del sistema de archivos NTFS. Los archivos dispersos grandes y muy fragmentados pueden superar la limitación de NTFS en las extensiones de disco antes de que se use el espacio disponible. Para obtener más información, vea [el tema sobre cómo ampliar un archivo con el error "disco lleno", aunque el volumen tenga espacio disponible](https://support.microsoft.com/default.aspx/kb/957180).

 

 

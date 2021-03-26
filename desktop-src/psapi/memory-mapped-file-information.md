---
title: Memory-Mapped información de archivo
description: Un archivo asignado a la memoria (o asignación de archivos) es el resultado de asociar el contenido de un archivo con una parte del espacio de direcciones virtuales de un proceso. Se puede usar para compartir un archivo o memoria entre dos o más procesos.
ms.assetid: b6ec2bc4-c504-4d0b-87f0-39bb1949accd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc6d33e7f3fe6bef36ea6e5a7f355b780d89b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149534"
---
# <a name="memory-mapped-file-information"></a>Memory-Mapped información de archivo

Un *archivo asignado a la memoria* (o *asignación de archivos*) es el resultado de asociar el contenido de un archivo con una parte del espacio de direcciones virtuales de un proceso. Se puede usar para compartir un archivo o memoria entre dos o más procesos.

La función [**GetMappedFileName**](/windows/desktop/api/Psapi/nf-psapi-getmappedfilenamea) recibe un identificador de proceso y un puntero a una dirección como entrada. Si la dirección está dentro de un archivo asignado a la memoria en el espacio de direcciones virtuales del proceso, la función devuelve el nombre del archivo asignado a la memoria. Los nombres de archivo devueltos por **GetMappedFileName** usan el formato de dispositivo, en lugar de Letras de unidad. Por ejemplo, el nombre de archivo c: \\ WinNT \\ system32 \\ CType. NLS sería similar al siguiente en forma de dispositivo:

\\Dispositivo \\ Harddisk0 \\ Partition1 \\ WinNT \\ system32 \\ CType. NLS

Para obtener más información sobre los archivos asignados a memoria, consulte [asignación de archivos](/windows/desktop/Memory/file-mapping). Para obtener un ejemplo en el que se convierten los nombres de archivo en el formato de dispositivo a Letras de unidad, vea [obtener un nombre de archivo de un identificador de archivo](/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle).

 

 
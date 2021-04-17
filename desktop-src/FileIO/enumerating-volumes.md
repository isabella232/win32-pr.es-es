---
description: Para realizar una lista completa de los volúmenes de un equipo o para manipular cada volumen a su vez, puede enumerar los volúmenes.
ms.assetid: 5adcd59a-48b7-4373-a10b-c352962f715a
title: Enumerar volúmenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc294d72fa3fad24536b175ee7e5e023066586c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687794"
---
# <a name="enumerating-volumes"></a>Enumerar volúmenes

Para realizar una lista completa de los volúmenes de un equipo o para manipular cada volumen a su vez, puede enumerar los volúmenes. Dentro de un volumen, puede [Buscar carpetas montadas](enumerating-volume-mount-points.md) u otros objetos en el volumen.

Tres funciones permiten a una aplicación enumerar volúmenes en un equipo:

-   [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)
-   [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)
-   [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)

Estas tres funciones funcionan de forma muy similar a las funciones [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)y [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .

Inicia una búsqueda de volúmenes con [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew). Si la búsqueda se realiza correctamente, procese los resultados según el diseño de la aplicación. A continuación, use [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) en un bucle para buscar y procesar cada volumen subsiguiente. Una vez agotado el suministro de volúmenes, cierre la búsqueda con [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose).

No debe asumir ninguna correlación entre el orden de los volúmenes que devuelven estas funciones y el orden de los volúmenes devueltos por otras funciones o herramientas. En concreto, no asuma ninguna correlación entre el orden de volumen y las letras de unidad asignadas por el BIOS (si existe) o el administrador de discos.

Vea [ejemplos de carpetas montadas](volume-mount-point-examples.md) para obtener un ejemplo de cómo enumerar los volúmenes de un equipo.

 

 




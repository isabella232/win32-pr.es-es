---
description: Apilamiento de configuración
ms.assetid: 1f0f75d6-3553-4ee1-8ee6-bd617da4a109
title: Apilamiento de configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9018a2484ce4e5b9121d08abffee54911531b7f421cfef75643594e827fe350e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905574"
---
# <a name="configuration-stacking"></a>Apilamiento de configuración

\[A partir Windows 8 y Windows Server 2012, la interfaz COM [de Virtual Disk Service](virtual-disk-service-portal.md) se sustituye por el [Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

El apilamiento implica la concatenación de un conjunto de asignaciones de bloques lógicos. Puede apilar varios LUN del mismo subsistema en un LUN. Puede apilar un LUN junto con volúmenes del mismo paquete en un volumen. Además, puede apilar varios LUN que los subsistemas heterogéneos encuentran en un volumen.

Como se muestra en la ilustración siguiente, la creación de un volumen no cambia el enlace existente de un LUN colaborador. De forma similar, el desenlace de un volumen no desenlace un LUN de contribución. En la ilustración se muestra la configuración de RAID 0 1 (0+1). Esta configuración conocida combina el seccionamiento (RAID 0) y la creación de reflejo (RAID 1), que empareja el acceso rápido a los datos de RAID 0 con la confiabilidad de RAID 1.

![Diagrama que muestra una configuración RAID 0 1 (0+1).](images/vdsstacklunvolzeroplusone.png)

Los LUN que contribuyen pueden tener tipos de enlace diferentes. Muchas configuraciones son posibles con VDS, pero son muy poco probables, como la siguiente ilustración. En este ejemplo, un plex de volumen es un LUN seccionado y el otro es un LUN reflejado triple.

![Diagrama que muestra una configuración vds donde un plex de volumen es un LUN seccionado y el otro es un LUN reflejado de tres vías.](images/vdsstacklunvol.png)

Aunque no es práctico, en este ejemplo se ilustra un aspecto importante del apilamiento. Dado que el apilamiento concatena plexos, VDS agrega los tres plex LUN a los dos plexos de volumen para un total de cinco plexos.

 

 

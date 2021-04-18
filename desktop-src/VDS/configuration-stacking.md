---
description: Apilamiento de configuración
ms.assetid: 1f0f75d6-3553-4ee1-8ee6-bd617da4a109
title: Apilamiento de configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b50b90629556b5ed00db712b49fe8fa4e48ea8cc
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104559528"
---
# <a name="configuration-stacking"></a>Apilamiento de configuración

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

La apilación implica la concatenación de un conjunto de asignaciones de bloques lógicos. Puede apilar varios LUN desde el mismo subsistema en un LUN. Puede apilar un LUN junto con volúmenes del mismo paquete en un volumen. Además, puede apilar varios LUN que se exponen mediante subsistemas heterogéneos en un volumen.

Como se muestra en la siguiente ilustración, la creación de un volumen no cambia el enlace existente de un LUN contribuyente. De forma similar, al Desenlazar un volumen no se deshace el enlace de un LUN contribuyente. En la ilustración se muestra la configuración de RAID 0 1 (0 + 1). Esta configuración conocida combina el seccionamiento (RAID 0) y la creación de reflejo (RAID 1), que empareja el acceso rápido a los datos de RAID 0 con la confiabilidad de RAID 1.

![Diagrama que muestra una configuración de RAID 0 1 (0 + 1).](images/vdsstacklunvolzeroplusone.png)

Los LUN de contribución pueden tener tipos de enlace diferentes. Hay muchas configuraciones posibles con VDS, pero son muy poco probables, como la siguiente ilustración. En este ejemplo, un Plex de volumen es un LUN seccionado y el otro es un LUN reflejado de tres vías.

![Diagrama que muestra una configuración de VDS en la que un Plex de volumen es un LUN seccionado y el otro es un LUN reflejado de 3 vías.](images/vdsstacklunvol.png)

Aunque no es práctico, este ejemplo muestra un aspecto importante del apilamiento. Dado que la apilación concatena complejos, VDS agrega los tres complejos de LUN a los dos complejos de volumen para un total de cinco complejos.

 

 

---
description: 'El administrador de memoria crea los siguientes grupos de memoria que el sistema utiliza para asignar memoria: bloque no paginado y grupo paginado.'
ms.assetid: 68ee9c72-f3a3-4f1f-a827-ed4210a665e4
title: Grupos de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60987b43347e55d8ee2d01672dbb8173ffc8dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678529"
---
# <a name="memory-pools"></a>Grupos de memoria

El administrador de memoria crea los siguientes grupos de memoria que el sistema utiliza para asignar memoria: bloque no paginado y grupo paginado. Ambos grupos de memoria se encuentran en la región del espacio de direcciones que se reserva para el sistema y se asignan en el espacio de direcciones virtuales de cada proceso. El bloque no paginado consta de direcciones de memoria virtual que se garantiza que residen en la memoria física siempre que se asignen los objetos de kernel correspondientes. El bloque paginado se compone de la memoria virtual que se puede paginar dentro y fuera del sistema. Para mejorar el rendimiento, los sistemas con un solo procesador tienen tres grupos paginados y los sistemas multiprocesador tienen cinco grupos paginados.

Los identificadores de los [objetos de kernel](../sysinfo/kernel-objects.md) se almacenan en el grupo paginado, por lo que el número de identificadores que se pueden crear se basa en la memoria disponible.

El sistema registra los límites y los valores actuales de su bloque no paginado, el grupo paginado y el uso del archivo de paginación. Para obtener más información, vea [información sobre el rendimiento](memory-performance-information.md)de la memoria.

 

 

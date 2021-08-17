---
description: 'El administrador de memoria crea los siguientes grupos de memoria que el sistema usa para asignar memoria: grupo no paginado y grupo paginado.'
ms.assetid: 68ee9c72-f3a3-4f1f-a827-ed4210a665e4
title: Grupos de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a49597cf90324395c50a4e44aac03815426f0c1de8ea2c7ca7aa85b5cdac95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809002"
---
# <a name="memory-pools"></a>Grupos de memoria

El administrador de memoria crea los siguientes grupos de memoria que el sistema usa para asignar memoria: grupo no paginado y grupo paginado. Ambos grupos de memoria se encuentran en la región del espacio de direcciones reservado para el sistema y asignado al espacio de direcciones virtuales de cada proceso. El grupo no con página consta de direcciones de memoria virtual que se garantiza que residan en la memoria física, siempre y cuando se asignen los objetos de kernel correspondientes. El grupo paginado consta de memoria virtual que se puede paginar dentro y fuera del sistema. Para mejorar el rendimiento, los sistemas con un solo procesador tienen tres grupos paginados y los sistemas de varios procesadores tienen cinco grupos paginados.

Los identificadores de [los objetos de kernel](../sysinfo/kernel-objects.md) se almacenan en el grupo paginado, por lo que el número de identificadores que puede crear se basa en la memoria disponible.

El sistema registra los límites y los valores actuales de su grupo no paginado, el grupo paginado y el uso de archivos de página. Para obtener más información, vea [Información de rendimiento de memoria](memory-performance-information.md).

 

 

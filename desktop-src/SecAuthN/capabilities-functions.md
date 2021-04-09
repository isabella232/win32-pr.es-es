---
description: La API del proveedor de red especifica una función de funcionalidad única.
ms.assetid: fc74a043-da13-485f-9f54-a43064add927
title: Funciones de funcionalidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cde32ba0d3116ce83e7ca6621666f5e9a86650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082404"
---
# <a name="capabilities-functions"></a>Funciones de funcionalidad

La API del proveedor de red especifica una función de funcionalidad única. Cuando el sistema operativo solicita información acerca de las capacidades de un proveedor de red, el [*enrutador de proveedor múltiple*](/windows/desktop/SecGloss/m-gly) (MPR) llama a la función [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) de cada proveedor de red cuya red está activa.

La función [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) devuelve una máscara de máscara que indica qué funciones de la API de proveedor de red admite el proveedor de red. La función **NPGetCaps** es la única función que un proveedor de red debe implementar. El sistema operativo llama a esta función para determinar qué otras funciones de la API del proveedor de red admite el proveedor.

 

 

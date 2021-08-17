---
description: La API del proveedor de red especifica una sola función de funcionalidades.
ms.assetid: fc74a043-da13-485f-9f54-a43064add927
title: Funciones de funcionalidades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab47d2c8323131b396640d9154e33749c1716db0d369d3a374f69131468613d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141278"
---
# <a name="capabilities-functions"></a>Funciones de funcionalidades

La API del proveedor de red especifica una sola función de funcionalidades. Cuando el sistema operativo solicita información sobre las [](/windows/desktop/SecGloss/m-gly) funcionalidades de un proveedor de red, el enrutador de varios proveedores (MPR) llama a la función [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) de cada proveedor de red cuya red está activa.

La [**función NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) devuelve una máscara de bits que indica qué funciones de la API del proveedor de red admite el proveedor de red. La **función NPGetCaps** es la única función que debe implementar un proveedor de red. El sistema operativo llama a esta función para determinar qué otras funciones de la API del proveedor de red admite el proveedor.

 

 

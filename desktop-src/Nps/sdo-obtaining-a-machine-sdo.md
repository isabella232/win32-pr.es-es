---
title: Obtener un SDO de máquinas
description: El primer paso en el uso de la API SDO es crear un objeto de equipo SDO.
ms.assetid: bdb01437-08d0-4279-94f2-840cb786cc44
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf85f9712e76bbdadcffa3914a86cc56576aecd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078003"
---
# <a name="obtaining-a-machine-sdo"></a>Obtener un SDO de máquinas

El primer paso en el uso de la API SDO es crear un objeto de equipo SDO.

Utilice la función [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) para obtener el identificador de clase (CLSID) del objeto de equipo SDO. El identificador de programación (ProgID) que se va a usar para el objeto es "IAS. SdoMachine".

Una vez que tenga el CLSID, llame a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con este CLSID. Especifique [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) como la interfaz para la que se va a devolver un puntero.

Consulte [adjuntar a un equipo SDO-Enabled](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) para ver el código de ejemplo que muestra cómo obtener un SDO de máquinas.

 

 
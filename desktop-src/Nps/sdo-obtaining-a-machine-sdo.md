---
title: Obtención de un SDO de máquina
description: El primer paso para usar la API de SDO es crear un objeto de máquina SDO.
ms.assetid: bdb01437-08d0-4279-94f2-840cb786cc44
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9217333440235d5adac544e00420f8564513510908a89a1da7494cf7ba2772ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128605"
---
# <a name="obtaining-a-machine-sdo"></a>Obtención de un SDO de máquina

El primer paso para usar la API de SDO es crear un objeto de máquina SDO.

Use la [**función CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) para obtener el identificador de clase (CLSID) para el objeto de máquina SDO. El identificador de programación (ProgID) que se va a usar para el objeto es "IAS. SdoMachine".

Una vez que tenga el CLSID, llame a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con este CLSID. Especifique [**ISdoMachine como**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) la interfaz para la que se va a devolver un puntero.

Consulte [Adjuntar a un equipo SDO-Enabled para](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) obtener código de ejemplo que muestra cómo obtener un SDO de máquina.

 

 
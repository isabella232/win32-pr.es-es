---
title: Asociar al equipo SDO
description: Con el puntero de interfaz devuelto por CoCreateInstance, llame al método ISdoMachine Attach.
ms.assetid: b28691ef-4054-4cd1-92aa-72ad9902fba3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d35b9088fc1848dcf581bf69db036dce57cdd2b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995330"
---
# <a name="attaching-to-the-sdo-computer"></a>Asociar al equipo SDO

Con el puntero de interfaz devuelto por [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), llame al método [**ISdoMachine:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) . Pase **null** como parámetro al método **Attach** . El valor **null** especifica que **Attach** asocia el objeto de equipo con el equipo local. No se admite la asociación a un equipo remoto.

Para determinar si el equipo local ya está adjunto, llame al método [**ISdoMachine:: GetAttachedComputer**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) .

Vea [asociar a un SDO-Enabled equipo](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) para ver el código de ejemplo que muestra cómo conectarse al equipo local.

 

 
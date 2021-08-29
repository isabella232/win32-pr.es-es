---
description: Device Power API facilita la determinación de qué dispositivos pueden reactivar el sistema a partir de un estado de suspensión y qué estados de suspensión admiten la activación. Para obtener más información sobre los estados de suspensión, vea Estados de energía del sistema.
ms.assetid: aaa776e5-3fc2-41bd-a805-6c09ef73807b
title: Administración de energía de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bd6fa4da0bcdb295334bafbb67250fb056b6729af8e7f637cfde9b281fb128a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143578"
---
# <a name="device-power-management"></a>Administración de energía de dispositivos

Device Power API facilita la determinación de qué dispositivos pueden reactivar el sistema a partir de un estado de suspensión y qué estados de suspensión admiten la activación. Para obtener más información sobre los estados de suspensión, vea [Estados de energía del sistema](system-power-states.md).

La [**función DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) se puede usar para buscar en la lista de dispositivos dispositivos que coincidan con los criterios especificados. Los criterios pueden incluir la capacidad del dispositivo para admitir un estado del sistema o reactivar desde ese estado. Las marcas admitidas actualmente se pueden encontrar en WinNT.h y DevPower.h.

La [**función DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) permite o deshabilita que un dispositivo especificado resalte el sistema de un estado de suspensión.

Device Power API permite a los desarrolladores crear una mejor experiencia de usuario al proporcionar al usuario más información sobre lo que hace el sistema y más control sobre los dispositivos del sistema. La energía del dispositivo es útil en situaciones en las que el consumo de energía es crítico, como en dispositivos portátiles que se ejecutan con baterías. Por ejemplo, el esquema de administración de energía que se usa en un equipo de escritorio puede no ser el esquema óptimo para un equipo portátil, por lo que es posible que el usuario quiera deshabilitar que determinados dispositivos apaguen el sistema. Esto puede ahorrar energía porque los dispositivos deshabilitados no extraerán energía mientras el sistema esté en modo de suspensión.

Para obtener un ejemplo, consulte [Uso de Device Power API.](using-the-device-power-api.md)

 

 




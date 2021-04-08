---
description: El dispositivo Power API facilita la determinación de los dispositivos que pueden reactivar el sistema desde un estado de suspensión y los Estados de suspensión en los que los dispositivos admiten la activación. Para obtener más información acerca de los Estados de suspensión, consulte Estados de energía del sistema.
ms.assetid: aaa776e5-3fc2-41bd-a805-6c09ef73807b
title: Administración de energía de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0982b7de23f7b7d8cf39686c854d64f284d1ce2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001960"
---
# <a name="device-power-management"></a>Administración de energía de dispositivos

El dispositivo Power API facilita la determinación de los dispositivos que pueden reactivar el sistema desde un estado de suspensión y los Estados de suspensión en los que los dispositivos admiten la activación. Para obtener más información acerca de los Estados de suspensión, consulte [Estados de energía del sistema](system-power-states.md).

La función [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) se puede usar para buscar los dispositivos que coinciden con los criterios especificados en la lista de dispositivos. Los criterios pueden incluir la capacidad del dispositivo para admitir un estado del sistema o reactivar desde ese estado. Las marcas admitidas actualmente se pueden encontrar en Winnt. h y DevPower. h.

La función [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) habilita o deshabilita el dispositivo especificado para que no reactiva el sistema desde un estado de suspensión.

El dispositivo Power API permite a los desarrolladores crear una mejor experiencia de usuario, ya que proporciona al usuario más información sobre lo que está haciendo el sistema y más control sobre los dispositivos del sistema. La potencia del dispositivo es útil en situaciones en las que el consumo de energía es crítico, como en dispositivos portátiles que se ejecutan con baterías. Por ejemplo, el esquema de administración de energía que se usa en un equipo de escritorio puede no ser el esquema óptimo para un equipo portátil, por lo que es posible que el usuario desee deshabilitar la activación de determinados dispositivos. Esto puede ahorrar energía porque los dispositivos deshabilitados no reproducirán energía mientras el sistema está en modo de suspensión.

Para ver un ejemplo, consulte [uso de la API de energía de dispositivos](using-the-device-power-api.md).

 

 




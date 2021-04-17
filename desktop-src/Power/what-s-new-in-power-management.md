---
description: Windows 10 ayuda a la aplicación a optimizar el consumo de energía cuando se ejecuta en un dispositivo móvil.
ms.assetid: a956b88c-8a75-4c1c-af27-53c69feb1596
title: Novedades de la administración de energía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6c8394c2e5e6750b5d01fd997d374a9f87e10d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677879"
---
# <a name="whats-new-in-power-management"></a>Novedades de la administración de energía (puede estar en inglés)

Windows 10 ayuda a la aplicación a optimizar el consumo de energía cuando se ejecuta en un dispositivo móvil.

## <a name="battery-saver"></a>Ahorro de batería

En esta versión, se puede notificar a la aplicación cuando el ahorro de batería está activado o desactivado. Al responder a las condiciones de energía cambiantes, la aplicación puede funcionar en concierto con el ahorro de batería para ahorrar energía y ayudar a ampliar la duración de la batería. Para obtener información general sobre el ahorro de batería, consulte [ahorro de batería (en las instrucciones de componentes de hardware)](/windows-hardware/design/component-guidelines/battery-saver).

-   [**GUID \_ de \_ \_ Estado de ahorro de energía**](power-setting-guids.md) : Use este nuevo GUID con la función [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) para recibir una notificación cuando el ahorro de batería esté activado o desactivado.

-   [**Del sistema \_ \_Estado de energía**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) : esta estructura se ha actualizado para admitir el ahorro de batería. El cuarto miembro, **SystemStatusFlag** (anteriormente denominado **Reserved1**), ahora indica si el ahorro de batería está activado o no. Utilice la función [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) para recuperar un puntero a esta estructura.

 

 

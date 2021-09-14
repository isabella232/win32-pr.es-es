---
description: Windows 10 ayuda a la aplicación a optimizar el consumo de energía cuando se ejecuta en un dispositivo móvil.
ms.assetid: a956b88c-8a75-4c1c-af27-53c69feb1596
title: Novedades de Power Management
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6c8394c2e5e6750b5d01fd997d374a9f87e10d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169126"
---
# <a name="whats-new-in-power-management"></a>Novedades de la administración de energía (puede estar en inglés)

Windows 10 ayuda a la aplicación a optimizar el consumo de energía cuando se ejecuta en un dispositivo móvil.

## <a name="battery-saver"></a>Ahorro de batería

En esta versión, se puede notificar a la aplicación ahorro de batería está activada o desactivada. Al responder a las condiciones de energía cambiantes, la aplicación puede trabajar en colaboración con ahorro de batería ahorrar energía y ayudar a ampliar la duración de la batería. Para obtener información general sobre ahorro de batería, [vea ahorro de batería (en las directrices de componentes de hardware).](/windows-hardware/design/component-guidelines/battery-saver)

-   [**GUID \_ ESTADO \_ DE \_ AHORRO DE**](power-setting-guids.md) ENERGÍA: use este nuevo GUID con la función [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) para recibir una notificación cuando ahorro de batería esté activado o desactivado.

-   [**SYSTEM \_ ESTADO \_ DE ENERGÍA:**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) esta estructura se ha actualizado para admitir ahorro de batería. El cuarto miembro, **SystemStatusFlag** (anteriormente denominado **Reserved1),** ahora indica si ahorro de batería está activado o no. Use la [**función GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) para recuperar un puntero a esta estructura.

 

 

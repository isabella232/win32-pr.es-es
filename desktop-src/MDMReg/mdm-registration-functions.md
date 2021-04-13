---
title: Funciones de registro de MDM
description: El registro de MDM usa las siguientes funciones.
ms.assetid: 1b063a56-f59f-4b02-949f-c8b6bbf45a13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821e08d9c6631bbb300a86ab6b9c480a3af0c25b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104359465"
---
# <a name="mdm-registration-functions"></a>Funciones de registro de MDM

El registro de MDM usa las siguientes funciones.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**DiscoverManagementService**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementservice)
</dt> <dd>

Detecta el servicio MDM.

</dd> <dt>

[**DiscoverManagementServiceEx**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementserviceex)
</dt> <dd>

Detecta el servicio MDM mediante un servidor candidato.

</dd> <dt>

[**GetDeviceRegistrationInfo**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getdeviceregistrationinfo)
</dt> <dd>

Recupera la información de registro del dispositivo.

</dd> <dt>

[**GetManagementAppHyperlink**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getmanagementapphyperlink)
</dt> <dd>

Recupera el hipervínculo de la aplicación de administración asociado al servicio MDM.

</dd> <dt>

[**IsDeviceRegisteredWithManagement**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-isdeviceregisteredwithmanagement)
</dt> <dd>

Comprueba si el dispositivo está registrado con un servicio MDM.

</dd> <dt>

[**IsManagementRegistrationAllowed**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-ismanagementregistrationallowed)
</dt> <dd>

Comprueba si la directiva local permite el registro de MDM.

</dd> <dt>

[**RegisterDeviceWithManagement**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagement)
</dt> <dd>

Registra un dispositivo con un servicio MDM mediante el protocolo de [ \[ inscripción MS-MDE \] : dispositivos móviles](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267).

</dd> <dt>

[**RegisterDeviceWithManagementUsingAADCredentials**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagementusingaadcredentials)
</dt> <dd>

Registra un dispositivo con un servicio MDM mediante credenciales Azure Active Directory (AAD).

</dd> <dt>

[**SetManagedExternally**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally)
</dt> <dd>

Indica al agente MDM que el dispositivo se administra externamente y no se va a registrar con un servicio MDM.

</dd> <dt>

[**UnregisterDeviceWithManagement**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-unregisterdevicewithmanagement)
</dt> <dd>

Anula el registro de un dispositivo con el servicio MDM

</dd> </dl>

 

 
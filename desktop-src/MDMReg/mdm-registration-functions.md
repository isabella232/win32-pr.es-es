---
title: Funciones de registro de MDM
description: Las siguientes funciones se declaran en `mdmregistration.h` y se usan en el registro de MDM.
ms.assetid: 1b063a56-f59f-4b02-949f-c8b6bbf45a13
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/19/2020
ms.openlocfilehash: f9149c4bd2f9f931a506dc35d05b5e1c641dc87445fbf88fd73ff9ad20ac514b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040375"
---
# <a name="mdm-registration-functions"></a>Funciones de registro de MDM

Las siguientes funciones se declaran en `mdmregistration.h` y se usan en el registro de MDM.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**DiscoverManagementService**](/windows/win32/api/MDMRegistration/nf-mdmregistration-discovermanagementservice) | Detecta el servicio MDM. |
| [**DiscoverManagementServiceEx**](/windows/win32/api/MDMRegistration/nf-mdmregistration-discovermanagementserviceex) | Detecta el servicio MDM mediante un servidor candidato. |
| [**GetDeviceManagementConfigInfo**](/windows/win32/api/mdmregistration/nf-mdmregistration-getdevicemanagementconfiginfo) | Obtiene la información de configuración asociada al identificador del proveedor. |
| [**GetDeviceRegistrationInfo**](/windows/win32/api/MDMRegistration/nf-mdmregistration-getdeviceregistrationinfo) | Recupera la información de registro del dispositivo. |
| [**GetManagementAppHyperlink**](/windows/win32/api/MDMRegistration/nf-mdmregistration-getmanagementapphyperlink) | Recupera el hipervínculo de la aplicación de administración asociado al servicio MDM. |
| [**IsDeviceRegisteredWithManagement**](/windows/win32/api/MDMRegistration/nf-mdmregistration-isdeviceregisteredwithmanagement) | Comprueba si el dispositivo está registrado con un servicio MDM. |
| [**IsManagementRegistrationAllowed**](/windows/win32/api/MDMRegistration/nf-mdmregistration-ismanagementregistrationallowed) | Comprueba si la directiva local permite el registro de MDM. |
| [**RegisterDeviceWithManagement**](/windows/win32/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagement) | Registra un dispositivo con un servicio MDM mediante [ \[ MS-MDE \] : Protocolo de inscripción de dispositivos móviles](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267). |
| [**RegisterDeviceWithManagementUsingAADCredentials**](/windows/win32/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagementusingaadcredentials) | Registra un dispositivo con un servicio MDM mediante Azure Active Directory credenciales de (AAD). |
| [**SetDeviceManagementConfigInfo**](/windows/win32/api/mdmregistration/nf-mdmregistration-setdevicemanagementconfiginfo) | Establece la información de configuración asociada al identificador del proveedor. |
| [**SetManagedExternally**](/windows/win32/api/MDMRegistration/nf-mdmregistration-setmanagedexternally) | Indica al agente mdm que el dispositivo se administra externamente y que no se va a registrar con un servicio MDM. |
| [**UnregisterDeviceWithManagement**](/windows/win32/api/MDMRegistration/nf-mdmregistration-unregisterdevicewithmanagement) | Anula el registro de un dispositivo con el servicio MDM. |

## <a name="related-topics"></a>Temas relacionados

* [Referencia de registro de MDM](./mdm-registration-reference.md)

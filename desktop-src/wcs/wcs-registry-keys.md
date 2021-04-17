---
title: Claves del Registro de WCS
description: WCS utiliza las claves del registro para indicar que se han producido determinados eventos de Perfil de color. Las aplicaciones deben consultar estas claves del registro para el estado actualizado del perfil de color del sistema.
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- Sistema de color de Windows (WCS), claves del registro
- WCS (sistema de colores de Windows), claves del registro
- Administración del color de imagen, claves del registro
- Administración del color, claves del registro
- colores, claves del registro
- Referencia WCS, claves del registro
- referencia de las claves del registro de WCS
- Sistema de color de Windows (WCS), registro
- WCS (sistema de colores de Windows), registro
- Administración del color de imagen, registro
- Administración del color, registro
- colores, registro
- Referencia WCS, registro
- referencia de WCS, registro
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a1c0072d9a00fe0cff4a4dbe57af839f65731b
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "105721170"
---
# <a name="wcs-registry-keys"></a>Claves del Registro de WCS

WCS utiliza las claves del registro para indicar que se han producido determinados eventos de Perfil de color. Las aplicaciones deben consultar estas claves del registro para el estado actualizado del perfil de color del sistema.

## <a name="active-color-profile-changed"></a>Perfil de color activo cambiado

Las aplicaciones pueden querer responder a los eventos de cambio de Perfil de color de un dispositivo de supervisión. Esto garantiza que siempre tienen información de color precisa para su destino, incluso si el usuario u otra aplicación ha cambiado el perfil activo para el dispositivo.

### <a name="desktop-applications"></a>Aplicaciones de escritorio

Las aplicaciones de escritorio deben escuchar los cambios en el registro para determinar cuándo ha cambiado una asociación de Perfil de color mediante [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue). Una aplicación debe registrarse tanto para los cambios de Asociación de perfil por usuario como para los cambios en todo el sistema.

[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) debe inicializarse con un HKEY proporcionado por [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa). **RegOpenKeyEx** se debe inicializar con las siguientes ubicaciones de árbol del registro:



|                                  |                                                                                                                                                    |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Asociaciones de perfil por usuario    | **HKEY \_ Current \_ User software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ ICM \\ ProfileAssociations \\ Display \\ {4d36e96e-E325-11ce-bfc1-08002be10318}** |
| Asociaciones de perfil en todo el sistema | **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ Class \\ {4d36e96e-E325-11ce-bfc1-08002be10318}**                                        |



 

Cuando se notifica a la aplicación de un cambio de clave del registro, primero debe consultar si se usan asociaciones por usuario o para todo el sistema llamando a [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent). A continuación, debe llamar a [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) con el valor de ámbito de administración de perfiles de WCS adecuado para obtener el nuevo perfil de color activo para el monitor. [**\_ \_ \_**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) Tenga en cuenta que no todos los cambios en las claves del registro se corresponden con un cambio real en el perfil de color activo actualmente. el deberá de la aplicación comprueba si el perfil devuelto por **WcsGetDefaultColorProfile** ha cambiado realmente.

### <a name="universal-windows-uwp-apps"></a>Aplicaciones de Windows universal (UWP)

Las aplicaciones universales de Windows no tienen acceso a las claves del registro anteriores. En su lugar, deben registrar un controlador para el evento [**DisplayInformation. ColorProfileChanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) . Este evento se desencadena cuando cambia el perfil de color activo para el monitor en el que se ejecuta la aplicación. ColorProfileChanged tiene en cuenta si se usan asociaciones de perfil por usuario o por todo el sistema. Esta información se abstrae de las aplicaciones para UWP.

Al responder al evento ColorProfileChanged, la aplicación debe consultar el perfil activo actualmente mediante [**DisplayInformation. GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).

 

 
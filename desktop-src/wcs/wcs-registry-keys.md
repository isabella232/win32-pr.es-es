---
title: Claves del Registro de WCS
description: WCS usa claves del Registro para indicar que se han producido determinados eventos de perfil de color. Las aplicaciones deben consultar estas claves del Registro para ver el estado actualizado del perfil de color del sistema.
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- Windows Sistema de colores (WCS), claves del Registro
- WCS (Windows color), claves del Registro
- administración del color de imagen, claves del Registro
- administración de colores, claves del Registro
- colors,registry keys
- Referencia de WCS, claves del Registro
- referencia de WCS,claves del Registro
- Windows Sistema de colores (WCS), registro
- WCS (Windows Color System),registry
- administración de color de imagen, registro
- administración de colores, registro
- colors,registry
- Referencia de WCS, registro
- referencia de WCS,registry
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c12047d83ccc2f80c26521a59a040fa45df0c21e9bb035efff6ed5d38e8827
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814355"
---
# <a name="wcs-registry-keys"></a>Claves del Registro de WCS

WCS usa claves del Registro para indicar que se han producido determinados eventos de perfil de color. Las aplicaciones deben consultar estas claves del Registro para ver el estado actualizado del perfil de color del sistema.

## <a name="active-color-profile-changed"></a>Perfil de color activo cambiado

Es posible que las aplicaciones quieran responder a eventos de cambio de perfil de color para un dispositivo de supervisión. Esto garantiza que siempre tienen información de color precisa para su destino, incluso si el usuario u otra aplicación ha cambiado el perfil activo del dispositivo.

### <a name="desktop-applications"></a>Aplicaciones de escritorio

Las aplicaciones de escritorio deben escuchar los cambios en el Registro para determinar cuándo ha cambiado una asociación de perfil de color [**mediante RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue). Una aplicación debe registrarse tanto para los cambios de asociación de perfiles por usuario como para los cambios en todo el sistema.

[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) debe inicializarse con un HKEY proporcionado por [**RegOpenKeyEx.**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) **RegOpenKeyEx** debe inicializarse con las siguientes ubicaciones de árbol del Registro:



|    &nbsp;  |  &nbsp;      | 
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Asociaciones de perfil por usuario    | **HKEY \_ CURRENT USER SOFTWARE Microsoft Windows NT \_ \\ \\ \\ CurrentVersion ICM \\ \\ ProfileAssociations \\ Display \\ {4d36e96e-e325-11ce-bfc1-08002be10318}** |
| Asociaciones de perfil de todo el sistema | **Clase de control HKEY \_ LOCAL \_ MACHINE SYSTEM \\ \\ CurrentControlSet \\ \\ \\ {4d36e96e-e325-11ce-bfc1-08002be10318}**                                        |



 

Cuando se notifica a la aplicación un cambio en la clave del Registro, primero debe consultar si se usan asociaciones por usuario o en todo el sistema mediante una llamada a [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent). A continuación, debe llamar [**a WcsGetDefaultColorProfile con**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) el valor de ÁMBITO DE ADMINISTRACIÓN [**DE \_ \_ PERFILES \_ DE WCS**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) correcto para obtener el nuevo perfil de color activo para el monitor. Tenga en cuenta que no todos los cambios de clave del Registro se corresponderán con un cambio real en el perfil de color activo actualmente; La aplicación mush comprueba si el perfil devuelto por **WcsGetDefaultColorProfile** ha cambiado realmente.

### <a name="universal-windows-uwp-apps"></a>Aplicaciones Windows universales (UWP)

Universal Windows Apps no tienen acceso a las claves del Registro anteriores. En su lugar, deben registrar un controlador para el [**evento DisplayInformation.ColorProfileChanged.**](/uwp/api/Windows.Graphics.Display.DisplayInformation) Este evento se activa cada vez que cambia el perfil de color activo para el monitor en el que se ejecuta la aplicación. ColorProfileChanged tiene en cuenta si se usan asociaciones de perfil por usuario o de todo el sistema; esta información se abstrae de las aplicaciones para UWP.

Al responder al evento ColorProfileChanged, la aplicación debe consultar el perfil activo actualmente mediante [**DisplayInformation.GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).

 

 
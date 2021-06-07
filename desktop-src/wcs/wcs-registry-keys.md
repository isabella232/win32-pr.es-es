---
title: Claves del Registro de WCS
description: WCS usa claves del Registro para indicar que se han producido determinados eventos de perfil de color. Las aplicaciones deben consultar estas claves del Registro para obtener el estado actualizado del perfil de color del sistema.
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- Sistema de colores de Windows (WCS), claves del Registro
- WCS (Sistema de colores de Windows), claves del Registro
- administración de colores de imagen, claves del Registro
- administración de colores, claves del Registro
- colors,registry keys
- Referencia de WCS, claves del Registro
- referencia de WCS,claves del Registro
- Sistema de colores de Windows (WCS), registro
- WCS (Sistema de colores de Windows), registro
- administración de colores de imagen, registro
- administración de colores, registro
- colors,registry
- WCS reference,registry
- referencia de WCS,registry
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058ec839b226e96542604f151f06e2654a4180d5
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444676"
---
# <a name="wcs-registry-keys"></a>Claves del Registro de WCS

WCS usa claves del Registro para indicar que se han producido determinados eventos de perfil de color. Las aplicaciones deben consultar estas claves del Registro para obtener el estado actualizado del perfil de color del sistema.

## <a name="active-color-profile-changed"></a>Cambio del perfil de color activo

Es posible que las aplicaciones quieran responder a eventos de cambio de perfil de color para un dispositivo de supervisión. Esto garantiza que siempre tienen información de color precisa para su destino, incluso si el usuario u otra aplicación ha cambiado el perfil activo para el dispositivo.

### <a name="desktop-applications"></a>Aplicaciones de escritorio

Las aplicaciones de escritorio deben escuchar los cambios en el Registro para determinar cuándo han cambiado las asociaciones de un perfil de color [**mediante RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue). Una aplicación debe registrarse tanto para los cambios de asociación de perfiles por usuario como para los cambios en todo el sistema.

[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) debe inicializarse con un HKEY proporcionado por [**RegOpenKeyEx.**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) **RegOpenKeyEx** debe inicializarse con las siguientes ubicaciones de árbol del Registro:



|    &nbsp;  |  &nbsp;      | 
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Asociaciones de perfil por usuario    | **HKEY \_ CURRENT USER SOFTWARE Microsoft Windows NT \_ \\ \\ \\ CurrentVersion \\ ICM \\ ProfileAssociations \\ Display \\ {4d36e96e-e325-11ce-bfc1-08002be10318}** |
| Asociaciones de perfil de todo el sistema | **Clase de control HKEY \_ LOCAL \_ MACHINE SYSTEM \\ \\ CurrentControlSet \\ \\ \\ {4d36e96e-e325-11ce-bfc1-08002be10318}**                                        |



 

Cuando se notifica a la aplicación un cambio de clave del Registro, primero debe consultar si se usan asociaciones por usuario o para todo el sistema mediante una llamada a [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent). A continuación, debe llamar [**a WcsGetDefaultColorProfile con**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) el valor de ÁMBITO DE ADMINISTRACIÓN DE [**\_ \_ PERFILES \_ DE WCS**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) correcto para obtener el nuevo perfil de color activo para el monitor. Tenga en cuenta que no todos los cambios de clave del Registro se corresponderán con un cambio real en el perfil de color activo actualmente. la aplicación mush comprueba si el perfil devuelto por **WcsGetDefaultColorProfile** ha cambiado realmente.

### <a name="universal-windows-uwp-apps"></a>Aplicaciones universales de Windows (UWP)

Las aplicaciones universales de Windows no tienen acceso a las claves del Registro anteriores. En su lugar, deben registrar un controlador para el [**evento DisplayInformation.ColorProfileChanged.**](/uwp/api/Windows.Graphics.Display.DisplayInformation) Este evento se activa cada vez que cambia el perfil de color activo para el monitor en el que se ejecuta la aplicación. ColorProfileChanged tiene en cuenta si se usan asociaciones de perfil por usuario o de todo el sistema; esta información se abstrae de las aplicaciones para UWP.

Al responder al evento ColorProfileChanged, la aplicación debe consultar el perfil activo actualmente mediante [**DisplayInformation.GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).

 

 
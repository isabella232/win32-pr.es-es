---
title: Marcadores personalizados
description: Los sistemas operativos Windows 2000 y versiones posteriores permiten a los desarrolladores proporcionar sus propios marcadores personalizados que funcionan con el servicio de acceso remoto (RAS).
ms.assetid: ad94f38d-812f-4329-8055-6274a21a3242
keywords:
- Marcadores personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35293de408a2a0faa146b93f9b5d5ebccf447acc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271318"
---
# <a name="custom-dialers"></a>Marcadores personalizados

Los sistemas operativos Windows 2000 y versiones posteriores permiten a los desarrolladores proporcionar sus propios marcadores personalizados que funcionan con el servicio de acceso remoto (RAS). El marcador personalizado se implementa como una única biblioteca de vínculos dinámicos (DLL) que exporta los siguientes puntos de entrada:

-   [**RasCustomDial**](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)
-   [**RasCustomDialDlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)
-   [**RasCustomHangup**](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)
-   [**RasCustomEntryDlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)
-   [**RasCustomDeleteEntryNotify**](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

El archivo DLL de marcado personalizado debe exportar todos estos puntos de entrada y debe implementar los puntos de entrada como funciones Unicode. Para obtener más información acerca de estas funciones, consulte la página de referencia de cada función en la Windows SDK referencia del servicio de acceso remoto.

Para que una conexión RAS use el marcador personalizado, la entrada de la libreta de teléfonos para la conexión debe contener la ruta de acceso al archivo DLL de marcado personalizado. Use las funciones de la API de RAS [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) y [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para establecer esta ruta de acceso en el miembro **szCustomDialDll** de la estructura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) para la entrada de la libreta de teléfonos.

## <a name="updating-the-registry-for-custom-dialers"></a>Actualización del registro de marcadores personalizados

Para que el sistema Marque una conexión que utiliza un marcador personalizado, la ruta de acceso al archivo DLL de marcado personalizado debe existir en el siguiente valor del registro.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
                  CustomDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_MULTI_SZ</dd>
</dl>
```

Dado que **CustomDLL** es de tipo **reg \_ multi \_ SZ**, puede contener rutas de acceso a varios archivos dll de marcado personalizado. Debe establecer la ruta de acceso a la DLL de marcado personalizado en este valor del registro, además de la entrada de la libreta de teléfonos de la conexión.

De forma predeterminada, este valor del registro solo lo pueden escribir los usuarios con privilegios de administrador o sistema. Por motivos de seguridad, no cambie los permisos de esta clave del registro.

## <a name="using-custom-dialers-at-system-logon"></a>Uso de marcadores personalizados al iniciar sesión en el sistema

Los sistemas operativos Windows 2000 y versiones posteriores permiten a un usuario establecer una conexión RAS en el momento del inicio de sesión. Para ello, el usuario comprueba el **Inicio de sesión mediante acceso telefónico a redes** en el cuadro de diálogo **información de inicio de sesión** . Cuando el usuario hace clic en el botón Aceptar, el sistema muestra las conexiones disponibles.

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

En la mayoría de los casos, un marcador personalizado funciona con los privilegios de seguridad del usuario que lo invoca. Sin embargo, si se invoca el marcador personalizado durante el inicio de sesión, funciona con privilegios del sistema. Por lo tanto, diseñe el marcador personalizado para que no se pueda usar para infringir la seguridad del sistema. Por ejemplo, el marcador no debería presentar una interfaz de usuario que permita al usuario escribir en el sistema de archivos del equipo. Entre las interfaces de usuario que proporcionan este tipo de acceso se incluyen el cuadro de diálogo **Buscar archivo** , el cuadro de diálogo común **Abrir archivo** y la **ayuda** de Windows.

## <a name="custom-dialer-user-interface-must-support-idcancel"></a>La interfaz de usuario de marcación personalizada debe ser compatible con IDCANCEL

Si el marcador personalizado muestra una interfaz de usuario, la interfaz de usuario debe admitir \_ mensajes de comandos de WM en los que LOWORD (*wParam*) es igual a IDCANCEL.

 

 
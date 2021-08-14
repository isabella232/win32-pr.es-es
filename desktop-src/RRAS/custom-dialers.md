---
title: Marcadores personalizados
description: Windows sistemas operativos 2000 y posteriores permiten a los desarrolladores proporcionar sus propios marcador personalizados que funcionan con el Servicio de acceso remoto (RAS).
ms.assetid: ad94f38d-812f-4329-8055-6274a21a3242
keywords:
- Marcadores personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69b23edd8501929181a54b1b511f365945f8e1c6277056e068cf58fb67bd26c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791505"
---
# <a name="custom-dialers"></a>Marcadores personalizados

Windows sistemas operativos 2000 y posteriores permiten a los desarrolladores proporcionar sus propios marcador personalizados que funcionan con el Servicio de acceso remoto (RAS). El marcador personalizado se implementa como una sola biblioteca de vínculos dinámicos (DLL) que exporta los siguientes puntos de entrada:

-   [**RasCustomDial**](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)
-   [**RasCustomDialDlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)
-   [**RasCustomCustomCustomUp**](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)
-   [**RasCustomEntryDlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)
-   [**RasCustomDeleteEntryNotify**](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

El archivo DLL de marcado personalizado debe exportar todos estos puntos de entrada y debe implementar los puntos de entrada como funciones Unicode. Para obtener más información sobre estas funciones, consulte la página de referencia de cada función en la referencia del servicio de acceso remoto del SDK de Windows.

Para que una conexión RAS use el marcador personalizado, la entrada de la libreta de teléfonos de la conexión debe contener la ruta de acceso al archivo DLL de marcado personalizado. Use las funciones [**rasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) y [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) de la API de RAS para establecer esta ruta de acceso en el **miembro szCustomDialDll** de la estructura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) de la entrada del libro de teléfonos.

## <a name="updating-the-registry-for-custom-dialers"></a>Actualización del Registro para marcador personalizados

Para que el sistema marque una conexión que use un marcador personalizado, la ruta de acceso al archivo DLL de marcado personalizado debe existir en el siguiente valor del Registro.

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
<dd>                  REG_MULTI_SZ</dd>
</dl>
```

Dado **que CustomDLL** es de tipo **REG MULTI \_ \_ SZ,** puede contener rutas de acceso a varios archivos DLL de marcado personalizado. Debe establecer la ruta de acceso al archivo DLL de marcado personalizado en este valor del Registro, además de la entrada de la libreta de teléfonos para la conexión.

De forma predeterminada, este valor del Registro solo lo puede escribir un usuario con privilegios de administrador o sistema. Por motivos de seguridad, no cambie los permisos de esta clave del Registro.

## <a name="using-custom-dialers-at-system-logon"></a>Uso de marcador personalizados en el inicio de sesión del sistema

Windows sistemas operativos 2000 y posteriores permiten a un usuario establecer una conexión RAS en el momento de iniciar sesión. Para ello, el usuario comprueba el inicio **de sesión** mediante redes de acceso telefónico en el cuadro de diálogo **Información de** inicio de sesión. Después de que el usuario haga clic en el botón Aceptar, el sistema mostrará las conexiones disponibles.

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

En la mayoría de los casos, un marcador personalizado funciona con los privilegios de seguridad del usuario que lo invoca. Sin embargo, si el marcador personalizado se invoca en el inicio de sesión, funciona con privilegios del sistema. Por lo tanto, diseñe el marcador personalizado para que no se pueda usar para infringir la seguridad del sistema. Por ejemplo, el marcador no debe presentar una interfaz de usuario que permita al usuario escribir acceso al sistema de archivos del equipo. Las interfaces de usuario que proporcionan este  acceso incluyen el cuadro de diálogo **Buscar archivo,** el cuadro de diálogo común Abrir archivo y Windows **Ayuda .**

## <a name="custom-dialer-user-interface-must-support-idcancel"></a>El marcador personalizado Interfaz de usuario debe admitir IDCANCEL

Si el marcador personalizado muestra una interfaz de usuario, la interfaz de usuario debe admitir mensajes WM COMMAND donde \_ LOWORD(*wParam*) es igual a IDCANCEL.

 

 
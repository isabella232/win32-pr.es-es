---
description: Los proveedores, a menos que sean proveedores desacoplados que se ejecutan dentro de una aplicación, se cargan en un proceso Wmiprvse.exe y no a través de Svchost.exe con un Winmgmt.exe proceso. Para obtener más información, vea Hospedaje y seguridad de proveedores.
ms.assetid: 8958669e-07e6-458c-a7f3-2df21cacc007
ms.tgt_platform: multiple
title: Proveedores de depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84e6245c92ccb47741474cb5d8d47a99b35d7e83107dda96ba8157c66b64a181
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117925241"
---
# <a name="debugging-providers"></a>Proveedores de depuración

Los proveedores, [](gloss-d.md) a menos que sean proveedores desacoplados que se ejecutan dentro de una aplicación, se cargan en un proceso de Wmiprvse.exe y no a través de Svchost.exe con un Winmgmt.exe proceso. Para obtener más información, vea [Provider Hosting and Security](provider-hosting-and-security.md).

Al detenerse en un punto de interrupción, el depurador de Visual Studio inmoviliza todo el proceso de host del proveedor, que suele ser el host compartido Wmiprvse.exe. Esto evita el funcionamiento de cualquier otro componente hospedado en ese proceso, incluida la extensión de Explorador de servidores WMI. Las aplicaciones cliente que llaman al proveedor también se bloquean. Los problemas resultantes son peores en Windows 2000 y versiones anteriores porque el proveedor se carga en el proceso de servicio WMI (Winmgmt.exe).

Si ejecuta WMI Explorador de servidores en otra instancia, Visual Studio IDE no se inmoviliza y puede liberar el punto de interrupción. Se recomienda ejecutar el proveedor en un proceso de hospedaje independiente durante la fase de desarrollo, de modo que la detención en un punto de interrupción solo inmoviliza el proceso que hospeda el proveedor. Las demás funciones de WMI siguen siendo accesibles para wmi Explorador de servidores cualquier otra aplicación o script basado en WMI. Además, si el proveedor se bloquea, no afecta al funcionamiento de otros proveedores cargados en el mismo proceso de host.

Para que el proveedor se cargue en su propio proceso de host, modifique el registro del proveedor para establecer la propiedad [**\_ \_ Win32Provider.HostingModel**](--win32provider.md) en donde MyProvider puede ser cualquier cadena que identifique de forma única al `NetworkServiceHost:[MyProvider]` proveedor. Por ejemplo, use el **\_ \_ valor Win32Provider.ClsId.** Cuando el proveedor esté listo para enviarse, devuelva **\_ \_ Win32Provider.HostingModel** al valor previsto, como **NetworkServiceHost.**

Si no está depurando la carga del proveedor, puede llamar al método Load de la clase [**MsfT \_ Providers**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) para forzar la carga del proveedor y, a continuación, asociarlo al proceso de Wmiprvse.exe que tiene cargado el archivo DLL y depurar según sea necesario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solución de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

[Clases de solución de problemas de WMI](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 

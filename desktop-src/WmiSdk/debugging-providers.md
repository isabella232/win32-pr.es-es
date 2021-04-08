---
description: Los proveedores, a menos que sean proveedores desacoplados que se ejecutan dentro de una aplicación, se cargan en un proceso de Wmiprvse.exe y no a través de Svchost.exe con un proceso de Winmgmt.exe. Para obtener más información, vea hospedaje y seguridad de proveedores.
ms.assetid: 8958669e-07e6-458c-a7f3-2df21cacc007
ms.tgt_platform: multiple
title: Depurar proveedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d9cadb72f512c22c56db2b546b7920b96bfbd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001592"
---
# <a name="debugging-providers"></a>Depurar proveedores

Los proveedores, a menos que sean [*proveedores desacoplados*](gloss-d.md) que se ejecutan dentro de una aplicación, se cargan en un proceso de Wmiprvse.exe y no a través de Svchost.exe con un proceso de Winmgmt.exe. Para obtener más información, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).

Al detenerse en un punto de interrupción, el depurador de Visual Studio inmoviliza todo el proceso de host del proveedor, que suele ser el host compartido Wmiprvse.exe. Esto evita el funcionamiento de cualquier otro componente hospedado en ese proceso, incluida la extensión de Explorador de servidores WMI. También se bloquean las aplicaciones cliente que llaman al proveedor. Los problemas que se producen son peor en Windows 2000 y versiones anteriores porque el proveedor se carga en el proceso del servicio WMI (Winmgmt.exe).

Si ejecuta WMI Explorador de servidores en otra instancia, el IDE de Visual Studio no se inmoviliza y podrá liberar el punto de interrupción. Se recomienda ejecutar el proveedor en un proceso de hospedaje independiente durante la fase de desarrollo, de modo que la detención en un punto de interrupción solo inmoviliza el proceso que hospeda el proveedor. Las demás funciones de WMI continúan siendo accesibles para WMI Explorador de servidores y otras aplicaciones o scripts basados en WMI. Además, si el proveedor se bloquea, no afecta al funcionamiento de otros proveedores cargados en el mismo proceso de host.

Para realizar la carga del proveedor en su propio proceso de host, modifique el registro del proveedor para establecer la propiedad [**\_ \_ Win32Provider. HostingModel**](--win32provider.md) en, `NetworkServiceHost:[MyProvider]` donde DataProvider puede ser cualquier cadena que identifique de forma única el proveedor. Por ejemplo, use el valor **\_ \_ Win32Provider. ClsId** . Cuando el proveedor esté listo para su envío, devuelva **\_ \_ Win32Provider. HostingModel** al valor previsto, como **NetworkServiceHost**.

Si no está depurando la carga del proveedor, puede llamar al [**método Load de la \_ clase de proveedores de msft**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) para forzar la carga del proveedor y, a continuación, asociar al proceso de Wmiprvse.exe que tiene la DLL cargada y depurar según sea necesario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solución de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

[Clases de solución de problemas de WMI](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 

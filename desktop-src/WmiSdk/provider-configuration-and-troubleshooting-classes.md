---
description: La clase Proveedores de MSFT y las clases de solución de problemas de WMI son un grupo de las clases de eventos MSFT acopladas \_ a los eventos del proveedor WMI.
ms.assetid: 5eaf7026-87bf-416b-9a6d-7f92f85b0882
ms.tgt_platform: multiple
title: Clases de configuración y solución de problemas del proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d37443047e9bbde709fc1c7367f0691d16215eff62e39196987b466aea0830
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050503"
---
# <a name="provider-configuration-and-troubleshooting-classes"></a>Clases de configuración y solución de problemas del proveedor

La [**clase \_ Proveedores de MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) y las clases de solución de problemas de WMI son un grupo de las clases de eventos [MSFT](msft-classes.md) acopladas a los eventos del proveedor WMI.

La [**clase MsfT \_ Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) contiene información de configuración para los proveedores e incluye los métodos siguientes que permiten cargar y descargar proveedores, o suspender y reanudar las operaciones del proveedor:

-   [**Método Load de la clase Providers de MSFT \_**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers)
-   [**Método UnLoad de la clase Providers de MSFT \_**](/previous-versions/windows/desktop/wmisystemprov/unload-method-in-class-msft-providers)
-   [**Método Resume de la clase Providers de MSFT \_**](/previous-versions/windows/desktop/wmisystemprov/resume-method-in-class-msft-providers)
-   [**Método Suspend de la clase Providers de MSFT \_**](/previous-versions/windows/desktop/wmisystemprov/suspend-method-in-class-msft-providers)

Las [clases de solución de problemas de WMI](wmi-troubleshooting-classes.md) se denominan para indicar si el evento se desencadena antes o después de un evento de proveedor. Por ejemplo, el objeto [**\_ \_ AccessCheck \_ Pre de MSFT WmiProvider**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) se genera inmediatamente antes de llamar a la implementación del proveedor de **IWbemEventSecurity::AccessCheck**, mientras que el objeto [**MSFT \_ WmiProvider \_ AccessCheck \_ Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) se llama inmediatamente después.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solución de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

[Clases de solución de problemas de WMI](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 

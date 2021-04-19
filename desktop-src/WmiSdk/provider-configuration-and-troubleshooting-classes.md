---
description: La \_ clase de proveedores de msft y las clases de solución de problemas de WMI son un grupo de las clases de eventos msft acopladas a eventos del proveedor WMI.
ms.assetid: 5eaf7026-87bf-416b-9a6d-7f92f85b0882
ms.tgt_platform: multiple
title: Clases de solución de problemas y configuración del proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be63fb5693898541bffae2abcb05b7595ae7fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716201"
---
# <a name="provider-configuration-and-troubleshooting-classes"></a>Clases de solución de problemas y configuración del proveedor

La clase de [**\_ proveedores de msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) y las clases de solución de problemas de WMI son un grupo de las [clases de eventos msft](msft-classes.md) acopladas a eventos del proveedor WMI.

La clase de [**\_ proveedores de msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) contiene información de configuración para los proveedores e incluye los siguientes métodos que le permiten cargar y descargar proveedores, o suspender y reanudar las operaciones del proveedor:

-   [**Método Load de la \_ clase de proveedores msft**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers)
-   [**Método Unload de la \_ clase de proveedores de msft**](/previous-versions/windows/desktop/wmisystemprov/unload-method-in-class-msft-providers)
-   [**Método resume de la \_ clase de proveedores msft**](/previous-versions/windows/desktop/wmisystemprov/resume-method-in-class-msft-providers)
-   [**Método Suspend de la \_ clase de proveedores msft**](/previous-versions/windows/desktop/wmisystemprov/suspend-method-in-class-msft-providers)

Las [clases de solución de problemas de WMI](wmi-troubleshooting-classes.md) se denominan para indicar si el evento se desencadena antes o después de un evento de proveedor. Por ejemplo, el [**objeto \_ \_ \_ anterior AccessCheck WmiProvider AccessCheck**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) se genera inmediatamente antes de llamar a la implementación del proveedor de **IWbemEventSecurity:: AccessCheck**, mientras que el objeto post de la llamada a [**\_ \_ AccessCheck \_ WmiProvider de msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) se llama inmediatamente después de.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solución de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

[Clases de solución de problemas de WMI](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 

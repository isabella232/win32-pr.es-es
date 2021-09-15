---
description: El proveedor WDM (Windows Driver Model) concede acceso a las clases, instancias, métodos y eventos de los controladores de hardware que se ajustan al modelo WDM.
ms.assetid: 2f9749ff-b318-4228-80fd-e3846dde21d2
title: Proveedor de WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d96ce356214f2788d3608b2ba85943e607394cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568097"
---
# <a name="wdm-provider"></a>Proveedor de WDM

El proveedor WDM (Windows Driver Model) concede acceso a las clases, instancias, métodos y eventos de los controladores de hardware que se ajustan al modelo WDM. Las clases para los controladores de hardware residen en el "espacio \\ de nombres wmi raíz".

Las clases WDM se definen principalmente en Wmi.mof.

WDM es una interfaz de sistema operativo a través de la cual los componentes de hardware proporcionan información y notificación de eventos. El proveedor WDM es un proveedor de clases, instancias, eventos y métodos que permite a las aplicaciones de administración acceder a datos y eventos desde controladores de dispositivo habilitados para WMI para WDM. Las clases creadas por el proveedor de WDM para representar los datos del controlador de dispositivo solo residen en el espacio de \\ nombres "WMI raíz". Este espacio de nombres ya debe existir antes de que el proveedor de WDM procese los controladores WDM instalados.

El proveedor de WDM registra información sobre las operaciones de WDM en el archivo WmiProv.log. Para obtener más información, vea [Archivos de registro WMI.](/windows/desktop/WmiSdk/wmi-log-files)

Como proveedor de clases, instancias, métodos y eventos, el proveedor WDM implementa la interfaz [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) estándar, así como los métodos [**IWbemServices siguientes:**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices)

-   [**CreateClassEnumAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [**CreateInstanceEnumAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**GetObjectAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**ExecMethodAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecNotificationQueryAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [**ExecQueryAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**PutInstanceAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

El proveedor wdm admite el evento extrínsico [**WMIEvent,**](/windows/desktop/WmiCoreProv/wmievent) que notifica a WMI los eventos de los controladores basados en WDM. Puede registrar los consumidores de eventos para eventos **WMIEvent** como lo haría con cualquier otro evento. Para obtener más información, vea [Recibir un evento WMI](/windows/desktop/WmiSdk/receiving-a-wmi-event). No se genera ningún evento de creación de clases al iniciar un controlador.

El proveedor WDM admite la clase siguiente:

-   [**WMIBinaryMofResource**](wmibinarymofresource.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proveedores WMI](/windows/desktop/WmiSdk/wmi-providers)
</dt> <dt>

[Acceso a datos desde controladores de dispositivos](/windows/desktop/WmiSdk/accessing-data-from-device-drivers)
</dt> </dl>

 

 

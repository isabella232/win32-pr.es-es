---
description: El proveedor WDM (Modelo de controlador de Windows) concede acceso a las clases, instancias, métodos y eventos de los controladores de hardware que se ajustan al modelo WDM.
ms.assetid: 2f9749ff-b318-4228-80fd-e3846dde21d2
title: Proveedor de WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d96ce356214f2788d3608b2ba85943e607394cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811432"
---
# <a name="wdm-provider"></a>Proveedor de WDM

El proveedor WDM (Modelo de controlador de Windows) concede acceso a las clases, instancias, métodos y eventos de los controladores de hardware que se ajustan al modelo WDM. Las clases para los controladores de hardware residen en el " \\ espacio de nombres WMI raíz".

Las clases WDM se definen principalmente en WMI. mof.

WDM es una interfaz del sistema operativo a través de la cual los componentes de hardware proporcionan información y notificación de eventos. El proveedor de WDM es una clase, una instancia, un evento y un proveedor de métodos que permite a las aplicaciones de administración tener acceso a los datos y eventos de los controladores de dispositivos habilitados para WMI para WDM. Las clases creadas por el proveedor WDM para representar los datos del controlador de dispositivo solo se encuentran en el espacio de nombres "raíz de \\ WMI". Este espacio de nombres ya debe existir antes de que el proveedor de WDM procese los controladores WDM instalados.

El proveedor de WDM registra información acerca de las operaciones WDM en el archivo WmiProv. log. Para obtener más información, consulte [archivos de registro de WMI](/windows/desktop/WmiSdk/wmi-log-files).

Como una clase, una instancia, un método y un proveedor de eventos, el proveedor WDM implementa la interfaz [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) estándar, así como los siguientes métodos [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) :

-   [**CreateClassEnumAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [**CreateInstanceEnumAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**GetObjectAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**ExecMethodAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecNotificationQueryAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [**ExecQueryAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**PutInstanceAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

El proveedor WDM admite el evento extrínseco de [**WMIEvent**](/windows/desktop/WmiCoreProv/wmievent) , que notifica a WMI los eventos de los controladores basados en WDM. Puede registrar los consumidores de eventos para los eventos de **WMIEvent** como lo haría con cualquier otro evento. Para obtener más información, consulte [recibir un evento WMI](/windows/desktop/WmiSdk/receiving-a-wmi-event). No se generan eventos de creación de clase al iniciar un controlador.

El proveedor WDM es compatible con la clase siguiente:

-   [**WMIBinaryMofResource**](wmibinarymofresource.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proveedores WMI](/windows/desktop/WmiSdk/wmi-providers)
</dt> <dt>

[Acceder a los datos desde los controladores de dispositivos](/windows/desktop/WmiSdk/accessing-data-from-device-drivers)
</dt> </dl>

 

 

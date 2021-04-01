---
description: Una de las primeras tareas que debe codificar para un proveedor es el proceso de inicialización, que cubre todas las tareas que debe realizar el proveedor y que le permite enviar y recibir información de WMI, controlar un objeto administrado y realizar otras tareas.
ms.assetid: 3dc145b8-1ce4-4caa-b2ac-31a3681e76f1
ms.tgt_platform: multiple
title: Inicializar un proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14a724d72d5e5c58eff30f2fa61da64d77a493f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913369"
---
# <a name="initializing-a-provider"></a>Inicializar un proveedor

Una de las primeras tareas que debe codificar para un proveedor es el proceso de inicialización, que cubre todas las tareas que debe realizar el proveedor y que le permite enviar y recibir información de WMI, controlar un objeto administrado y realizar otras tareas. Cada tipo de proveedor tiene un conjunto diferente de tareas que debe realizar y tiene un conjunto de interfaces únicas que acompañan.

Sin embargo, todos los proveedores se inicializan a través de la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e informan a WMI de su estado de inicialización a través de la interfaz [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) .

En el procedimiento siguiente se describe cómo inicializar un proveedor.

**Para inicializar un proveedor**

1.  Implemente [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) para su proveedor.

    Cuando WMI determina que un cliente requiere los servicios de un proveedor, WMI carga el proveedor llamando al método [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) .

2.  Implemente las interfaces exclusivas del tipo de proveedor.
3.  Informe a WMI de que el proveedor ha terminado con la inicialización mediante una llamada a [**IWbemProviderInitSink:: SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus).

    Todas las implementaciones de [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) deben llamar a [**IWbemProviderInitSink:: SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) para notificar el estado de inicialización a WMI. El método **SetStatus** permite a WMI determinar si un proveedor está listo para recibir solicitudes y el tipo de solicitudes que el proveedor está listo para recibir.

En el procedimiento siguiente se describe cómo notificar una inicialización correcta.

**Para notificar una inicialización correcta**

-   Establezca el parámetro *IStatus* de [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) en **WBEM \_ S \_ inicializado**.

    Al devolver **WBEM \_ S \_ inicializado**, un proveedor indica una preparación para controlar las solicitudes de aplicaciones, WMI y otros proveedores. Después de haber \_ \_ inicializado WBEM S, WMI realiza una llamada al método [**IWbemProviderInit:: QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) en el proveedor. Esta consulta recupera un puntero a la interfaz principal del proveedor.

En el procedimiento siguiente se describe cómo notificar un error durante la inicialización.

**Para notificar un error durante la inicialización**

-   Establezca el parámetro *IStatus* de [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) en **WBEM \_ E \_**. Los proveedores de vistas de WMI que devuelven **WBEM \_ E \_ no** funcionan correctamente.

    WMI libera el puntero [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) después de que WMI haya obtenido un puntero a la interfaz principal del proveedor o después de que se haya producido un error en la inicialización.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollar un proveedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protección del proveedor](securing-your-provider.md)
</dt> </dl>

 

 




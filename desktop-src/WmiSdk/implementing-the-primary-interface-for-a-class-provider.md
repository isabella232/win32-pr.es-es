---
description: 'Hay dos maneras de implementar un proveedor de clases: implementar la interfaz como proveedor de inserción o como proveedor de extracción.'
ms.assetid: 2c6d3f73-e219-409b-9347-492035c1eb9f
ms.tgt_platform: multiple
title: Implementar la interfaz principal para un proveedor de clases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3ef1b31e1228b832e4d23945f3af0c4df223ddd3edebdd1ec6e34e0e0e8d449
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030445"
---
# <a name="implementing-the-primary-interface-for-a-class-provider"></a>Implementar la interfaz principal para un proveedor de clases

Hay dos maneras de implementar un proveedor de clases: implementar la interfaz como proveedor de inserción o como proveedor de extracción.

En este tema se de abordan las siguientes secciones:

-   [Implementar la interfaz principal para un proveedor de clases push](#implementing-the-primary-interface-for-a-push-class-provider)
-   [Implementar la interfaz principal para un proveedor de clases de extracción](#implementing-the-primary-interface-for-a-pull-class-provider)

## <a name="implementing-the-primary-interface-for-a-push-class-provider"></a>Implementar la interfaz principal para un proveedor de clases push

Mientras que todos los proveedores implementan [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para la inicialización y al menos otra interfaz como interfaz principal, un proveedor de inserción implementa solo **IWbemProviderInit**.

Asegúrese de que la implementación realiza las siguientes tareas:

-   Recupera los datos de clase adecuados.
-   Coloca los datos en el repositorio WMI.
-   Elimina los datos obsoletos.

Después de completar el proceso de inicialización, WMI controla todas las solicitudes de aplicación para las clases que pertenecen al proveedor de inserción sin ninguna interacción adicional del proveedor. Después, el proveedor de inserción actúa eficazmente como un cliente de WMI en lugar de un proveedor. Para obtener más información sobre cómo implementar [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit), vea [Inicializar un proveedor](initializing-a-provider.md).

> [!Note]  
> Al llamar a WMI para crear, actualizar o quitar datos en un proveedor de inserción, establezca el parámetro *lFlags* para incluir la marca **WBEM \_ FLAG \_ OWNER \_ UPDATE** en todas las llamadas a [**métodos IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)

 

## <a name="implementing-the-primary-interface-for-a-pull-class-provider"></a>Implementar la interfaz principal para un proveedor de clases de extracción

Un proveedor de extracción de clase debe [**implementar IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) como la interfaz principal. La **interfaz IWbemServices** admite la recuperación de datos, la actualización de datos, la eliminación de datos, la enumeración y el procesamiento de consultas. Sin embargo, dado que las aplicaciones y los proveedores también usan **IWbemServices** para solicitar servicios de WMI, **IWbemServices** contiene muchos métodos que son irrelevantes para un proveedor de clases. La implementación debe admitir la recuperación y enumeración de clases, a través de [**los métodos GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) y [**CreateClassEnumAsync,**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) respectivamente. En la tabla siguiente se enumeran los **métodos IWbemServices asincrónicos** adicionales que puede implementar para un proveedor de clases.



| Método                                                     | Característica      |
|------------------------------------------------------------|--------------|
| [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) | Modificación |
| [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) | Eliminación     |



 

> [!Note]  
> Dado que es posible que la devolución de llamada al receptor no se devuelva en el mismo nivel de autenticación que requiere el cliente, se recomienda usar la comunicación semisincronosa en lugar de la comunicación asincrónica. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

 

El proveedor de clases debe proporcionar una implementación de código auxiliar que devuelva **WBEM \_ E PROVIDER \_ NOT \_ \_ CAPABLE** para todos los demás [**métodos IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que no admiten el conjunto de características. En concreto, WMI no admite el procesamiento de consultas para los proveedores de clases. Por lo tanto, un proveedor de clases debe devolver **WBEM \_ E PROVIDER NOT \_ \_ \_ CAPABLE** desde su implementación de [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync), establecer su propiedad de registro **QuerySupportLevels** en **NULL** o ambos.

Las interfaces que implementa un proveedor de clases son muy similares a las interfaces de un proveedor de instancias y un proveedor de métodos. De hecho, un único proveedor puede actuar como los tres tipos de proveedor implementando todos los métodos y registrándose correctamente.

 

 




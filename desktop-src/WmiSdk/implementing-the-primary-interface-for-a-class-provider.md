---
description: 'Hay dos maneras de implementar un proveedor de clases: implementar la interfaz como un proveedor de inserción o como un proveedor de extracción.'
ms.assetid: 2c6d3f73-e219-409b-9347-492035c1eb9f
ms.tgt_platform: multiple
title: Implementar la interfaz principal para un proveedor de clases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f760dba053cadf56d37445c997fc52a99b242a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360944"
---
# <a name="implementing-the-primary-interface-for-a-class-provider"></a>Implementar la interfaz principal para un proveedor de clases

Hay dos maneras de implementar un proveedor de clases: implementar la interfaz como un proveedor de inserción o como un proveedor de extracción.

En este tema se describen las siguientes secciones:

-   [Implementar la interfaz principal para un proveedor de clase de inserciones](#implementing-the-primary-interface-for-a-push-class-provider)
-   [Implementar la interfaz principal para un proveedor de clase de extracción](#implementing-the-primary-interface-for-a-pull-class-provider)

## <a name="implementing-the-primary-interface-for-a-push-class-provider"></a>Implementar la interfaz principal para un proveedor de clase de inserciones

Mientras que todos los proveedores implementan [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para la inicialización y al menos otra interfaz como su interfaz principal, un proveedor de inserciones solo implementa **IWbemProviderInit**.

Asegúrese de que la implementación realiza las siguientes tareas:

-   Recupera los datos de clase adecuados.
-   Coloca los datos en el repositorio WMI.
-   Elimina los datos obsoletos.

Después de completar el proceso de inicialización, WMI controla todas las solicitudes de aplicación para las clases que pertenecen al proveedor de inserciones sin más interacción con el proveedor. Después, el proveedor de inserciones actúa eficazmente como un cliente de WMI en lugar de un proveedor. Para obtener más información sobre la implementación de [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit), vea [inicializar un proveedor](initializing-a-provider.md).

> [!Note]  
> Al llamar a WMI para crear, actualizar o quitar datos en un proveedor de inserciones, establezca el parámetro *lFlags* para incluir la marca de actualización del propietario de la **\_ marca \_ \_ WBEM** en todas las llamadas a métodos [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

 

## <a name="implementing-the-primary-interface-for-a-pull-class-provider"></a>Implementar la interfaz principal para un proveedor de clase de extracción

Un proveedor de extracción de clases debe implementar [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) como la interfaz principal. La interfaz **IWbemServices** admite la recuperación de datos, la actualización de datos, la eliminación de datos, la enumeración y el procesamiento de consultas. Sin embargo, dado que las aplicaciones y los proveedores también usan **IWbemServices** para solicitar servicios de WMI, **IWbemServices** contiene muchos métodos que son irrelevantes para un proveedor de clases. La implementación de debe admitir la recuperación y enumeración de clases, a través de los métodos [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) y [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) , respectivamente. En la tabla siguiente se enumeran los métodos **IWbemServices** asincrónicos adicionales que se pueden implementar para un proveedor de clases.



| Método                                                     | Característica      |
|------------------------------------------------------------|--------------|
| [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) | Modificación |
| [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) | Eliminación     |



 

> [!Note]  
> Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

 

El proveedor de clases debe proporcionar una implementación de código auxiliar que devuelva el **\_ proveedor WBEM E \_ no sea \_ \_ compatible** con todos los demás métodos [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que no admitan su conjunto de características. En concreto, WMI no admite el procesamiento de consultas para los proveedores de clases. Como tal, un proveedor de clases debe devolver el **proveedor de WBEM \_ E \_ \_ no \_ compatible** desde su implementación de [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync), establezca su propiedad de registro **QuerySupportLevels** en **null** o en ambas.

Las interfaces que implementa un proveedor de clases son muy similares a las interfaces de un proveedor de instancias y un proveedor de métodos. De hecho, un solo proveedor puede actuar como los tres tipos de proveedor implementando todos los métodos y registrando correctamente.

 

 




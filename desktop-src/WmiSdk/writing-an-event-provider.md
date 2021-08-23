---
description: Un proveedor de eventos es un objeto COM que proporciona a WMI notificaciones de eventos intrínsecos y extrínsecos.
ms.assetid: 075bdc65-4ea3-4f91-9823-1d2d0dc13423
ms.tgt_platform: multiple
title: Escribir un proveedor de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04abf060ef5316790b04682430abd92d0a6bea31175f0e192fc7f73d047633d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757215"
---
# <a name="writing-an-event-provider"></a>Escribir un proveedor de eventos

Un proveedor de eventos es un objeto COM que proporciona a WMI notificaciones de eventos intrínsecos y extrínsecos. Un evento intrínseco notifica un cambio de datos interno a WMI, mientras que un evento extrínseco notifica un evento definido por el usuario no descrito por un evento intrínseco. Por ejemplo, un evento en respuesta a los cambios, la creación o la eliminación de la clase [**\_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) se clasificaría como un evento intrínseco. Un evento que se genera en función de algo distinto de la modificación, creación o eliminación de un objeto WMI existente es un evento extrínsico. Independientemente de la clase admitida, puede implementar todos los proveedores de eventos de la misma manera.

En el procedimiento siguiente se describe cómo implementar un proveedor de eventos.

**Para implementar un proveedor de eventos**

1.  Diseñe y registre el proveedor de clases con WMI.

    Los proveedores de clases se registran con WMI mediante la creación de una [**\_ \_ instancia de Win32Provider**](--win32provider.md) y una [**\_ \_ clase EventProviderRegistration.**](--eventproviderregistration.md) Para obtener más información, [vea Registrar un proveedor de eventos.](registering-an-event-provider.md)

2.  Implemente [**la interfaz IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para el proveedor.

    La [**interfaz IWbemProviderInit es**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) una interfaz común que WMI usa para cargar e inicializar todos los proveedores. Para obtener más información, vea [Inicializar un proveedor.](initializing-a-provider.md)

3.  Implemente [**IWbemEventProvider como**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) interfaz principal para el proveedor.

    La [**interfaz IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) usa el **método ProviderEvents** para proporcionar eventos a WMI. Para obtener más información, vea [Implementar la interfaz principal para un proveedor de eventos](implementing-the-primary-interface-for-an-event-provider.md).

    > [!Note]  
    > Los proveedores de eventos deben usar el modelo de multithreading "Both".

     

4.  Opcionalmente, también puede implementar la [**interfaz IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) para aumentar el rendimiento del proveedor de eventos.

    La [**interfaz IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) permite al proveedor optimizar las consultas antes de enviar una respuesta a WMI y es más útil para un proveedor que proporciona eventos de varios tipos y que necesita realizar tantas optimizaciones internas como sea posible. Para obtener más información, vea [Optimizar un proveedor de eventos.](optimizing-an-event-provider.md)

5.  Implemente [**la interfaz IWbemEventProviderSecurity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) para limitar los consumidores a determinados identificadores de seguridad (SID) o implemente [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) para proteger el propio receptor. El proveedor también puede establecer la propiedad **\_ DESCRIPTOR DE SEGURIDAD** en la clase de eventos para proteger eventos individuales en el código MOF. Para obtener más información, [vea Securing WMI Events](securing-wmi-events.md).
6.  Agregue cualquier código adicional necesario para el proveedor.

    Al diseñar el proveedor, lo más probable es que tenga que llamar a interfaces WMI. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

    Al recuperar información para un cliente, es posible que tenga que acceder a los niveles de seguridad de ese cliente. Para obtener más información, [vea Suplantar un cliente.](impersonating-a-client.md)

7.  Reemplace el proveedor existente por el nuevo código.

    No es necesario realizar este paso si no tiene un proveedor preexistnte sobre el que copiar. Para obtener más información, vea [Actualizar un proveedor](updating-a-provider.md).

Una aplicación cliente puede solicitar un evento registrándose en WMI como consumidor de eventos. Para obtener más información, vea [Recibir un evento WMI](receiving-a-wmi-event.md).

 

 

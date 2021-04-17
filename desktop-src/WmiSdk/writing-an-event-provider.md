---
description: Un proveedor de eventos es un objeto COM que proporciona a WMI notificaciones de eventos intrínsecos y extrínsecos.
ms.assetid: 075bdc65-4ea3-4f91-9823-1d2d0dc13423
ms.tgt_platform: multiple
title: Escribir un proveedor de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb118d89f214e9fc651c1c9d93abfcfe43f49fc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715814"
---
# <a name="writing-an-event-provider"></a>Escribir un proveedor de eventos

Un proveedor de eventos es un objeto COM que proporciona a WMI notificaciones de eventos intrínsecos y extrínsecos. Un evento intrínseco informa de un cambio de datos interno en WMI, mientras que un evento extrínseco informa de un evento definido por el usuario no descrito por un evento intrínseco. Por ejemplo, un evento en respuesta a los cambios, la creación o la eliminación de la clase [**\_ DiscoLógico de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) clasificaría como un evento intrínseco. Un evento que se genera en función de algo distinto de la modificación, creación o eliminación de un objeto WMI existente es un evento extrínseco. Independientemente de la clase admitida, puede implementar todos los proveedores de eventos de la misma manera.

En el procedimiento siguiente se describe cómo implementar un proveedor de eventos.

**Para implementar un proveedor de eventos**

1.  Diseñe y registre el proveedor de clases con WMI.

    Los proveedores de clases se registran en WMI mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y una clase [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) . Para obtener más información, vea [registrar un proveedor de eventos](registering-an-event-provider.md).

2.  Implemente la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para el proveedor.

    La interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) es una interfaz común que WMI usa para cargar e inicializar todos los proveedores. Para obtener más información, vea [inicializar un proveedor](initializing-a-provider.md).

3.  Implemente [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) como la interfaz principal para el proveedor.

    La interfaz [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) utiliza el método **ProviderEvents** para proporcionar eventos a WMI. Para obtener más información, vea [implementar la interfaz principal para un proveedor de eventos](implementing-the-primary-interface-for-an-event-provider.md).

    > [!Note]  
    > Los proveedores de eventos deben usar el modelo de multithreading "both".

     

4.  Opcionalmente, también puede implementar la interfaz [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) para aumentar el rendimiento del proveedor de eventos.

    La interfaz [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) permite al proveedor optimizar las consultas antes de enviar una respuesta a WMI, y es muy útil para un proveedor que proporciona eventos de varios tipos y que necesita realizar tantas optimizaciones internas como sea posible. Para obtener más información, consulte [optimización de un proveedor de eventos](optimizing-an-event-provider.md).

5.  Implemente la interfaz [**IWbemEventProviderSecurity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) para limitar a los consumidores a determinados identificadores de seguridad (SID) o implemente [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) para proteger el receptor. El proveedor también puede establecer la propiedad del **\_ descriptor de seguridad** en la clase de eventos para proteger los eventos individuales en el código MOF. Para obtener más información, consulte [protección de eventos WMI](securing-wmi-events.md).
6.  Agregue el código adicional necesario para el proveedor.

    Al diseñar el proveedor, lo más probable es que necesite llamar a interfaces de WMI. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

    Al recuperar información de un cliente, es posible que necesite tener acceso a los niveles de seguridad de ese cliente. Para obtener más información, vea [Suplantar a un cliente](impersonating-a-client.md).

7.  Reemplace el proveedor preexistente con el código nuevo.

    No es necesario que realice este paso si no tiene un proveedor preexistente en el que realizar la copia. Para obtener más información, consulte [actualización de un proveedor](updating-a-provider.md).

Una aplicación cliente puede solicitar un evento registrándose a sí mismo con WMI como consumidor de eventos. Para obtener más información, consulte [recibir un evento WMI](receiving-a-wmi-event.md).

 

 

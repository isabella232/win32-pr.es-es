---
description: Mediante el uso de la clase SMTPEventConsumer, puede enviar un correo electrónico a un usuario designado cuando se produce un evento especificado. Esta clase es un consumidor de eventos estándar que proporciona WMI.
ms.assetid: ed10e6f7-8e18-4cde-bd46-a7791547c7da
ms.tgt_platform: multiple
title: Envío de correo electrónico basado en un evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68bcef0858f7022fcb36006f038b20dedc940da60ee6c61e0372f5a74663093a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860433"
---
# <a name="sending-email-based-on-an-event"></a>Envío de correo electrónico basado en un evento

Mediante el uso [de la clase SMTPEventConsumer,](smtpeventconsumer.md) puede enviar un correo electrónico a un usuario designado cuando se produce un evento especificado. Esta clase es un [consumidor de eventos estándar](standard-consumer-classes.md) que proporciona WMI.

La [clase SMTPEventConsumer](smtpeventconsumer.md) requiere las siguientes condiciones para enviar un mensaje de correo electrónico en respuesta a un evento:

-   La [clase SMTPEventConsumer](smtpeventconsumer.md) debe compilarse en el espacio de nombres correcto. Para obtener más información, [vea Supervisión y respuesta a eventos con consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md)
-   Debe existir un servidor SMTP en la red.
-   El mensaje de correo electrónico no puede tener datos adjuntos.
-   El mensaje de correo electrónico debe codificarse en US-ASCII.

El procedimiento básico para usar consumidores estándar es siempre el mismo y se encuentra en Supervisión y respuesta a [eventos con consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md) El procedimiento siguiente agrega al procedimiento básico; es específico de la [clase SMTPEventConsumer;](smtpeventconsumer.md) y describe cómo crear un consumidor de eventos que envía correo electrónico.

En el procedimiento siguiente se describe cómo crear un consumidor de eventos que envía correo electrónico.

**Para crear un consumidor de eventos que envíe correo electrónico**

1.  Instale y registre la [clase SMTPEventConsumer,](smtpeventconsumer.md) si es necesario.

    El programa de instalación de WMI compila la clase [SMTPEventConsumer](smtpeventconsumer.md) en el espacio de nombres de suscripción \\ raíz.

2.  Identifique el evento que desea supervisar y cree la consulta de eventos.

    Puede haber un evento intrínseco existente que use para supervisar el evento. La mayoría de los eventos intrínsecos están asociados a cambios en las instancias de clase del espacio de nombres \\ "root cimv2". Al analizar las clases de la referencia [Clases WMI,](wmi-classes.md) es probable que encuentre una clase que identifique el evento que desea supervisar. Por ejemplo, use la [**clase \_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) para supervisar los cambios en una unidad de disco duro.

    Si no hay ningún evento intrínseco existente que use, podría haber un proveedor de eventos extrínseco que pueda funcionar. Por ejemplo, use la [**clase RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) del proveedor del Registro para supervisar los cambios en el registro del sistema.

    Si no existe una clase que identifique el evento que desea supervisar, debe crear su propio proveedor de eventos y definir nuevas clases de eventos extrínsecos. Para obtener más información, vea [Escribir un proveedor de eventos.](writing-an-event-provider.md)

3.  En el Managed Object Format (MOF), cree una instancia de [SMTPEventConsumer](smtpeventconsumer.md) para recibir eventos.

    Use las propiedades de la instancia de para definir el mensaje de correo electrónico que se enviará cuando se produzca un evento. Por ejemplo, la **propiedad ToLine** define la dirección de correo electrónico y la **propiedad Message** define el texto del mensaje de correo electrónico. Debe definir la dirección de correo electrónico, el asunto y el texto de un mensaje, pero un mensaje de correo electrónico no puede tener datos adjuntos. Para obtener más información, vea [Designing Managed Object Format (MOF) Classes .](designing-managed-object-format--mof--classes.md)

4.  Cree una consulta de eventos que especifique los eventos que desea supervisar.

    Para obtener más información, [vea Consulta con WQL.](querying-with-wql.md)

5.  Cree una instancia de [**\_ \_ EventFilter y**](--eventfilter.md) almacene la consulta en la **propiedad Query.**

    Para obtener más información, [vea Consulta con WQL.](querying-with-wql.md)

6.  Cree una instancia de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para asociar el filtro y el consumidor.
7.  Compile el archivo MOF mediante [**Mofcomp.exe**](mofcomp.md).


## <a name="example"></a>Ejemplo

El ejemplo de esta sección está en código MOF, pero puede crear las instancias mediante programación mediante [scripting API](scripting-api-for-wmi.md) para WMI o la API COM [para WMI.](com-api-for-wmi.md)

En el procedimiento siguiente se describe cómo usar el ejemplo.

**Para usar el ejemplo**

1.  Copie el siguiente MOF en un archivo de texto y guárdelo con una extensión .mof.
2.  En una ventana del símbolo del sistema, compile el archivo MOF con el siguiente comando:

    Nombre de archivo *Mofcomp:.mof* *

> [!Note]  
> Cuando el código MOF se compila en el espacio de nombres de la suscripción \\ raíz, [SMTPEventConsumer](smtpeventconsumer.md) se compila en el mismo espacio de nombres.

 

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of __EventFilter as $FILTER
{
    Name = "LowDiskspaceFilter";
    
    EventNamespace = "\\\\.\\root\\cimv2";  

    Query = "SELECT * FROM __InstanceModificationEvent WITHIN 10 "
            "WHERE TargetInstance ISA \"Win32_LogicalDisk\" "
            "AND TargetInstance.FreeSpace < 846000000 "
            "AND PreviousInstance.FreeSpace >= 846000000 "
            "AND (TargetInstance.DeviceID = \"C:\" "
            "OR TargetInstance.DeviceID = \"D:\")";
    QueryLanguage = "WQL";
};


instance of SMTPEventConsumer as $CONSUMER
{
    Name = "LowDisk";
    ToLine = "SysAd@MyCompany.com, MyAlias@MyCompany.com";
    CcLine = "MyHome@MyISP.com";
    ReplyToLine = "MyAlias@MyCompany.com";
    SMTPServer = "SmartHost";
    Subject = "WARNING: Low disk space";
    Message = "WARNING: Your %TargetInstance.DeviceID% is"
        " getting dangerously low.";
};

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER ;
    Filter = $FILTER ;
};
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 

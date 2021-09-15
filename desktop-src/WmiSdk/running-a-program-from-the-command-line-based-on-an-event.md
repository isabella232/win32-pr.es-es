---
description: La clase CommandLineEventConsumer ejecuta un programa ejecutable especificado desde una línea de comandos cuando se produce un evento especificado. Esta clase es un consumidor de eventos estándar que proporciona WMI.
ms.assetid: b912a4a1-7b1c-43a9-b098-fcfd62a2c2db
ms.tgt_platform: multiple
title: Ejecutar un programa desde la línea de comandos basado en un evento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: de7f4fb5e679a6b5767635c70e2ffb5eda3ba800
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359098"
---
# <a name="running-a-program-from-the-command-line-based-on-an-event"></a>Ejecutar un programa desde la línea de comandos basado en un evento

La [**clase CommandLineEventConsumer**](commandlineeventconsumer.md) ejecuta un programa ejecutable especificado desde una línea de comandos cuando se produce un evento especificado. Esta clase es un consumidor de eventos estándar que proporciona WMI.

Al usar [**CommandLineEventConsumer,**](commandlineeventconsumer.md)debe proteger el archivo ejecutable que desea iniciar. Si el ejecutable no está en una ubicación segura o no está protegido con una lista de control de acceso seguro (ACL), un usuario sin privilegios de acceso puede reemplazar el ejecutable por otro ejecutable. Puede usar las clases [**\_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) o [**Win32 \_ LogicalShareSecuritySetting de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) para cambiar mediante programación la seguridad de un archivo o recurso compartido. Para obtener más información, [vea Crear un descriptor de seguridad para un nuevo objeto en C++.](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)

El procedimiento básico para usar consumidores estándar es siempre el mismo y se encuentra en Supervisión y respuesta a eventos [con consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md) El siguiente procedimiento se agrega al procedimiento básico, es específico de la clase [**CommandLineEventConsumer**](commandlineeventconsumer.md) y describe cómo crear un consumidor de eventos que ejecuta un programa.

> [!Caution]
>
> La [**clase CommandLineEventConsumer**](commandlineeventconsumer.md) tiene restricciones de seguridad especiales. Un miembro local del grupo Administradores del equipo local debe configurar este consumidor estándar. Si usa una cuenta de dominio para crear la suscripción, la cuenta LocalSystem debe tener los permisos necesarios en el dominio para comprobar que el creador es miembro del grupo de administradores local.
>
> [**CommandLineEventConsumer**](commandlineeventconsumer.md) no se puede usar para iniciar un proceso que se ejecuta de forma interactiva.

 

En el procedimiento siguiente se describe cómo crear un consumidor de eventos que ejecuta un proceso desde una línea de comandos.

**Para crear un consumidor de eventos que ejecuta un proceso desde una línea de comandos**

1.  En el Managed Object Format (MOF), cree una instancia de [**CommandLineEventConsumer**](commandlineeventconsumer.md) para recibir los eventos que solicite en la consulta. Para obtener más información, vea [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).
2.  Cree una instancia de [**\_ \_ EventFilter**](--eventfilter.md) y asíéle un nombre.
3.  Cree una consulta para especificar el tipo de evento. Para obtener más información, [vea Consulta con WQL.](querying-with-wql.md)
4.  Cree una instancia de [**\_ \_ FilterToConsumerBinding para**](--filtertoconsumerbinding.md) asociar el filtro a la instancia de [**CommandLineEventConsumer**](commandlineeventconsumer.md).
5.  Compile el archivo MOF mediante [**Mofcomp.exe**](mofcomp.md).

## <a name="example"></a>Ejemplo

En el ejemplo de código siguiente se crea una nueva clase denominada "MyCmdLineConsumer" para generar eventos cuando se crea una instancia de la nueva clase al final de un MOF. El ejemplo está en código MOF, pero puede crear las instancias mediante programación mediante [scripting API](scripting-api-for-wmi.md) para WMI o la API COM [para WMI.](com-api-for-wmi.md)

En el procedimiento siguiente se describe cómo crear una nueva clase denominada MyCmdLineConsumer.

**Para crear una nueva clase denominada MyCmdLineConsumer**

1.  Cree el archivo c: cmdlinetest.bat con un comando que ejecuta un programa visible, como \\ \_ "calc.exe".
2.  Copie el MOF en un archivo de texto y guárdelo con una extensión .mof.
3.  En una ventana Comandos, compile el archivo MOF mediante el siguiente comando: **Mofcomp filename.mof**.

> [!Note]  
> El programa especificado en cmdline \_test.bat debe ejecutarse.

 

``` syntax
// Set the namespace as root\subscription.
// The CommandLineEventConsumer is already compiled
// in the root\subscription namespace. 
#pragma namespace ("\\\\.\\Root\\subscription")

class MyCmdLineConsumer
{
 [key]string Name;
};

// Create an instance of the command line consumer
// and give it the alias $CMDLINECONSUMER

instance of CommandLineEventConsumer as $CMDLINECONSUMER
{
 Name = "CmdLineConsumer_Example";
 CommandLineTemplate = "c:\\cmdline_test.bat";
 RunInteractively = True;
 WorkingDirectory = "c:\\";
};    

// Create an instance of the event filter
// and give it the alias $CMDLINEFILTER
// The filter queries for instance creation event
// for instances of the MyCmdLineConsumer class

instance of __EventFilter as $CMDLINEFILTER
{
    Name = "CmdLineFilter";
    Query = "SELECT * FROM __InstanceCreationEvent"
        " WHERE TargetInstance.__class = \"MyCmdLineConsumer\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding
// between filter and consumer instances.

instance of __FilterToConsumerBinding
{
     Consumer = $CMDLINECONSUMER;
     Filter = $CMDLINEFILTER;
};

// Create an instance of this class right now. 
// The commands in c:\\cmdline_test.bat execute
// as the result of creating the instance
// of MyCmdLineConsumer.
 
instance of MyCmdLineConsumer
{
     Name = "CmdLineEventConsumer test";
};
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 

---
description: Ejecuta un script predefinido en un lenguaje de scripting arbitrario cuando se le entrega un evento.
ms.assetid: 2c0aa216-4255-49ff-9bbd-d6c62b5b9139
ms.tgt_platform: multiple
title: Clase ActiveScriptEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActiveScriptEventConsumer
- ActiveScriptEventConsumer.CreatorSID
- ActiveScriptEventConsumer.KillTimeout
- ActiveScriptEventConsumer.MachineName
- ActiveScriptEventConsumer.MaximumQueueSize
- ActiveScriptEventConsumer.Name
- ActiveScriptEventConsumer.ScriptingEngine
- ActiveScriptEventConsumer.ScriptFileName
- ActiveScriptEventConsumer.ScriptText
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: 11e2886fd5d0804946433e102e24617df768dcec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716703"
---
# <a name="activescripteventconsumer-class"></a>Clase ActiveScriptEventConsumer

La clase **ActiveScriptEventConsumer** ejecuta un script predefinido en un lenguaje de scripting arbitrario cuando se le entrega un evento. Esta clase es uno de los consumidores de eventos estándar que proporciona WMI. Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).


```cmd
Mofcomp -n:root\<namespace> scrcons.mof
```



Puede configurar el rendimiento de todas las instancias de **ActiveScriptEventConsumer** en un sistema mediante el establecimiento de los valores de la propiedad [**timeout**](scriptingstandardconsumersetting.md) o **MaximumScripts** en la instancia única de **ScriptingStandardConsumerSetting**.

## <a name="syntax"></a>Sintaxis

``` syntax
[AMENDMENT]
class ActiveScriptEventConsumer : __EventConsumer
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  uint32 KillTimeout = 0;
  string MachineName;
  uint32 MaximumQueueSize;
  string Name;
  string ScriptingEngine;
  string ScriptFileName;
  string ScriptText;
};
```

## <a name="members"></a>Miembros

La clase **ActiveScriptEventConsumer** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **ActiveScriptEventConsumer** tiene estas propiedades.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz que representa el identificador de seguridad (SID), que identifica de forma única al creador del consumidor de eventos de script activo. Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**KillTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número, en segundos, que se permite ejecutar el script. Si es 0 (cero), que es el valor predeterminado, el script no se termina.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del equipo al que WMI envía eventos. Por Convención de los consumidores estándar de Microsoft, el consumidor de script no se puede ejecutar de forma remota. Los consumidores de terceros también pueden usar esta propiedad. Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cola máxima, en bytes, para el consumidor de eventos de script activo. Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [ **clave**](standard-qualifiers.md)
</dt> </dl>

Identificador único para el consumidor de eventos. Si cambia el nombre del consumidor, el resultado son dos consumidores iguales que tienen nombres diferentes.

</dd> <dt>

**ScriptFileName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del archivo desde el que se lee el texto del script, diseñado como una alternativa a especificar el texto del script en la propiedad **ScriptText** . Esta propiedad debe ser **null** si la propiedad **ScriptText** no es **null**.

> [!Note]  
> Cuando se especifica **ScriptFileName**, es importante proteger el archivo ejecutable que se está iniciando. Si el archivo ejecutable no está en una ubicación segura o está protegido con una lista de control de acceso (ACL) segura, cualquiera puede reemplazar el ejecutable por otro diferente. Para obtener más información acerca de las ACL, vea [crear un descriptor de seguridad (SD) para un nuevo objeto en C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

</dd> <dt>

**ScriptingEngine**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del motor de scripting que se va a usar, por ejemplo, "VBScript". Esta propiedad no puede ser **null**.

</dd> <dt>

**ScriptText**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Texto del script que se expresa en un lenguaje conocido por el motor de scripting. Esta propiedad debe ser **null** si la propiedad **ScriptFileName** no es **null**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta clase se deriva de la clase abstracta [**\_ \_ EventConsumer**](--eventconsumer.md) . Se encuentra en el espacio de \\ nombres de la suscripción raíz.

Cuando se especifica el texto de un script en la instancia de consumidor de eventos, el script tiene acceso a la instancia de evento en la variable de entorno de script **TargetEvent**.

Los scripts se ejecutan en el contexto de seguridad de LocalSystem. Como medida de seguridad, solo un administrador del sistema local o un administrador de dominio puede configurar el consumidor de scripting. Los derechos de acceso no se comprueban hasta el tiempo de ejecución. Una vez configurado el consumidor, cualquier usuario puede desencadenar el evento que provoca el script.

Un error al cargar el motor de scripting o analizar y validar el script se considera un error. Los códigos de retorno de error del script y el final del script mediante un tiempo de espera también se consideran errores.

El valor de **ScriptText** o **ScriptFileName** debe ser not **null**. Si ambas propiedades son **null** o not **null**, se genera un error.

Cuando WMI se ejecuta como un servicio, los scripts ejecutados por **ActiveScriptEventConsumer** no generan resultados de pantalla. Los scripts que usan **MsgBox** se ejecutan, pero no muestran información en la pantalla. No se admite la ejecución del servicio WMI como un archivo ejecutable, pero WMI permite que los scripts que utilizan la función **MsgBox** muestren la salida o acepten datos proporcionados por el usuario. No se puede usar ninguno de los métodos proporcionados por el objeto [Wscript](/previous-versions//at5ydy31(v=vs.85)) porque **ActiveScriptEventConsumer** no utiliza Windows Script Host (WSH).

## <a name="examples"></a>Ejemplos

El ejemplo de [creación de registro de eventos de WMI permanente para supervisar archivos](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) de PowerShell en la galería de TechNet usa **ActiveScriptEventConsumer** como parte de un script complejo para configurar un registro de eventos de WMI permanente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Espacio de nombres<br/>                | \\Suscripción raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Scrcons. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scrcons.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de consumidor estándar](standard-consumer-classes.md)
</dt> <dt>

[Ejecutar un script basado en un evento](running-a-script-based-on-an-event.md)
</dt> <dt>

[Recepción de eventos en todo momento](receiving-events-at-all-times.md)
</dt> <dt>

[Crear un consumidor lógico](creating-a-logical-consumer.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> <dt>

[**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md)
</dt> </dl>

 


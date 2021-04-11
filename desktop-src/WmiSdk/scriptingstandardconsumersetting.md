---
description: La clase singleton ScriptingStandardConsumerSetting proporciona datos de registro que son comunes a todas las instancias de la clase de consumidor estándar ActiveScriptEventConsumer.
ms.assetid: d217e058-3529-4173-b896-ebff3d7b05c6
ms.tgt_platform: multiple
title: Clase ScriptingStandardConsumerSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScriptingStandardConsumerSetting
- ScriptingStandardConsumerSetting.Caption
- ScriptingStandardConsumerSetting.Description
- ScriptingStandardConsumerSetting.MaximumScripts
- ScriptingStandardConsumerSetting.SettingID
- ScriptingStandardConsumerSetting.Timeout
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: 43eae14eea445f546f731605c94b38e770b08691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276135"
---
# <a name="scriptingstandardconsumersetting-class"></a>Clase ScriptingStandardConsumerSetting

La clase singleton **ScriptingStandardConsumerSetting** proporciona datos de registro que son comunes a todas las instancias de la clase de consumidor estándar [**ActiveScriptEventConsumer**](activescripteventconsumer.md) . Una instancia de **ActiveScriptEventConsumer** usa las propiedades **MaximumScripts** y **timeout** . Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Singleton, AMENDMENT]
class ScriptingStandardConsumerSetting : CIM_Setting
{
  string Caption = "Scripting Standard Consumer Setting";
  string Description = "Registration data common to all instances of the Scripting Standard Consumer";
  uint32 MaximumScripts = 300;
  string SettingID = "ScriptingStandardConsumerSetting";
  uint32 Timeout = 0;
};
```

## <a name="members"></a>Miembros

La clase **ScriptingStandardConsumerSetting** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **ScriptingStandardConsumerSetting** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](standard-qualifiers.md) (64)
</dt> </dl>

Breve descripción de un objeto de una cadena de una línea. Contiene la cadena **ScriptingStandardConsumerSetting** porque se trata de una clase singleton.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una descripción de texto de un objeto.

</dd> <dt>

**MaximumScripts**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Número máximo de scripts que se ejecutan antes de que un consumidor inicie una nueva instancia. Para borrar las pérdidas de memoria de los scripts, cierre el consumidor con regularidad. El valor predeterminado es 300.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](standard-qualifiers.md) (256)
</dt> </dl>

Identificador del objeto de configuración.

</dd> <dt>

**Tiempo de espera**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**unidades**](standard-qualifiers.md) ("minutos")
</dt> </dl>

Número máximo de minutos antes de que un consumidor inicie una nueva instancia. Si es 0 (cero), la propiedad **MaximumScripts** controla la duración del consumidor. El intervalo válido para el **tiempo de espera** es de 0 a 71.000 y el valor predeterminado es 0 (cero).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La instancia única de la clase **ScriptingStandardConsumerSetting** reside en el \\ espacio de nombres root cimv2.

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

[**Configuración de CIM \_**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> <dt>

[Clases de consumidor estándar](standard-consumer-classes.md)
</dt> <dt>

[Ejecutar un script basado en un evento](running-a-script-based-on-an-event.md)
</dt> <dt>

[Crear un consumidor lógico](creating-a-logical-consumer.md)
</dt> <dt>

[Recepción de eventos en todo momento](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 


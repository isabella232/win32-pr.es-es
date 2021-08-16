---
description: La clase ScriptingStandardConsumerSetting singleton proporciona datos de registro comunes a todas las instancias de la clase de consumidor estándar ActiveScriptEventConsumer.
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
ms.openlocfilehash: a69d30511d01fba2df39483d1f76616bfae7c92812ce75989fd0c23558558b33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316209"
---
# <a name="scriptingstandardconsumersetting-class"></a>Clase ScriptingStandardConsumerSetting

La clase **ScriptingStandardConsumerSetting** singleton proporciona datos de registro comunes a todas las instancias de la clase de consumidor estándar [**ActiveScriptEventConsumer.**](activescripteventconsumer.md) Una **instancia de ActiveScriptEventConsumer** usa las **propiedades MaximumScripts** y **Timeout.** Para obtener más información, [vea Supervisión y respuesta a eventos con consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md)

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

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

La **clase ScriptingStandardConsumerSetting** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase ScriptingStandardConsumerSetting** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](standard-qualifiers.md) (64)
</dt> </dl>

Breve descripción de un objeto de una cadena de una línea. Contiene la cadena **ScriptingStandardConsumerSetting porque** se trata de una clase singleton.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción de texto de un objeto.

</dd> <dt>

**MaximumScripts**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Número máximo de scripts que se ejecutan antes de que un consumidor inicie una nueva instancia. Para borrar las pérdidas de memoria de los scripts, apague el consumidor con regularidad. El valor predeterminado es 300.

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

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**unidades**](standard-qualifiers.md) ("Minutos")
</dt> </dl>

Número máximo de minutos antes de que un consumidor inicie una nueva instancia. Si es 0 (cero), la **propiedad MaximumScripts** controla la duración del consumidor. El intervalo válido para **Timeout es** de 0 a 71 000 y el valor predeterminado es 0 (cero).

</dd> </dl>

## <a name="remarks"></a>Comentarios

La instancia única de la **clase ScriptingStandardConsumerSetting** reside en el espacio de \\ nombres raíz cimv2.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Espacio de nombres<br/>                | Suscripción \\ raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Scrcons.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scrcons.exe</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Configuración de CIM \_**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> <dt>

[Clases de consumidor estándar](standard-consumer-classes.md)
</dt> <dt>

[Ejecutar un script basado en un evento](running-a-script-based-on-an-event.md)
</dt> <dt>

[Creación de un consumidor lógico](creating-a-logical-consumer.md)
</dt> <dt>

[Recepción de eventos en todo momento](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 


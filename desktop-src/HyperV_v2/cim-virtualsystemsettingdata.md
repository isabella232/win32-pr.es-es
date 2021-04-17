---
description: Describe los aspectos virtuales de un sistema virtual a través de un conjunto de propiedades específicas de virtualización. CIM \_ VirtualSystemSettingData también se utiliza como clase de nivel superior de configuraciones del sistema virtual.
ms.assetid: 501e659d-f190-41f9-aafa-447048a60e7c
title: CIM_VirtualSystemSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingData
- CIM_VirtualSystemSettingData.VirtualSystemIdentifier
- CIM_VirtualSystemSettingData.VirtualSystemType
- CIM_VirtualSystemSettingData.Notes
- CIM_VirtualSystemSettingData.CreationTime
- CIM_VirtualSystemSettingData.ConfigurationID
- CIM_VirtualSystemSettingData.ConfigurationDataRoot
- CIM_VirtualSystemSettingData.ConfigurationFile
- CIM_VirtualSystemSettingData.SnapshotDataRoot
- CIM_VirtualSystemSettingData.SuspendDataRoot
- CIM_VirtualSystemSettingData.SwapFileDataRoot
- CIM_VirtualSystemSettingData.LogDataRoot
- CIM_VirtualSystemSettingData.AutomaticStartupAction
- CIM_VirtualSystemSettingData.AutomaticStartupActionDelay
- CIM_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- CIM_VirtualSystemSettingData.AutomaticShutdownAction
- CIM_VirtualSystemSettingData.AutomaticRecoveryAction
- CIM_VirtualSystemSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ff2c9725c8469b3e2c29d2e98a708d27e80378f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668091"
---
# <a name="cim_virtualsystemsettingdata-class"></a>\_Clase VirtualSystemSettingData de CIM

Describe los aspectos virtuales de un sistema virtual a través de un conjunto de propiedades específicas de virtualización. **CIM \_ VirtualSystemSettingData** también se utiliza como clase de nivel superior de configuraciones del sistema virtual.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingData : CIM_SettingData
{
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ VirtualSystemSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ VirtualSystemSettingData** tiene estas propiedades.

<dl> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La acción que se debe realizar para el sistema virtual cuando se produce un error en el software ejecutado por el sistema virtual. Los errores resueltos por esta propiedad solo incluyen aquellos que son detectables por la plataforma del host, como una condición de estado de espera no interrumpida.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Ninguno** (2)


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

**Reiniciar** (3)


</dt> <dd></dd> <dt>

<span id="Revert_to_snapshot"></span><span id="revert_to_snapshot"></span><span id="REVERT_TO_SNAPSHOT"></span>

**Revertir a instantánea** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La acción que se realizará para el sistema virtual cuando se apague el host.

<dt>

<span id="Turn_Off"></span><span id="turn_off"></span><span id="TURN_OFF"></span>

**Desactivar** (2)


</dt> <dd></dd> <dt>

<span id="Save_state"></span><span id="save_state"></span><span id="SAVE_STATE"></span>

**Guardar estado** (3)


</dt> <dd></dd> <dt>

<span id="Shutdown"></span><span id="shutdown"></span><span id="SHUTDOWN"></span>

**Shutdown** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Acción que se realizará en el sistema virtual cuando se inicie el host.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Ninguno** (2)


</dt> <dd></dd> <dt>

<span id="Restart_if_previously_active"></span><span id="restart_if_previously_active"></span><span id="RESTART_IF_PREVIOUSLY_ACTIVE"></span>

**Reiniciar si previamente estaba activo** (3)


</dt> <dd></dd> <dt>

<span id="Always_startup"></span><span id="always_startup"></span><span id="ALWAYS_STARTUP"></span>

**Siempre startup** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Retraso de la acción de inicio. Este valor es una variante de intervalo del tipo de datos **DateTime** .

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El número de secuencia para la activación del sistema virtual cuando se inicia el sistema host. Un número menor indica la activación anterior. Si una o más configuraciones muestran el mismo valor, la secuencia depende de la implementación. Un valor de "0" indica que la secuencia depende de la implementación.

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La ruta de acceso del directorio donde se almacena la información sobre la configuración del sistema virtual. El formato de esta propiedad es un URI basado en RFC 2079.

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La ruta de acceso relativa del archivo donde se almacena la información sobre la configuración del sistema virtual. La ruta de acceso relativa se anexa al valor de la propiedad **ConfigurationDataRoot** . El formato de esta propiedad es un URI basado en RFC 2079.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador único de la configuración del sistema virtual.

> [!Note]  
> **ConfigurationID** es diferente del **InstanceID** y se asigna mediante la implementación a un sistema virtual o una configuración de sistema virtual. **ConfigurationID** no es una clave y se puede producir el mismo valor para más de una instancia.

 

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se creó la configuración del sistema virtual.

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La ruta de acceso relativa del directorio donde se almacena la información de registro del sistema virtual. La ruta de acceso relativa se anexa al valor de la propiedad **ConfigurationDataRoot** . El formato de esta propiedad es un URI basado en RFC 2079.

</dd> <dt>

**Notas**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una matriz que contiene las notas proporcionadas por el usuario que están relacionadas con el sistema virtual.

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La ruta de acceso del archivo donde se almacena la información relacionada con la recuperación del sistema virtual. El formato de esta propiedad es un URI basado en RFC 2079.

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La ruta de acceso relativa del directorio donde se almacena la información sobre las instantáneas del sistema virtual. La ruta de acceso relativa se anexa al valor de la propiedad **ConfigurationDataRoot** . El formato de esta propiedad es un URI basado en RFC 2079.

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La ruta de acceso relativa del directorio donde se almacena la información relacionada con la suspensión del sistema virtual. La ruta de acceso relativa se anexa al valor de la propiedad **ConfigurationDataRoot** . El formato de esta propiedad es un URI basado en RFC 2079.

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso relativa al archivo del directorio donde se almacenan los archivos de intercambio del sistema virtual. La ruta de acceso relativa se anexa al valor de la propiedad **ConfigurationDataRoot** . El formato de esta propiedad es un URI basado en RFC 2079.

</dd> <dt>

**Virtualsystemidentifer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre único del sistema dentro de la plataforma de virtualización. **Virtualsystemidentifer** no es el nombre de host asignado a la instancia del sistema operativo que se ejecuta dentro del sistema virtual, ni tampoco es una dirección IP o dirección MAC asignada a ninguno de sus puertos de red.

**Virtualsystemidentifer** puede contener reglas específicas de implementación, como patrones simples o una expresión regular que la implementación pueda interpretar al establecer **virtualsystemidentifer**.

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo del sistema virtual.

> [!Note]  
> Si no se conoce el tipo de sistema virtual, este valor debe establecerse en "DMTF: Unknown".

 

A esta propiedad se le da formato con el siguiente formato de Backus Naur form (ABNF) ampliado:

vs-Type = DMTF-Value/Other-org-Value/Legacy-Value; DMTF-Value = "DMTF:" Defining-org ":" org-vs-Type; otro: org-Value = Defining-org ":" org-vs-Type;

El valor del formato ABNF anterior es:

-   *DMTF:*   valor de propiedad definido por DMTF y que se define en la descripción de esta propiedad.
-   *other-org-Value*   es un valor de propiedad definido por una entidad comercial distinta de DMTF y no se define en la descripción de esta propiedad.
-   valor *heredado:* valor de propiedad definido por una entidad comercial distinta de DMTF y no se define en la descripción de esta propiedad. Estos valores están permitidos pero se recomienda que estén en desuso a lo largo del tiempo.
-   *definir: org*   un identificador para la entidad comercial que define el tipo de sistema virtual. Debe incluir un nombre con copyright, marca registrada o un nombre único que sea propiedad de la entidad empresarial. No debe ser "DMTF" y no debe contener un signo de dos puntos.
-   *org-vs-escriba*   un identificador para el tipo de sistema virtual dentro de la entidad empresarial que lo define. Debe ser único dentro de la definición de-org. org-vs-Type puede usar cualquier carácter permitido para las cadenas CIM, excepto los siguientes: U0000-U001F (controles C0 Unicode), U0020 (espacio), U007F (controles C0 Unicode) o U0080-U009F (controles C1 de Unicode).
-   Si es necesario estructurar el valor en segmentos, los segmentos deben separarse con un solo signo de dos puntos.
-   Los valores de esta propiedad deben procesarse de forma confidencial. Están diseñados para procesarse mediante programación, en lugar de ser un nombre para mostrar y deben ser cortos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SettingData de CIM \_**](cim-settingdata.md)
</dt> </dl>

 

 





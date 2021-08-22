---
description: Describe los aspectos virtuales de un sistema virtual a través de un conjunto de propiedades específicas de virtualización. CIM \_ VirtualSystemSettingData también se usa como la clase de nivel superior de las configuraciones del sistema virtual.
ms.assetid: 501e659d-f190-41f9-aafa-447048a60e7c
title: CIM_VirtualSystemSettingData clase
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
ms.openlocfilehash: 1caed7797343eac9babd320af42fd6c9aaaffeff054211cc55bda0d437582d57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068495"
---
# <a name="cim_virtualsystemsettingdata-class"></a>Cim \_ VirtualSystemSettingData (clase)

Describe los aspectos virtuales de un sistema virtual a través de un conjunto de propiedades específicas de virtualización. **CIM \_ VirtualSystemSettingData también** se usa como la clase de nivel superior de las configuraciones del sistema virtual.

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

La **clase CIM \_ VirtualSystemSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase CIM \_ VirtualSystemSettingData** tiene estas propiedades.

<dl> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Acción que se debe realizar para el sistema virtual cuando se produce un error en el software ejecutado por el sistema virtual. Los errores solucionados por esta propiedad solo incluyen aquellos que la plataforma host puede detectar, como una condición de estado de espera no interrumpible.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Ninguno** (2)


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

**Reiniciar** (3)


</dt> <dd></dd> <dt>

<span id="Revert_to_snapshot"></span><span id="revert_to_snapshot"></span><span id="REVERT_TO_SNAPSHOT"></span>

**Revertir a la instantánea** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Acción que se debe realizar para el sistema virtual cuando se cierra el host.

<dt>

<span id="Turn_Off"></span><span id="turn_off"></span><span id="TURN_OFF"></span>

**Desactivar** (2)


</dt> <dd></dd> <dt>

<span id="Save_state"></span><span id="save_state"></span><span id="SAVE_STATE"></span>

**Guardar estado** (3)


</dt> <dd></dd> <dt>

<span id="Shutdown"></span><span id="shutdown"></span><span id="SHUTDOWN"></span>

**Apagado** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Acción que se debe realizar en el sistema virtual cuando se inicia el host.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Ninguno** (2)


</dt> <dd></dd> <dt>

<span id="Restart_if_previously_active"></span><span id="restart_if_previously_active"></span><span id="RESTART_IF_PREVIOUSLY_ACTIVE"></span>

**Reiniciar si previamente está activo** (3)


</dt> <dd></dd> <dt>

<span id="Always_startup"></span><span id="always_startup"></span><span id="ALWAYS_STARTUP"></span>

**Inicio siempre** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Retraso de la acción de inicio. Este valor es una variante de intervalo del **tipo de datos datetime.**

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de secuencia para la activación del sistema virtual cuando se inicia el sistema host. Un número inferior indica una activación anterior. Si una o varias configuraciones muestran el mismo valor, la secuencia depende de la implementación. Un valor de "0" indica que la secuencia depende de la implementación.

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso al archivo del directorio donde se almacena información sobre la configuración del sistema virtual. El formato de esta propiedad es un URI basado en RFC 2079.

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso relativa del archivo donde se almacena información sobre la configuración del sistema virtual. La ruta de acceso relativa se anexa al valor de la **propiedad ConfigurationDataRoot.** El formato de esta propiedad es un URI basado en RFC 2079.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador único de la configuración del sistema virtual.

> [!Note]  
> **ConfigurationID** es diferente de **InstanceID** y se asigna mediante la implementación a un sistema virtual o a una configuración del sistema virtual. **ConfigurationID** no es una clave y puede producirse el mismo valor para más de una instancia.

 

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
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

Ruta de acceso de archivo relativa del directorio donde se almacena la información de registro del sistema virtual. La ruta de acceso relativa se anexa al valor de la **propiedad ConfigurationDataRoot.** El formato de esta propiedad es un URI basado en RFC 2079.

</dd> <dt>

**Notas**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz que contiene notas proporcionadas por el usuario relacionadas con el sistema virtual.

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso del archivo donde se almacena la información relacionada con la recuperación del sistema virtual. El formato de esta propiedad es un URI basado en RFC 2079.

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso relativa del directorio donde se almacena información sobre las instantáneas del sistema virtual. La ruta de acceso relativa se anexa al valor de la **propiedad ConfigurationDataRoot.** El formato de esta propiedad es un URI basado en RFC 2079.

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso relativa del directorio donde se almacena la información relacionada de suspensión sobre el sistema virtual. La ruta de acceso relativa se anexa al valor de la **propiedad ConfigurationDataRoot.** El formato de esta propiedad es un URI basado en RFC 2079.

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso de archivo relativa del directorio donde se almacenan los archivos de intercambio del sistema virtual. La ruta de acceso relativa se anexa al valor de la **propiedad ConfigurationDataRoot.** El formato de esta propiedad es un URI basado en RFC 2079.

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre único del sistema dentro de la plataforma de virtualización. **VirtualSystemIdentifier** no es el nombre de host asignado a la instancia del sistema operativo que se ejecuta en el sistema virtual, ni es una dirección IP o dirección MAC asignada a ninguno de sus puertos de red.

**VirtualSystemIdentifier puede** contener reglas específicas de implementación, como patrones simples o una expresión regular que la implementación puede interpretar al establecer **VirtualSystemIdentifier.**

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo del sistema virtual.

> [!Note]  
> Si el tipo de sistema virtual es desconocido, este valor debe establecerse en "DMTF:unknown".

 

Esta propiedad tiene formato con el siguiente formato de forma de Backus Naur aumentada (ABNF):

vs-type = dmtf-value / other-org-value / legacy-value; dmtf-value = "DMTF:" defining-org ":" org-vs-type; other-org-value = defining-org ":" org-vs-type;

El valor del formato ABNF anterior es:

-   *dmtf-value*   un valor de propiedad definido por DMTF y se define en la descripción de esta propiedad.
-   *other-org-value*   es un valor de propiedad definido por una entidad empresarial que no sea DMTF y no se define en la descripción de esta propiedad.
-   *valor heredado un*   valor de propiedad definido por una entidad empresarial que no sea DMTF y no se define en la descripción de esta propiedad. Estos valores se permiten, pero se recomienda que estén en desuso con el tiempo.
-   *define-org*   un identificador para la entidad empresarial que define el tipo de sistema virtual. Debe incluir un nombre con derechos de autor, una marca comercial o un nombre único que sea propiedad de la entidad empresarial. No debe ser "DMTF" y no debe contener dos puntos.
-   *org-vs-type un*   identificador para el tipo de sistema virtual dentro de la entidad empresarial de definición. Debe ser único en defining-org. org-vs-type puede usar cualquier carácter permitido para las cadenas CIM, excepto lo siguiente: U0000-U001F (controles Unicode C0), U0020 (espacio), U007F (controles Unicode C0) o U0080-U009F (controles Unicode C1).
-   Si es necesario estructurar el valor en segmentos, los segmentos deben separarse con un solo signo de dos puntos.
-   Los valores de esta propiedad deben procesarse con distinguen mayúsculas de minúsculas. Están diseñados para procesarse mediante programación, en lugar de ser un nombre para mostrar, y deben ser cortos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 





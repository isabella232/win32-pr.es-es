---
description: Una versión concreta de la \_ clase de trabajo CIM. Esta clase representa una unidad de trabajo de instancias genéricas que se va a ejecutar, como un lote o un trabajo de impresión.
ms.assetid: fad4d894-d1f5-428d-819f-74966dd9f410
title: CIM_ConcreteJob (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob
- CIM_ConcreteJob.InstanceID
- CIM_ConcreteJob.Name
- CIM_ConcreteJob.JobState
- CIM_ConcreteJob.TimeOfLastStateChange
- CIM_ConcreteJob.TimeBeforeRemoval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 949d7c85643919f784a82e7722c9d49a9d9d2e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687046"
---
# <a name="cim_concretejob-class"></a>\_Clase ConcreteJob de CIM

Una versión concreta de la clase de [**\_ trabajo CIM**](cim-job.md) . Esta clase representa una unidad de trabajo de instancias genéricas que se va a ejecutar, como un lote o un trabajo de impresión.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteJob : CIM_Job
{
  string   InstanceID;
  string   Name;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = "00000000000500.000000:000";
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ ConcreteJob** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **CIM \_ ConcreteJob** tiene estos métodos.



| Método                                                           | Descripción                                                                          |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**GetError**](cim-concretejob-geterror.md)                     | Recupera información de error para el estado operativo de un trabajo concreto.<br/> |
| [**RequestStateChange**](cim-concretejob-requeststatechange.md) | Solicita el cambio de estado especificado a un trabajo concreto.<br/>                    |



 

### <a name="properties"></a>Propiedades

La clase **CIM \_ ConcreteJob** tiene estas propiedades.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")
</dt> </dl>

Identifica de forma única y opaca una instancia de esta clase dentro del ámbito del espacio de nombres contenedor.

> [!IMPORTANT]
>
> Con el fin de garantizar la unicidad dentro del espacio de nombres, el valor de la propiedad **InstanceID** debe construirse en el patrón siguiente: *OrgID*:*LocalID*
>
> *OrgID* debe incluir un nombre con copyright, marca registrada o de otro tipo que sea propiedad de la entidad empresarial que define el **InstanceID**, o bien un identificador registrado asignado por una entidad global reconocida. Este patrón es similar a la estructura de los nombres de clase de esquema. Además, para garantizar la exclusividad, el primer signo de dos puntos en **InstanceID** debe estar entre el *OrgID* y el *LocalID*. Por lo tanto, el *OrgID* no debe contener un signo de dos puntos (': ').
>
> La entidad de negocio elige *LocalID* y no se debe volver a usar para identificar distintos elementos del mundo real subyacentes.
>
> Si no se usa el patrón anterior, la entidad de definición debe asegurarse de que el valor **InstanceID** resultante no se vuelva a usar en las propiedades **InstanceID** producidas por este proveedor u otros proveedores para este espacio de nombres.
>
> En el caso de las instancias definidas por el grupo de tareas de administración distribuida (DMTF), el patrón debe usarse con el valor de *OrgID* establecido en CIM.

 

</dd> <dt>

**JobState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El estado operativo del trabajo y la transición entre estos Estados.

<dt>

<span id="New"></span><span id="new"></span><span id="NEW"></span>

<span id="New"></span><span id="new"></span><span id="NEW"></span>**Nuevo** (2)


</dt> <dd>

nunca se ha iniciado el trabajo.

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)


</dt> <dd>

El trabajo se está pasando de los Estados "nuevo", "suspendido" o "servicio" al estado "en ejecución".

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (4)


</dt> <dd>

El trabajo se está ejecutando.

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspendido** (5)


</dt> <dd>

El trabajo se ha detenido, pero se puede reiniciar sin problemas.

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (6)


</dt> <dd>

El trabajo se está pasando a un estado "completado", "terminado" o "eliminado".

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (7)


</dt> <dd>

El trabajo se ha completado con normalidad.

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminada** (8)


</dt> <dd>

El trabajo se ha detenido mediante una solicitud de cambio de estado ' Finalizar '. El trabajo y todos sus procesos subyacentes finalizan y se pueden reiniciar (es específico del trabajo) solo como un nuevo trabajo.

</dd> <dt>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>**Eliminado** (9)


</dt> <dd>

La solicitud de cambio de estado "Kill" detuvo el trabajo. Es posible que los procesos subyacentes hayan dejado de ejecutarse y que sea necesario realizar una limpieza para liberar recursos.

</dd> <dt>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Excepción** (10)


</dt> <dd>

El trabajo está en un estado anómalo que podría ser indicativo de una condición de error. El estado real puede mostrarse a través de objetos específicos del trabajo.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servicio** (11)


</dt> <dd>

El trabajo está en un estado específico del proveedor que admite la detección de problemas, la resolución o ambos.

</dd> <dt>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Consulta pendiente** (12)


</dt> <dd>

Esperar a que un cliente resuelva una consulta.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (13.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768... 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre")
</dt> </dl>

Nombre descriptivo de la instancia. Además, el nombre descriptivo se puede usar como una propiedad para una búsqueda o una consulta.

> [!Note]  
> El nombre no tiene que ser único en el espacio de nombres.

 

</dd> <dt>

**TimeBeforeRemoval**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Indica cuánto tiempo se conserva un trabajo completado. El valor predeterminado es "00000000000500.000000:000" (cinco minutos).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha u hora en que cambió por última vez el estado del trabajo.

> [!Note]  
> Si el estado del trabajo no ha cambiado y se rellena esta propiedad, debe establecerse en un valor de intervalo cero.

 

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

[**Trabajo de CIM \_**](cim-job.md)
</dt> </dl>

 


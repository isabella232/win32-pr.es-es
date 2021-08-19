---
description: Una versión concreta de la clase \_ Job de CIM. Esta clase representa una unidad de trabajo de creación de instancias genérica que se va a ejecutar, como un lote o un trabajo de impresión.
ms.assetid: fad4d894-d1f5-428d-819f-74966dd9f410
title: CIM_ConcreteJob clase
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
ms.openlocfilehash: a62ab2392ce2c069aa88ebb465f7028368f30bd5432cf96559c7eebe6edb8bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813166"
---
# <a name="cim_concretejob-class"></a>\_Cim ConcreteJob (clase)

Una versión concreta de la [**clase \_ Job de CIM.**](cim-job.md) Esta clase representa una unidad de trabajo de creación de instancias genérica que se va a ejecutar, como un lote o un trabajo de impresión.

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

La **clase \_ Cim ConcreteJob** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ Cim ConcreteJob** tiene estos métodos.



| Método                                                           | Descripción                                                                          |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**GetError**](cim-concretejob-geterror.md)                     | Recupera información de error para el estado operativo de un trabajo concreto.<br/> |
| [**RequestStateChange**](cim-concretejob-requeststatechange.md) | Solicita el cambio de estado especificado a un trabajo concreto.<br/>                    |



 

### <a name="properties"></a>Propiedades

La **clase \_ Cim ConcreteJob** tiene estas propiedades.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")
</dt> </dl>

Identifica de forma única y opaca una instancia de esta clase dentro del ámbito del espacio de nombres contenedor.

> [!IMPORTANT]
>
> Para garantizar la unidad dentro del espacio de nombres, el valor de la propiedad **InstanceID** debe construirse con el siguiente patrón: *OrgID*:*LocalID*
>
> *OrgID* debe incluir un nombre con derechos de autor, marca comercial o único que sea propiedad de la entidad empresarial que define el **InstanceID,** o debe ser un identificador registrado asignado por una autoridad global reconocida. Este patrón es similar a la estructura de los nombres de clase de esquema. Además, para garantizar la unidad, el primer signo de dos puntos de **InstanceID** debe estar entre *orgID* y *LocalID*. Por lo *tanto, orgID* no debe contener dos puntos (':').
>
> La entidad empresarial elige *LocalID* y no se debe volver a usar para identificar los distintos elementos subyacentes del mundo real.
>
> Si no se usa el patrón anterior, la entidad de definición debe asegurarse de que el valor **instanceID** resultante no se vuelva a usar en ninguna propiedad **InstanceID** producida por este proveedor u otros proveedores para este espacio de nombres.
>
> En el caso de las instancias definidas por el Grupo de tareas de administración distribuida (DMTF), el patrón debe usarse con *el OrgID* establecido en CIM.

 

</dd> <dt>

**JobState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El estado operativo del trabajo y la transición entre esos estados.

<dt>

<span id="New"></span><span id="new"></span><span id="NEW"></span>

<span id="New"></span><span id="new"></span><span id="NEW"></span>**Nuevo** (2)


</dt> <dd>

el trabajo nunca se ha iniciado.

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**A partir** de (3)


</dt> <dd>

El trabajo se mueve de los estados "Nuevo", "Suspendido" o "Servicio" al estado "En ejecución".

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En** ejecución (4)


</dt> <dd>

El trabajo se está ejecutando.

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspendido** (5)


</dt> <dd>

El trabajo se detiene, pero se puede reiniciar sin problemas.

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Apagar** (6)


</dt> <dd>

El trabajo se mueve a un estado "Completed", "Terminated" o "Killed".

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (7)


</dt> <dd>

El trabajo se ha completado con normalidad.

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Finalizado** (8)


</dt> <dd>

El trabajo se ha detenido mediante una solicitud de cambio de estado "Terminate". El trabajo y todos sus procesos subyacentes finalizan y se pueden reiniciar (esto es específico del trabajo) solo como un nuevo trabajo.

</dd> <dt>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>**Se ha** abatido (9)


</dt> <dd>

El trabajo se ha detenido mediante una solicitud de cambio de estado "Kill". Es posible que los procesos subyacentes se hayan dejado en ejecución y que se necesite limpieza para liberar recursos.

</dd> <dt>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Excepción** (10)


</dt> <dd>

El trabajo está en un estado anómalo que podría ser indicativo de una condición de error. Es posible que se muestre el estado real a través de objetos específicos del trabajo.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servicio** (11)


</dt> <dd>

El trabajo está en un estado específico del proveedor que admite la detección o resolución de problemas, o ambos

</dd> <dt>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Consulta pendiente** (12)


</dt> <dd>

Esperando a que un cliente resuelva una consulta.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (13..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Nombre descriptivo de la instancia. Además, el nombre descriptivo se puede usar como propiedad para una búsqueda o consulta.

> [!Note]  
> El nombre no tiene que ser único dentro del espacio de nombres .

 

</dd> <dt>

**TimeBeforeRemoval**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [ **obligatorios**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Indica cuánto tiempo se conserva un trabajo completado. El valor predeterminado es "000000000000500.00000:000" (cinco minutos).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha u hora en que cambió por última vez el estado del trabajo.

> [!Note]  
> Si el estado del trabajo no ha cambiado y esta propiedad se rellena, debe establecerse en un valor de intervalo cero.

 

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

[**Trabajo \_ cim**](cim-job.md)
</dt> </dl>

 


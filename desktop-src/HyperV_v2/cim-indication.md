---
description: Cim Indication es la clase base abstracta para todas las notificaciones sobre los cambios en los objetos de esquema y los datos de objetos de esquema, los eventos detectados por \_ los proveedores y la instrumentación. Las subclases de indicación CIM \_ representan tipos específicos de notificaciones.
ms.assetid: 85a70425-7b32-449c-9fc0-1cfbf34d9187
title: CIM_Indication clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Indication
- CIM_Indication.IndicationIdentifier
- CIM_Indication.CorrelatedIndications
- CIM_Indication.IndicationTime
- CIM_Indication.PerceivedSeverity
- CIM_Indication.OtherSeverity
- CIM_Indication.IndicationFilterName
- CIM_Indication.SequenceContext
- CIM_Indication.SequenceNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e859e7834a051bad0a5ea402e8bd6c3685b5ad54
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883530"
---
# <a name="cim_indication-class"></a>Cim \_ Indication (clase)

**CIM \_ Indicación** es la clase base abstracta para todas las notificaciones sobre los cambios en los objetos de esquema y los datos de objetos de esquema, los eventos detectados por los proveedores y la instrumentación. Las subclases de **\_ indicación CIM** representan tipos específicos de notificaciones.

## <a name="syntax"></a>Sintaxis

``` syntax
[Indication, Version("2.24.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_Indication : __ExtrinsicEvent
{
  string   IndicationIdentifier;
  string   CorrelatedIndications[];
  datetime IndicationTime;
  uint16   PerceivedSeverity;
  string   OtherSeverity;
  string   IndicationFilterName;
  string   SequenceContext;
  sint64   SequenceNumber;
};
```

## <a name="members"></a>Miembros

La **clase \_ CIM Indication** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM Indication** tiene estas propiedades.

<dl> <dt>

**CorrelatedIndications**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU \| X733. Notificaciones correlacionadas"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Indicación cim \_**.**IndicationIdentifier**")
</dt> </dl>

Matriz que contiene los **valores IndicationIdentifier** de las notificaciones relacionadas con esta.

</dd> <dt>

**IndicationFilterName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ IndicationFilter.Name")
</dt> </dl>

Identificador del filtro de indicación que procesa la indicación. El servicio de envío establece esta propiedad. Esta propiedad se correlaciona con la **propiedad Name** del **objeto \_ IndicationFilter de CIM.** El valor de **IndicationFilterName** debe usar el formato siguiente:

-   *&lt; OrgID: &gt;**&lt; LocalID &gt;*
-   *&lt; OrgID &gt;* debe incluir un nombre con derechos de autor, marca comercial o único que sea propiedad de la entidad empresarial propietaria del objeto.
-   *&lt; OrgID &gt;* no debe contener dos puntos (:)
-   *&lt; LocalID &gt;* un identificador único elegido por la entidad empresarial propietaria del objeto.

</dd> <dt>

**IndicationIdentifier**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU \| X733. Identificador de notificación")
</dt> </dl>

Identificador de la indicación. Esta propiedad se puede usar como valor de clave en la matriz de propiedades **CorrelatedIndications.** Por lo tanto, **IndicationIdentifier** debe ser un valor único dentro del espacio de nombres de esta instancia de clase.

Para asegurarse de **que IndicationIdentifier** es único, debe usar el formato siguiente:

-   *&lt; OrgID: &gt;**&lt; LocalID &gt;*
-   *&lt; OrgID &gt;* debe incluir un nombre con derechos de autor, marca comercial o único que sea propiedad de la entidad empresarial propietaria del objeto.
-   *&lt; OrgID &gt;* no debe contener dos puntos (:)
-   *&lt; LocalID &gt;* un identificador único elegido por la entidad empresarial propietaria del objeto.
-   Para las instancias definidas por DMTF, *&lt; OrgID &gt;* debe establecerse en "CIM".

</dd> <dt>

**IndicationTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora y fecha en que se creó la indicación. La propiedad se puede establecer en **NULL** si la entidad que creó la indicación no es capaz de determinar esta información.

> [!Note]  
> El **valor IndicationTime** puede ser el mismo para las indicaciones que se generan en sucesión rápida.

 

</dd> <dt>

**OtherSeverity**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ AlertIndication**](cim-alertindication.md).**PerceivedSeverity**")
</dt> </dl>

Gravedad de la indicación desde el punto de vista del notificador cuando **PerceivedSeverity** está establecido en "1" (Otros).

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU \| X733. Gravedad percibida")
</dt> </dl>

Gravedad de la indicación desde el punto de vista del notificador.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd>

La gravedad percibida de la indicación es desconocida o indeterminada.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd>

Indica que el valor de gravedad se puede encontrar en la **propiedad OtherSeverity.**

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Información** (2)


</dt> <dd>

La información debe usarse al proporcionar una respuesta informativa.

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degradado/Advertencia** (3)


</dt> <dd>

Debe usarse cuando sea adecuado para permitir que el usuario decida si se necesita una acción.

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Menor** (4)


</dt> <dd>

Se necesita una acción, pero la situación no es grave en este momento.

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principal** (5)


</dt> <dd>

La acción es necesaria AHORA.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (6)


</dt> <dd>

Ahora es necesario tomar medidas y el ámbito es amplio (quizás se produciría una interrupción inesperada en un recurso crítico).

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Irrecuperable o irrecuperable** (7)


</dt> <dd>

se produjo un error, pero es demasiado tarde para tomar medidas correctivas.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**SequenceContext**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Cim \_ Indication**.**SequenceNumber**")
</dt> </dl>

Contexto de secuencia del identificador de secuencia para la indicación. Si un servicio no admite identificadores de secuencia para las indicaciones, esta propiedad debe establecerse en **NULL.** Si la indicación se ha entregado de nuevo, esta propiedad sigue siendo la misma.

> [!Note]  
> El identificador de secuencia de la indicación permite a un agente de escucha identificar indicaciones duplicadas cuando el servicio intenta volver a entregar las indicaciones, reordenar las indicaciones que llegan desordenadas y detectar indicaciones perdidas.

 

Para asegurarse de **que SequenceContext** es único, debe usar el formato siguiente:

-   *indication-service-name* \# *cim-service-start-id* \# *listener-destination-creation-time*
-   *indication-service-name* es el valor de la **propiedad Name** de la instancia de **CIM \_ IndicationService** que entrega la indicación.
-   *cim-service-start-id es* un identificador que identifica de forma única la operación de inicio de un servicio. Por ejemplo, podría ser una marca de tiempo de la hora de inicio o un contador que aumente para cada inicio o reinicio del servicio.
-   *listener-destination-creation-time* es una marca de tiempo de la hora de creación de la instancia **de Cim \_ ListenerDestination** que representa el destino del agente de escucha. nSince este formato es solo una recomendación, los clientes CIM deben tratar el valor como un identificador opaco para el contexto de secuencia y no deben confiar en este formato.

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Cim \_ Indication**.**SequenceContext**")
</dt> </dl>

Número de secuencia del identificador de secuencia para la indicación.

> [!Note]  
> El identificador de secuencia de la indicación permite a un agente de escucha identificar indicaciones duplicadas cuando el servicio intenta volver a entregar las indicaciones, reordenar las indicaciones que llegan desordenadas y detectar indicaciones perdidas.

 

El número de secuencia tiene las siguientes características:

-   El número de secuencia se restablece a "0" cada vez que cambia **el valor de SequenceContext.**
-   Cada vez que el destino del agente de escucha recibe una nueva indicación, el número de secuencia aumenta en "1".
-   El número de secuencia se ajusta a "0" cuando se supera el intervalo de valores.
-   Si la indicación se ha entregado de nuevo, **SequenceNumber** sigue siendo el mismo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 


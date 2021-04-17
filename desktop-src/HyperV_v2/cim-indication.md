---
description: '\_La indicación CIM es la clase base abstracta para todas las notificaciones sobre los cambios en los objetos de esquema y los datos de objetos de esquema, eventos detectados por proveedores e instrumentación. Las subclases de la \_ indicación CIM representan tipos específicos de notificaciones.'
ms.assetid: 85a70425-7b32-449c-9fc0-1cfbf34d9187
title: CIM_Indication (clase)
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
ms.openlocfilehash: 46b8d50f2e90d9a51c8ffa0b93de9ac16c889340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687402"
---
# <a name="cim_indication-class"></a>\_Clase de indicación CIM

**CIM \_ La indicación** es la clase base abstracta para todas las notificaciones sobre los cambios en los objetos de esquema y los datos de objetos de esquema, eventos detectados por proveedores e instrumentación. Las subclases de la **\_ indicación CIM** representan tipos específicos de notificaciones.

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

La clase de **\_ indicación CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ indicación CIM** tiene estas propiedades.

<dl> <dt>

**CorrelatedIndications**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RECOMMENDATION. itu \| X733. Notificaciones correlacionadas "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indicación de CIM**.**IndicationIdentifier**")
</dt> </dl>

Una matriz que contiene los valores de **IndicationIdentifier** de las notificaciones que están relacionadas con este.

</dd> <dt>

**IndicationFilterName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ IndicationFilter.Name")
</dt> </dl>

Identificador del filtro de indicación que procesa la indicación. El servicio de envío establece esta propiedad. Esta propiedad se correlaciona con la propiedad **Name** del objeto **CIM \_ IndicationFilter** . El valor de **IndicationFilterName** debe tener el formato siguiente:

-   *<OrgID>*:*<LocalID>*
-   *<OrgID>* debe incluir un nombre con copyright, marca registrada o único que sea propiedad de la entidad empresarial a la que pertenece el objeto.
-   *<OrgID>* no debe contener dos puntos (:)
-   *<LocalID>* identificador único elegido por la entidad comercial que posee el objeto.

</dd> <dt>

**IndicationIdentifier**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RECOMMENDATION. itu \| X733. Identificador de notificación ")
</dt> </dl>

Identificador de la indicación. Esta propiedad se puede utilizar como un valor de clave en la matriz de propiedades **CorrelatedIndications** . Por lo tanto, **IndicationIdentifier** debe ser un valor único dentro del espacio de nombres de esta instancia de clase.

Para asegurarse de que **IndicationIdentifier** sea único, debe usar el siguiente formato:

-   *<OrgID>*:*<LocalID>*
-   *<OrgID>* debe incluir un nombre con copyright, marca registrada o único que sea propiedad de la entidad empresarial a la que pertenece el objeto.
-   *<OrgID>* no debe contener dos puntos (:)
-   *<LocalID>* identificador único elegido por la entidad comercial que posee el objeto.
-   En el caso de las instancias definidas por DMTF, *<OrgID>* debe establecerse en "CIM".

</dd> <dt>

**IndicationTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se creó la indicación. La propiedad se puede establecer en **null** si la entidad que creó la indicación no es capaz de determinar esta información.

> [!Note]  
> El valor de **IndicationTime** puede ser el mismo para las indicaciones que se generan en una sucesión rápida.

 

</dd> <dt>

**OtherSeverity**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ AlertIndication**](cim-alertindication.md).**PerceivedSeverity**")
</dt> </dl>

La gravedad de la indicación del punto de vista del notificador cuando **PerceivedSeverity** se establece en "1" (otro).

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("RECOMMENDATION. itu \| X733. Gravedad percibida ")
</dt> </dl>

La gravedad de la indicación del punto de vista del notificador.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd>

la gravedad percibida de la indicación es desconocida o indeterminada.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd>

Indica que el valor de la gravedad se puede encontrar en la propiedad **OtherSeverity** .

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Información** (2)


</dt> <dd>

La información se debe utilizar al proporcionar una respuesta informativa.

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degradado/ADVERTENCIA** (3)


</dt> <dd>

Debe usarse cuando sea adecuado para permitir que el usuario decida si es necesario realizar alguna acción.

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Secundaria** (4)


</dt> <dd>

La acción es necesaria, pero la situación no es seria en este momento.

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principal** (5)


</dt> <dd>

La acción es necesaria ahora.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (6)


</dt> <dd>

La acción es necesaria ahora y el ámbito es amplio (es posible que se produzca una interrupción inminente en un recurso crítico).

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Irrecuperable/no recuperable** (7)


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

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indicación CIM**.**SequenceNumber**")
</dt> </dl>

El contexto de secuencia del identificador de secuencia para la indicación. Si un servicio no admite identificadores de secuencia para las indicaciones, esta propiedad debe establecerse en **null**. Si se vuelve a entregar la indicación, esta propiedad sigue siendo la misma.

> [!Note]  
> El identificador de secuencia de la indicación permite a un agente de escucha identificar las indicaciones duplicadas cuando el servicio intenta volver a ofrecer indicaciones, reordenar las indicaciones que llegan desordenadas y detectar las indicaciones perdidas.

 

Para asegurarse de que **SequenceContext** sea único, debe usar el siguiente formato:

-   *indicación-nombre* \# de servicio *CIM-Service-Start-ID* \# *agente de escucha-destino-creación-hora*
-   *indica-Service-Name* es el valor de la propiedad **Name** de la instancia de **\_ IndicationService de CIM** que entrega la indicación.
-   *CIM-Service-Start-ID* es un identificador que identifica de forma única la operación de inicio de un servicio. Por ejemplo, podría ser una marca de tiempo de la hora de inicio o un contador que aumente para cada inicio o reinicio del servicio.
-   *Listener-Destination-Creation-time* es una marca de tiempo de la hora de creación de la instancia de **\_ ListenerDestination de CIM** que representa el destino del agente de escucha. nSince este formato es solo una recomendación, los clientes CIM tratarán el valor como un identificador opaco para el contexto de secuencia y no se basarán en este formato.

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indicación CIM**.**SequenceContext**")
</dt> </dl>

El número de secuencia del identificador de secuencia para la indicación.

> [!Note]  
> El identificador de secuencia de la indicación permite a un agente de escucha identificar las indicaciones duplicadas cuando el servicio intenta volver a ofrecer indicaciones, reordenar las indicaciones que llegan desordenadas y detectar las indicaciones perdidas.

 

El número de secuencia tiene las siguientes características:

-   El número de secuencia se restablece en "0" cada vez que cambia el valor de **SequenceContext** .
-   Siempre que el destino del agente de escucha recibe una nueva indicación, el número de secuencia aumenta en "1".
-   El número de secuencia se ajusta a "0" cuando se supera el intervalo de valores.
-   Si se vuelve a entregar la indicación, **SequenceNumber** sigue siendo el mismo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 


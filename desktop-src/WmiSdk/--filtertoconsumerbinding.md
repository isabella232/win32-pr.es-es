---
description: Se utiliza en el registro de los consumidores de eventos permanentes para relacionar una instancia de \_ \_ EventConsumer con una instancia de \_ \_ EventFilter.
ms.assetid: e6a06161-0f1c-4754-ac34-263ccf7bf10d
ms.tgt_platform: multiple
title: __FilterToConsumerBinding (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __FilterToConsumerBinding
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0fd9b7f3cf60d14d27fdf5b5014b57e6f599d67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716872"
---
# <a name="__filtertoconsumerbinding-class"></a>\_\_Clase FilterToConsumerBinding

La clase del sistema **\_ \_ FilterToConsumerBinding** se usa en el registro de los consumidores de eventos permanentes para relacionar una instancia de [**\_ \_ EventConsumer**](--eventconsumer.md) con una instancia de [**\_ \_ EventFilter**](--eventfilter.md).**\_ \_ FilterToConsumerBinding** es una clase de asociación.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __FilterToConsumerBinding : __IndicationRelated
{
  __EventConsumer REF Consumer;
  uint8               CreatorSID[];
  boolean             DeliverSynchronously = False;
  uint32              DeliveryQoS;
  __EventFilter   REF Filter;
  boolean             MaintainSecurityContext = False;
  boolean             SlowDownProviders = False;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ FilterToConsumerBinding** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ FilterToConsumerBinding** tiene estas propiedades.

<dl> <dt>

**Consumidor**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ EventConsumer**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [ **clave**](standard-qualifiers.md)
</dt> </dl>

Referencia a una instancia de [**\_ \_ EventConsumer**](--eventconsumer.md) que representa la ruta de acceso del objeto a un consumidor lógico, el destinatario de un evento. Un consumidor lógico es una instancia de una clase derivada de **\_ \_ EventConsumer**.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Identificador de seguridad (SID) que identifica de forma única al usuario que creó el enlace. En función del sistema operativo, WMI almacena el SID de administrador o el SID del usuario que crea una instancia de **\_ \_ FilterToConsumerBinding**. Para obtener más información, vea [enlazar un filtro de eventos con un consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) y [supervisar y responder a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).

</dd> <dt>

**DeliverSynchronously**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Obsoleto. En su lugar, use la propiedad **DeliveryQoS** en lugar de esta propiedad, porque si **DeliverSynchronously** está establecido en **true** , invalida el valor de la propiedad **DeliveryQoS** .

</dd> <dt>

**DeliveryQoS**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Calidad de servicio de una suscripción. Si la propiedad **DeliverSynchronously** está establecida en **true**, invalida el valor de la propiedad **DeliveryQoS** .

<dt>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**WMIMSG \_ MARCAR \_ QoS \_ sincrónico** (0)


</dt> <dd>

Entrega sincrónica

**False**. El evento se entrega al consumidor lógico sincrónicamente.

</dd> <dt>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**WMIMSG \_ MARCAR \_ QoS \_ Express** (1)


</dt> <dd>

Entrega rápida

**True**. El evento se entrega al consumidor lógico de forma asincrónica.

</dd> </dl>

</dd> <dt>

**Filter**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ EventFilter**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [ **clave**](standard-qualifiers.md)
</dt> </dl>

Referencia a una instancia de [**\_ \_ EventFilter**](--eventfilter.md) que representa la ruta de acceso del objeto a un filtro de eventos que es una consulta que especifica el tipo de evento que se va a recibir.

</dd> <dt>

**MaintainSecurityContext**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si **es true**, los eventos se entregan en el mismo contexto de seguridad en el que se encontraban en el momento en que se proporcionaron.

> [!Note]  
> Solo un consumidor implementado como un archivo DLL (un consumidor en proceso) puede recibir eventos en el contexto de seguridad del proveedor. Para obtener más información sobre los proveedores y la seguridad en proceso, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md). Para obtener más información y ejemplos, vea reemplazar:[recibir eventos de forma segura](receiving-events-securely.md).

 

</dd> <dt>

**SlowDownProviders**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si **es true**, los proveedores se ralentizan si este consumidor no puede continuar.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ FilterToConsumerBinding** se deriva de [**\_ \_ IndicationRelated**](--indicationrelated.md), que no tiene propiedades.

Los consumidores de eventos permanentes usan la clase del sistema **\_ \_ FilterToConsumerBinding** para enlazar filtros de eventos a los consumidores finales. Una vez enlazados el filtro y el consumidor, WMI puede reenviar los eventos que coinciden con el filtro al consumidor correspondiente.

## <a name="examples"></a>Ejemplos

El ejemplo de [creación de registro de eventos de WMI permanente para supervisar archivos](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) de PowerShell en la galería de TechNet usa **\_ \_ FilterToConsumerBinding** como parte de un script complejo para configurar un registro de eventos de WMI permanente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_IndicationRelated**](--indicationrelated.md)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[Supervisión de eventos](monitoring-events.md)
</dt> <dt>

[Crear un filtro de eventos](creating-an-event-filter.md)
</dt> <dt>

[Proteger eventos WMI](securing-wmi-events.md)
</dt> </dl>

 

 





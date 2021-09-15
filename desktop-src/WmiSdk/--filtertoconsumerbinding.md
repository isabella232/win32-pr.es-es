---
description: Se usa en el registro de consumidores de eventos permanentes para relacionar una instancia de \_ \_ EventConsumer con una instancia de \_ \_ EventFilter.
ms.assetid: e6a06161-0f1c-4754-ac34-263ccf7bf10d
ms.tgt_platform: multiple
title: __FilterToConsumerBinding clase
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568521"
---
# <a name="__filtertoconsumerbinding-class"></a>\_\_FilterToConsumerBinding (clase)

La clase del sistema **\_ \_ FilterToConsumerBinding** se usa en el registro de consumidores de eventos permanentes para relacionar una instancia de [**\_ \_ EventConsumer**](--eventconsumer.md) con una instancia de [**\_ \_ EventFilter**](--eventfilter.md).**\_ \_ FilterToConsumerBinding es** una clase de asociación.

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

## <a name="members"></a>Members

La **\_ \_ clase FilterToConsumerBinding** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase FilterToConsumerBinding** tiene estas propiedades.

<dl> <dt>

**Consumidor**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ EventConsumer**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [ **Clave**](standard-qualifiers.md)
</dt> </dl>

Referencia a una instancia de [**\_ \_ EventConsumer que**](--eventconsumer.md) representa la ruta de acceso del objeto a un consumidor lógico, el destinatario de un evento. Un consumidor lógico es una instancia de una clase derivada de **\_ \_ EventConsumer.**

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Identificador de seguridad (SID) que identifica de forma única al usuario que creó el enlace. En función del sistema operativo, WMI almacena el SID de administrador o el SID del usuario que crea una instancia de **\_ \_ FilterToConsumerBinding**. Para obtener más información, vea [Enlazar un filtro de eventos con](binding-an-event-filter-with-a-logical-consumer.md) un consumidor lógico y supervisar y Responder a eventos con [consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md)

</dd> <dt>

**DeliverSynchronously**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obsoleto. En su lugar, use la propiedad **DeliveryQoS** en lugar de esta propiedad, ya que si **DeliverSynchronously** se establece en **True,** invalida el valor de la **propiedad DeliveryQoS.**

</dd> <dt>

**DeliveryQoS**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Calidad de servicio para una suscripción. Si la **propiedad DeliverSynchronously** se establece en **True,** invalida el valor de la **propiedad DeliveryQoS.**

<dt>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**WMIMSG \_ MARCA \_ QOS \_ SINCRÓNICA** (0)


</dt> <dd>

Entrega sincrónica

**False**. El evento se entrega al consumidor lógico de forma sincrónica.

</dd> <dt>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**WMIMSG \_ MARCA \_ QOS \_ EXPRESS** (1)


</dt> <dd>

Entrega rápida

**True**. El evento se entrega al consumidor lógico de forma asincrónica.

</dd> </dl>

</dd> <dt>

**Filter**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ EventFilter**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [ **Clave**](standard-qualifiers.md)
</dt> </dl>

Referencia a una instancia de [**\_ \_ EventFilter**](--eventfilter.md) que representa la ruta de acceso del objeto a un filtro de eventos que es una consulta que especifica el tipo de evento que se va a recibir.

</dd> <dt>

**MaintainSecurityContext**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Si **es True**, los eventos se entregan en el mismo contexto de seguridad en el que estaba el proveedor cuando los proporcionó.

> [!Note]  
> Solo un consumidor implementado como un archivo DLL (un consumidor en proceso) puede recibir eventos en el contexto de seguridad del proveedor. Para obtener más información sobre los proveedores en proceso y la seguridad, vea [Provider Hosting and Security](provider-hosting-and-security.md). Para obtener más información y ejemplos, vea replace:[Receiving Events Securely](receiving-events-securely.md).

 

</dd> <dt>

**SlowDownProviders**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Si **es True,** los proveedores se ralentizan si este consumidor no puede mantenerse al día.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **\_ \_ clase FilterToConsumerBinding** se deriva de [**\_ \_ IndicationRelated**](--indicationrelated.md), que no tiene propiedades.

Los consumidores de eventos permanentes usan la clase del sistema **\_ \_ FilterToConsumerBinding** para enlazar filtros de eventos a consumidores finales. Una vez enlazados el filtro y el consumidor, WMI puede reenviar eventos que coincidan con el filtro al consumidor correspondiente.

## <a name="examples"></a>Ejemplos

El ejemplo Crear registro de eventos [WMI](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) permanente para supervisar archivos de PowerShell en la Galería de TechNet usa **\_ \_ FilterToConsumerBinding** como parte de un script complejo para configurar un registro de eventos WMI permanente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_\_IndicationRelated**](--indicationrelated.md)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[Supervisión de eventos](monitoring-events.md)
</dt> <dt>

[Creación de un filtro de eventos](creating-an-event-filter.md)
</dt> <dt>

[Protección de eventos WMI](securing-wmi-events.md)
</dt> </dl>

 

 





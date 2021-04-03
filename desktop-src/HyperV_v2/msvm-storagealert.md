---
description: Representa un evento que se genera cada vez que cambia la propiedad OperationalStatus de la \_ clase MSVM ResourcePool o MSVM \_ LogicalDisk.
ms.assetid: 20E7C22A-A151-4EDC-90D8-4BCD53C42355
title: Msvm_StorageAlert (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAlert
- Msvm_StorageAlert.AlertingManagedElement
- Msvm_StorageAlert.AlertingElementFormat
- Msvm_StorageAlert.OtherAlertingElementFormat
- Msvm_StorageAlert.AlertType
- Msvm_StorageAlert.PerceivedSeverity
- Msvm_StorageAlert.ProbableCause
- Msvm_StorageAlert.ProbableCauseDescription
- Msvm_StorageAlert.EventTime
- Msvm_StorageAlert.OwningEntity
- Msvm_StorageAlert.MessageArguments
- Msvm_StorageAlert.MessageID
- Msvm_StorageAlert.Message
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fa7f0430631082a9690cf2083f6b075ca62ee26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082938"
---
# <a name="msvm_storagealert-class"></a>MSVM \_ StorageAlert (clase)

Representa un evento que se genera cada vez que cambia la propiedad **OperationalStatus** de la clase [**MSVM \_ ResourcePool**](msvm-resourcepool.md) o [**MSVM \_ LogicalDisk**](msvm-logicaldisk.md) .

La siguiente sintaxis se simplifica desde el código MOF e incluye estas propiedades.

## <a name="syntax"></a>Sintaxis

``` syntax
[Indication, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAlert : CIM_AlertIndication
{
  string   AlertingManagedElement[];
  uint16   AlertingElementFormat;
  uint16   OtherAlertingElementFormat;
  uint16   AlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  datetime EventTime;
  string   OwningEntity;
  string   MessageArguments[];
  string   MessageID;
  string   Message;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ StorageAlert** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ StorageAlert** tiene estas propiedades.

<dl> <dt>

**AlertingElementFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **ModelCorrespondence** ("CIM \_ AlertIndication. AlertingManagedElement", "CIM \_ AlertIndication. OtherAlertingElementFormat")
</dt> </dl>

Especifica el formato de la propiedad **AlertingManagedElement** . El formato es CIMObjectPath, con el formato *<NamespacePath> : <ClassName> "" <Prop1> = \\ <Value1> \\ , " <Prop2> = \\ " <Value2> \\ "*, que especifica una instancia en el esquema CIM.

Esta propiedad se hereda de la **clase \_ AlertIndication de CIM** .

Los valores posibles son:

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)
</dt> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)
</dt> </dl>

</dd> <dt>

**AlertingManagedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Las rutas de acceso WMI de la instancia para la que se genera la alerta.

</dd> <dt>

**AlertType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la clasificación principal de la alerta. Los posibles valores para esta propiedad son:

<dl> <dt>

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Alerta de calidad de servicio** (3)
</dt> </dl>

</dd> <dt>

**EventTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se detectó el evento subyacente.

</dd> <dt>

**Message**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Un mensaje con formato que se construye combinando algunos o todos los elementos dinámicos que se especifican en la propiedad **MessageArguments** con los elementos estáticos identificados de forma exclusiva por la propiedad **MessageID** en un registro de mensajes u otro Catálogo asociado a la propiedad **OwningEntity** .

</dd> <dt>

**MessageArguments**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una matriz que contiene el contenido dinámico del mensaje. Si el valor de **MessageID** es 32930, el argumento de la posición 0 es el **PoolID** de la instancia de [**MSVM \_ ResourcePool**](msvm-resourcepoolcomponent.md) para el que se genera la alerta.

</dd> <dt>

**Identificador**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica de forma única, dentro del ámbito de la propiedad **OwningEntity** , el formato de la propiedad de **mensaje** . Los posibles valores para esta propiedad son:

32930 ("mensaje de rendimiento insuficiente de QoS del bloque de almacenamiento")

</dd> <dt>

**OtherAlertingElementFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una cadena que define los "otros" valores para **AlertingManagedElement**. Este valor debe establecerse en un valor distinto de NULL cuando **AlertingManagedElement** se establece en un valor de 1 ("Other"). Para todos los demás valores de **AlertingManagedElement**, el valor de esta cadena debe establecerse en NULL.

Esta propiedad se hereda de la **clase \_ AlertIndication de CIM** .

</dd> <dt>

**OwningEntity**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica de forma única la entidad propietaria de la definición del formato del **mensaje** descrito en esta instancia. El valor de esta propiedad siempre es "Microsoft-Windows-Hyper-V".

"Microsoft-Windows-Hyper-V"

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe la gravedad de la indicación de alerta. Los posibles valores para esta propiedad son:

<dl> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Información** (2)
</dt> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degradado/ADVERTENCIA** (3)
</dt> </dl>

</dd> <dt>

**ProbableCause**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe la causa probable de la situación que produjo la indicación de la alerta.

<dl> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Problema de capacidad de almacenamiento** (50)
</dt> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Alerta anterior desactivada** (59)
</dt> </dl>

</dd> <dt>

**ProbableCauseDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una descripción textual que corresponde al valor de la propiedad **ProbableCause** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

El proveedor WMI de Hyper-V no genera eventos para discos virtuales individuales a fin de evitar el desbordamiento de clientes con eventos en el caso de las funciones de gran escala de los sistemas de almacenamiento subyacentes.

Cuando un cliente recibe un evento **MSVM \_ StorageAlert** , si el valor de la propiedad **ProbableCause** es 50 (problema de capacidad de almacenamiento), el cliente puede detectar qué discos virtuales están funcionando fuera de su Directiva de QoS mediante uno de estos procedimientos:

-   Consulte todas las instancias de [**\_ LogicalDisk de MSVM**](msvm-logicaldisk.md) que se asignaron desde el grupo de recursos para el que se generó el evento. Estas instancias de **MSVM \_ LogicalDisk** están asociadas al grupo de recursos a través de la Asociación [**\_ ElementAllocatedFromPool de MSVM**](msvm-elementallocatedfrompool.md) .
-   Filtre la lista de resultados seleccionando instancias cuyo OperationalStatus contiene un rendimiento insuficiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                                 |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_ALERTINDICATION CIM**](cim-alertindication.md)
</dt> <dt>

[**MSVM \_ LogicalDisk**](msvm-logicaldisk.md)
</dt> <dt>

[**MSVM \_ ResourcePool**](msvm-resourcepoolcomponent.md)
</dt> </dl>

 

 





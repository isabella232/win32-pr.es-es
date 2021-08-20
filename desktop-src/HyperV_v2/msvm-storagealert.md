---
description: Representa un evento que se genera cada vez que cambia la propiedad OperationalStatus de la clase Msvm ResourcePool o \_ Msvm \_ LogicalDisk.
ms.assetid: 20E7C22A-A151-4EDC-90D8-4BCD53C42355
title: Msvm_StorageAlert clase
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
ms.openlocfilehash: 478b4617f56c73e425d833842b313767f85c385e9142314a7ca8978b5783f492
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950234"
---
# <a name="msvm_storagealert-class"></a>Clase StorageAlert de Msvm \_

Representa un evento que se genera cada vez que cambia la propiedad **OperationalStatus** de la clase [**\_ Msvm ResourcePool**](msvm-resourcepool.md) o [**Msvm \_ LogicalDisk.**](msvm-logicaldisk.md)

La sintaxis siguiente se simplifica a partir del código MOF e incluye estas propiedades.

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

La **clase \_ StorageAlert de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ StorageAlert de Msvm** tiene estas propiedades.

<dl> <dt>

**AlertingElementFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **ModelCorrespondence** ("CIM \_ AlertIndication.AlertingManagedElement", "CIM \_ AlertIndication.OtherAlertingElementFormat")
</dt> </dl>

Especifica el formato de la **propiedad AlertingManagedElement.** El formato es CIMObjectPath, con el formato *<NamespacePath> : . " <ClassName> <Prop1> = \\ <Value1> \\ ", " <Prop2> = \\ " " <Value2> \\ ,* que especifica una instancia en el esquema CIM.

Esta propiedad se hereda de la **clase \_ AlertIndication de CIM.**

Los valores posibles son:

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)
</dt> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)
</dt> </dl>

</dd> <dt>

**AlertingManagedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Rutas de acceso WMI de la instancia para la que se genera la alerta.

</dd> <dt>

**AlertType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
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

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se detectó el evento subyacente.

</dd> <dt>

**Mensaje**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Mensaje con formato que se construye combinando algunos o todos los elementos dinámicos especificados en la propiedad **MessageArguments** con los elementos estáticos identificados de forma única por la propiedad **MessageID** en un registro de mensajes u otro catálogo asociado a la **propiedad OwningEntity.**

</dd> <dt>

**MessageArguments**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz que contiene el contenido dinámico del mensaje. Si el valor de **MessageID** es 32930, el argumento en la posición 0 es el **PoolID** de la instancia de [**\_ ResourcePool de Msvm**](msvm-resourcepoolcomponent.md) para la que se genera la alerta.

</dd> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica de forma única, dentro del ámbito de la **propiedad OwningEntity,** el formato de la **propiedad Message.** Los posibles valores para esta propiedad son:

32930 ("Storage de rendimiento insuficiente de QoS del grupo")

</dd> <dt>

**OtherAlertingElementFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que define los valores "Other" para **AlertingManagedElement.** Este valor DEBE establecerse en un valor distinto de NULL cuando **AlertingManagedElement** se establece en un valor de 1 ("Other"). Para todos los demás valores **de AlertingManagedElement**, el valor de esta cadena debe establecerse en NULL.

Esta propiedad se hereda de la **clase \_ AlertIndication de CIM.**

</dd> <dt>

**OwningEntity**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica de forma única la entidad propietaria de la definición del formato del **mensaje** descrito en esta instancia. El valor de esta propiedad siempre es "Microsoft-Windows- Hyper-V".

"Microsoft-Windows- Hyper-V"

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe la gravedad de la indicación de alerta. Los posibles valores para esta propiedad son:

<dl> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Información** (2)
</dt> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degradado o advertencia** (3)
</dt> </dl>

</dd> <dt>

**ProbableCause**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe la causa probable de la situación que dio lugar a la indicación de alerta.

<dl> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Storage problema de capacidad de almacenamiento** (50)
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

Descripción textual que corresponde al valor de la **propiedad ProbableCause.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

El proveedor WMI de Hyper-V no genera eventos para discos virtuales individuales con el fin de evitar la saturación de clientes con eventos en caso de errores de funcionamiento a gran escala de los sistemas de almacenamiento subyacentes.

Cuando un cliente recibe un evento **\_ StorageAlert de Msvm,** si el valor de la propiedad **ProbableCause** es 50 (problema de capacidad de Storage), el cliente puede detectar qué discos virtuales funcionan fuera de su directiva qoS mediante uno de estos procedimientos:

-   Consulte todas las [**instancias de \_ Msvm LogicalDisk**](msvm-logicaldisk.md) que se asignaron desde el grupo de recursos para el que se generó el evento. Estas **instancias de Msvm \_ LogicalDisk** están asociadas al grupo de recursos mediante la asociación [**\_ ElementAllocatedFromPool de Msvm.**](msvm-elementallocatedfrompool.md)
-   Filtre la lista de resultados seleccionando instancias cuyo OperationalStatus contiene Rendimiento insuficiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ AlertIndication**](cim-alertindication.md)
</dt> <dt>

[**Msvm \_ LogicalDisk**](msvm-logicaldisk.md)
</dt> <dt>

[**ResourcePool de Msvm \_**](msvm-resourcepoolcomponent.md)
</dt> </dl>

 

 





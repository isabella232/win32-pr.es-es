---
description: Representa una colección de puntos de referencia del sistema virtual.
ms.assetid: dc293f94-a683-468f-af05-ba99824d773e
title: Msvm_ReferencePointCollection (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointCollection
- Msvm_ReferencePointCollection.CollectionID
- Msvm_ReferencePointCollection.ElementName
- Msvm_ReferencePointCollection.ReferencePointType
- Msvm_ReferencePointCollection.ConsistencyLevel
- Msvm_ReferencePointCollection.VirtualSystemCollectionId
- Msvm_ReferencePointCollection.HasAssociatedLog
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 570590221ee8568d78e150fec3c359365c8434cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910142"
---
# <a name="msvm_referencepointcollection-class"></a>MSVM \_ ReferencePointCollection (clase)

Representa una colección de puntos de referencia del sistema virtual.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointCollection : CIM_Collection
{
  string  CollectionID;
  string  ElementName;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemCollectionId;
  boolean HasAssociatedLog;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ ReferencePointCollection** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ ReferencePointCollection** tiene estas propiedades.

<dl> <dt>

**Recopilación**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificación única del objeto de colección.

</dd> <dt>

**ConsistencyLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Nivel de coherencia del punto de referencia.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Coherencia de bloqueos** (1)


</dt> <dd>

El punto de referencia indica un punto en el tiempo en el que el sistema virtual se encontraba en un estado coherente con el bloqueo.

</dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Coherente** con la aplicación (2)


</dt> <dd>

El punto de referencia indica un punto en el tiempo en el que el sistema virtual estuvo en un estado coherente con la aplicación.

</dd> </dl>

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")
</dt> </dl>

Nombre definido por el usuario para la colección. Tenga en cuenta que no se garantiza que sea único.

</dd> <dt>

**HasAssociatedLog**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

**true** si todos los puntos de referencia de miembro tienen registros asociados. Esto solo es válido para los puntos de referencia basados en el registro. En el caso de los puntos de referencia basados en RCT, **HasAssociatedLog** se establece en **false**. En el caso de los puntos de referencia basados en el registro, una vez descartado el registro, **HasAssociatedLog** se convierte en **false**.

</dd> <dt>

**ReferencePointType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **en**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Indica el tipo del punto de referencia.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basado en el registro** (1)


</dt> <dd>

Seguimiento del registro de réplica de Hyper-V.

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT basado** (2)


</dt> <dd>

Basado en Change Tracking resistente de los discos virtuales.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Específico del proveedor** (32768... 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**VirtualSystemCollectionId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md).**CollectionID**")
</dt> </dl>

Identificador del [**\_ VirtualSystemCollection de MSVM**](msvm-virtualsystemcollection.md) al que pertenece este punto de referencia.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Colección CIM**](cim-collection.md)
</dt> </dl>

 


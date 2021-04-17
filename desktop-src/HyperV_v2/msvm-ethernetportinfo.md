---
description: Una asociación entre una instancia de la \_ clase MSVM EthernetSwitchPort y una instancia de la \_ clase MSVM EthernetPortData que representa los datos recopilados sobre el puerto mediante una extensión de conmutador.
ms.assetid: 08677914-af09-47b7-9d4d-406696e1f504
title: Msvm_EthernetPortInfo (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortInfo
- Msvm_EthernetPortInfo.Antecedent
- Msvm_EthernetPortInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c78dca7adedcf52d93530efdab0da6113855c6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687645"
---
# <a name="msvm_ethernetportinfo-class"></a>MSVM \_ EthernetPortInfo (clase)

Una asociación entre una instancia de la clase [**MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) y una instancia de la clase [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md) que representa los datos recopilados sobre el puerto mediante una extensión de conmutador.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortInfo : CIM_Dependency
{
  Msvm_EthernetSwitchPort REF Antecedent;
  Msvm_EthernetPortData   REF Dependent;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ EthernetPortInfo** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ EthernetPortInfo** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **MSVM \_ EthernetSwitchPort**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. antecedente")
</dt> </dl>

Instancia de la clase [**MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) que representa el puerto del conmutador.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **MSVM \_ EthernetPortData**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. Dependent")
</dt> </dl>

Instancia de la clase [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md) que representa los datos del puerto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


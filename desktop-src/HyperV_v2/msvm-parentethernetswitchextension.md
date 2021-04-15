---
description: Representa la asociación entre una extensión de conmutador Ethernet primaria y una extensión de conmutador Ethernet secundaria.
ms.assetid: a0a60214-d85d-4c64-b720-1c34abc25287
title: Msvm_ParentEthernetSwitchExtension (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ParentEthernetSwitchExtension
- Msvm_ParentEthernetSwitchExtension.Antecedent
- Msvm_ParentEthernetSwitchExtension.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8e215a01c9de98baa545dbb32b8279db4555f9cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688557"
---
# <a name="msvm_parentethernetswitchextension-class"></a>MSVM \_ ParentEthernetSwitchExtension (clase)

Representa la asociación entre una extensión de conmutador Ethernet primaria y una extensión de conmutador Ethernet secundaria.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ParentEthernetSwitchExtension : CIM_Dependency
{
  Msvm_EthernetSwitchExtension REF Antecedent;
  Msvm_EthernetSwitchExtension REF Dependent;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ ParentEthernetSwitchExtension** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ ParentEthernetSwitchExtension** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Referencia a una instancia de la clase [**MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) que representa la extensión del conmutador primario.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")
</dt> </dl>

Referencia a una instancia de la clase [**MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) que representa la extensión de conmutador secundario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


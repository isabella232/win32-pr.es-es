---
description: Describe los datos de configuración de un controlador de pantalla sintético virtual.
ms.assetid: cea79b24-4175-49db-a8b4-a9efb1fd0b96
title: Msvm_SyntheticDisplayControllerSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticDisplayControllerSettingData
- Msvm_SyntheticDisplayControllerSettingData.ResolutionType
- Msvm_SyntheticDisplayControllerSettingData.HorizontalResolution
- Msvm_SyntheticDisplayControllerSettingData.VerticalResolution
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 52935800eda641eb9015247e9320f33f22b40251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276178"
---
# <a name="msvm_syntheticdisplaycontrollersettingdata-class"></a>MSVM \_ SyntheticDisplayControllerSettingData (clase)

Describe los datos de configuración de un controlador de pantalla sintético virtual.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticDisplayControllerSettingData : CIM_ResourceAllocationSettingData
{
  uint8  ResolutionType;
  uint16 HorizontalResolution;
  uint16 VerticalResolution;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ SyntheticDisplayControllerSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ SyntheticDisplayControllerSettingData** tiene estas propiedades.

<dl> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Resolución horizontal.

</dd> <dt>

**ResolutionType**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El tipo de resolución.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Máximo** (2)


</dt> <dd></dd> <dt>

<span id="Single"></span><span id="single"></span><span id="SINGLE"></span>

<span id="Single"></span><span id="single"></span><span id="SINGLE"></span>**Single** (3)


</dt> <dd></dd> <dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Valor predeterminado** (4)


</dt> <dd>

> [!Note]  
> Agregado en Windows 10, versión 1703.

 

</dd> </dl>

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Resolución vertical.

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

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 





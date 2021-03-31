---
description: Contiene un resumen de información sobre el sistema del equipo virtual especificado.
ms.assetid: ab31d5db-a8d3-47bc-a024-0f4c4b93a34b
title: Msvm_ComputerSystemSummaryInformation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystemSummaryInformation
- Msvm_ComputerSystemSummaryInformation.Antecedent
- Msvm_ComputerSystemSummaryInformation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35248bcfa14609e8db25b148088b6feb8d161116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907992"
---
# <a name="msvm_computersystemsummaryinformation-class"></a>MSVM \_ ComputerSystemSummaryInformation (clase)

Contiene un resumen de información sobre el sistema del equipo virtual especificado.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Association, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ComputerSystemSummaryInformation : CIM_ElementView
{
  CIM_ComputerSystem          REF Antecedent;
  Msvm_SummaryInformationBase REF Dependent;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ ComputerSystemSummaryInformation** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ ComputerSystemSummaryInformation** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Un [**objeto \_ ComputerSystem de CIM**](cim-computersystem.md) que es una instancia de la representación normalizada del recurso administrado.

> [!Note]
>
> Tipo de DataType actualizado desde [**MSVM \_ ComputerSystem**](msvm-computersystem.md) en Windows 10, versión 1703.

 

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **MSVM \_ SummaryInformationBase**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")
</dt> </dl>

Instancia de [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) que representa una vista desnormalizada o agregada del recurso administrado representado por el [**MSVM \_ ComputerSystem**](msvm-computersystem.md) al que hace referencia la propiedad antecedente.

> [!Note]
>
> DataType actualizado desde [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) en Windows 10, versión 1703.

 

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

[**\_ELEMENTVIEW CIM**](cim-elementview.md)
</dt> </dl>

 


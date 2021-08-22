---
description: Contiene un resumen de información sobre el sistema de equipo virtual especificado.
ms.assetid: ab31d5db-a8d3-47bc-a024-0f4c4b93a34b
title: Msvm_ComputerSystemSummaryInformation clase
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
ms.openlocfilehash: 78ac2b89336a415bedd23e0ca4ecd6589abdefbf75a54900d716c78152d34d4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531765"
---
# <a name="msvm_computersystemsummaryinformation-class"></a>Clase Msvm \_ ComputerSystemSummaryInformation

Contiene un resumen de información sobre el sistema de equipo virtual especificado.

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

La **clase \_ ComputerSystemSummaryInformation de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ ComputerSystemSummaryInformation** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedentes")
</dt> </dl>

Objeto [**\_ ComputerSystem**](cim-computersystem.md) de CIM que es una instancia de en la representación normalizada del recurso administrado.

> [!Note]
>
> Tipo de datos actualizado desde [**Msvm \_ ComputerSystem**](msvm-computersystem.md) en Windows 10, versión 1703.

 

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Msvm \_ SummaryInformationBase**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")
</dt> </dl>

Instancia de [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) que representa una vista des normalizada o agregada del recurso administrado representado por el sistema de equipos de [**Msvm \_**](msvm-computersystem.md) al que hace referencia la propiedad Antecedentes.

> [!Note]
>
> Tipo de datos actualizado desde [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) en Windows 10, versión 1703.

 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ ElementView**](cim-elementview.md)
</dt> </dl>

 


---
description: La clase HostedBootSAP de CIM define el sistema \_ de equipo unitario de hospedaje para una clase \_ BootSAP de CIM.
ms.assetid: 2113de13-e7af-4a1c-ba80-27e2c57af8a0
ms.tgt_platform: multiple
title: CIM_HostedBootSAP clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootSAP
- CIM_HostedBootSAP.Dependent
- CIM_HostedBootSAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a69bad7de1a680054f93a9cb63596fff30538b31c02019e08ac58f643a0d81c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923595"
---
# <a name="cim_hostedbootsap-class"></a>Clase \_ HostedBootSAP de CIM

La **clase \_ HostedBootSAP de CIM** define el sistema de equipo unitario de hospedaje para una clase [**\_ BootSAP de CIM.**](cim-bootsap.md) Puesto que esta relación se subclasifica desde [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md), hereda el esquema de ámbito y nomenclatura definido para [**CIM \_ ServiceAccessPoint,**](cim-serviceaccesspoint.md)donde un punto de acceso se aplaza a su sistema de hospedaje. En este caso, **CIM \_ BootSAP** debe aplazar a su clase [**\_ UnitaryComputerSystem de CIM**](cim-unitarycomputersystem.md) de hospedaje.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{625B4512-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootSAP : CIM_HostedAccessPoint
{
  CIM_BootSAP               REF Dependent;
  CIM_UnitaryComputerSystem REF Antecedent;
};
```

## <a name="members"></a>Miembros

La **clase \_ HostedBootSAP de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ HostedBootSAP de CIM** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ UnitaryComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Un [**cim \_ unitaryComputerSystem**](cim-unitarycomputersystem.md) que describe el sistema de equipo unitario.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ BootSAP**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

[**\_ BootSAP cim**](cim-bootsap.md) que describe el SAP de arranque hospedado en el sistema informático unitario.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ HostedBootSAP** de CIM se deriva de [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md).

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md)
</dt> </dl>

 


---
description: La \_ clase CIM HostedBootSAP define el sistema de equipo unitario de hospedaje para una \_ clase BOOTSAP de CIM.
ms.assetid: 2113de13-e7af-4a1c-ba80-27e2c57af8a0
ms.tgt_platform: multiple
title: CIM_HostedBootSAP (clase)
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
ms.openlocfilehash: 12e801f420ca2c56cc8960175391cdd9a669a00d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000616"
---
# <a name="cim_hostedbootsap-class"></a>\_Clase HostedBootSAP de CIM

La clase **CIM \_ HostedBootSAP** define el sistema de equipo unitario de hospedaje para una clase [**\_ BootSAP de CIM**](cim-bootsap.md) . Puesto que esta relación se subclase de [**\_ HostedAccessPoint de CIM**](cim-hostedaccesspoint.md), hereda el esquema de ámbito y de nomenclatura definido para [**\_ punto de CIM**](cim-serviceaccesspoint.md), donde un punto de acceso se pospone a su sistema de hospedaje. En este caso, **\_ BootSAP CIM** debe diferir a su [**clase \_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md) de hospedaje.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

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

La clase **CIM \_ HostedBootSAP** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ HostedBootSAP** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ UnitaryComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Un [**\_ UnitaryComputerSystem de CIM**](cim-unitarycomputersystem.md) que describe el sistema del equipo unitario.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ BootSAP**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")
</dt> </dl>

Un [**\_ BootSAP de CIM**](cim-bootsap.md) que describe el SAP de arranque hospedado en el sistema del equipo unitario.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **CIM \_ HostedBootSAP** se deriva de [**\_ HostedAccessPoint de CIM**](cim-hostedaccesspoint.md).

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_HOSTEDACCESSPOINT CIM**](cim-hostedaccesspoint.md)
</dt> </dl>

 


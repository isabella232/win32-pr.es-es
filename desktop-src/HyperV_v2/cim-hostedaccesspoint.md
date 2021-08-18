---
description: Representa una asociación entre un punto de acceso de servicio (SAP) y el sistema que lo hospeda.
ms.assetid: 82db71d6-6d14-408e-87e0-fe869e454d4d
title: CIM_HostedAccessPoint (administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedAccessPoint
- CIM_HostedAccessPoint.Antecedent
- CIM_HostedAccessPoint.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2079d34af64b7819f7c7dc4991a00a9a01b350ee45c54b910a35f1008d45e510
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014633"
---
# <a name="cim_hostedaccesspoint-class-hyper-v-management"></a>CIM_HostedAccessPoint (administración de Hyper-V)

Representa una asociación entre un punto de acceso de servicio (SAP) y el sistema que lo hospeda. Un sistema puede hospedar varios puntos de acceso. Si se modela la implementación de SAP, debe implementarse mediante una característica de dispositivo o software que forma parte del sistema que hospeda sap.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_HostedAccessPoint : CIM_HostedDependency
{
  CIM_System             REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase \_ HostedAccessPoint** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ HostedAccessPoint** de CIM tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Sistema CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Sistema de hospedaje.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Los SAP que se hospedan en el sistema.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ HostedDependency**](cim-hosteddependency.md)
</dt> </dl>

 


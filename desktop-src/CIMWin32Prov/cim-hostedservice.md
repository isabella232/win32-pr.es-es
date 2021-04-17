---
description: La \_ clase CIM HostedService representa una asociación entre un servicio y el sistema en el que reside la funcionalidad.
ms.assetid: 23bb385d-dd22-4126-aea9-d2f22527223e
ms.tgt_platform: multiple
title: CIM_HostedService (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Dependent
- CIM_HostedService.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c63b28fed7977c9fce78fe1030afbe66d5b2d75e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659595"
---
# <a name="cim_hostedservice-class-cimwin32-wmi-providers"></a>CIM_HostedService (clase) (proveedores WMI de CIMWin32)

La clase **CIM \_ HostedService** representa una asociación entre un servicio y el sistema en el que reside la funcionalidad. Un sistema puede hospedar muchos servicios, que aplazan el sistema de hospedaje. El modelo no representa servicios hospedados en varios sistemas.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{83B2A7AA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedService : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_System  REF Antecedent;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ HostedService** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ HostedService** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ Sistema CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

[**\_ Sistema CIM**](cim-system.md) que describe el sistema de hospedaje.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ servicio CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Un [**\_ servicio CIM**](cim-service.md) que describe el servicio hospedado en el sistema.

</dd> </dl>

## <a name="remarks"></a>Observaciones

**CIM \_ HostedService** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).

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

[**Dependencia de CIM \_**](cim-dependency.md)
</dt> </dl>

 


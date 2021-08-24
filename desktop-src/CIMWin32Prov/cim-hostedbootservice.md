---
description: La clase \_ HostedBootService de CIM asocia un sistema de hospedaje y un servicio de arranque. Puesto que esta relación se subclasifica de CIM HostedService, hereda el esquema de ámbito y nomenclatura definido para el servicio, donde un servicio se aplaza a su \_ sistema de hospedaje.
ms.assetid: 91621288-a231-4423-94df-7601bdf2ebe1
ms.tgt_platform: multiple
title: CIM_HostedBootService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootService
- CIM_HostedBootService.Antecedent
- CIM_HostedBootService.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: abfd506a3962e05a8ab1087dc3a5dc43d4cd74fac08fac7344d3ff22fff49909
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921685"
---
# <a name="cim_hostedbootservice-class"></a>Clase \_ HostedBootService de CIM

La **clase \_ HostedBootService de CIM** asocia un sistema de hospedaje y un servicio de arranque. Puesto que esta relación se encuentra en subclases de [**CIM \_ HostedService,**](cim-hostedservice.md)hereda el esquema de ámbito y nomenclatura definido para el servicio, donde un servicio se aplaza a su sistema de hospedaje.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{6DAE7092-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootService : CIM_HostedService
{
  CIM_System      REF Antecedent;
  CIM_BootService REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase \_ HostedBootService** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ HostedBootService** de CIM tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Sistema CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (antecedente)
</dt> </dl>

Sistema [**CIM \_ que**](cim-system.md) describe el sistema de hospedaje.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ BootService**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Un [**servicio de \_ arranque CIM**](cim-bootservice.md) que describe el servicio de arranque hospedado en el sistema.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ HostedBootService** de CIM se deriva de [**CIM \_ HostedService**](cim-hostedservice.md).

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ HostedService**](cim-hostedservice.md)
</dt> </dl>

 


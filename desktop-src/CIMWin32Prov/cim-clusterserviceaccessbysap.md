---
description: La \_ clase CIM ClusterServiceAccessBySAP representa la relación entre un servicio de agrupación en clústeres y sus puntos de acceso.
ms.assetid: b1e03ef1-909c-4836-a75f-c8d88a4d0087
ms.tgt_platform: multiple
title: CIM_ClusterServiceAccessBySAP (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusterServiceAccessBySAP
- CIM_ClusterServiceAccessBySAP.Dependent
- CIM_ClusterServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b6e6f0df20f182be392de3fbb0cb13068cbeffc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000668"
---
# <a name="cim_clusterserviceaccessbysap-class"></a>\_Clase ClusterServiceAccessBySAP de CIM

La clase **CIM \_ ClusterServiceAccessBySAP** representa la relación entre un servicio de agrupación en clústeres y sus puntos de acceso.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[UUID("{88F073D8-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ClusterServiceAccessBySAP : CIM_ServiceAccessBySAP
{
  CIM_ClusteringSAP     REF Dependent;
  CIM_ClusteringService REF Antecedent;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ ClusterServiceAccessBySAP** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ ClusterServiceAccessBySAP** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ClusteringService**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Un [**\_ ClusteringService de CIM**](cim-clusteringservice.md) que describe el servicio de agrupación en clústeres.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ClusteringSAP**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")
</dt> </dl>

Un [**\_ ClusteringSAP de CIM**](cim-clusteringsap.md) que describe un punto de acceso para el servicio de agrupación en clústeres.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **CIM \_ ClusterServiceAccessBySAP** se deriva de [**\_ ServiceAccessBySAP de CIM**](cim-serviceaccessbysap.md).

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

[**\_SERVICEACCESSBYSAP CIM**](cim-serviceaccessbysap.md)
</dt> </dl>

 


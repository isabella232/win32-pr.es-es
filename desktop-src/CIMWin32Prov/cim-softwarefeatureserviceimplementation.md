---
description: La clase CIM SoftwareFeatureServiceImplementation representa una asociación entre un servicio y cómo \_ se implementa en el software.
ms.assetid: fa80cc91-8dd7-4726-a24a-5c4dfa3e786b
ms.tgt_platform: multiple
title: CIM_SoftwareFeatureServiceImplementation clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureServiceImplementation
- CIM_SoftwareFeatureServiceImplementation.Dependent
- CIM_SoftwareFeatureServiceImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc521de933a4567c0760495880baf9251a774938
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167977"
---
# <a name="cim_softwarefeatureserviceimplementation-class"></a>Cim \_ SoftwareFeatureServiceImplementation (clase)

La **\_ clase CIM SoftwareFeatureServiceImplementation** representa una asociación entre un servicio y cómo se implementa en el software. Un servicio se puede proporcionar mediante más de una característica de software, que funciona conjuntamente entre sí. Además, una característica de software puede proporcionar más de un servicio. Cuando varias características de software están asociadas a un único servicio, se supone que los elementos funcionan juntos para proporcionar el servicio. Si existen implementaciones diferentes de un servicio, cada implementación produciría instancias individuales del objeto de servicio. Las instancias individuales tendrían entonces asociaciones con las implementaciones únicas.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[UUID("{8AC984F4-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureServiceImplementation : CIM_Dependency
{
  CIM_Service         REF Dependent;
  CIM_SoftwareFeature REF Antecedent;
};
```

## <a name="members"></a>Members

La **\_ clase CIM SoftwareFeatureServiceImplementation** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM SoftwareFeatureServiceImplementation** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ SoftwareFeature**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Cim [**\_ SoftwareFeature que**](cim-softwarefeature.md) describe la característica de software anterior.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Servicio CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")
</dt> </dl>

Un [**servicio CIM \_**](cim-service.md) que describe el servicio dependiente.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ CIM SoftwareFeatureServiceImplementation** se deriva de [**la dependencia \_ CIM**](cim-dependency.md).

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

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

[**Dependencia \_ cim**](cim-dependency.md)
</dt> </dl>

 


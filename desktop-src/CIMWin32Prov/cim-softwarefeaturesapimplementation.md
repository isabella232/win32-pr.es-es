---
description: La clase CIM SoftwareFeatureSAPImplementation representa una asociación entre un punto de acceso de servicio (SAP) y cómo \_ se implementa en el software.
ms.assetid: d9a5a747-b37b-4005-a661-2bfc6a83bbb2
ms.tgt_platform: multiple
title: CIM_SoftwareFeatureSAPImplementation clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSAPImplementation
- CIM_SoftwareFeatureSAPImplementation.Dependent
- CIM_SoftwareFeatureSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4130163ce90aea7a72b4d76a5c6c20b0631edf3b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160339"
---
# <a name="cim_softwarefeaturesapimplementation-class"></a>Cim \_ SoftwareFeatureSAPImplementation (clase)

La **clase \_ CIM SoftwareFeatureSAPImplementation** representa una asociación entre un punto de acceso de servicio (SAP) y cómo se implementa en el software. Más de una característica de software puede proporcionar una sap para que funcione junto con otra. Además, una característica de software puede proporcionar más de un SAP. Cuando muchas características de software están asociadas a un único SAP, se supone que los elementos funcionan juntos para proporcionar el punto de acceso. Si existen implementaciones diferentes de un SAP, cada implementación daría como resultado instancias individuales del objeto de SAP. Las instancias individuales tendrían entonces asociaciones con las implementaciones únicas.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintaxis siguiente se simplifica a Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[UUID("{7EFCC186-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_SoftwareFeature    REF Antecedent;
};
```

## <a name="members"></a>Members

La **clase \_ CIM SoftwareFeatureSAPImplementation** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM SoftwareFeatureSAPImplementation** tiene estas propiedades.

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

Tipo de datos: **Cim \_ ServiceAccessPoint**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")
</dt> </dl>

Servicio [**\_ CIMAccessPoint**](cim-serviceaccesspoint.md) que describe el punto de acceso de servicio dependiente.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ CIM SoftwareFeatureSAPImplementation** se deriva de [**la dependencia \_ CIM**](cim-dependency.md).

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Dependencia \_ cim**](cim-dependency.md)
</dt> </dl>

 


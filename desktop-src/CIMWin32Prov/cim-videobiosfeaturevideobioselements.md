---
description: La \_ clase VideoBIOSFeatureVideoBIOSElements de CIM asocia una característica de BIOS de vídeo y sus elementos de BIOS de vídeo agregados.
ms.assetid: f1419505-213f-450e-8c96-45f547dd71da
ms.tgt_platform: multiple
title: CIM_VideoBIOSFeatureVideoBIOSElements (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSFeatureVideoBIOSElements
- CIM_VideoBIOSFeatureVideoBIOSElements.PartComponent
- CIM_VideoBIOSFeatureVideoBIOSElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 421b6814499240b3364ac1aed622e2b7c96e7313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153047"
---
# <a name="cim_videobiosfeaturevideobioselements-class"></a>\_Clase VideoBIOSFeatureVideoBIOSElements de CIM

La **clase \_ VideoBIOSFeatureVideoBIOSElements de CIM** asocia una característica de BIOS de vídeo y sus elementos de BIOS de vídeo agregados.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[UUID("{B3F86390-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VideoBIOSFeatureVideoBIOSElements : CIM_SoftwareFeatureSoftwareElements
{
  CIM_VideoBIOSElement REF PartComponent;
  CIM_VideoBIOSFeature REF GroupComponent;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ VideoBIOSFeatureVideoBIOSElements** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ VideoBIOSFeatureVideoBIOSElements** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ VideoBIOSFeature**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Un [**\_ VideoBIOSFeature de CIM**](cim-videobiosfeature.md) que describe la característica BIOS de vídeo.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ VideoBIOSElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Un [**\_ VideoBIOSElement de CIM**](cim-videobioselement.md) que describe el elemento de BIOS de vídeo que implementa las funciones descritas en la característica BIOS de vídeo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **CIM \_ VideoBIOSFeatureVideoBIOSElements** se deriva de [**\_ SoftwareFeatureSoftwareElements de CIM**](cim-softwarefeaturesoftwareelements.md).

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

[**\_SOFTWAREFEATURESOFTWAREELEMENTS CIM**](cim-softwarefeaturesoftwareelements.md)
</dt> </dl>

 


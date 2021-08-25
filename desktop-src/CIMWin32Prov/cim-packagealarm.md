---
description: La asociación Cim PackageAlarm representa la relación en la que se instala un dispositivo \_ de alarma como parte de un paquete. La instalación indica problemas con el entorno del paquete&8212; su estado de seguridad \# o su estado general.
ms.assetid: 4911502a-de9c-46b4-91f6-a042c69fd052
ms.tgt_platform: multiple
title: CIM_PackageAlarm clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageAlarm
- CIM_PackageAlarm.Dependent
- CIM_PackageAlarm.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c8fde43197bd71712986c52e6badcb4e13c13c39be81ad806a74fb3da7e8337a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820735"
---
# <a name="cim_packagealarm-class"></a>Cim \_ PackageAlarm (clase)

La [**\_ asociación Cim PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) representa la relación en la que se instala un dispositivo de alarma como parte de un paquete. La instalación indica problemas con el entorno del paquete su estado de seguridad o su estado general.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Aggregation, UUID("{FAF76B90-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageAlarm : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_AlarmDevice     REF Antecedent;
};
```

## <a name="members"></a>Miembros

La **clase \_ Cim PackageAlarm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ Cim PackageAlarm** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ AlarmDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

AlarmDevice [**\_ cim**](cim-alarmdevice.md) que describe el dispositivo de alarma del paquete.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ PhysicalPackage**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Un [**paquete \_ físico CIM**](cim-physicalpackage.md) que describe el paquete físico cuyo estado, seguridad, entorno, etc. está alarmado.

</dd> </dl>

## <a name="remarks"></a>Comentarios

**CIM \_ PackageAlarm se** deriva de la [**dependencia \_ CIM**](cim-dependency.md).

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

[**Dependencia \_ cim**](cim-dependency.md)
</dt> </dl>

 


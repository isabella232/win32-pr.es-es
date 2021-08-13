---
description: La clase \_ de asociación Cim DeviceAccessedByFile especifica el dispositivo lógico al que se accede mediante la clase DeviceFile CIM a la que se \_ hace referencia.
ms.assetid: 8ba44f40-8b84-4f5c-b719-aded10877654
ms.tgt_platform: multiple
title: CIM_DeviceAccessedByFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceAccessedByFile
- CIM_DeviceAccessedByFile.Dependent
- CIM_DeviceAccessedByFile.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 24526d7743b1f4939f2240c751f7da2bfecfacfe13d2ddf3cbc7fdd73c1d260e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119321645"
---
# <a name="cim_deviceaccessedbyfile-class"></a>Cim \_ DeviceAccessedByFile (clase)

La **clase \_ de asociación Cim DeviceAccessedByFile** especifica el dispositivo lógico al que se accede mediante la clase [**\_ DeviceFile CIM**](cim-devicefile.md) a la que se hace referencia.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{05D1FFF2-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceAccessedByFile : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_DeviceFile    REF Antecedent;
};
```

## <a name="members"></a>Miembros

La **clase \_ Cim DeviceAccessedByFile** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM DeviceAccessedByFile** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ DeviceFile**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Un [**archivo \_ DeviceFile CIM**](cim-devicefile.md) que describe el archivo de dispositivo.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")
</dt> </dl>

Un [**dispositivo \_ lógico CIM**](cim-logicaldevice.md) que describe el dispositivo al que se accede mediante el archivo de dispositivo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

WMI no implementa esta clase.

La **clase \_ Cim DeviceAccessedByFile** se deriva de la [**dependencia \_ CIM**](cim-dependency.md).

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

[**Dependencia \_ cim**](cim-dependency.md)
</dt> </dl>

 


---
description: La \_ clase CIM DeviceServiceImplementation representa una asociación entre un servicio y cómo se implementa.
ms.assetid: 5e2e3975-8338-4bf4-8c73-5be4b93fa2c8
ms.tgt_platform: multiple
title: CIM_DeviceServiceImplementation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceServiceImplementation
- CIM_DeviceServiceImplementation.Dependent
- CIM_DeviceServiceImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ae96d94c95ddda684dbb4d17a2d8eb52fc6ffd4b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000691"
---
# <a name="cim_deviceserviceimplementation-class"></a>\_Clase DeviceServiceImplementation de CIM

La clase **CIM \_ DeviceServiceImplementation** representa una asociación entre un servicio y cómo se implementa. Cuando hay varios dispositivos asociados a un servicio, los elementos funcionan conjuntamente para proporcionar el servicio. Si existen implementaciones diferentes de un servicio, cada implementación tiene como resultado la creación de instancias individuales del objeto de servicio.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{290FC242-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceServiceImplementation : CIM_Dependency
{
  CIM_Service       REF Dependent;
  CIM_LogicalDevice REF Antecedent;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ DeviceServiceImplementation** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ DeviceServiceImplementation** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ LogicalDevice de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que describe el dispositivo lógico.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ servicio CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")
</dt> </dl>

Un [**\_ servicio CIM**](cim-service.md) que describe el servicio implementado mediante el dispositivo lógico.

</dd> </dl>

## <a name="remarks"></a>Observaciones

WMI no implementa esta clase.

La clase **CIM \_ DeviceServiceImplementation** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).

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

 


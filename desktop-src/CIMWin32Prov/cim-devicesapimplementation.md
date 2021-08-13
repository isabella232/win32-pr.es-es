---
description: La clase Cim DeviceSAPImplementation representa una asociación entre un punto de acceso de servicio \_ (SAP) y cómo se implementa.
ms.assetid: 6c059507-bfc0-4630-9b39-9c4bae2bf138
ms.tgt_platform: multiple
title: CIM_DeviceSAPImplementation clase (proveedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSAPImplementation
- CIM_DeviceSAPImplementation.Dependent
- CIM_DeviceSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1643441d24e465ff7311daae52e4bc7773b556c7719ec7a93c35ff478740fd0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119321615"
---
# <a name="cim_devicesapimplementation-class-cimwin32-wmi-providers"></a>CIM_DeviceSAPImplementation clase (proveedores WMI CIMWin32)

La **clase \_ Cim DeviceSAPImplementation** representa una asociación entre un punto de acceso de servicio (SAP) y cómo se implementa. Cuando muchos dispositivos lógicos están asociados a un SAP, los elementos funcionan juntos para proporcionar el punto de acceso. Si existen implementaciones diferentes de un SAP, cada implementación produce instancias individuales del objeto SAP.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[UUID("{1BE949DA-DB36-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_DeviceSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_LogicalDevice      REF Antecedent;
};
```

## <a name="members"></a>Miembros

La **clase \_ DeviceSAPImplementation** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ DeviceSAPImplementation** de CIM tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ Cim LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Un [**\_ dispositivo lógico CIM**](cim-logicaldevice.md) que describe el dispositivo lógico.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cim \_ ServiceAccessPoint**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidar**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Servicio [**\_ CIMAccessPoint que**](cim-serviceaccesspoint.md) describe el punto de acceso de servicio implementado mediante el dispositivo lógico.

</dd> </dl>

## <a name="remarks"></a>Comentarios

WMI no implementa esta clase.

La **clase \_ DeviceSAPImplementation** de CIM se deriva de [**la dependencia \_ CIM**](cim-dependency.md).

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

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

 


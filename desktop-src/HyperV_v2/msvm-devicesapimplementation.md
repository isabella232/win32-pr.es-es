---
description: 'Msvm_DeviceSAPImplementation clase : asociación entre un punto de acceso de servicio (SAP) y cómo se implementa.'
ms.assetid: 36108521-A699-4498-A962-DC0801D9EE81
title: Msvm_DeviceSAPImplementation clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DeviceSAPImplementation
- Msvm_DeviceSAPImplementation.Antecedent
- Msvm_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f5a8ccd02926d781f46ef86b26873c5dad86565ac90df47a5835cdf2ca4823a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525415"
---
# <a name="msvm_devicesapimplementation-class"></a>Clase Msvm \_ DeviceSAPImplementation

Asociación entre un punto de acceso de servicio (SAP) y cómo se implementa. La cardinalidad de esta asociación es de varios a varios. Un SAP se puede proporcionar mediante más de un dispositivo lógico, que funciona conjuntamente. Cualquier dispositivo puede proporcionar más de un SAP. Cuando muchos dispositivos lógicos están asociados a un único SAP, se supone que estos elementos funcionan juntos para proporcionar el punto de acceso. Si existen implementaciones diferentes de un SAP, cada una de estas implementaciones daría lugar a instancias individuales del objeto de SAP. Estas instancias individuales tendrían asociaciones con las implementaciones únicas.

La sintaxis siguiente se Managed Object Format código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ DeviceSAPImplementation** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ DeviceSAPImplementation** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El dispositivo lógico. Esta propiedad se hereda de [**CIM \_ DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Punto de acceso de servicio implementado mediante el dispositivo lógico. Esta propiedad se hereda de [**CIM \_ DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase \_ Msvm DeviceSAPImplementation** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Ejemplos

Consulte [Consulta de objetos de red.](querying-networking-objects.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dispositivos \_ CIMSAPImplementation**](cim-devicesapimplementation.md)
</dt> <dt>

[**Dispositivos \_ CIMSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)
</dt> </dl>

 


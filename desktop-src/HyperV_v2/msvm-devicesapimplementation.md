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
ms.openlocfilehash: 6fbe3c9b85e0a8c9f0c6a07d1db03784c4ac15e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112103"
---
# <a name="msvm_devicesapimplementation-class"></a>Clase Msvm \_ DeviceSAPImplementation

Asociación entre un punto de acceso de servicio (SAP) y cómo se implementa. La cardinalidad de esta asociación es de varios a varios. Un SAP se puede proporcionar mediante más de un dispositivo lógico, que funciona conjuntamente. Cualquier dispositivo puede proporcionar más de un SAP. Cuando muchos dispositivos lógicos están asociados a un único SAP, se supone que estos elementos funcionan juntos para proporcionar el punto de acceso. Si existen implementaciones diferentes de un SAP, cada una de estas implementaciones daría como resultado instancias individuales del objeto de SAP. Estas instancias individuales tendrían entonces asociaciones con las implementaciones únicas.

La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.

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

Tipo de datos: **[ **\_ Cim LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El dispositivo lógico. Esta propiedad se hereda de [**CIM \_ DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Cim \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**
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
| Cliente mínimo compatible<br/> | Windows 8 solo \[ aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Dispositivos \_ CIMSAPImplementation**](cim-devicesapimplementation.md)
</dt> <dt>

[**Dispositivos \_ CIMSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)
</dt> </dl>

 


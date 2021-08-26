---
title: Propiedad IVMVirtualMachine Name (VPCCOMInterfaces.h)
description: Nombre de la configuración de la máquina virtual.
ms.assetid: 90acedbf-4159-48a3-a9e9-6f1ee00dab8b
keywords:
- Nombre de la propiedad Virtual PC
- Propiedad de nombre Virtual PC , IVMVirtualMachine (interfaz)
- IVMVirtualMachine interface Virtual PC , propiedad Name
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Name
- IVMVirtualMachine.get_Name
- IVMVirtualMachine.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5219e6fcb24805feb0370bd157d014767a9348e87e500d8c94fa26ff502b6597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006805"
---
# <a name="ivmvirtualmachinename-property"></a>IVMVirtualMachine::Name, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera y establece el nombre de la configuración de la máquina virtual.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Name(
  [in]          BSTR virtualMachineName
);

HRESULT get_Name(
  [out, retval] BSTR *virtualMachineName
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica el nombre de la configuración de la máquina virtual. La longitud del nombre no puede tener más de 80 caracteres y la longitud total de la ruta de acceso completa que incluye el archivo de configuración de nombre de máquina virtual no puede ser superior a **MAX \_ PATH** (260) caracteres.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                    | Significado                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                       | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                         | El parámetro es **NULL.**<br/>                                                           |
| <dl> <dt>E \_ Invalidarg</dt> <dt>0x80000003</dt> </dl>                      | El parámetro no es válido o es una cadena vacía.<br/>                                    |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>                 | La configuración es desconocida.<br/>                                                        |
| <dl> <dt>Máquina virtual \_ E \_ PREF \_ VM \_ ACTIVE</dt> <dt>0xA0040302</dt> </dl>            | La máquina virtual se ejecuta o se guarda.<br/>                                             |
| <dl> <dt>Máquina virtual \_ E \_ CONFIG NO NAME \_ \_ 0xA0040400</dt> <dt></dt> </dl>            | El *parámetro virtualMachineName* está vacío.<br/>                                         |
| <dl> <dt>Máquina virtual \_ E \_ CONFIG NAME TOO LONG \_ \_ \_ 0xA00400401</dt> <dt></dt> </dl>    | El parámetro contiene demasiados caracteres.<br/>                                          |
| <dl> <dt>Máquina virtual \_ E \_ CONFIG NAME INVALID \_ \_ \_ CHAR</dt> <dt>0xA0040402</dt> </dl> | El parámetro contiene uno de los siguientes caracteres no válidos " \* ?:<>/ \| \\ "".<br/> |
| <dl> <dt>Máquina virtual \_ E \_ CONFIG DUPLICATE NAME \_ \_ 0xA0040403</dt> <dt></dt> </dl>     | El nombre especificado ya existe como nombre de otra máquina virtual.<br/>            |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                 | Se produjo un error inesperado.<br/>                                                    |



## <a name="remarks"></a>Comentarios

Los nombres de máquina virtual no tienen en cuenta mayúsculas de minúsculas, por ejemplo, "MyVM" y "myvm" hacen referencia a la misma máquina virtual. Esta es la propiedad predeterminada para [**IVMVirtualMachine**](ivmvirtualmachine.md).

Si VPC.exe está en ejecución y la máquina virtual se guarda, el establecimiento de **la propiedad Name** no se realizará correctamente. Si VPC.exe está en ejecución y la máquina virtual se guarda, el establecimiento de la propiedad **Name** se realizará correctamente VPC.exe siguiente inicio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualMachine se define como \_ f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 


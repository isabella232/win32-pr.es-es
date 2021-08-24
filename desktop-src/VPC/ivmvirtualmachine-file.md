---
title: Propiedad IVMVirtualMachine File (VPCCOMInterfaces.h)
description: Recupera la ruta de acceso completa del archivo .vmc para la configuración de la máquina virtual.
ms.assetid: fc215068-e908-417c-bd68-214539a0a14e
keywords:
- Propiedad de archivo Virtual PC
- Propiedad de archivo Virtual PC , interfaz IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC , Propiedad File
topic_type:
- apiref
api_name:
- IVMVirtualMachine.File
- IVMVirtualMachine.get_File
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3868cc0210f23353d478b9377178778f4fc5fcf564e0f1a9f386f7152d058bac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768075"
---
# <a name="ivmvirtualmachinefile-property"></a>IVMVirtualMachine::File, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la ruta de acceso completa del archivo .vmc para la configuración de la máquina virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_File(
  [out, retval] BSTR *virtualMachineXMLFile
);
```



## <a name="property-value"></a>Valor de propiedad

Nombre completo del archivo \* ".vmc" que describe esta configuración de máquina virtual.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>     |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>        |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | La configuración es desconocida.<br/>     |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualMachine se define como \_ f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 


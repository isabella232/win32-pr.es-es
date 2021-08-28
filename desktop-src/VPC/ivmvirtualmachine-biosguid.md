---
title: Propiedad IVMVirtualMachine BIOSGUID (VPCCOMInterfaces.h)
description: GUID del BIOS.
ms.assetid: d866838d-31e9-41f1-be57-43e778b9db95
keywords:
- BIOSGUID, propiedad Virtual PC
- Propiedad BIOSGUID Pc virtual, interfaz IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, propiedad BIOSGUID
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BIOSGUID
- IVMVirtualMachine.get_BIOSGUID
- IVMVirtualMachine.put_BIOSGUID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bdad9260cb4edb6f168c82f1ee9f888b3cdacdbe6fca7ea7c40bab21c0a9856
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117938307"
---
# <a name="ivmvirtualmachinebiosguid-property"></a>IVMVirtualMachine::BIOSGUID, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera y establece el GUID del BIOS.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BIOSGUID(
  [in]          BSTR biosGUID
);

HRESULT get_BIOSGUID(
  [out, retval] BSTR *biosGUID
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica el GUID del BIOS. Incluya llaves izquierda y derecha alrededor de los dígitos hexadecimales.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                               | Significado                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                  | La operación se realizó correctamente.<br/>                       |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                    | El parámetro es **NULL.**<br/>                          |
| <dl> <dt>E \_ InvalidarG</dt> <dt>0x80000003</dt> </dl>                 | El parámetro no es válido o es una cadena vacía.<br/>   |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>            | La configuración es desconocida.<br/>                       |
| <dl> <dt>Máquina virtual \_ E \_ MÁQUINA VIRTUAL EN EJECUCIÓN O \_ \_ \_ GUARDADA</dt> <dt>0XA004020B</dt> </dl> | La máquina virtual está en estado en ejecución o guardado.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>            | Se produjo un error inesperado.<br/>                   |



## <a name="remarks"></a>Comentarios

Esta propiedad no contendrá información válida hasta que la máquina virtual se haya iniciado por primera vez. Se devolverá una cadena vacía si se lee antes del inicio inicial.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 


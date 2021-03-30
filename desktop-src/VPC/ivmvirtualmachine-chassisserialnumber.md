---
title: Propiedad IVMVirtualMachine ChassisSerialNumber (VPCCOMInterfaces. h)
description: Número de serie del chasis.
ms.assetid: 03e02e6e-6819-4052-a0e0-9167eb5fdf4b
keywords:
- Propiedad ChassisSerialNumber Virtual PC
- Propiedad ChassisSerialNumber Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad ChassisSerialNumber
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ChassisSerialNumber
- IVMVirtualMachine.get_ChassisSerialNumber
- IVMVirtualMachine.put_ChassisSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00edbac12248f624ac06d1f7b88c3782c3f5a3df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079467"
---
# <a name="ivmvirtualmachinechassisserialnumber-property"></a>IVMVirtualMachine:: ChassisSerialNumber (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera y establece el número de serie del chasis.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_ChassisSerialNumber(
  [in]          BSTR chasisSerialNumber
);

HRESULT get_ChassisSerialNumber(
  [out, retval] BSTR *chassisSerialNumber
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica el número de serie del chasis.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                               | Significado                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                  | La operación se realizó correctamente.<br/>                                               |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                    | El parámetro es **null**.<br/>                                                  |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                 | El parámetro tiene más de 32 caracteres, una cadena vacía o no es válido.<br/> |
| <dl> <dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt> </dl>            | La configuración es desconocida.<br/>                                               |
| <dl> <dt>Máquina virtual \_ \_Máquina virtual en \_ ejecución \_ o \_ guardada</dt> <dt>0xA004020B</dt> </dl> | La máquina virtual está en estado en ejecución o guardada.<br/>                         |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>            | Se produjo un error inesperado.<br/>                                           |



## <a name="remarks"></a>Observaciones

Esta propiedad no contendrá información válida hasta que la máquina virtual se haya iniciado por primera vez. Se devolverá una cadena vacía si se lee antes del inicio inicial.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 


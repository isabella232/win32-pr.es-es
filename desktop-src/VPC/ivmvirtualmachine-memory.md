---
title: Propiedad de memoria IVMVirtualMachine (VPCCOMInterfaces. h)
description: Cantidad de memoria física en la máquina virtual, en megabytes.
ms.assetid: 1a1d4cc7-a537-49f0-981f-0b72eca9013e
keywords:
- Propiedad de memoria virtual PC
- Propiedad de memoria virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad de memoria
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Memory
- IVMVirtualMachine.get_Memory
- IVMVirtualMachine.put_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b73251b58639e0311e33120cd4bb0e778a017b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651382"
---
# <a name="ivmvirtualmachinememory-property"></a>IVMVirtualMachine:: Memory (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera y establece la cantidad de memoria física en la máquina virtual, en megabytes.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Memory(
  [in]          long megabytesOfMemory
);

HRESULT get_Memory(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica la cantidad de memoria física, en megabytes.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                         | Significado                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                            | La operación se realizó correctamente.<br/>                  |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>              | El parámetro es **null**.<br/>                     |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>           | El parámetro no es válido o está fuera del intervalo.<br/> |
| <dl> <dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt> </dl>      | La configuración es desconocida.<br/>                  |
| <dl> <dt>Máquina virtual \_ E \_ Pref \_ not \_ found</dt> <dt>0xA0040300</dt> </dl> | No se encontró la preferencia.<br/>                  |
| <dl> <dt>Máquina virtual \_ E \_ preft \_ VM \_ Active</dt> <dt>0xA0040302</dt> </dl> | La máquina virtual está en ejecución o guardada.<br/>       |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>      | Se produjo un error inesperado.<br/>              |



## <a name="remarks"></a>Observaciones

La cantidad de memoria física en una máquina virtual debe ser de al menos 4 MB. El límite superior de la memoria depende de la configuración del host, pero puede tener como máximo 3.712 MB.

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

 


---
title: Método IVMVirtualMachine AddNetworkAdapter (VPCCOMInterfaces.h)
description: Agrega una interfaz de red a la máquina virtual.
ms.assetid: 1fa39d2c-4a5a-42cb-afa4-520bf19b8cc8
keywords:
- AddNetworkAdapter method Virtual PC
- Método AddNetworkAdapter Virtual PC , interfaz IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC , Método AddNetworkAdapter
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 799aa859ab8cd2bea4da29154af00c6537bfd180b0719f6d0252b1b0ddea8bd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866745"
---
# <a name="ivmvirtualmachineaddnetworkadapter-method"></a>IVMVirtualMachine::AddNetworkAdapter (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Agrega una interfaz de red a la máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddNetworkAdapter(
  [out, retval] IVMNetworkAdapter **networkAdapter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*networkAdapter* \[ out, retval\]
</dt> <dd>

Objeto [**IVMNetworkAdapter.**](ivmnetworkadapter.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                            | Descripción                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                  | La operación se realizó correctamente.<br/>                        |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                    | El *parámetro networkAdapter* es **NULL.**<br/>          |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>            | La configuración es desconocida.<br/>                        |
| <dl> <dt>**Máquina virtual \_ E \_ PREF \_ ILLEGAL \_ VALUE**</dt> <dt>0xA0040301</dt> </dl>   | No se pueden agregar más de cuatro (4) adaptadores de red.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ MÁQUINA VIRTUAL EN EJECUCIÓN O GUARDADA \_ \_ \_ 0XA004020B**</dt> <dt></dt> </dl> | La máquina virtual está en estado en ejecución o guardado.<br/>  |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>            | Se produjo un error inesperado.<br/>                    |



 

## <a name="remarks"></a>Comentarios

Solo puede agregar una nueva interfaz de red a una máquina virtual detenida. El adaptador de red recién creado no está conectado a una red virtual.

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

 


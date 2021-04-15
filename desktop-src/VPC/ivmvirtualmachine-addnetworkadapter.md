---
title: Método IVMVirtualMachine AddNetworkAdapter (VPCCOMInterfaces. h)
description: Agrega una interfaz de red a la máquina virtual.
ms.assetid: 1fa39d2c-4a5a-42cb-afa4-520bf19b8cc8
keywords:
- Método AddNetworkAdapter Virtual PC
- Método AddNetworkAdapter Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método AddNetworkAdapter
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
ms.openlocfilehash: b8d24351e5f5a32aff08e755329ac12baaaaf546
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695985"
---
# <a name="ivmvirtualmachineaddnetworkadapter-method"></a>IVMVirtualMachine:: AddNetworkAdapter (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Agrega una interfaz de red a la máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddNetworkAdapter(
  [out, retval] IVMNetworkAdapter **networkAdapter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*adaptador* \[ de la out, retval\]
</dt> <dd>

Objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                            | Descripción                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                  | La operación se realizó correctamente.<br/>                        |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                    | El parámetro *adaptador de adaptador* es **null**.<br/>          |
| <dl> <dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt> </dl>            | La configuración es desconocida.<br/>                        |
| <dl> <dt>**Máquina virtual \_ E \_ prefe el \_ \_ valor no válido**</dt> <dt>0xA0040301</dt> </dl>   | No se pueden agregar más de cuatro (4) adaptadores de red.<br/> |
| <dl> <dt>**Máquina virtual \_ \_Máquina virtual en \_ ejecución \_ o \_ guardada**</dt> <dt>0xA004020B</dt> </dl> | La máquina virtual está en estado en ejecución o guardada.<br/>  |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>            | Se produjo un error inesperado.<br/>                    |



 

## <a name="remarks"></a>Observaciones

Solo puede Agregar una nueva interfaz de red a una máquina virtual detenida. El adaptador de red recién creado no está conectado a una red virtual.

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

 


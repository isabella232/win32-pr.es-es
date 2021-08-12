---
title: Método IVMNetworkAdapter AttachToVirtualNetwork (VPCCOMInterfaces.h)
description: Asocia la interfaz de red a la red virtual especificada.
ms.assetid: c743e930-c22e-4f32-b691-f7adc2485fed
keywords:
- Método Virtual PC AttachToVirtualNetwork
- Método AttachToVirtualNetwork pc virtual, interfaz IVMNetworkAdapter
- IVMNetworkAdapter interface Virtual PC , Método AttachToVirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.AttachToVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b03bf8bd0bcde6ba0353ce62e227c100a17ed1df0b2267ad54cd127c95c5836b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593233"
---
# <a name="ivmnetworkadapterattachtovirtualnetwork-method"></a>IVMNetworkAdapter::AttachToVirtualNetwork (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Asocia la interfaz de red a la red virtual especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AttachToVirtualNetwork(
  [in] IVMVirtualNetwork *virtualNetwork
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*virtualNetwork* \[ En\]
</dt> <dd>

La red virtual a la que se conectará esta NIC virtual. Vea [**IVMVirtualNetwork**](ivmvirtualnetwork.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                          | Descripción                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                                                                                       | La operación se realizó correctamente.<br/>                           |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                  | El parámetro es **NULL.**<br/>                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                               | El parámetro no contiene una red virtual válida.<br/> |
| <dl> <dt>**HRESULT \_ DESDE \_ WIN32(ACCESO DE ERROR \_ \_ DENEGADO)**</dt> <dt>0x80070005</dt> </dl> | Se denegó el acceso a la red virtual solicitada.<br/>     |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                          | La máquina virtual no es válida o ya no existe.<br/>     |
| <dl> <dt>**IDENTIFICADOR DE RED VIRTUAL NO VÁLIDO DE LA \_ \_ MÁQUINA \_ \_ \_ VIRTUAL E**</dt> </dl>                                                                        | El parámetro no es una red virtual existente.<br/>       |
| <dl> <dt>**EXCEPCIÓN \_ DISP E \_**</dt> </dl>                                                                                          | Se produjo un error inesperado.<br/>                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMNetworkAdapter se define como \_ e32e4165-22b8-4dc0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 


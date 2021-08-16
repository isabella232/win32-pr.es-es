---
title: Método IVMVirtualMachineEvents OnEnhancedVideoModeChanged (VPCCOMInterfaces.h)
description: Recibe la notificación de que ha cambiado la compatibilidad de una máquina virtual con el modo de vídeo mejorado.
ms.assetid: be22a859-4687-4647-9f53-f79ae8ad52a5
keywords:
- Método Virtual PC OnEnhancedVideoModeChanged
- Método Virtual PC OnEnhancedVideoModeChanged, interfaz IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC , OnEnhancedVideoModeChanged method
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnEnhancedVideoModeChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13bcdee9db2cf4b37b40d0cc77d6592c5ca1552b0a59642a01c2fe84bf4f69f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056623"
---
# <a name="ivmvirtualmachineeventsonenhancedvideomodechanged-method"></a>IVMVirtualMachineEvents::OnEnhancedVideoModeChanged (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recibe la notificación de que ha cambiado la compatibilidad de una máquina virtual con el modo de vídeo mejorado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnEnhancedVideoModeChanged(
  [in] VARIANT_BOOL enhancedVideoMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*enhancedVideoMode* \[ En\]
</dt> <dd>

Indica si el modo de vídeo mejorado está disponible.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents se define como 9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 


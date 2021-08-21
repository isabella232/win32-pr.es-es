---
title: Método OnConfigurationChanged de IVMVirtualMachineEvents (VPCCOMInterfaces.h)
description: Recibe la notificación de que ha cambiado un valor en la configuración de esta máquina virtual.
ms.assetid: 1955f23e-b318-41aa-b82e-81283be81608
keywords:
- Equipo virtual del método OnConfigurationChanged
- Método OnConfigurationChanged De PC virtual, interfaz IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC , OnConfigurationChanged method
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnConfigurationChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36ca4d3b72d9cd2b06db2ca7b7b65e0c63795a4db0e52ccd9b76a62ff8b192e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056643"
---
# <a name="ivmvirtualmachineeventsonconfigurationchanged-method"></a>IVMVirtualMachineEvents::OnConfigurationChanged (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recibe la notificación de que ha cambiado un valor en la configuración de esta máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnConfigurationChanged(
  [in] BSTR    configKey,
  [in] VARIANT configData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*configKey* \[ En\]
</dt> <dd>

Valor dentro de la configuración que ha cambiado.

</dd> <dt>

*configData* \[ En\]
</dt> <dd>

Nuevo valor para la configuración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Se llama a este método cuando cambia la configuración de esta máquina virtual. El programa cliente debe implementar este método de interfaz para recibir la notificación del evento vmVirtualMachineEvent ConfigurationChanged que se \_ origina en [**IVMVirtualMachine**](ivmvirtualmachine.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents se define como 9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 


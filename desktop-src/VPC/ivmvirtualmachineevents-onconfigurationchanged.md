---
title: Método IVMVirtualMachineEvents OnConfigurationChanged (VPCCOMInterfaces. h)
description: Recibe la notificación de que ha cambiado un valor de la configuración de esta máquina virtual.
ms.assetid: 1955f23e-b318-41aa-b82e-81283be81608
keywords:
- Método OnConfigurationChanged Virtual PC
- Método OnConfigurationChanged Virtual PC, interfaz IVMVirtualMachineEvents
- Interfaz IVMVirtualMachineEvents Virtual PC, método OnConfigurationChanged
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
ms.openlocfilehash: 10459562da2d87b8c883217e003cd822ef923fad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995893"
---
# <a name="ivmvirtualmachineeventsonconfigurationchanged-method"></a>IVMVirtualMachineEvents:: OnConfigurationChanged (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recibe la notificación de que ha cambiado un valor de la configuración de esta máquina virtual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnConfigurationChanged(
  [in] BSTR    configKey,
  [in] VARIANT configData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*configKey* \[ de\]
</dt> <dd>

Valor dentro de la configuración que ha cambiado.

</dd> <dt>

*configData* \[ de\]
</dt> <dd>

Nuevo valor de la configuración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Se llama a este método cuando cambia la configuración de esta máquina virtual. El programa cliente debe implementar este método de interfaz para recibir la notificación del \_ evento vmVirtualMachineEvent ConfigurationChanged que se origina desde [**IVMVirtualMachine**](ivmvirtualmachine.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents se define como 9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 


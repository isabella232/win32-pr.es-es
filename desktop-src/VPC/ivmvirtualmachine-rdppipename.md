---
title: Propiedad IVMVirtualMachine RdpPipeName (VPCCOMInterfaces.h)
description: Recupera el nombre de la canalización con nombre de conexión RDP usada para el vídeo y la entrada.
ms.assetid: 0c2d0f23-40cd-4a86-96dd-546fb3570871
keywords:
- RdpPipeName, propiedad Virtual PC
- Propiedad RdpPipeName Virtual PC , interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Pc virtual, propiedad RdpPipeName
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RdpPipeName
- IVMVirtualMachine.get_RdpPipeName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0616cd36e35690649cac145b9462b96af19499e3a10f7fdee3ec2820891544d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119394455"
---
# <a name="ivmvirtualmachinerdppipename-property"></a>Propiedad IVMVirtualMachine::RdpPipeName

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el nombre de la canalización con nombre de conexión RDP usada para el vídeo y la entrada.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_RdpPipeName(
  [out, retval] BSTR *RdpPipeName
);
```



## <a name="property-value"></a>Valor de propiedad

Nombre de la conexión RDP denominada canalización que se usa para el vídeo y la entrada.

## <a name="error-codes"></a>Códigos de error

Si el método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**



| Nombre o valor                                                                                                                                                         | Significado                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                            | La operación se realizó correctamente.<br/>          |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>              | El parámetro RdpPipeName es **NULL.**<br/> |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl> | La máquina virtual no se está ejecutando.<br/>    |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>      | Se produjo un error desconocido.<br/>             |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualMachine se define como \_ f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 


---
title: Propiedad IVMVirtualMachine BaseBoardSerialNumber (VPCCOMInterfaces.h)
description: Número de serie de la placa base.
ms.assetid: 374ad471-e0de-4e55-bab6-f7ddf3e5797f
keywords:
- BaseBoardSerialNumber, propiedad Virtual PC
- Interfaz Virtual PC de la propiedad BaseBoardSerialNumber , IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC , BaseBoardSerialNumber, propiedad
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BaseBoardSerialNumber
- IVMVirtualMachine.get_BaseBoardSerialNumber
- IVMVirtualMachine.put_BaseBoardSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2aaf205874eb7b8aaaead44a4d1a4b2775be4e01e076f1cc716058f8f9e45a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653085"
---
# <a name="ivmvirtualmachinebaseboardserialnumber-property"></a>IVMVirtualMachine::BaseBoardSerialNumber, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera y establece el número de serie de la placa base.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BaseBoardSerialNumber(
  [in]          BSTR baseBoardSerialNumber
);

HRESULT get_BaseBoardSerialNumber(
  [out, retval] BSTR *baseBoardSerialNumber
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica el número de serie de la placa base.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                               | Significado                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                  | La operación se realizó correctamente.<br/>                                               |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                    | El parámetro es **NULL.**<br/>                                                  |
| <dl> <dt>E \_ InvalidarG</dt> <dt>0x80000003</dt> </dl>                 | El parámetro tiene más de 32 caracteres, una cadena vacía o no es válido.<br/> |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>            | La configuración es desconocida.<br/>                                               |
| <dl> <dt>Máquina virtual \_ E \_ MÁQUINA VIRTUAL EN EJECUCIÓN O \_ \_ \_ GUARDADA</dt> <dt>0XA004020B</dt> </dl> | La máquina virtual está en estado en ejecución o guardado.<br/>                         |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>            | Se produjo un error inesperado.<br/>                                           |



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

 


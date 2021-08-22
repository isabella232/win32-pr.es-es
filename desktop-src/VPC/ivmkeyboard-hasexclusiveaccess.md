---
title: Propiedad HasExclusiveAccess de IVMKeyboard (VPCCOMInterfaces.h)
description: Indica si este objeto tiene control exclusivo sobre el dispositivo de teclado de la máquina virtual.
ms.assetid: edba154e-e700-488c-9133-91649daecef1
keywords:
- Equipo virtual de la propiedad HasExclusiveAccess
- Interfaz virtual de la propiedad HasExclusiveAccess, IVMKeyboard
- IVMKeyboard interface Virtual PC , Propiedad HasExclusiveAccess
topic_type:
- apiref
api_name:
- IVMKeyboard.HasExclusiveAccess
- IVMKeyboard.get_HasExclusiveAccess
- IVMKeyboard.put_HasExclusiveAccess
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c01e13e331824a0d1b6834cbb27da7eb4b5420a3cd3dbec94cdbdd494c79c95b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136728"
---
# <a name="ivmkeyboardhasexclusiveaccess-property"></a>IVMKeyboard::HasExclusiveAccess, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Indica si este objeto tiene control exclusivo sobre el dispositivo de teclado (VM) de la máquina virtual.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_HasExclusiveAccess(
  [in]          VARIANT_BOOL makeExclusive
);

HRESULT get_HasExclusiveAccess(
  [out, retval] VARIANT_BOOL *isExclusive
);
```



## <a name="property-value"></a>Valor de propiedad

**TRUE** si se ha adquirido el acceso exclusivo al dispositivo de teclado de la máquina virtual; en caso contrario, **FALSE.**

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                   | Significado                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                      | La operación se realizó correctamente.<br/>                                                                                                                                                                                                        |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                        | El *parámetro isExclusive* es **NULL.**<br/>                                                                                                                                                                                             |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                   | El modo exclusivo solicitado ya está establecido para este dispositivo. Esto puede ocurrir al intentar establecer el modo exclusivo cuando ya se ha adquirido o al intentar liberar el modo exclusivo cuando no se había adquirido previamente.<br/> |
| <dl> <dt>Máquina virtual \_ E SET \_ \_ EXCLUSIVE MODE \_ \_ FAIL</dt> <dt>0xA0040825</dt> </dl> | No se pudo establecer o liberar el modo exclusivo como se solicitó. Esto podría deberse a que la máquina virtual ya no se está ejecutando o porque otro proceso ya ha adquirido el modo exclusivo en el dispositivo de teclado de la máquina virtual.<br/>                                 |
| <dl> <dt>E \_ InvalidarG</dt> <dt>0x80000003</dt> </dl>                     | La cadena especificada está vacía o contiene un código de clave no válido.<br/>                                                                                                                                                                      |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                | Se produjo un error inesperado.<br/>                                                                                                                                                                                                    |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMKeyboard se define como \_ 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 


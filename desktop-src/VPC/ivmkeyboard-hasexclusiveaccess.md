---
title: Propiedad IVMKeyboard HasExclusiveAccess (VPCCOMInterfaces. h)
description: Indica si este objeto tiene control exclusivo sobre el dispositivo de teclado de la máquina virtual.
ms.assetid: edba154e-e700-488c-9133-91649daecef1
keywords:
- Propiedad HasExclusiveAccess Virtual PC
- Propiedad HasExclusiveAccess Virtual PC, interfaz IVMKeyboard
- Interfaz IVMKeyboard Virtual PC, propiedad HasExclusiveAccess
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
ms.openlocfilehash: f62c235f3b4325a70a939239ac1e44360b3b5d9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150952"
---
# <a name="ivmkeyboardhasexclusiveaccess-property"></a>IVMKeyboard:: HasExclusiveAccess (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Indica si este objeto tiene control exclusivo sobre el dispositivo de teclado (VM) de la máquina virtual.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_HasExclusiveAccess(
  [in]          VARIANT_BOOL makeExclusive
);

HRESULT get_HasExclusiveAccess(
  [out, retval] VARIANT_BOOL *isExclusive
);
```



## <a name="property-value"></a>Valor de propiedad

**True** si se ha adquirido acceso exclusivo al dispositivo de teclado de la máquina virtual; de lo contrario, **false** .

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                   | Significado                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                      | La operación se realizó correctamente.<br/>                                                                                                                                                                                                        |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                        | El parámetro *isExclusive* es **null**.<br/>                                                                                                                                                                                             |
| <dl> <dt>S \_ FALSO</dt> <dt>1</dt> </dl>                                   | El modo exclusivo solicitado ya está establecido para este dispositivo. Esto puede ocurrir cuando se intenta establecer el modo exclusivo cuando ya se ha adquirido o cuando se intenta liberar el modo exclusivo cuando no se ha adquirido previamente.<br/> |
| <dl> <dt>Máquina virtual \_ E \_ establezca \_ el \_ modo exclusivo \_ FAIL</dt> <dt>0xA0040825</dt> </dl> | No se pudo establecer o liberar el modo exclusivo como se solicitó. Esto puede deberse a que la máquina virtual ya no se está ejecutando o a que otro proceso ya ha adquirido el modo exclusivo en el dispositivo de teclado de la máquina virtual.<br/>                                 |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                     | La cadena especificada está vacía o contiene un código de clave no válido.<br/>                                                                                                                                                                      |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>                | Se produjo un error inesperado.<br/>                                                                                                                                                                                                    |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard se define como 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 


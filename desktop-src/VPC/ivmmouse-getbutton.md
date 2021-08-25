---
title: Método IVMMouse GetButton (VPCCOMInterfaces.h)
description: Recupera el estado actual del botón del mouse especificado.
ms.assetid: eb534f88-387d-42fb-bfc3-bca17685021e
keywords:
- Método GetButton de Virtual PC
- Método GetButton De PC virtual, interfaz IVMMouse
- IVMMouse interface Virtual PC , método GetButton
topic_type:
- apiref
api_name:
- IVMMouse.GetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af37a303c90fb9c60020f19f22767ec508c53fdc54bcefa533dabc780c38f16a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007165"
---
# <a name="ivmmousegetbutton-method"></a>IVMMouse::GetButton (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera el estado actual (arriba o abajo) del botón del mouse especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetButton(
  [in]          VMMouseButton buttonIndex,
  [out, retval] VARIANT_BOOL  *isDown
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*buttonIndex* \[ En\]
</dt> <dd>

Índice del botón cuyo estado se solicita. Para obtener una lista de valores, [**consulte VMMouseButton**](vmmousebutton.md).

</dd> <dt>

*isDown* \[ out, retval\]
</dt> <dd>

Estado del botón indicado. **TRUE** si el botón está actualmente fuera de servicio en la máquina virtual; en caso contrario, **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                        | Descripción                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                | El *parámetro isDown* es **NULL.**<br/>                                                  |
| <dl> <dt>**E \_ Invalidarg**</dt> <dt>0x80000003</dt> </dl>             | El *parámetro buttonIndex* no es válido.<br/>                                            |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt> </dl>   | La máquina virtual a la que está conectado este dispositivo del mouse no se está ejecutando actualmente.<br/> |
| <dl> <dt>**Máquina virtual \_ E \_ MOUSE \_ NOT \_ ACTIVE**</dt> <dt>0xA0040800</dt> </dl> | El dispositivo del mouse no se ha encendido.<br/>                                            |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>        | Se produjo un error inesperado.<br/>                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMmouse se define como \_ ac903f6d-6346-4f29-8875-5d511a13895e<br/>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 


---
title: Método IVMMouse SetButton (VPCCOMInterfaces.h)
description: Establece el estado actual (arriba o abajo) del botón del mouse especificado.
ms.assetid: 52b24472-68d6-4a42-8ae5-b1434a6d67f3
keywords:
- SetButton, método Virtual PC
- Método SetButton De PC virtual, interfaz IVMMouse
- IVMMouse interface Virtual PC , método SetButton
topic_type:
- apiref
api_name:
- IVMMouse.SetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04bdd3d7e0075b050c5184beee0a5da21f184040a03731317f2d61e09c07fd9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974115"
---
# <a name="ivmmousesetbutton-method"></a>IVMMouse::SetButton (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Establece el estado actual (arriba o abajo) del botón del mouse especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetButton(
  [in] VMMouseButton buttonIndex,
  [in] VARIANT_BOOL  down
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*buttonIndex* \[ En\]
</dt> <dd>

Índice del botón. Para obtener una lista de valores, [**consulte VMMouseButton**](vmmousebutton.md).

</dd> <dt>

*down* \[ En\]
</dt> <dd>

Nuevo estado del botón. Use **TRUE** si el estado del botón se va a establecer en down y **FALSE** si se va a configurar en .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                        | Descripción                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                              | La operación se realizó correctamente.<br/>                                                                                                          |
| <dl> <dt>**E \_ Invalidarg**</dt> <dt>0x80000003</dt> </dl>             | El *parámetro buttonIndex* no es válido.<br/>                                                                                              |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt> </dl>   | La máquina virtual a la que está conectado este dispositivo del mouse no se está ejecutando actualmente.<br/>                                                   |
| <dl> <dt>**Máquina virtual \_ E \_ MOUSE \_ NOT \_ ACTIVE**</dt> <dt>0xA0040800</dt> </dl> | No se pudo completar la operación porque el dispositivo del mouse no está encendido o no está activo actualmente en la máquina virtual.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>        | Se produjo un error inesperado.<br/>                                                                                                      |



 

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

 


---
title: Método IVMMouse Click (VPCCOMInterfaces.h)
description: Simula un clic del botón del mouse.
ms.assetid: f16e36d6-34ca-4d65-95e4-1a6660d0abd0
keywords:
- Hacer clic en el método Virtual PC
- Haga clic en el método Virtual PC , interfaz IVMMouse
- IVMMouse interface Virtual PC , Click (método)
topic_type:
- apiref
api_name:
- IVMMouse.Click
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d1d1aaf538ac6b30a27df904729f2ad3187ebde29cb915c3d7ef35d1e9cf57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974255"
---
# <a name="ivmmouseclick-method"></a>IVMMouse::Click (Método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Simula un clic del botón del mouse.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Click(
  [in] VMMouseButton buttonIndex
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*buttonIndex* \[ En\]
</dt> <dd>

Índice del botón en el que se hace clic. Para obtener una lista de valores, [**consulte VMMouseButton**](vmmousebutton.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                        | Descripción                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                              | La operación se realizó correctamente.<br/>                                                                                                          |
| <dl> <dt>**E \_ InvalidarG**</dt> <dt>0x80000003</dt> </dl>             | El parámetro es **NULL.**<br/>                                                                                                             |
| <dl> <dt>**Máquina virtual \_ E \_ LA MÁQUINA VIRTUAL NO \_ \_ SE**</dt> <dt>0XA0040206</dt> </dl>   | La máquina virtual a la que está conectado este dispositivo del mouse no se está ejecutando actualmente.<br/>                                                   |
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

 


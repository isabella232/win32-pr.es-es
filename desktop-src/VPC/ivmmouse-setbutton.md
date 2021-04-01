---
title: Método IVMMouse SetButton (VPCCOMInterfaces. h)
description: Establece el estado actual (arriba o abajo) del botón del mouse especificado.
ms.assetid: 52b24472-68d6-4a42-8ae5-b1434a6d67f3
keywords:
- Método SetButton Virtual PC
- Método SetButton Virtual PC, interfaz IVMMouse
- Interfaz IVMMouse Virtual PC, método SetButton
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
ms.openlocfilehash: c2d30ae131ac33eeff339b98511fd2da60a1e606
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150951"
---
# <a name="ivmmousesetbutton-method"></a>IVMMouse:: SetButton (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

*buttonIndex* \[ de\]
</dt> <dd>

Índice del botón. Para obtener una lista de valores, vea [**VMMouseButton**](vmmousebutton.md).

</dd> <dt>

*abajo* \[ de\]
</dt> <dd>

Nuevo estado del botón. Use **true** si el estado del botón se va a establecer en Down y **false** si se va a establecer en up.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                        | Descripción                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                              | La operación se realizó correctamente.<br/>                                                                                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>             | El parámetro *buttonIndex* no es válido.<br/>                                                                                              |
| <dl> <dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt> </dl>   | La máquina virtual a la que está conectado este dispositivo de mouse no se está ejecutando actualmente.<br/>                                                   |
| <dl> <dt>**Máquina virtual \_ E \_ mouse \_ no \_ activo**</dt> <dt>0xA0040800</dt> </dl> | No se pudo completar la operación porque el dispositivo del mouse no está encendido o no está activo actualmente en la máquina virtual.<br/> |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>        | Se produjo un error inesperado.<br/>                                                                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMmouse se define como ac903f6d-6346-4f29-8875-5d511a13895e<br/>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 


---
title: Método IVMKeyboard PressAndReleaseKey (VPCCOMInterfaces. h)
description: Simula que se presiona una tecla y luego se libera.
ms.assetid: 2a7fc36f-f1bf-4f1d-b8f7-ea5b167c82a7
keywords:
- Método PressAndReleaseKey Virtual PC
- Método PressAndReleaseKey Virtual PC, interfaz IVMKeyboard
- Interfaz IVMKeyboard Virtual PC, método PressAndReleaseKey
topic_type:
- apiref
api_name:
- IVMKeyboard.PressAndReleaseKey
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4adbcac2c79c02ce69584bbfdf21a6b08b350a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695961"
---
# <a name="ivmkeyboardpressandreleasekey-method"></a>IVMKeyboard::P método ressAndReleaseKey

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Simula que se presiona una tecla y luego se libera.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PressAndReleaseKey(
  [in] BSTR key
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*clave* \[ de de\]
</dt> <dd>

Código clave de la tecla que se va a presionar y liberar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                 | Descripción                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>                                   |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **null**.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | La cadena especificada está vacía o contiene un código de clave no válido.<br/> |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>                               |



 

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

 


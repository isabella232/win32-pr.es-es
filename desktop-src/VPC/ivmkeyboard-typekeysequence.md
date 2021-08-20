---
title: Método IVMKeyboard TypeKeySequence (VPCCOMInterfaces.h)
description: Simula una lista delimitada por comas de claves que se escriben.
ms.assetid: ba4d4e43-cb2e-49ae-940d-2e81286d3473
keywords:
- TypeKeySequence, método Virtual PC
- Método TypeKeySequence Virtual PC , interfaz IVMKeyboard
- IVMKeyboard interface Virtual PC , TypeKeySequence (método)
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeKeySequence
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565d31d04a31f72ea25b3477fb91d53d252f6173eec8bc2f40133db38eeb1619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998865"
---
# <a name="ivmkeyboardtypekeysequence-method"></a>IVMKeyboard::TypeKeySequence (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Simula una lista delimitada por comas de claves que se escriben.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT TypeKeySequence(
  [in] BSTR keySequence
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*keySequence* \[ En\]
</dt> <dd>

Secuencia delimitada por comas de códigos de clave que se va a escribir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                 | Descripción                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>                                   |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **NULL.**<br/>                                      |
| <dl> <dt>**E \_ Invalidarg**</dt> <dt>0x80000003</dt> </dl>      | La cadena especificada está vacía o contiene un código de clave no válido.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>                               |



 

## <a name="remarks"></a>Comentarios

Una cadena de secuencia de claves es un conjunto delimitado por comas de identificadores de clave que se usan para simular la secuencia de pulsación y liberación de teclas de un teclado estándar de estilo AT de 101 teclas de EE. UU.

Si aparece un identificador de clave en la cadena sin un modificador anterior, se envía un código presionado por tecla a la sesión de máquina virtual, seguido inmediatamente de su código correspondiente liberado por clave. Los modificadores de clave se pueden usar para cambiar este comportamiento.

Por ejemplo, el modificador DOWN enviará el código presionado por la tecla para el siguiente identificador de clave sin enviar el código liberado por clave. Esto resulta útil para simular las teclas Ctrl, Alt y Mayús cuando se mantienen presionadas mientras se envían otras claves. Para liberar la clave, debe incluirse de nuevo en la cadena de clave junto con un modificador UP anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMKeyboard se define como \_ 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> <dt>

[Secuencias de claves](key-sequences.md)
</dt> </dl>

 


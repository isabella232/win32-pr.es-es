---
title: Método IVMKeyboard TypeKeySequence (VPCCOMInterfaces. h)
description: Simula una lista delimitada por comas de las claves que se van a escribir.
ms.assetid: ba4d4e43-cb2e-49ae-940d-2e81286d3473
keywords:
- Método TypeKeySequence Virtual PC
- Método TypeKeySequence Virtual PC, interfaz IVMKeyboard
- Interfaz IVMKeyboard Virtual PC, método TypeKeySequence
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
ms.openlocfilehash: c34bd96077c1d28aad196ee0d6b11de122725d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997046"
---
# <a name="ivmkeyboardtypekeysequence-method"></a>IVMKeyboard:: TypeKeySequence (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Simula una lista delimitada por comas de las claves que se van a escribir.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT TypeKeySequence(
  [in] BSTR keySequence
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*keySequence* \[ de\]
</dt> <dd>

Secuencia delimitada por comas de códigos de tecla que se van a escribir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                 | Descripción                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>                                   |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **null**.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | La cadena especificada está vacía o contiene un código de clave no válido.<br/> |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>                               |



 

## <a name="remarks"></a>Observaciones

Una cadena de secuencia de claves es un conjunto delimitado por comas de identificadores de clave que se usan para simular la secuencia de pulsación de tecla y de versión de un teclado en estilo estándar 101 de EE. UU..

Si aparece un identificador de clave en la cadena sin un modificador anterior, se envía un código presionado con la tecla a la sesión de la máquina virtual, seguido inmediatamente del código de liberación de claves correspondiente. Los modificadores de clave se pueden usar para cambiar este comportamiento.

Por ejemplo, el modificador DOWN enviará el código presionado por la tecla para el siguiente identificador de clave sin enviar el código liberado por la clave. Esto resulta útil para simular las teclas Ctrl, Alt y Mayús cuando se mantienen presionadas mientras se envían otras claves. Para liberar la clave, se debe volver a incluir en la cadena de clave junto con un modificador anterior.

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
</dt> <dt>

[Secuencias de claves](key-sequences.md)
</dt> </dl>

 


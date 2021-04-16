---
title: Método ISoftKbd SetKeyboardLabelTextCombination (Softkbdc. h)
description: El método ISoftKbd SetKeyboardLabelTextCombination establece una combinación de etiqueta y texto que se usa para describir un teclado en pantalla.
ms.assetid: fe054eae-1a44-41ad-9a44-bc0b46df7c7b
keywords:
- Método SetKeyboardLabelTextCombination marco de trabajo de servicios de texto
- Método SetKeyboardLabelTextCombination marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método SetKeyboardLabelTextCombination
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelTextCombination
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98dad124455625f0da3ada1a717c692437398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686113"
---
# <a name="isoftkbdsetkeyboardlabeltextcombination-method"></a>ISoftKbd:: SetKeyboardLabelTextCombination (método)

El método **ISoftKbd:: SetKeyboardLabelTextCombination** establece una combinación de etiqueta y texto que se usa para describir un teclado en pantalla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetKeyboardLabelTextCombination(
  [in] DWORD nModifierCombination
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nModifierCombination* \[ de\]
</dt> <dd>

Combinación de etiqueta y texto que se usa para describir el teclado en pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                        | Descripción                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Método realizado correctamente.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El parámetro *nModifierCombination* no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::SetKeyboardLabelText**](isoftkbd-setkeyboardlabeltext.md)
</dt> </dl>

 

 






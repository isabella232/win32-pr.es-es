---
title: Método ISoftKbd SetKeyboardLabelTextCombination (Softkbdc.h)
description: El método ISoftKbd SetKeyboardLabelTextCombination establece una combinación de etiqueta y texto que se usa para describir un teclado suave.
ms.assetid: fe054eae-1a44-41ad-9a44-bc0b46df7c7b
keywords:
- Método SetKeyboardLabelTextCombination Text Services Framework
- Método SetKeyboardLabelTextCombination Text Services Framework interfaz , ISoftKbd
- Interfaz ISoftKbd Text Services Framework , método SetKeyboardLabelTextCombination
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
ms.openlocfilehash: 39b01d4335e52bf20aca1b5cd59b5bc1dd926f6c4752f2b0f421e613d48b2f94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952562"
---
# <a name="isoftkbdsetkeyboardlabeltextcombination-method"></a>ISoftKbd::SetKeyboardLabelTextCombination (método)

El **método ISoftKbd::SetKeyboardLabelTextCombination** establece una combinación de etiqueta y texto que se usa para describir un teclado suave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetKeyboardLabelTextCombination(
  [in] DWORD nModifierCombination
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nModifierCombination* \[ En\]
</dt> <dd>

Combinación de etiqueta y texto que se usa para describir el teclado suave.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Valor                                                                                        | Descripción                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Método realizado correctamente.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El *parámetro nModifierCombination* no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::SetKeyboardLabelText**](isoftkbd-setkeyboardlabeltext.md)
</dt> </dl>

 

 






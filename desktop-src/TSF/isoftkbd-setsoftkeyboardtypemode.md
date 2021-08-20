---
title: Método ISoftKbd SetSoftKeyboardTypeMode (Softkbdc.h)
description: El método ISoftKbd SetSoftKeyboardTypeMode establece el modo de tipo para un teclado flexible.
ms.assetid: 0b5b5056-59b3-41c7-bc43-70b5c3cd51c2
keywords:
- Método SetSoftKeyboardTypeMode Text Services Framework
- Método SetSoftKeyboardTypeMode Text Services Framework , interfaz ISoftKbd
- Interfaz ISoftKbd Text Services Framework , método SetSoftKeyboardTypeMode
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50a43fd160444c2c1d29226aadb898ca60eec6038759452ca8451466337f1b3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952491"
---
# <a name="isoftkbdsetsoftkeyboardtypemode-method"></a>ISoftKbd::SetSoftKeyboardTypeMode (método)

El **método ISoftKbd::SetSoftKeyboardTypeMode** establece el modo de tipo para un teclado flexible.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSoftKeyboardTypeMode(
  [in] TYPEMODE TypeMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TypeMode* \[ En\]
</dt> <dd>

Modo de tipo. Los valores posibles se definen para la [**enumeración TYPEMODE.**](typemode.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Valor                                                                                        | Descripción                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Método realizado correctamente.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El *parámetro TypeMode* no es válido.<br/> |



 

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

[**ISoftKbd::GetSoftKeyboardTypeMode**](isoftkbd-getsoftkeyboardtypemode.md)
</dt> <dt>

[**TYPEMODE**](typemode.md)
</dt> </dl>

 

 






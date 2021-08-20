---
title: Método ISoftKbd SelectSoftKeyboard (Softkbdc.h)
description: El método ISoftKbd SelectSoftKeyboard selecciona el teclado flexible especificado.
ms.assetid: 7e85d346-3741-457d-aadd-11d3a6710e85
keywords:
- Selección del método SelectSoftKeyboard Text Services Framework
- Método SelectSoftKeyboard Text Services Framework , interfaz ISoftKbd
- Interfaz ISoftKbd Text Services Framework , método SelectSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.SelectSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f4a723488717198f88653efa0ad0c2137f4ad9a7667621befa6f6ea4709b7f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952561"
---
# <a name="isoftkbdselectsoftkeyboard-method"></a>ISoftKbd::SelectSoftKeyboard (método)

El **método ISoftKbd::SelectSoftKeyboard** selecciona el teclado flexible especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SelectSoftKeyboard(
  [in] DWORD dwKeyboardId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwKeyboardId* \[ En\]
</dt> <dd>

Identificador del teclado flexible que se selecciona.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Valor                                                                                        | Descripción                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Método realizado correctamente.<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El *parámetro dwKeyboardId* no es válido.<br/> |



 

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
</dt> </dl>

 

 






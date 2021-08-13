---
title: EM_INSERTIMAGE mensaje (Richedit.h)
description: Reemplaza la selección por un blob que muestra una imagen.
ms.assetid: 147B298B-C4A9-455B-9736-A0B09D72902B
keywords:
- EM_INSERTIMAGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_INSERTIMAGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7418a8fe4b7c627d211bce7bf2591ed684d82e42089fbe9bedeb2f76a6b9d3e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437895"
---
# <a name="em_insertimage-message"></a>Mensaje \_ INSERTIMAGE EM

Reemplaza la selección por un blob que muestra una imagen.


```C++
#define EM_INSERTIMAGE       (WM_USER + 314)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**RICHEDIT \_ IMAGE \_ PARAMETERS**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) que contiene el blob de imagen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o uno de los siguientes códigos de error.



| Código devuelto                                                                                    | Descripción                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | No se puede insertar la imagen. <br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | El *parámetro lParam* es NULL o apunta a una imagen no válida. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente disponible.<br/>                  |



 

## <a name="remarks"></a>Observaciones

Si la selección es un punto de inserción, el blob de imagen se inserta en el punto de inserción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ INSERTTABLE**](em-inserttable.md)
</dt> </dl>

 

 






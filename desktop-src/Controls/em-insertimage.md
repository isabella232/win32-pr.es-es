---
title: Mensaje EM_INSERTIMAGE (RichEdit. h)
description: Reemplaza la selección por un BLOB que muestra una imagen.
ms.assetid: 147B298B-C4A9-455B-9736-A0B09D72902B
keywords:
- EM_INSERTIMAGE controles de mensajes de Windows
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
ms.openlocfilehash: dc9ff1e0fd355cf5dd8d43d211c44fda6417c638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489449"
---
# <a name="em_insertimage-message"></a>\_Mensaje INSERTIMAGE em

Reemplaza la selección por un BLOB que muestra una imagen.


```C++
#define EM_INSERTIMAGE       (WM_USER + 314)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**de \_ \_ parámetros de imagen de RICHEDIT**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) que contiene el BLOB de la imagen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve \_ si es correcto, o uno de los siguientes códigos de error.



| Código devuelto                                                                                    | Descripción                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**E \_ ERROR**</dt> </dl>        | No se puede insertar la imagen. <br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | El parámetro *lParam* es null o apunta a una imagen no válida. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente.<br/>                  |



 

## <a name="remarks"></a>Observaciones

Si la selección es un punto de inserción, el BLOB de imagen se inserta en el punto de inserción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_INSERTTABLE em**](em-inserttable.md)
</dt> </dl>

 

 






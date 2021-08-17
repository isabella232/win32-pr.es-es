---
title: Método IDWriteTextLayout3 InvalidateLayout
description: Invalida el diseño, lo que obliga a que el diseño se reemita antes de llamar a las métricas o a las funciones de dibujo. Esto resulta útil si cambia la localidad de una fuente y se debe volver a dibujar el diseño, o si cambia el tamaño de un cliente implementado por IDWriteInlineObject.
ms.assetid: 65b42ee1-5b67-1f6d-0e4b-ee60b192e7b7
keywords:
- InvalidateLayout method Direct Write
- InvalidateLayout method Direct Write , IDWriteTextLayout3 (interfaz)
- IdWriteTextLayout3 interface Direct Write , InvalidateLayout (método)
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.InvalidateLayout
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af698ce5f94918be281e633342060f70ba3f62655d7aec3794686a7793c4364a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816086"
---
# <a name="idwritetextlayout3invalidatelayout-method"></a>Método IDWriteTextLayout3::InvalidateLayout

Invalida el diseño, lo que obliga a que el diseño se reemita antes de llamar a las métricas o a las funciones de dibujo. Esto resulta útil si cambia la localidad de una fuente y se debe volver a dibujar el diseño, o si cambia el tamaño de un cliente implementado por IDWriteInlineObject.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InvalidateLayout();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                 |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 






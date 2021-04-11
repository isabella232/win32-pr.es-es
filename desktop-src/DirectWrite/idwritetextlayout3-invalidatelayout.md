---
title: IDWriteTextLayout3 InvalidateLayout, método
description: Invalida el diseño, forzando el diseño para que se remedie antes de llamar a las métricas o funciones de dibujo. Esto resulta útil si el emplazamiento de una fuente cambia y el diseño debe volver a dibujarse, o si el tamaño de un cliente implementa IDWriteInlineObject cambios.
ms.assetid: 65b42ee1-5b67-1f6d-0e4b-ee60b192e7b7
keywords:
- Método InvalidateLayout de escritura directa
- Método InvalidateLayout de escritura directa, interfaz IDWriteTextLayout3
- Interfaz IDWriteTextLayout3 Direct Write, método InvalidateLayout
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
ms.openlocfilehash: b5df97d4590f62f586a570d52428b6560a7d88df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150527"
---
# <a name="idwritetextlayout3invalidatelayout-method"></a>IDWriteTextLayout3:: InvalidateLayout (método)

Invalida el diseño, forzando el diseño para que se remedie antes de llamar a las métricas o funciones de dibujo. Esto resulta útil si el emplazamiento de una fuente cambia y el diseño debe volver a dibujarse, o si el tamaño de un cliente implementa IDWriteInlineObject cambios.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InvalidateLayout();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                 |
| Teléfono mínimo compatible<br/>  | Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 






---
description: Indica si el lápiz óptico está al revés.
ms.assetid: 04b05287-000d-455f-88e5-821c7fdb8119
title: ITabletCursor::IsInverted (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.IsInverted
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 81bbb5f4f93026e0d6910cb7f23d0a7d2ddeea5595e87f816faa016d22986d0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223075"
---
# <a name="itabletcursorisinverted-method"></a>ITabletCursor::IsInverted (método)

Indica si el lápiz óptico está al revés.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsInverted();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                             | Descripción                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | El lápiz óptico se invierte.<br/>        |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | El lápiz óptico no se invierte.<br/>    |
| <dl> <dt>**E \_ FAIL**</dt> </dl>  | Se ha producido un error no especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITabletCursor**](itabletcursor.md)
</dt> <dt>

[**ITabletCursorButton (Interfaz)**](itabletcursorbutton.md)
</dt> </dl>

 

 





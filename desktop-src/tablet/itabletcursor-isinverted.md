---
description: Indica si el lápiz está en la parte inferior.
ms.assetid: 04b05287-000d-455f-88e5-821c7fdb8119
title: 'ITabletCursor:: IsInverted (método)'
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
ms.openlocfilehash: 041b81c38f3370421c96a4c0d66201254a715e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659919"
---
# <a name="itabletcursorisinverted-method"></a>ITabletCursor:: IsInverted (método)

Indica si el lápiz está en la parte inferior.

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
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Se invierte el lápiz óptico.<br/>        |
| <dl> <dt>**S \_ false**</dt> </dl> | No se invierte el lápiz.<br/>    |
| <dl> <dt>**E \_ FAIL**</dt> </dl>  | Se ha producido un error no especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITabletCursor**](itabletcursor.md)
</dt> <dt>

[**Interfaz ITabletCursorButton**](itabletcursorbutton.md)
</dt> </dl>

 

 





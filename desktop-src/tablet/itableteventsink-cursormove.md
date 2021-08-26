---
description: Se produce cuando el cursor se mueve sobre el digitalizador de tabletas.
ms.assetid: cd2863af-59a9-4dd0-a679-84861a70ef53
title: ITabletEventSink::CursorMove (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorMove
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 030fa5ba4adc725288d5135ccd24409d4fc02cddbc16da52aa375a275a73be5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843495"
---
# <a name="itableteventsinkcursormove-method"></a>ITabletEventSink::CursorMove (método)

Se produce cuando el cursor se mueve sobre el digitalizador de tabletas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CursorMove(
   TABLET_CONTEXT_ID tcid,
   CURSOR_ID         cid,
   HWND              hWnd,
   LONG              xPos,
   LONG              yPos
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tcid* 
</dt> <dd>

Denificador único del digitalizador de tabletas.

</dd> <dt>

*Cid* 
</dt> <dd>

Identificador único del lápiz óptico de tableta.

</dd> <dt>

*hWnd* 
</dt> <dd>

Ventana sobre la que se movió el cursor.

</dd> <dt>

*xPos* 
</dt> <dd>

Posición X del lápiz óptico.

</dd> <dt>

*yPos* 
</dt> <dd>

Posición Y del lápiz óptico.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITabletEventSink (interfaz)**](itableteventsink.md)
</dt> </dl>

 

 





---
description: Se produce cuando el cursor se mueve sobre el digitalizador de Tablet PC.
ms.assetid: cd2863af-59a9-4dd0-a679-84861a70ef53
title: 'ITabletEventSink:: CursorMove (método)'
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
ms.openlocfilehash: f6950e0b30c1b8fc8ccf3e60a8aaa05b9eeb3215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688500"
---
# <a name="itableteventsinkcursormove-method"></a>ITabletEventSink:: CursorMove (método)

Se produce cuando el cursor se mueve sobre el digitalizador de Tablet PC.

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

Dentifier único del digitalizador de Tablet PC.

</dd> <dt>

*Cid* 
</dt> <dd>

Identificador único del lápiz de Tablet PC.

</dd> <dt>

*hWnd* 
</dt> <dd>

Ventana en la que se ha desplace el cursor.

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
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 





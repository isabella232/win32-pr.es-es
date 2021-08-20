---
description: Se produce cuando el lápiz óptico sale del intervalo de detección físico (proximidad) de la tableta.
ms.assetid: ded01278-126d-415d-9a7b-1e6fe3650a37
title: ITabletEventSink::CursorOutOfRange (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorOutOfRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 215ab448d573f83222d04547c4dccbeb88d7fe7c4358b3cca0ed09e936e286d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041680"
---
# <a name="itableteventsinkcursoroutofrange-method"></a>ITabletEventSink::CursorOutOfRange (método)

Se produce cuando el lápiz óptico sale del intervalo de detección físico (proximidad) de la tableta.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CursorOutOfRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tcid* \[ En\]
</dt> <dd>

Identificador de la tableta.

</dd> <dt>

*Cid* 
</dt> <dd>

Identificador del lápiz óptico.

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
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITabletEventSink (interfaz)**](itableteventsink.md)
</dt> </dl>

 

 





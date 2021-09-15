---
description: Se produce cuando se agrega un nuevo lápiz óptico al sistema.
ms.assetid: bd0f0d2a-c0d9-48fc-bc90-f63f038639f3
title: ITabletEventSink::CursorNew (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorNew
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 31db152eb15d6f980234dc556e277691d3f14959
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467984"
---
# <a name="itableteventsinkcursornew-method"></a>ITabletEventSink::CursorNew (método)

Se produce cuando se agrega un nuevo lápiz óptico al sistema.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CursorNew(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tcid* \[ En\]
</dt> <dd>

Identificador del contexto de tableta donde se agregó el nuevo lápiz óptico.

</dd> <dt>

*Cid* 
</dt> <dd>

Identificador del nuevo objeto de lápiz óptico.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITabletEventSink (interfaz)**](itableteventsink.md)
</dt> </dl>

 

 





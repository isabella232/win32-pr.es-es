---
description: Recupera el identificador del lápiz óptico.
ms.assetid: 27320a2f-1e4a-4d7d-a1f8-5244f4a03415
title: 'ITabletCursor:: GetId (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5d4f71d2cd465bfd2d1ff4c245154a300c431df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423987"
---
# <a name="itabletcursorgetid-method"></a>ITabletCursor:: GetId (método)

Recupera el identificador del lápiz óptico.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetId(
  [out] CURSOR_ID *pCid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCid* \[ enuncia\]
</dt> <dd>

Identificador del lápiz de Tablet PC.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

\_El ID. de cursor se define como un valor DWORD.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz ITabletCursor**](itabletcursor.md)
</dt> </dl>

 

 





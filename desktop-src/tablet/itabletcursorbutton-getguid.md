---
description: Recupera el identificador único del botón de lápiz óptico.
ms.assetid: 06bd6a84-46cd-4c62-92d6-50caae359e43
title: ITabletCursorButton::GetGuid (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetGuid
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f4492aa98630491730435080981172bc60a1eeccfe0c84ed76e3b4d504a79ad1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844285"
---
# <a name="itabletcursorbuttongetguid-method"></a>ITabletCursorButton::GetGuid (método)

Recupera el identificador único del botón de lápiz óptico.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetGuid(
  [out] GUID *pguidBtn
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pguidBtn* \[ out\]
</dt> <dd>

Valor único que identifica el botón del lápiz óptico.

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

[**ITabletCursorButton (Interfaz)**](itabletcursorbutton.md)
</dt> </dl>

 

 





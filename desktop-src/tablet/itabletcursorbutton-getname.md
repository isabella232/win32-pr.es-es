---
description: Recupera el nombre del botón del lápiz óptico.
ms.assetid: 26fad9bc-43c2-4b00-b76b-bf9f1242da77
title: ITabletCursorButton::GetName (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 41155aa15a2efaeb789387ae3ea7c6863ab0010884ecacb2f7bd3a75453e57b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716825"
---
# <a name="itabletcursorbuttongetname-method"></a>ITabletCursorButton::GetName (método)

Recupera el nombre del botón del lápiz óptico.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppwszName* \[ out\]
</dt> <dd>

El nombre del botón del lápiz óptico.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

Es responsabilidad del autor de la llamada liberar la memoria devuelta de este método mediante [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITabletCursorButton (Interfaz)**](itabletcursorbutton.md)
</dt> </dl>

 


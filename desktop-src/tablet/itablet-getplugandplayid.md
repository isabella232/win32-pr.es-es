---
description: Devuelve una cadena que contiene el Plug and Play del dispositivo de tableta.
ms.assetid: a0b6619b-f80c-470b-aa3f-f0b30a9dbda8
title: ITablet::GetPlugAndPlayId (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetPlugAndPlayId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 2c7028e11a7a8ec6d1e6c79c461ce05f50dfe0b4b69108f0f1527b4fbd9ba3fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041915"
---
# <a name="itabletgetplugandplayid-method"></a>ITablet::GetPlugAndPlayId (método)

Devuelve una cadena que contiene el Plug and Play del dispositivo de tableta.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPlugAndPlayId(
  [out] LPWSTR *ppwszPPId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppwszPPId* \[ out\]
</dt> <dd>

Puntero a una cadena que contiene el identificador Plug and Play para el dispositivo de tableta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Comentarios

Es responsabilidad del autor de la llamada liberar la memoria devuelta de este método mediante [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITablet (interfaz)**](itablet.md)
</dt> </dl>

 


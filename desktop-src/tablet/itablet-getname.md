---
description: Devuelve una cadena que contiene el nombre del dispositivo de tableta gráfica.
ms.assetid: 025620b5-ab68-4e36-ae26-2226a2fdeb61
title: 'ITablet:: GetName (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c2d6bd20a011b1bf5cfbe7582445de45728bbd7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277216"
---
# <a name="itabletgetname-method"></a>ITablet:: GetName (método)

Devuelve una cadena que contiene el nombre del dispositivo de tableta gráfica.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppwszName* \[ enuncia\]
</dt> <dd>

Puntero a una cadena que contiene el nombre del dispositivo de tableta gráfica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

Es responsabilidad del llamador liberar la memoria devuelta desde este método mediante [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz ITablet**](itablet.md)
</dt> </dl>

 


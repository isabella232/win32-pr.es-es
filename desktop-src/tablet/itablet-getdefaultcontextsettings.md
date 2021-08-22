---
description: Recupera la configuración de contexto predeterminada para la tableta.
ms.assetid: 59d1bab0-a8b8-4e23-9311-2921f9035dc4
title: ITablet::GetDefaultContextSettings (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetDefaultContextSettings
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 646756a924bd9b848f2141b796205f2cf2374140811b7dd87f8ffd64c69ee8d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119336265"
---
# <a name="itabletgetdefaultcontextsettings-method"></a>ITablet::GetDefaultContextSettings (método)

Recupera la configuración de contexto predeterminada para la tableta.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDefaultContextSettings(
  [out] TABLET_CONTEXT_SETTINGS **ppTCS
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppTCS* \[ out\]
</dt> <dd>

Configuración de contexto predeterminada para la tableta.

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



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITablet (interfaz)**](itablet.md)
</dt> </dl>

 


---
title: Método GetParam de IConfigAsfWriter2
description: El método GetParam recupera el valor actual del parámetro de configuración de filtro especificado.
ms.assetid: 81d915a1-6190-46e3-a5cb-7f5fc242b8dd
keywords:
- Método GetParam windows Media Format
- Método GetParam windows Media Format, interfaz IConfigAsfWriter2
- IConfigAsfWriter2 interface windows Media Format , GetParam method
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.GetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a411e4b1896174e25a1f671f3f42fd83c1376713f10e9e4cb2b2d2186b3d551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809145"
---
# <a name="iconfigasfwriter2getparam-method"></a>IConfigAsfWriter2::GetParam (método)

El **método GetParam** recupera el valor actual del parámetro de configuración de filtro especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetParam(
  [in]  DWORD dwParam,
  [out] DWORD *pdwParam1,
  [out] DWORD *pdwParam2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwParam* \[ En\]
</dt> <dd>

Especifica el parámetro que se recuperará. Debe ser un valor definido en la [ \_ enumeración \_ AM ASFWRITERCONFIG \_ PARAM.](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))

</dd> <dt>

*pdwParam1* \[ out\]
</dt> <dd>

Puntero a una variable que recupera el valor del parámetro especificado en *dwParam*.

</dd> <dt>

*pdwParam2* \[ out\]
</dt> <dd>

No se usa, debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve S \_ OK. Si se produce un error, devuelve un código de error **HRESULT.**

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IConfigAsfWriter2 (Interfaz)**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md)
</dt> </dl>

 

 
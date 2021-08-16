---
title: IConfigAsfWriter2 SetParam (método)
description: El método SetParam establece el valor del parámetro de configuración de filtro especificado.
ms.assetid: b8067fb2-c379-4b26-b4f7-c790604e3edc
keywords:
- Formato multimedia de Windows del método SetParam
- Método SetParam windows Media Format , interfaz IConfigAsfWriter2
- IConfigAsfWriter2 interface windows Media Format , SetParam (método)
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.SetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e7c73831ec45e6e0b65444e93e976fe349a2d4576d578f3399c60c399628cbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847503"
---
# <a name="iconfigasfwriter2setparam-method"></a>IConfigAsfWriter2::SetParam (método)

El **método SetParam** establece el valor del parámetro de configuración de filtro especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetParam(
  [in] DWORD dwParam,
  [in] DWORD dwParam1,
  [in] DWORD dwParam2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwParam* \[ En\]
</dt> <dd>

Especifica el parámetro que se establecerá. Debe ser un valor definido en la [ \_ \_ enumeración AM ASFWRITERCONFIG \_ PARAM.](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))

</dd> <dt>

*dwParam1* \[ En\]
</dt> <dd>

Especifica el valor que se asignará al *parámetro dwParam.*

</dd> <dt>

*dwParam2* \[ En\]
</dt> <dd>

No se usa; debe ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve S \_ OK. Si se produce un error, devuelve un código de error **HRESULT.**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IConfigAsfWriter2 (Interfaz)**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2::GetParam**](iconfigasfwriter2-getparam.md)
</dt> </dl>

 

 
---
title: IConfigAsfWriter2 GetParam, método
description: El método GetParam recupera el valor actual del parámetro de configuración de filtro especificado.
ms.assetid: 81d915a1-6190-46e3-a5cb-7f5fc242b8dd
keywords:
- Método GetParam formato de Windows Media
- Método GetParam formato de Windows Media, interfaz IConfigAsfWriter2
- Interfaz IConfigAsfWriter2 formato de Windows Media, método GetParam
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.GetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d72b8011072424679729686dd5a14c92bae90f66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695712"
---
# <a name="iconfigasfwriter2getparam-method"></a>IConfigAsfWriter2:: GetParam (método)

El método **GetParam** recupera el valor actual del parámetro de configuración de filtro especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetParam(
  [in]  DWORD dwParam,
  [out] DWORD *pdwParam1,
  [out] DWORD *pdwParam2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwParam* \[ de\]
</dt> <dd>

Especifica el parámetro que se va a recuperar. Debe ser un valor definido en la enumeración de [ \_ \_ \_ parámetros AM ASFWRITERCONFIG](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) .

</dd> <dt>

*pdwParam1* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recupera el valor del parámetro especificado en *dwParam*.

</dd> <dt>

*pdwParam2* \[ enuncia\]
</dt> <dd>

No se utiliza, debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve S \_ correcto. Si se produce un error, devuelve un código de error **HRESULT** .

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md)
</dt> </dl>

 

 
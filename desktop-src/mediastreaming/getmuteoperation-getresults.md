---
title: GetMuteOperation. GetResults, método
description: Devuelve los resultados de la operación asincrónica iniciada por GetMuteAsync.
ms.assetid: 5B6DB1B3-54D4-486D-AA03-5FEEC92304B0
keywords:
- Método GetResults API de streaming de multimedia
- Método GetResults API de streaming multimedia, interfaz GetMuteOperation
- GetMuteOperation interface media streaming API, GetResults (método)
topic_type:
- apiref
api_name:
- GetMuteOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33c43dc7fee228b1808ff4f607ee6a72faf1e770
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149210"
---
# <a name="getmuteoperationgetresults-method"></a>GetMuteOperation. GetResults, método

Devuelve los resultados de la operación asincrónica iniciada por [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetResults(
  [out, retval] boolean *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de out, retval\]
</dt> <dd>

Valor de silencio. Un valor de True indica que el audio está silenciado actualmente. Un valor de False indica que el audio no está silenciado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Normalmente, se llama al método **GetResults** desde el controlador de eventos que se registró estableciendo la propiedad [**completed**](getmuteoperation-completed.md) .

## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetMuteOperation**](getmuteoperation.md)
</dt> </dl>

 


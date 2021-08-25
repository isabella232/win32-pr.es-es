---
title: IConfigAsfWriter2 StreamNumFromPin (método)
description: El método StreamNumFromPin recupera el número de secuencia asociado al pin de entrada especificado.
ms.assetid: f645a742-e6dc-4041-8a56-3bbb5188a9a9
keywords:
- Formato multimedia de windows del método StreamNumFromPin
- Método StreamNumFromPin de Windows Media Format, interfaz IConfigAsfWriter2
- IConfigAsfWriter2 interface windows Media Format , StreamNumFromPin method
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.StreamNumFromPin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9124d3acaea81e36b212f3dec001374cc035efca449f35af5e43fa18ce50d6dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839826"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a>IConfigAsfWriter2::StreamNumFromPin (método)

El **método StreamNumFromPin** recupera el número de secuencia asociado al pin de entrada especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPin* \[ En\]
</dt> <dd>

Puntero a la **interfaz IPin** en el pin de entrada.

</dd> <dt>

*pwStreamNum* \[ out\]
</dt> <dd>

Puntero que recibe el número de secuencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve S \_ OK. Si se produce un error, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

A veces es posible que tenga que usar las interfaces del SDK Windows formato multimedia directamente para manipular una secuencia antes de ejecutar un gráfico de filtros. Dado que no se puede suponer que un número de flujo de ASF es el mismo que el número de DirectShow pin, se proporciona este método.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IConfigAsfWriter2 (Interfaz)**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

 
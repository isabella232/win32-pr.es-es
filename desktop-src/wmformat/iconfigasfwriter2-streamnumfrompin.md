---
title: IConfigAsfWriter2 StreamNumFromPin, método
description: El método StreamNumFromPin recupera el número de secuencia asociado al pin de entrada especificado.
ms.assetid: f645a742-e6dc-4041-8a56-3bbb5188a9a9
keywords:
- Método StreamNumFromPin formato de Windows Media
- Método StreamNumFromPin formato de Windows Media, interfaz IConfigAsfWriter2
- Interfaz IConfigAsfWriter2 formato de Windows Media, método StreamNumFromPin
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.StreamNumFromPin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c63a31d515e70b0ee0ac5be617ee52fe23bd5416
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420850"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a>IConfigAsfWriter2:: StreamNumFromPin (método)

El método **StreamNumFromPin** recupera el número de secuencia asociado al pin de entrada especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPin* \[ de\]
</dt> <dd>

Puntero a la interfaz **IPin** en el PIN de entrada.

</dd> <dt>

*pwStreamNum* \[ enuncia\]
</dt> <dd>

Puntero que recibe el número de secuencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve S \_ correcto. Si se produce un error, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

En ocasiones, puede que necesite usar las interfaces del SDK de Windows Media Format directamente para manipular un flujo antes de ejecutar un gráfico de filtro. Dado que no se puede suponer que un número de secuencia ASF es el mismo que el número de PIN de DirectShow, se proporciona este método.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

 
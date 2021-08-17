---
description: Especifica la matriz de canales, que se usa para convertir los canales de origen en los canales de destino (por ejemplo, para convertir 5.1 en estéreo).
ms.assetid: 2f2a82bd-f051-4b05-a9c8-37aa4403fab4
title: MFPKEY_WMRESAMP_CHANNELMTX (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a326cfe27632204f2975ac8b7c3a605c666464f8f62846a5c622a469f2f6e104
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117689259"
---
# <a name="mfpkey_wmresamp_channelmtx-property"></a>Propiedad \_ CHANNELMTX de MFPKEY \_ WMRESAMP

Especifica la matriz de canales, que se usa para convertir los canales de origen en los canales de destino (por ejemplo, para convertir 5.1 en estéreo).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ I4 \| VT \_ ARRAY

## <a name="applies-to"></a>Se aplica a

-   [Audio Resampler DSP](audioresampler.md)

## <a name="remarks"></a>Comentarios

El valor de la propiedad es una matriz de coeficientes Ns x Nd, donde Ns es el número de canales de origen y Nd es el número de canales de destino. Los coeficientes se especifican en decibelios mediante la fórmula siguiente:

(int) (65536 \* 20 \* log10(dB))

La matriz se almacena como una matriz en orden de fila principal, donde el número de fila es el canal de origen y el número de columna es el canal de destino.

Por lo tanto, si la matriz es la siguiente:

``` syntax
00       01       ...      0(Ns-1)
10       11       ...      1(Ns-1)
...      ...      ...      ...
(Nd-1)0 (Nd-1)1 ... (Nd-1)(Ns-1)
```

a continuación, especificaría la matriz como:

``` syntax
[ 00, 01, ..., 0(Ns-1), 10, 11, ..., 1(Ns-1), ..., (Nd-1)0, (Nd-1)1, ..., (Nd-1)(Ns-1) ]
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 

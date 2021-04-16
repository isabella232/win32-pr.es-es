---
description: Especifica la matriz de canales, que se usa para convertir los canales de origen en los canales de destino (por ejemplo, para convertir de 5,1 a estéreo).
ms.assetid: 2f2a82bd-f051-4b05-a9c8-37aa4403fab4
title: Propiedad MFPKEY_WMRESAMP_CHANNELMTX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e39f9a9344dd080362859592fcf1f71657ee8f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696891"
---
# <a name="mfpkey_wmresamp_channelmtx-property"></a>\_ \_ Propiedad CHANNELMTX de MFPKEY WMRESAMP

Especifica la matriz de canales, que se usa para convertir los canales de origen en los canales de destino (por ejemplo, para convertir de 5,1 a estéreo).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

Matriz de VT \_ I4 \| VT \_

## <a name="applies-to"></a>Se aplica a

-   [DSP de remuestreador de audio](audioresampler.md)

## <a name="remarks"></a>Observaciones

El valor de la propiedad es una matriz de coeficientes NS x ND, donde NS es el número de canales de origen y ND es el número de canales de destino. Los coeficientes se especifican en decibelios mediante la siguiente fórmula:

Inter (65536 \* 20 \* Log10 (dB))

La matriz se almacena como una matriz en el orden principal de la fila, donde el número de fila es el canal de origen y el número de columna es el canal de destino.

Por lo tanto, si la matriz es la siguiente:

``` syntax
00       01       ...      0(Ns-1)
10       11       ...      1(Ns-1)
...      ...      ...      ...
(Nd-1)0 (Nd-1)1 ... (Nd-1)(Ns-1)
```

a continuación, debe especificar la matriz como:

``` syntax
[ 00, 01, ..., 0(Ns-1), 10, 11, ..., 1(Ns-1), ..., (Nd-1)0, (Nd-1)1, ..., (Nd-1)(Ns-1) ]
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 

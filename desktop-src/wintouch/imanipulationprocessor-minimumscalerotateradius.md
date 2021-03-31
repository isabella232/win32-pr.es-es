---
title: Propiedad MinimumScaleRotateRadius de IManipulationProcessor
description: Especifica el tamaño de los contactos de distancia de un gesto de escala o giro que debe ser el desencadenador de la manipulación.
ms.assetid: b4c49f41-c5ea-4c6a-872b-2d982e588b09
keywords:
- Propiedad MinimumScaleRotateRadius Touch de Windows
- Propiedad MinimumScaleRotateRadius Touch de Windows, interfaz IManipulationProcessor
- Interfaz IManipulationProcessor Touch de Windows, propiedad MinimumScaleRotateRadius
topic_type:
- apiref
api_name:
- IManipulationProcessor.MinimumScaleRotateRadius
- IManipulationProcessor.get_MinimumScaleRotateRadius
- IManipulationProcessor.put_MinimumScaleRotateRadius
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- manipulations.h
ms.openlocfilehash: 502d55e409f58127ddee94f5ba694a109c1ee1cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784156"
---
# <a name="imanipulationprocessorminimumscalerotateradius-property"></a>IManipulationProcessor:: MinimumScaleRotateRadius (propiedad)

Especifica el tamaño de los contactos de distancia de un gesto de escala o giro que debe ser el desencadenador de la manipulación.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_MinimumScaleRotateRadius(
  [in]  FLOAT MinimumScaleRotateRadius
);

HRESULT get_MinimumScaleRotateRadius(
  [out] FLOAT *MinimumScaleRotateRadius
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica la distancia mínima entre contactos para desencadenar gestos de escala o giro.

## <a name="error-codes"></a>Códigos de error

## <a name="remarks"></a>Observaciones

> [!Note]  
> Esta propiedad se establece en centipixels (100 $ de un píxel).

 

Si se establece este valor, el procesador de manipulación pasará por alto los gestos que tengan un radio demasiado pequeño. Esto resulta útil si desea evitar que un usuario manipule un objeto en un valor demasiado pequeño de un radio. Por ejemplo, si usa un procesador de manipulación con un círculo y desea asegurarse de que mantiene un radio superior a 100 píxeles, debe establecer este valor en 10000.

## <a name="examples"></a>Ejemplos


```C++
pManip->put_MinimumScaleRotateRadius(4000.0f);  
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 





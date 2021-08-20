---
title: Propiedad IManipulationProcessor MinimumScaleRotateRadius
description: Especifica el tamaño de los contactos de distancia en un gesto de escala o rotación que deben ser para desencadenar la manipulación.
ms.assetid: b4c49f41-c5ea-4c6a-872b-2d982e588b09
keywords:
- Propiedad MinimumScaleRotateRadius Windows Touch
- Propiedad MinimumScaleRotateRadius Windows Touch , interfaz IManipulationProcessor
- Interfaz IManipulationProcessor Windows touch , propiedad MinimumScaleRotateRadius
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
ms.openlocfilehash: 81ad10d5b041469daff216b7a23a4f5b6f4b3922e3bce438c2183e2551acf5d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030082"
---
# <a name="imanipulationprocessorminimumscalerotateradius-property"></a>Propiedad IManipulationProcessor::MinimumScaleRotateRadius

Especifica el tamaño de los contactos de distancia en un gesto de escala o rotación que deben ser para desencadenar la manipulación.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_MinimumScaleRotateRadius(
  [in]  FLOAT MinimumScaleRotateRadius
);

HRESULT get_MinimumScaleRotateRadius(
  [out] FLOAT *MinimumScaleRotateRadius
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica la distancia mínima entre los contactos para desencadenar gestos de escala o rotación.

## <a name="error-codes"></a>Códigos de error

## <a name="remarks"></a>Comentarios

> [!Note]  
> Esta propiedad se establece en centipixels (100ths of a pixel).

 

Al establecer este valor, el procesador de manipulación omitirá los gestos que tienen un radio demasiado pequeño. Esto resulta útil si desea impedir que un usuario manipule un objeto a un radio demasiado pequeño. Por ejemplo, si usa un procesador de manipulación con un círculo y desea asegurarse de que mantiene un radio superior a 100 píxeles, establecería este valor en 10 000.

## <a name="examples"></a>Ejemplos


```C++
pManip->put_MinimumScaleRotateRadius(4000.0f);  
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 





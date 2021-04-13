---
title: IDCompositionMatrixTransform SetMatrixElement (int, int, IDCompositionAnimation)
description: Anima el valor de un elemento de la matriz de esta transformación 2D.
ms.assetid: 16A9E136-5F0C-4F34-A127-BF06C4530499
keywords:
- Método SetMatrixElement DirectComposition
- Método SetMatrixElement DirectComposition, interfaz IDCompositionMatrixTransform
- IDCompositionMatrixTransform interface DirectComposition, SetMatrixElement (método)
topic_type:
- apiref
api_name:
- IDCompositionMatrixTransform.SetMatrixElement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b4bf2a43e762b85b8b8cfd0c15468b3dc438221
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421147"
---
# <a name="idcompositionmatrixtransformsetmatrixelementint-int-idcompositionanimation-method"></a>Método IDCompositionMatrixTransform:: SetMatrixElement (int, int, IDCompositionAnimation \* )

Anima el valor de un elemento de la matriz de esta transformación 2D.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMatrixElement(
  [in] int                    row,
  [in] int                    column,
  [in] IDCompositionAnimation *animation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fila* \[ de de\]
</dt> <dd>

Índice de fila del elemento que se va a cambiar. Este valor debe estar comprendido entre 0 y 2, ambos inclusive.

</dd> <dt>

*columna* \[ de de\]
</dt> <dd>

Índice de columna del elemento que se va a cambiar. Este valor debe estar comprendido entre 0 y 1, ambos incluidos.

</dd> <dt>

*animación* \[ de de\]
</dt> <dd>

Animación que representa cómo cambia el valor del elemento especificado con el tiempo. Este parámetro no debe ser NULL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve S \_ correcto. De lo contrario, devuelve un código de error **HRESULT** . Consulte [códigos de error de DirectComposition](directcomposition-error-codes.md) para obtener una lista de códigos de error.

## <a name="remarks"></a>Observaciones

Este método realiza una copia de la animación especificada. Si el objeto al que hace referencia el parámetro *Animation* se cambia después de llamar a este método, el cambio no afecta al elemento a menos que se vuelva a llamar a este método. Si el elemento se animaba previamente, al llamar a este método se reemplaza la animación anterior con la nueva animación.

Este método produce un error si la *animación* es un puntero no válido o si no se creó con la misma interfaz [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) que la transformación afectada. La interfaz no puede ser una implementación personalizada; con este método solo se pueden usar las interfaces creadas por Microsoft DirectComposition.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> </dl>

 

 
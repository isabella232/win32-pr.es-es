---
title: Método IDCompositionMatrixTransform SetMatrixElement(int, int, IDCompositionAnimation )
description: Anima el valor de un elemento de la matriz de esta transformación 2D.
ms.assetid: 16A9E136-5F0C-4F34-A127-BF06C4530499
keywords:
- Método SetMatrixElement DirectComposition
- Método SetMatrixElement DirectComposition , interfaz IDCompositionMatrixTransform
- Interfaz IDCompositionMatrixTransform DirectComposition, método SetMatrixElement
topic_type:
- apiref
api_name:
- IDCompositionMatrixTransform.SetMatrixElement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c5a0813243f3d04a729f000c9e42a1eb1ade6406273a1217ca067d8e2f1c3a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043223"
---
# <a name="idcompositionmatrixtransformsetmatrixelementint-int-idcompositionanimation-method"></a>Método IDCompositionMatrixTransform::SetMatrixElement(int, int, IDCompositionAnimation \* )

Anima el valor de un elemento de la matriz de esta transformación 2D.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMatrixElement(
  [in] int                    row,
  [in] int                    column,
  [in] IDCompositionAnimation *animation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*row* \[ En\]
</dt> <dd>

Índice de fila del elemento que se debe cambiar. Este valor debe estar entre 0 y 2, ambos incluidos.

</dd> <dt>

*columna* \[ En\]
</dt> <dd>

Índice de columna del elemento que se debe cambiar. Este valor debe estar entre 0 y 1, ambos incluidos.

</dd> <dt>

*animación* \[ En\]
</dt> <dd>

Animación que representa cómo cambia el valor del elemento especificado con el tiempo. Este parámetro no debe ser NULL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve S \_ OK. De lo contrario, devuelve un código de error **HRESULT.** Consulte [Códigos de error de DirectComposition](directcomposition-error-codes.md) para obtener una lista de códigos de error.

## <a name="remarks"></a>Comentarios

Este método realiza una copia de la animación especificada. Si se cambia el objeto al que hace referencia el parámetro *de* animación después de llamar a este método, el cambio no afecta al elemento a menos que se vuelva a llamar a este método. Si el elemento se animaba previamente, al llamar a este método se reemplaza la animación anterior por la nueva animación.

Se produce un error en este método si *la* animación es un puntero no válido o si no se creó mediante la misma [**interfaz IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) que la transformación afectada. La interfaz no puede ser una implementación personalizada; solo se pueden usar interfaces creadas por Microsoft DirectComposition con este método.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> </dl>

 

 
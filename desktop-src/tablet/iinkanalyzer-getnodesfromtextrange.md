---
description: Recupera una colección de objetos IContextNode que son relevantes para el intervalo de texto especificado para los nodos de contexto especificados.
ms.assetid: 39a5dd52-7007-4395-8668-261eca78a090
title: Método IInkAnalyzer::GetNodesFromTextRange (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetNodesFromTextRange
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: df9eb6e1e748088abaa4780aedfded4e26977018d70dd79f518159185594a90b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057825"
---
# <a name="iinkanalyzergetnodesfromtextrange-method"></a>IInkAnalyzer::GetNodesFromTextRange (método)

Recupera una colección de objetos [**IContextNode**](icontextnode.md) que son relevantes para el intervalo de texto especificado para los nodos de contexto especificados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNodesFromTextRange(
  [in, out] LONG          *plStart,
  [in, out] LONG          *plLength,
  [out]     IContextNodes **ppContextNodes,
  [in]      IContextNodes *pNodesToSearch = defaultvalue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*plStart* \[ in, out\]
</dt> <dd>

Referencia al inicio del intervalo de texto en la *parte pNodesToSearch* de la cadena reconocida.

</dd> <dt>

*plLength* \[ in, out\]
</dt> <dd>

Referencia a la longitud del intervalo de texto en la *parte pNodesToSearch* de la cadena reconocida.

</dd> <dt>

*ppContextNodes* \[ out\]
</dt> <dd>

Puntero a los [**objetos IContextNode**](icontextnode.md) que son relevantes para el intervalo de texto especificado para los nodos de contexto especificados.

</dd> <dt>

*pNodesToSearch* \[ En\]
</dt> <dd>

Objetos [**IContextNode**](icontextnode.md) a los que se va a limitar la búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

El intervalo de texto especificado debe ser relativo a la parte *pNodesToSearch* de la cadena reconocida de [**IInkAnalyzer,**](iinkanalyzer.md)en lugar de a la cadena reconocida de la **IInkAnalyzer completa.**

Este método modifica los valores de los parámetros *plStart* y *plLength* expandiendo el intervalo de texto a los límites de palabras más cercanos.

Por ejemplo, si la cadena reconocida es "I am late" y se llama a este método con los valores de parámetro 6 para *plStart* y 1 para *plLength*, que corresponde a la letra "a" en "late", este método devuelve una colección que contiene un único [**IContextNode**](icontextnode.md), inkWord o TextWord que corresponde a la palabra "late". En este ejemplo, este método también modifica el valor de *plStart* a 5 y el valor de *plLength* a 4, que corresponde a la palabra "late".

> [!Note]  
> El *parámetro plStart* es relativo a la cadena reconocida del *parámetro pNodesToSearch.*

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> </dl>

 

 





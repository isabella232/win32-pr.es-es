---
description: Busca el intervalo de texto en la cadena reconocida que corresponde a una colección de objetos IContextNode.
ms.assetid: 2c5bc4a1-08de-4872-b552-6d22924ce2a8
title: Método IInkAnalyzer::GetTextRangeFromNodes (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetTextRangeFromNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 147877ef8871f7b07e2aa501a107c1e40bd75e80009e5bee97dca03346bb853a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092135"
---
# <a name="iinkanalyzergettextrangefromnodes-method"></a>IInkAnalyzer::GetTextRangeFromNodes (método)

Busca el intervalo de texto en la cadena reconocida que corresponde a una colección de [**objetos IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTextRangeFromNodes(
  [out] LONG          *plStart,
  [out] LONG          *plLength,
  [in]  IContextNodes *pNodesToSearch
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*plStart* \[ out\]
</dt> <dd>

Entero de 32 bits con signo que indica el inicio del intervalo de texto. Este parámetro se pasa sin inicializar.

</dd> <dt>

*plLength* \[ out\]
</dt> <dd>

Entero de 32 bits con signo que indica la longitud del intervalo de texto. Este parámetro se pasa sin inicializar.

</dd> <dt>

*pNodesToSearch* \[ En\]
</dt> <dd>

Colección de objetos [**IContextNode**](icontextnode.md) para los que se va a buscar el intervalo de texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Si *pNodesToSearch* contiene objetos [**IContextNode**](icontextnode.md) que no son adyacentes, este método devuelve el intervalo de texto más pequeño que cubre todos los **objetos IContextNode.**

Este método produce una excepción E INVALIDARG cuando \_ *pNodesToSearch* contiene un [**IContextNode**](icontextnode.md) que no está asociado a [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> </dl>

 

 





---
description: Busca el intervalo de texto en la cadena reconocida que corresponde a una colección de objetos IContextNode.
ms.assetid: 2c5bc4a1-08de-4872-b552-6d22924ce2a8
title: 'IInkAnalyzer:: GetTextRangeFromNodes (método) (IACom. h)'
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
ms.openlocfilehash: da27206a33ca58cebd10192393c4cf2efd1d5919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715204"
---
# <a name="iinkanalyzergettextrangefromnodes-method"></a>IInkAnalyzer:: GetTextRangeFromNodes (método)

Busca el intervalo de texto en la cadena reconocida que corresponde a una colección de objetos [**IContextNode**](icontextnode.md) .

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

*plStart* \[ enuncia\]
</dt> <dd>

Entero de 32 bits con signo que indica el inicio del intervalo de texto. Este parámetro se pasa sin inicializar.

</dd> <dt>

*plLength* \[ enuncia\]
</dt> <dd>

Entero de 32 bits con signo que indica la longitud del intervalo de texto. Este parámetro se pasa sin inicializar.

</dd> <dt>

*pNodesToSearch* \[ de\]
</dt> <dd>

Colección de objetos [**IContextNode**](icontextnode.md) para los que se va a buscar el intervalo de texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Si *pNodesToSearch* contiene objetos [**IContextNode**](icontextnode.md) que no son adyacentes, este método devuelve el intervalo de texto más pequeño que abarca todos los objetos **IContextNode** .

Este método produce una excepción E \_ INVALIDARG cuando *pNodesToSearch* contiene un [**IContextNode**](icontextnode.md) que no está asociado a [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> </dl>

 

 





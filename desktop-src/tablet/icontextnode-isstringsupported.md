---
description: Indica si la cadena reconocida de este IContextNode procede del Diccionario del sistema, del Diccionario del usuario o de la lista de palabras.
ms.assetid: 9eaee549-ae78-4a67-a39e-2096c7d5d9cd
title: 'IContextNode:: IsStringSupported (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 853b244cdd6f9e61d4474876190daeccaa2c8779
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696531"
---
# <a name="icontextnodeisstringsupported-method"></a>IContextNode:: IsStringSupported (método)

Indica si la cadena reconocida de este [**IContextNode**](icontextnode.md) procede del Diccionario del sistema, del Diccionario del usuario o de la lista de palabras.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsStringSupported(
  [out, retval] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pfIsSupported* \[ out, retval\]
</dt> <dd>

**Variante \_ TRUE** si el valor de cadena reconocido de este [**IContextNode**](icontextnode.md) es compatible con [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) con los nodos de sugerencia correspondientes aplicados; de lo contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> </dl>

 

 





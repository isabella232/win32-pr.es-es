---
description: Indica si la cadena reconocida de este IContextNode provenía del diccionario del sistema, el diccionario de usuarios o la lista de palabras.
ms.assetid: 9eaee549-ae78-4a67-a39e-2096c7d5d9cd
title: Método IContextNode::IsStringSupported (IACom.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267687"
---
# <a name="icontextnodeisstringsupported-method"></a>IContextNode::IsStringSupported (método)

Indica si la cadena reconocida de este [**IContextNode**](icontextnode.md) provenía del diccionario del sistema, el diccionario de usuarios o la lista de palabras.

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

**VARIANT \_ TRUE** si el valor de cadena reconocido de [**este IContextNode**](icontextnode.md) es compatible con [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) con los nodos de sugerencia correspondientes aplicados; en caso contrario, **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> </dl>

 

 





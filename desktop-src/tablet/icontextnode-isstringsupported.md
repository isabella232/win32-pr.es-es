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
ms.openlocfilehash: 2eef383f059897665c013e3575d452564295ccd9bd014ae8084fd1635892bd99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709115"
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
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> </dl>

 

 





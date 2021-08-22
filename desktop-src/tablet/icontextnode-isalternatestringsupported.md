---
description: Indica si la cadena reconocida especificada provenía del diccionario del sistema, el diccionario de usuarios o la lista de palabras.
ms.assetid: 1504e633-5917-4ac6-b043-95d4bc75b020
title: Método IContextNode::IsAlternateStringSupported (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsAlternateStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: cbf18c63ce81a439092ba3bdabfae38c5f52882ec5364ef5c8fbd67cab5d81a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119266305"
---
# <a name="icontextnodeisalternatestringsupported-method"></a>IContextNode::IsAlternateStringSupported (método)

Indica si la cadena reconocida especificada provenía del diccionario del sistema, el diccionario de usuarios o la lista de palabras. Cualquier restricción de datos, como listas de palabras, guías o factoids, en cualquier nodo de sugerencia correspondiente se usará para determinar si se admite la cadena.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsAlternateStringSupported(
  [in]  BSTR         bstrAlternateString,
  [out] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrAlternateString* \[ En\]
</dt> <dd>

Cadena reconocida que se debe comprobar.

</dd> <dt>

*pfIsSupported* \[ out\]
</dt> <dd>

**VARIANT \_ TRUE** si la cadena especificada es compatible con [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) con los nodos de sugerencia correspondientes aplicados; **VARIANT \_ FALSE** si no se admite.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

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

 

 





---
description: Indica si la cadena reconocida especificada procede del Diccionario del sistema, del Diccionario del usuario o de la lista de palabras.
ms.assetid: 1504e633-5917-4ac6-b043-95d4bc75b020
title: 'IContextNode:: IsAlternateStringSupported (método) (IACom. h)'
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
ms.openlocfilehash: 93dfcdc59851aad3b06fb1451178e97b36ee0a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666501"
---
# <a name="icontextnodeisalternatestringsupported-method"></a>IContextNode:: IsAlternateStringSupported (método)

Indica si la cadena reconocida especificada procede del Diccionario del sistema, del Diccionario del usuario o de la lista de palabras. Los datos restrictivos, como wordlists, Guides o Factoids, en cualquier nodo de sugerencia correspondiente se utilizarán para determinar si se admite la cadena.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsAlternateStringSupported(
  [in]  BSTR         bstrAlternateString,
  [out] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrAlternateString* \[ de\]
</dt> <dd>

Cadena reconocida que se va a comprobar.

</dd> <dt>

*pfIsSupported* \[ enuncia\]
</dt> <dd>

**Variante \_ TRUE** si el [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) admite la cadena especificada con los nodos de sugerencia correspondientes aplicados; **Variante \_ FALSE** si no se admite.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

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

 

 





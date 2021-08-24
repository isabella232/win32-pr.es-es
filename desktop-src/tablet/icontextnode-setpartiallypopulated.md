---
description: Modifica el valor que indica si este IContextNode está parcial o totalmente rellenado.
ms.assetid: 4d8e1ec0-757d-4346-a77e-263bd612972b
title: Método IContextNode::SetPartiallyPopulated (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6df87085a82117a694b48d08c3e6e1f8500c8959060052f553a53f1a285d9707
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713474"
---
# <a name="icontextnodesetpartiallypopulated-method"></a>IContextNode::SetPartiallyPopulated (método)

Modifica el valor que indica si este [**IContextNode**](icontextnode.md) está parcial o totalmente rellenado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPartiallyPopulated(
  [in] VARIANT_BOOL fPartiallyPopulated
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fPartiallyPopulated* \[ En\]
</dt> <dd>

**VARIANT \_ TRUE** si [**este IContextNode**](icontextnode.md) se rellena parcialmente; en caso contrario, **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

Use este método cuando la aplicación mantenga su propia estructura de datos, que se sincroniza con la de [**IInkAnalyzer**](iinkanalyzer.md). Para obtener más información, vea [Proxy de datos con análisis de entrada de lápiz.](data-proxy-with-ink-analysis.md)

Al virtualizar el árbol de documentos, asegúrese de establecer el valor PropertyGuidsForContextNodes.RotatedBoundingBox (mediante ContextNode.AddPropertyValue) en todos los objetos ContextNode. InkAnalyzer calcula la propiedad RotatedBoundingBox y, de forma predeterminada, debe estar en todos los contextNodes de escritura. Sin embargo, si la aplicación virtualiza los resultados del análisis estableciendo la propiedad PartiallyPopulated, al controlar el evento PopulateContextNode, asegúrese de rellenar la propiedad RotatedBoundingBox. Si no se establece la propiedad RotatedBoundingBox, se podrían usar más datos de documento en la operación de análisis actual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**\_IAnalysisProxyEvents::P opulateContextNode**](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[**IContextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 





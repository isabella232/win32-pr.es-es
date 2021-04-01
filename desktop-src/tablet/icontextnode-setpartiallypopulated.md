---
description: Modifica el valor que indica si este IContextNode se rellena parcial o totalmente.
ms.assetid: 4d8e1ec0-757d-4346-a77e-263bd612972b
title: 'IContextNode:: SetPartiallyPopulated (método) (IACom. h)'
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
ms.openlocfilehash: 31707468945fd3c5eb413bcdb984748a55867982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082154"
---
# <a name="icontextnodesetpartiallypopulated-method"></a>IContextNode:: SetPartiallyPopulated (método)

Modifica el valor que indica si este [**IContextNode**](icontextnode.md) se rellena parcial o totalmente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPartiallyPopulated(
  [in] VARIANT_BOOL fPartiallyPopulated
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fPartiallyPopulated* \[ de\]
</dt> <dd>

**Variante \_ TRUE** si este [**IContextNode**](icontextnode.md) se rellena parcialmente; de lo contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Use este método cuando la aplicación mantenga su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md). Para obtener más información, consulte [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

Al virtualizar el árbol del documento, asegúrese de establecer el valor PropertyGuidsForContextNodes. RotatedBoundingBox (mediante ContextNode. AddPropertyValue) en todos los objetos ContextNode. La propiedad RotatedBoundingBox se calcula mediante InkAnalyzer y, de forma predeterminada, debe estar en todos los ContextNodes de escritura. Sin embargo, si la aplicación Virtualiza los resultados del análisis estableciendo la propiedad PartiallyPopulated, al controlar el evento PopulateContextNode Asegúrese de rellenar la propiedad RotatedBoundingBox. Si no se establece la propiedad RotatedBoundingBox, se usarán potencialmente más datos de documento en la operación de análisis actual.

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
</dt> <dt>

[**\_IAnalysisProxyEvents::P opulateContextNode**](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[**IContextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 





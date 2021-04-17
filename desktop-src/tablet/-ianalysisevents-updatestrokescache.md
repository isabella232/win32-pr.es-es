---
description: Se produce antes de que IInkAnalyzer tenga acceso a los datos del trazo.
ms.assetid: fed46476-4531-4516-9375-d7b654efb3be
title: 'Evento _IAnalysisEvents:: UpdateStrokesCache (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.UpdateStrokesCache
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5d16011d8c5fe571d228b632fecb7a973bafcbf5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105697996"
---
# <a name="_ianalysiseventsupdatestrokescache-event"></a>\_Evento IAnalysisEvents:: UpdateStrokesCache

Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) tenga acceso a los datos del trazo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UpdateStrokesCache(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulStrokeIdsCount* \[ de\]
</dt> <dd>

Número de identificadores de trazo en *plStrokeIds*.

</dd> <dt>

*plStrokeIds* \[ de\]
</dt> <dd>

Los identificadores de los trazos cuyos datos de paquetes se han borrado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

El [**IInkAnalyzer**](iinkanalyzer.md) genera este evento durante el análisis de tinta cuando tiene acceso a uno o varios trazos para los que se han borrado los datos del paquete. Para actualizar los datos del paquete de trazos, utilice el método [**IInkAnalyzer:: UpdateStrokesData Method**](iinkanalyzer-updatestrokesdata.md) .

El [**IInkAnalyzer**](iinkanalyzer.md) no genera este evento cuando se tiene acceso a un nodo de hoja de tinta parcialmente rellenado cuando el **IInkAnalyzer** no ha establecido la ubicación del nodo.

Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer:: Analyze (método)**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer:: BackgroundAnalyze (método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer:: UpdateStrokesData (método)**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[**IContextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 





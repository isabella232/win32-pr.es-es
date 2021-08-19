---
description: Se produce antes de que IInkAnalyzer acceda a los datos del trazo.
ms.assetid: fed46476-4531-4516-9375-d7b654efb3be
title: _IAnalysisEvents::UpdateStrokesCache (IACom.h)
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
ms.openlocfilehash: 9a5854c8061a12dc558a2ca20ebd893880f899b2113065abd9b8122c53812aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047377"
---
# <a name="_ianalysiseventsupdatestrokescache-event"></a>\_Evento IAnalysisEvents::UpdateStrokesCache

Se produce antes de que [**IInkAnalyzer**](iinkanalyzer.md) acceda a los datos del trazo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UpdateStrokesCache(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulStrokeIdsCount* \[ En\]
</dt> <dd>

Número de identificadores de trazo en *plStrokeIds*.

</dd> <dt>

*plStrokeIds* \[ En\]
</dt> <dd>

Identificadores de los trazos cuyos datos de paquete se han borrado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

[**IInkAnalyzer**](iinkanalyzer.md) genera este evento durante el análisis de entrada de lápiz cuando accede a uno o varios trazos para los que se han borrado los datos del paquete. Para actualizar los datos del paquete de trazo, use el [**método IInkAnalyzer::UpdateStrokesData .**](iinkanalyzer-updatestrokesdata.md)

[**IInkAnalyzer**](iinkanalyzer.md) no genera este evento al acceder a un nodo hoja de entrada de lápiz parcialmente rellenado cuando la ubicación del nodo no se ha establecido mediante **IInkAnalyzer**.

Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [Proxy de datos con análisis de entrada de lápiz.](data-proxy-with-ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::Analyze (Método)**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze (Método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer::UpdateStrokesData (Método)**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[**IContextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 





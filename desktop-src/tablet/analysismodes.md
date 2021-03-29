---
description: Especifica cómo el IInkAnalyzer realiza el análisis de tinta.
ms.assetid: bc526445-0c9c-4c53-8b02-32cf758266e6
title: Enumeración AnalysisModes (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisModes
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b9fdebd3ef3cd505b49ff6c82f7609bc339af0a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423507"
---
# <a name="analysismodes-enumeration"></a>Enumeración AnalysisModes

Especifica cómo el [**IInkAnalyzer**](iinkanalyzer.md) realiza el análisis de tinta.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum AnalysisModes { 
  AnalysisModes_None                     = 0x0000,
  AnalysisModes_AutomaticReconciliation  = 0x0002,
  AnalysisModes_StrokeCacheAutoCleanup   = 0x0004,
  AnalysisModes_PersonalizationEnabled   = 0x0008,
  AnalysisModes_Default                  = 0x000d
} AnalysisModes;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**AnalysisModes \_ ninguno**
</dt> <dd>

No se especifica ningún modo.

</dd> <dt>

<span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**AnalysisModes \_ AutomaticReconciliation**
</dt> <dd>

Indica si el [**IInkAnalyzer**](iinkanalyzer.md) inicia automáticamente la operación de conciliación en cuanto los resultados intermedios o finales estén listos.

Si este modo está habilitado, no se genera el evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) . Si este modo está deshabilitado, se genera el evento **\_ IAnalysisEvents:: ReadyToReconcile** .

</dd> <dt>

<span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**AnalysisModes \_ StrokeCacheAutoCleanup**
</dt> <dd>

Si [**IInkAnalyzer**](iinkanalyzer.md) borra automáticamente los trazos innecesarios de la memoria caché del trazo antes de realizar el análisis.

Si este modo está habilitado, el [**IInkAnalyzer**](iinkanalyzer.md) borra los datos del trazo antes de realizar el análisis. El código también debe controlar el evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) . Si no se controla el evento **\_ IAnalysisEvents:: UpdateStrokesCache** , se produce una excepción. Esta comprobación se realiza en las fases de análisis (o BackgroundAnalyze) y de conciliación.

Si este modo está deshabilitado, el [**IInkAnalyzer**](iinkanalyzer.md) no borra los datos del trazo. Para borrar los datos del trazo, llame al [**método IInkAnalyzer:: ClearStrokeData**](iinkanalyzer-clearstrokedata.md). Si este modo está deshabilitado, se desencadena el evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) para que **IInkAnalyzer** pueda recuperar los datos de trazo más recientes de cualquier trazo que haya desactivado la memoria caché. Si se borra la memoria caché del trazo, pero el evento **\_ IAnalysisEvents:: UpdateStrokesCache** no está controlado, se produce una excepción.

</dd> <dt>

<span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**AnalysisModes \_ PersonalizationEnabled**
</dt> <dd>

Está habilitada la personalización del reconocimiento de escritura a mano.

</dd> <dt>

<span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**\_Valor predeterminado de AnalysisModes**
</dt> <dd>

Todos los modos están habilitados.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración permite una combinación bit a bit de sus valores de miembro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer:: GetAnalysisModes (método)**](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[**IInkAnalyzer:: SetAnalysisModes (método)**](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md)
</dt> <dt>

[**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 





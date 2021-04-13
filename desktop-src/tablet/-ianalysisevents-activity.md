---
description: 'Se produce cuando se llama al método IInkAnalyzer:: Analyze o al método IInkAnalyzer:: BackgroundAnalyze.'
ms.assetid: 339b41c6-f388-4b81-b2bc-3705b39d9cc9
title: '_IAnalysisEvents:: Activity (evento) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Activity
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f235d3414b0d514f32b4ebd197c04a8721968a2a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104361962"
---
# <a name="_ianalysiseventsactivity-event"></a>\_Evento IAnalysisEvents:: Activity

Se produce cuando se llama al método [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) o al método [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Activity();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Este evento indica que [**IInkAnalyzer**](iinkanalyzer.md) está realizando el análisis de tinta. Este evento no indica el progreso de la operación de análisis de tinta.

Para realizar cualquiera de las siguientes acciones, implemente un controlador de eventos **\_ IAnalysisEvents:: Activity** :

-   Indicar al usuario que el analizador de tinta está realizando el análisis de tinta.
-   Procesar los datos proporcionados por el usuario durante el análisis sincrónico.
-   Reciba una notificación de las solicitudes del sistema, como la repintado de la ventana de la aplicación, durante el análisis de tinta.

El [**IInkAnalyzer**](iinkanalyzer.md) genera este evento con frecuencia durante la fase de análisis de diseño y la fase de clasificación de escritura y dibujo del análisis de tinta. El **IInkAnalyzer** genera este evento durante la fase de reconocimiento de escritura a mano antes y después de obtener acceso a un reconocedor de tinta.

El número de eventos de actividad que genera un [**IInkAnalyzer**](iinkanalyzer.md) se ve afectado por:

-   El reconocedor de tinta que [**IInkAnalyzer**](iinkanalyzer.md) aplica al reconocimiento de tinta.
-   El número y la longitud de los trazos que el [**IInkAnalyzer**](iinkanalyzer.md) está analizando.
-   Número de trazos que se clasifican como de escritura.

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

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**IInkAnalyzer:: Analyze (método)**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer:: BackgroundAnalyze (método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 





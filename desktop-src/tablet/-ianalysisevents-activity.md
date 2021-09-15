---
description: Se produce cuando se llama al método IInkAnalyzer::Analyze o al método IInkAnalyzer::BackgroundAnalyze.
ms.assetid: 339b41c6-f388-4b81-b2bc-3705b39d9cc9
title: _IAnalysisEvents::Activity (Evento) (IACom.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360349"
---
# <a name="_ianalysiseventsactivity-event"></a>\_Evento IAnalysisEvents::Activity

Se produce cuando [**se llama al método IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md) o al método [**IInkAnalyzer::BackgroundAnalyze.**](iinkanalyzer-backgroundanalyze.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Activity();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

Este evento indica que [**IInkAnalyzer**](iinkanalyzer.md) está realizando análisis de entrada de lápiz. Este evento no indica el progreso de la operación de análisis de entrada de lápiz.

Para realizar cualquiera de las siguientes acciones, implemente un controlador de eventos **\_ IAnalysisEvents::Activity:**

-   Indique al usuario que el analizador de entrada de lápiz está realizando análisis de entrada de lápiz.
-   Procesar la entrada del usuario durante el análisis sincrónico.
-   Recibir una notificación de las solicitudes del sistema, como volver a dibujar la ventana de la aplicación, durante el análisis de entrada de lápiz.

[**IInkAnalyzer**](iinkanalyzer.md) genera este evento con frecuencia durante la fase de análisis de diseño y la fase de clasificación de escritura y dibujo del análisis de entrada de lápiz. **IInkAnalyzer** genera este evento durante la fase de reconocimiento de escritura a mano antes y después de acceder a un reconocedor de lápiz.

El número de eventos de actividad [**que genera un IInkAnalyzer**](iinkanalyzer.md) se ve afectado por:

-   Reconocedor de entrada de lápiz que [**IInkAnalyzer**](iinkanalyzer.md) aplica al reconocimiento de entrada de lápiz.
-   Número y longitud de trazos que [**el IInkAnalyzer**](iinkanalyzer.md) está analizando.
-   Número de trazos que se clasifican como escritura.

Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [Proxy de datos con análisis de entrada de lápiz.](data-proxy-with-ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**IInkAnalyzer::Analyze (Método)**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze (Método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 





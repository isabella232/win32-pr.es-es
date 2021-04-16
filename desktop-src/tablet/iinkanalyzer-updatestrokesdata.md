---
description: Actualiza los datos del paquete para los trazos especificados.
ms.assetid: 7fca4c39-eef2-4019-86a0-27cd0e4e7510
title: 'IInkAnalyzer:: UpdateStrokesData (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.UpdateStrokesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 151403a7114bca2644d0425fdba0155135ac9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705693"
---
# <a name="iinkanalyzerupdatestrokesdata-method"></a>IInkAnalyzer:: UpdateStrokesData (método)

Actualiza los datos del paquete para los trazos especificados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UpdateStrokesData(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds,
  [in] ULONG ulStrokePacketDescriptionCount,
  [in] GUID  *pStrokePacketDescriptionGuids,
  [in] ULONG *pulPacketDataCountPerStroke,
  [in] LONG  *plStrokePacketData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulStrokeIdsCount* \[ de\]
</dt> <dd>

Número de trazos que se van a actualizar.

</dd> <dt>

*plStrokeIds* \[ de\]
</dt> <dd>

Una matriz que contiene los identificadores de trazo.

</dd> <dt>

*ulStrokePacketDescriptionCount* \[ de\]
</dt> <dd>

El número de propiedades de cada paquete.

</dd> <dt>

*pStrokePacketDescriptionGuids* \[ de\]
</dt> <dd>

Una matriz que contiene los identificadores de propiedad de paquete.

</dd> <dt>

*pulPacketDataCountPerStroke* \[ de\]
</dt> <dd>

Una matriz que contiene el número de paquetes de cada trazo.

</dd> <dt>

*plStrokePacketData* \[ de\]
</dt> <dd>

Una matriz que contiene los datos del paquete para los trazos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

el parámetro *plStrokePacketData* contiene los datos de paquete de todos los trazos. El parámetro *pStrokePacketDescriptionGuids* contiene los identificadores únicos globales (GUID) que describen los tipos de datos de paquete incluidos para cada punto de cada trazo. Para obtener una lista completa de las propiedades de paquete disponibles, consulte [constantes de PacketPropertyGuids](packetpropertyguids-constants.md).

Solo los trazos con las mismas descripciones de paquetes se pueden actualizar en una única llamada al **método IInkAnalyzer:: UpdateStrokesData**.

Este método no actualiza la región desfasada del analizador de tinta (consulte el [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Si un trazo especificado no está asociado al [**IInkAnalyzer**](iinkanalyzer.md), este método omite el identificador.

Si ninguno de los trazos especificados identifica un trazo asociado al [**IInkAnalyzer**](iinkanalyzer.md), este método devuelve sin actualizar **IInkAnalyzer**.

Este método devuelve un código de error cuando *plStrokeIds* es **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer:: AddStroke (método)**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer:: AddStrokeForLanguage (método)**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer:: AddStrokeToCustomRecognizer (método)**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer:: AddStrokes (método)**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer:: AddStrokesForLanguage (método)**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer:: AddStrokesToCustomRecognizer (método)**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer:: ClearStrokeData (método)**](iinkanalyzer-clearstrokedata.md)
</dt> <dt>

[**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 





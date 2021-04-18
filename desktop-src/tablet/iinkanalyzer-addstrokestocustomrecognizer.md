---
description: Agrega datos de trazo para varios trazos a un nodo de reconocedor personalizado.
ms.assetid: 77ded896-8573-42de-a41e-4866894dfe2b
title: 'IInkAnalyzer:: AddStrokesToCustomRecognizer (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6df1b31957f3b4087b51fbad0e7b527c2ede799c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715215"
---
# <a name="iinkanalyzeraddstrokestocustomrecognizer-method"></a>IInkAnalyzer:: AddStrokesToCustomRecognizer (método)

Agrega datos de trazo para varios trazos a un nodo de reconocedor personalizado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddStrokesToCustomRecognizer(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulStrokeIdsCount* \[ de\]
</dt> <dd>

Número de trazos que se van a agregar.

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

</dd> <dt>

*pCustomRecognizer* \[ de\]
</dt> <dd>

[**IContextNode**](icontextnode.md) de tipo **CustomRecognizer** al que se van a agregar los trazos.

</dd> <dt>

*ppContextNodeStrokeAddedTo* \[ enuncia\]
</dt> <dd>

[**IContextNode**](icontextnode.md) en el que el analizador de tinta ha agregado los trazos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodeStrokeAddedTo* cuando ya no necesite usar el objeto.

 

Cuando *ppContextNodeStrokeAddedTo* es **null**, indica que el llamador no está interesado en el valor devuelto del método.

[**IInkAnalyzer**](iinkanalyzer.md) agrega los trazos a un [**IContextNode**](icontextnode.md) de tipo **CustomRecognizer** (consulte tipos de [nodo de contexto](context-node-types.md)). Este nodo está en la colección de subnodos del nodo raíz (consulte métodos [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md) y [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) ).

[**IInkAnalyzer**](iinkanalyzer.md) asigna el identificador de referencia cultural del subproceso de entrada activo a los trazos y agrega los trazos al primer nodo **UnclassifiedInk** bajo el nodo **CustomRecognizer** . Si no existe ningún nodo **UnclassifiedInk** , se crea. Si el [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) asociado con el nodo **CustomRecognizer** no admite el identificador de referencia cultural, el **IInkAnalyzer** continúa analizando y generando una advertencia [**IAnalysisWarning**](ianalysiswarning.md) . Esta advertencia tiene un valor [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) de **AnalysisWarningCode \_ LanguageIdNotRespected**.

*plStrokePacketData* contiene los datos de paquete de todos los trazos. *pStrokePacketDescriptionGuids* contiene los identificadores únicos globales (GUID) que describen los tipos de datos de paquetes incluidos para cada punto de cada trazo. Para obtener una lista completa de las propiedades de paquete disponibles, consulte [constantes de PacketPropertyGuids](packetpropertyguids-constants.md).

> [!Note]  
> Solo se pueden agregar trazos con las mismas descripciones de paquete en una única llamada al **método IInkAnalyzer:: AddStrokesToCustomRecognizer**.

 

Este método expande la región desfasada a la Unión del valor actual de la región y el rectángulo de selección de los trazos agregados.

[**IInkAnalyzer**](iinkanalyzer.md) devuelve un **valor HRESULT** de **E \_ INVALIDARG** en las siguientes circunstancias.

-   El [**IInkAnalyzer**](iinkanalyzer.md) ya contiene un trazo con el mismo identificador que uno de los trazos que se van a agregar.
-   El parámetro *pCustomRecognizer* contiene un nodo de reconocedor personalizado que está asociado a un objeto [**IInkAnalyzer**](iinkanalyzer.md) diferente.
-   El parámetro *pCustomRecognizer* contiene una [**IContextNode**](icontextnode.md) que no es de tipo **CustomRecognizer**.

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

[Tipos de nodo de contexto](context-node-types.md)
</dt> <dt>

[**IInkAnalyzer:: AddStrokeToCustomRecognizer (método)**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer:: CreateCustomRecognizer (método)**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 


---
description: Agrega datos de trazo para varios trazos a un nodo de reconocedor personalizado.
ms.assetid: 77ded896-8573-42de-a41e-4866894dfe2b
title: Método IInkAnalyzer::AddStrokesToCustomRecognizer (IACom.h)
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
ms.openlocfilehash: 9c50bcd1faa9df94847e3100309fc8598511dd760fa5efd6ccdf84812020fd63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719224"
---
# <a name="iinkanalyzeraddstrokestocustomrecognizer-method"></a>Método IInkAnalyzer::AddStrokesToCustomRecognizer

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

*ulStrokeIdsCount* \[ En\]
</dt> <dd>

Número de trazos que se agregarán.

</dd> <dt>

*plStrokeIds* \[ En\]
</dt> <dd>

Matriz que contiene los identificadores de trazo.

</dd> <dt>

*ulStrokePacketDescriptionCount* \[ En\]
</dt> <dd>

Número de propiedades de cada paquete.

</dd> <dt>

*pStrokePacketDescriptionGuids* \[ En\]
</dt> <dd>

Matriz que contiene los identificadores de propiedad de paquete.

</dd> <dt>

*pulPacketDataCountPerStroke* \[ En\]
</dt> <dd>

Matriz que contiene el número de paquetes en cada trazo.

</dd> <dt>

*plStrokePacketData* \[ En\]
</dt> <dd>

Matriz que contiene los datos del paquete para los trazos.

</dd> <dt>

*pCustomRecognizer* \[ En\]
</dt> <dd>

[**IContextNode de**](icontextnode.md) tipo **CustomRecognizer** al que se agregan los trazos.

</dd> <dt>

*ppContextNodeStrokeAddedTo* \[ out\]
</dt> <dd>

[**IContextNode al**](icontextnode.md) que el analizador de entrada de lápiz agregó los trazos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodeStrokeAddedTo* cuando ya no necesite usar el objeto .

 

Cuando *ppContextNodeStrokeAddedTo* es **NULL,** indica que el autor de la llamada no está interesado en el valor devuelto del método .

[**IInkAnalyzer**](iinkanalyzer.md) agrega los trazos a un [**IContextNode**](icontextnode.md) de tipo **CustomRecognizer** (vea [Tipos de nodo de contexto).](context-node-types.md) Este nodo está en la colección de subnodos del nodo raíz (vea Los métodos [**IInkAnalyzer::GetRootNode e**](iinkanalyzer-getrootnode.md) [**IContextNode::GetSubNodes).**](icontextnode-getsubnodes.md)

[**IInkAnalyzer**](iinkanalyzer.md) asigna el identificador de referencia cultural del subproceso de entrada activo a los trazos y agrega los trazos al primer nodo **UnclassifiedInk** bajo el **nodo CustomRecognizer.** Si no **existe ningún nodo UnclassifiedInk,** se crea. Si [**el IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) asociado al nodo **CustomRecognizer** no admite el identificador de referencia cultural, **IInkAnalyzer** continúa analizando y genera una advertencia [**IAnalysisWarning.**](ianalysiswarning.md) Esta advertencia tiene el [**valor AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) **de AnalysisWarningCode \_ LanguageIdNotRespected.**

*plStrokePacketData contiene* datos de paquetes para todos los trazos. *pStrokePacketDescriptionGuids* contiene los identificadores únicos globales (GUID) que describen los tipos de datos de paquetes incluidos para cada punto de cada trazo. Para obtener una lista completa de las propiedades de paquete disponibles, vea [PacketPropertyGuids Constants](packetpropertyguids-constants.md).

> [!Note]  
> Solo se pueden agregar trazos con las mismas descripciones de paquetes en una sola llamada al método **IInkAnalyzer::AddStrokesToCustomRecognizer**.

 

Este método expande la región desusada a la unión del valor actual de la región y el cuadro de límite de los trazos agregados.

[**IInkAnalyzer devuelve**](iinkanalyzer.md) un **valor HRESULT** de **E \_ INVALIDARG en** las siguientes circunstancias.

-   [**IInkAnalyzer**](iinkanalyzer.md) ya contiene un trazo con el mismo identificador que uno de los trazos que se van a agregar.
-   El *parámetro pCustomRecognizer* contiene un nodo de reconocedor personalizado que está asociado a un objeto [**IInkAnalyzer**](iinkanalyzer.md) diferente.
-   El *parámetro pCustomRecognizer* contiene un [**IContextNode**](icontextnode.md) que no es de tipo **CustomRecognizer.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[Tipos de nodo de contexto](context-node-types.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokeToCustomRecognizer (Método)**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer::CreateCustomRecognizer (Método)**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 


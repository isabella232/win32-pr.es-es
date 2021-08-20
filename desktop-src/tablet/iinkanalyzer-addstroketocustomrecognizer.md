---
description: Agrega datos de trazo para un solo trazo a un nodo de reconocedor personalizado.
ms.assetid: ab43c9f8-15fe-49db-b9d1-57d34b95d99f
title: Método IInkAnalyzer::AddStrokeToCustomRecognizer (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 0a3ce58f462053b48e6cecdc7eb276a1e162f88b0e7de373648a537b3b712cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967334"
---
# <a name="iinkanalyzeraddstroketocustomrecognizer-method"></a>Método IInkAnalyzer::AddStrokeToCustomRecognizer

Agrega datos de trazo para un solo trazo a un nodo de reconocedor personalizado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddStrokeToCustomRecognizer(
  [in]  ULONG        ulStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulStrokeId* \[ En\]
</dt> <dd>

Identificador del trazo que se agregará.

</dd> <dt>

*ulStrokePacketDataCount* \[ En\]
</dt> <dd>

Número de paquetes en el trazo.

</dd> <dt>

*plStrokePacketData* \[ En\]
</dt> <dd>

Matriz que contiene los datos del paquete para el trazo.

</dd> <dt>

*ulStrokePacketDescriptionCount* \[ En\]
</dt> <dd>

Número de propiedades de paquete en cada paquete.

</dd> <dt>

*pStrokePacketDescriptionGuids* \[ En\]
</dt> <dd>

Matriz que contiene los identificadores de propiedad de paquete.

</dd> <dt>

*pCustomRecognizer* \[ En\]
</dt> <dd>

[**IContextNode de**](icontextnode.md) tipo **CustomRecognizer** al que se va a agregar el trazo.

</dd> <dt>

*ppContextNodeStrokeAddedTo* \[ out\]
</dt> <dd>

[**IContextNode al**](icontextnode.md) que el analizador de entrada de lápiz agregó el trazo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodeStrokeAddedTo* cuando ya no necesite usar el objeto .

 

Cuando *ppContextNodeStrokeAddedTo* es **NULL,** indica que el autor de la llamada no está interesado en el valor devuelto del método .

[**IInkAnalyzer agrega**](iinkanalyzer.md) el trazo a [**un IContextNode**](icontextnode.md) de tipo **CustomRecognizer** (vea [Tipos de nodo de contexto).](context-node-types.md) Este nodo está en la colección de subnodos del nodo raíz (vea Los métodos [**IInkAnalyzer::GetRootNode e**](iinkanalyzer-getrootnode.md) [**IContextNode::GetSubNodes).**](icontextnode-getsubnodes.md)

[**IInkAnalyzer**](iinkanalyzer.md) asigna el identificador de referencia cultural del subproceso de entrada activo al trazo y agrega el trazo al primer nodo **UnclassifiedInk** bajo el **nodo CustomRecognizer.** Si no **existe ningún nodo UnclassifiedInk,** se crea. Si [**el IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) asociado al nodo **CustomRecognizer** no admite el identificador de referencia cultural, **IInkAnalyzer** continúa analizando y genera una advertencia [**IAnalysisWarning.**](ianalysiswarning.md) Esta advertencia tiene el [**valor AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) **de AnalysisWarningCode \_ LanguageIdNotRespected.**

*plStrokePacketData contiene* datos de paquetes para todos los puntos del trazo. *pStrokePacketDescriptionGuids* contiene los identificadores únicos globales (GUID) que describen los tipos de datos de paquetes incluidos para cada punto de cada trazo. Para obtener una lista completa de las propiedades de paquete disponibles, vea [PacketPropertyGuids Constants](packetpropertyguids-constants.md).

Este método expande la región desusada a la unión del valor actual de la región y el cuadro de límite del trazo agregado.

[**IInkAnalyzer devuelve**](iinkanalyzer.md) un **valor HRESULT** de **E \_ INVALIDARG en** las siguientes circunstancias.

-   [**IInkAnalyzer**](iinkanalyzer.md) ya contiene un trazo con el mismo identificador que el trazo que se va a agregar.
-   El *parámetro pCustomRecognizer* contiene un nodo de reconocedor personalizado que está asociado a un objeto [**IInkAnalyzer**](iinkanalyzer.md) diferente.
-   El *parámetro pCustomRecognizer* contiene un [**IContextNode**](icontextnode.md) que no es de tipo **CustomRecognizer.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[Tipos de nodo de contexto](context-node-types.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokesToCustomRecognizer (Método)**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer::CreateCustomRecognizer (Método)**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 


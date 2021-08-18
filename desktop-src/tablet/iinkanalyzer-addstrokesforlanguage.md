---
description: Agrega datos de trazo para varios trazos al IInkAnalyzer y asigna el identificador de referencia cultural especificado a los trazos.
ms.assetid: 1274b24f-204b-4a84-a7c0-0205b6068ae8
title: Método IInkAnalyzer::AddStrokesForLanguage (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesForLanguage
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 52e2dc742dc91b37bce29d477cf91f7178f2ae2a62ce3a329d2b9bf79c46b33a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719613"
---
# <a name="iinkanalyzeraddstrokesforlanguage-method"></a>IInkAnalyzer::AddStrokesForLanguage (método)

Agrega datos de trazo para varios trazos al [**IInkAnalyzer**](iinkanalyzer.md) y asigna el identificador de referencia cultural especificado a los trazos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddStrokesForLanguage(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plIdofStrokesToAdd,
  [in]  LONG         lStrokesLCID,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulStrokeIdsCount* \[ En\]
</dt> <dd>

Número de trazos que se agregarán.

</dd> <dt>

*plIdofStrokesToAdd* \[ En\]
</dt> <dd>

Matriz que contiene los identificadores de trazo.

</dd> <dt>

*lStrokesLCID* \[ En\]
</dt> <dd>

Valor que representa el identificador de referencia cultural que se asignará a los trazos.

</dd> <dt>

*ulStrokePacketDescriptionCount* \[ En\]
</dt> <dd>

Número de propiedades de cada paquete.

</dd> <dt>

*pStrokePacketDescriptionGuids* \[ En\]
</dt> <dd>

Matriz que contiene los identificadores de propiedad del paquete.

</dd> <dt>

*pulPacketDataCountPerStroke* \[ En\]
</dt> <dd>

Matriz que contiene el número de paquetes en cada trazo.

</dd> <dt>

*plStrokePacketData* \[ En\]
</dt> <dd>

Matriz que contiene los datos del paquete para los trazos.

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

[**IInkAnalyzer agrega los**](iinkanalyzer.md) trazos a un [**IContextNode**](icontextnode.md) de tipo UnclassifiedInk (vea [Tipos de nodos de contexto).](context-node-types.md) Este nodo está en la colección de subnodos del nodo raíz (vea Los métodos [**IInkAnalyzer::GetRootNode**](iinkanalyzer-getrootnode.md) y [**IContextNode::GetSubNodes).**](icontextnode-getsubnodes.md)

[**IInkAnalyzer**](iinkanalyzer.md) asigna el identificador de referencia cultural *lStrokeLCID* a los trazos y agrega los trazos al primer nodo de contexto UnclassifiedInk bajo el nodo raíz del analizador de entrada de lápiz que contiene trazos con el mismo identificador de referencia cultural. Si el analizador de entrada de lápiz no tiene un nodo con el mismo identificador de referencia cultural, crea un nuevo nodo de contexto UnclassifiedInk en su nodo raíz y agrega los trazos al nuevo nodo de contexto UnclassifiedInk.

*plStrokePacketData contiene* datos de paquetes para todos los trazos. *pStrokePacketDescriptionGuids* contiene los identificadores únicos globales (GUID) que describen los tipos de datos de paquete incluidos para cada punto de cada trazo. Para obtener una lista completa de las propiedades de paquete disponibles, [vea PacketPropertyGuids Constants](packetpropertyguids-constants.md).

> [!Note]  
> Solo se pueden agregar trazos con las mismas descripciones de paquetes en una sola llamada al método [**IInkAnalyzer::AddStrokes**](iinkanalyzer-addstrokes.md).

 

Este método expande la región desusada a la unión del valor actual de la región y el cuadro de límite de los trazos agregados.

Si [**IInkAnalyzer**](iinkanalyzer.md) ya contiene un trazo con el mismo identificador que uno de los trazos que se van a agregar, **IInkAnalyzer** devuelve un **HRESULT** de **E \_ INVALIDARG.**

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

[**IInkAnalyzer::AddStroke (Método)**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokeForLanguage (Método)**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokes (Método)**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer::RemoveStroke (Método)**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer::RemoveStrokes (Método)**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 


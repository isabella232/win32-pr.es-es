---
description: Agrega datos de trazo para un único trazo al IInkAnalyzer y asigna el identificador de referencia cultural del subproceso de entrada activo al trazo.
ms.assetid: 0e603e5a-d722-4ab8-bc59-605e131c863b
title: Método IInkAnalyzer::AddStroke (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f7ba08e779e115c243918d94e5b41e8a7d77f54fab92b045274135ead2ae0264
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590595"
---
# <a name="iinkanalyzeraddstroke-method"></a>IInkAnalyzer::AddStroke (método)

Agrega datos de trazo para un único trazo al [**IInkAnalyzer**](iinkanalyzer.md) y asigna el identificador de referencia cultural del subproceso de entrada activo al trazo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddStroke(
  [in]  LONG         lStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lStrokeId* \[ En\]
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

*ppContextNodeStrokeAddedTo* \[ out\]
</dt> <dd>

Puntero al [**IContextNode al**](icontextnode.md) que [**IInkAnalyzer**](iinkanalyzer.md) agregó el trazo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodeStrokeAddedTo* cuando ya no necesite usar el objeto .

 

Cuando *ppContextNodeStrokeAddedTo* es **NULL,** indica que el autor de la llamada no está interesado en el valor devuelto del método .

[**IInkAnalyzer**](iinkanalyzer.md) agrega el trazo a un [**IContextNode**](icontextnode.md) de tipo UnclassifiedInk (vea [Tipos de nodos de contexto).](context-node-types.md) Este nodo está en la colección de subnodos del nodo raíz (vea Los métodos [**IInkAnalyzer::GetRootNode**](iinkanalyzer-getrootnode.md) y [**IContextNode::GetSubNodes).**](icontextnode-getsubnodes.md)

[**IInkAnalyzer**](iinkanalyzer.md) asigna el identificador de referencia cultural del subproceso de entrada activo al trazo y agrega el trazo al primer nodo de contexto UnclassifiedInk bajo el nodo raíz del analizador de entrada de lápiz que contiene trazos con el mismo identificador de referencia cultural. Si el analizador de entrada de lápiz no tiene un nodo con el mismo identificador de referencia cultural, crea un nuevo nodo de contexto UnclassifiedInk en su nodo raíz y agrega el trazo al nuevo nodo de contexto UnclassifiedInk.

*plStrokePacketData contiene* datos de paquetes para todos los puntos del trazo. *pStrokePacketDescriptionGuids* contiene los identificadores únicos globales (GUID) que describen los tipos de datos de paquete incluidos para cada punto del trazo. Para obtener una lista completa de las propiedades de paquete disponibles, [vea PacketPropertyGuids Constants](packetpropertyguids-constants.md).

Este método expande la región desusada a la unión del valor actual de la región y el cuadro de límite del trazo agregado.

Si [**IInkAnalyzer**](iinkanalyzer.md) ya contiene un trazo con el mismo identificador de trazo, **IInkAnalyzer** devuelve **un HRESULT** de **E \_ INVALIDARG**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**InkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokeForLanguage (Método)**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokes (Método)**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokesForLanguage (Método)**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer::RemoveStroke (Método)**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer::RemoveStrokes (Método)**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 


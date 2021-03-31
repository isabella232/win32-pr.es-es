---
description: Agrega datos de trazo para varios trazos al IInkAnalyzer y asigna el identificador de referencia cultural especificado a los trazos.
ms.assetid: 1274b24f-204b-4a84-a7c0-0205b6068ae8
title: 'IInkAnalyzer:: AddStrokesForLanguage (método) (IACom. h)'
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
ms.openlocfilehash: 7f1c8bde9f1fe9d9c7123fa3c40540d0fd2660ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275473"
---
# <a name="iinkanalyzeraddstrokesforlanguage-method"></a>IInkAnalyzer:: AddStrokesForLanguage (método)

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

*ulStrokeIdsCount* \[ de\]
</dt> <dd>

Número de trazos que se van a agregar.

</dd> <dt>

*plIdofStrokesToAdd* \[ de\]
</dt> <dd>

Una matriz que contiene los identificadores de trazo.

</dd> <dt>

*lStrokesLCID* \[ de\]
</dt> <dd>

Valor que representa el identificador de referencia cultural que se va a asignar a los trazos.

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

[**IInkAnalyzer**](iinkanalyzer.md) agrega los trazos a un [**IContextNode**](icontextnode.md) de tipo UnclassifiedInk (consulte tipos de [nodo de contexto](context-node-types.md)). Este nodo está en la colección de subnodos del nodo raíz (consulte métodos [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md) y [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) ).

[**IInkAnalyzer**](iinkanalyzer.md) asigna el identificador de referencia cultural de *lStrokeLCID* a los trazos y agrega los trazos al primer nodo de contexto UnclassifiedInk en el nodo raíz del analizador de tinta que contiene los trazos con el mismo identificador de referencia cultural. Si el analizador de tintas no tiene un nodo con el mismo identificador de referencia cultural, crea un nuevo nodo de contexto UnclassifiedInk en el nodo raíz y agrega los trazos al nuevo nodo de contexto UnclassifiedInk.

*plStrokePacketData* contiene los datos de paquete de todos los trazos. *pStrokePacketDescriptionGuids* contiene los identificadores únicos globales (GUID) que describen los tipos de datos de paquetes incluidos para cada punto de cada trazo. Para obtener una lista completa de las propiedades de paquete disponibles, consulte [constantes de PacketPropertyGuids](packetpropertyguids-constants.md).

> [!Note]  
> Solo se pueden agregar trazos con las mismas descripciones de paquete en una única llamada al [**método IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md).

 

Este método expande la región desfasada a la Unión del valor actual de la región y el rectángulo de selección de los trazos agregados.

Si el [**IInkAnalyzer**](iinkanalyzer.md) ya contiene un trazo con el mismo identificador que uno de los trazos que se van a agregar, el **IInkAnalyzer** devuelve un **valor HRESULT** de **E \_ INVALIDARG**.

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

[**IInkAnalyzer:: AddStrokes (método)**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer:: RemoveStroke (método)**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer:: RemoveStrokes (método)**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 


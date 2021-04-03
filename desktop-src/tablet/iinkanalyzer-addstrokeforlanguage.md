---
description: Agrega datos de trazo para un solo trazo al IInkAnalyzer y asigna un identificador de referencia cultural específico al trazo.
ms.assetid: 65eb805e-05ed-4144-b17e-872c47ab33fa
title: 'IInkAnalyzer:: AddStrokeForLanguage (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeForLanguage
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 674a58ef891d919d09f86f28a35748de3537db91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908017"
---
# <a name="iinkanalyzeraddstrokeforlanguage-method"></a>IInkAnalyzer:: AddStrokeForLanguage (método)

Agrega datos de trazo para un solo trazo al [**IInkAnalyzer**](iinkanalyzer.md) y asigna un identificador de referencia cultural específico al trazo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddStrokeForLanguage(
  [in]  LONG         lStrokeId,
  [in]  LONG         lStrokeLCID,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lStrokeId* \[ de\]
</dt> <dd>

Identificador del trazo que se va a agregar.

</dd> <dt>

*lStrokeLCID* \[ de\]
</dt> <dd>

Identificador de referencia cultural que se va a asignar al trazo.

</dd> <dt>

*ulStrokePacketDataCount* \[ de\]
</dt> <dd>

Número de paquetes del trazo.

</dd> <dt>

*plStrokePacketData* \[ de\]
</dt> <dd>

Una matriz que contiene los datos del paquete del trazo.

</dd> <dt>

*ulStrokePacketDescriptionCount* \[ de\]
</dt> <dd>

El número de propiedades de cada paquete.

</dd> <dt>

*pStrokePacketDescriptionGuids* \[ de\]
</dt> <dd>

Una matriz que contiene los identificadores de propiedad de paquete.

</dd> <dt>

*ppContextNodeStrokeAddedTo* \[ enuncia\]
</dt> <dd>

Puntero cuyo valor se establece en el puntero del [**IContextNode**](icontextnode.md) que contiene el trazo que se acaba de agregar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodeStrokeAddedTo* cuando ya no necesite usar el objeto.

 

Cuando *ppContextNodeStrokeAddedTo* es **null**, indica que el llamador no está interesado en el valor devuelto del método.

El [**IInkAnalyzer**](iinkanalyzer.md) agrega el trazo a un [**IContextNode**](icontextnode.md) de tipo UnclassifiedInk (consulte [tipos de nodo de contexto](context-node-types.md)). Este nodo está en la colección de subnodos del nodo raíz (consulte métodos [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md) y [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) ).

[**IInkAnalyzer**](iinkanalyzer.md) asigna el identificador de referencia cultural de *lStrokeLCID* al trazo y agrega el trazo al primer nodo de contexto UnclassifiedInk en el nodo raíz del analizador de tinta que contiene los trazos con el mismo identificador de referencia cultural. Si el analizador de tintas no tiene un nodo con el mismo identificador de referencia cultural, crea un nuevo nodo de contexto UnclassifiedInk en el nodo raíz y agrega el trazo al nuevo nodo de contexto UnclassifiedInk.

*plStrokePacketData* contiene datos de paquetes para todos los puntos del trazo. *pStrokePacketDescriptionGuids* contiene los identificadores únicos globales (GUID) que describen los tipos de datos de paquete incluidos para cada punto del trazo. Para obtener una lista completa de las propiedades de paquete disponibles, consulte [constantes de PacketPropertyGuids](packetpropertyguids-constants.md).

Este método expande la región desfasada a la Unión del valor actual de la región y el rectángulo de selección del trazo agregado.

Si el [**IInkAnalyzer**](iinkanalyzer.md) ya contiene un trazo con el mismo identificador de trazo, el **IInkAnalyzer** devuelve un **valor HRESULT** de **E \_ INVALIDARG**.

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

[**IInkAnalyzer:: AddStrokes (método)**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer:: AddStrokesForLanguage (método)**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer:: RemoveStroke (método)**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer:: RemoveStrokes (método)**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 


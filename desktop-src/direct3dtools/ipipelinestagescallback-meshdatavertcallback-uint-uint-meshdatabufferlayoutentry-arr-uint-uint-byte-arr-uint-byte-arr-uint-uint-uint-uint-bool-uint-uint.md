---
description: Devolución de llamada que notifica al host de las fases de canalización información de malla devuelta por la solicitud a la que se ha avisado.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataVertCallback\_UINT\_UINT\_MeshDataBufferLayoutEntry\_arr\_UINT\_UINT\_BYTE\_arr\_UINT\_BYTE\_arr\_UINT\_UINT\_UINT\_UINT\_BOOL\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback::MeshDataVertCallback (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E75EDE35-AC8E-4452-B79B-860C39B156F0
api_name:
- IPipeLineStagesCallback.MeshDataVertCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e51321373de80a4e90835a46c53e895bff7114df
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625951"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uintspanipipelinestagescallbackmeshdatavertcallback-method"></a><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>IPipeLineStagesCallback::MeshDataVertCallback (método)

Devolución de llamada que notifica al host de las fases de canalización información de malla devuelta por la solicitud a la que se ha avisado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MeshDataVertCallback(
   UINT                         numVertices,
   UINT                         numBufferLayoutEntries,
   MeshDataBufferLayoutEntry [] count1_entries,
   UINT                         stride,
   UINT                         numVBBytes,
   BYTE []                      count4_pVBData,
   UINT                         numIBBytes,
   BYTE []                      count6_pIBData,
   UINT                         indexSize,
   UINT                         IBOffset,
   UINT                         baseVertex,
   UINT                         minVertex,
   BOOL                         IBIndexesVB,
   UINT                         numIndices,
   UINT                         topology
);
```

## <a name="parameters"></a>Parámetros

*numVertices*   
Número de vértices en los resultados.

*numBufferLayoutEntries*   
Número de entradas de diseño de búfer en los resultados.

*entradas \_ count1*   
El diseño del búfer se completa. Estos describen la firma de salida del sombreador.

*Paso*   
Tamaño (stride) de un fragmento de salida completo.

*numVBBytes*   
Tamaño del búfer de vértices en bytes.

*count4 \_ pVBData*   
Búfer de vértice.

*numIBBytes*   
Tamaño del búfer de índice en bytes.

*count6 \_ pIBData*   
Búfer de índice.

*indexSize*   
Tamaño de cada índice en bytes.

*IBOffset*   
Desplazamiento en el búfer de índice que especifica dónde deben empezar a usarse los índices.

*baseVertex*   
Desplazamiento en el búfer de vértices que especifica dónde deben empezar a usarse los vértices.

*minVertex*   

*IBIndexesVB*   
True cuando se usa el búfer de índice; de lo contrario, false.

*numIndices*   
Número de índices usados.

*Topología*   
Topolology del sombreador. Esto no es necesariamente lo mismo que la topología de la llamada a draw asociada.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IPipeLineStagesCallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 

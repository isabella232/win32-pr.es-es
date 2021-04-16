---
description: Devolución de llamada que notifica al host de las fases de canalización de la información de malla devuelta por la solicitud asociada.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataVertCallback\_UINT\_UINT\_MeshDataBufferLayoutEntry\_arr\_UINT\_UINT\_BYTE\_arr\_UINT\_BYTE\_arr\_UINT\_UINT\_UINT\_UINT\_BOOL\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback:: MeshDataVertCallback (método)'
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
ms.openlocfilehash: 3c878851b0c3cfe32128d766f4dcb35a7437579d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537192"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uintspanipipelinestagescallbackmeshdatavertcallback-method"></a><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>IPipeLineStagesCallback:: MeshDataVertCallback (método)

Devolución de llamada que notifica al host de las fases de canalización de la información de malla devuelta por la solicitud asociada.

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
El número de vértices de los resultados.

*numBufferLayoutEntries*   
El número de entradas de diseño de búfer en los resultados.

*entradas de count1 \_*   
El diseño del búfer es completo. Estos describen la firma de salida del sombreador.

*STRI*   
Tamaño (STRIDE) de un fragmento de salida completo.

*numVBBytes*   
Tamaño del búfer de vértices en bytes.

*count4 \_ pVBData*   
Búfer de vértices.

*numIBBytes*   
Tamaño del búfer de índice en bytes.

*count6 \_ pIBData*   
Búfer de índice.

*indexSize*   
Tamaño de cada índice en bytes.

*IBOffset*   
Desplazamiento en el búfer de índice que especifica dónde se deben empezar a usar los índices.

*baseVertex*   
Desplazamiento en el búfer de vértice que especifica dónde se deben empezar a usar los vértices.

*minVertex*   

*IBIndexesVB*   
True cuando se utiliza el búfer de índice; en caso contrario, false.

*numIndices*   
Número de índices usados.

*topología*   
Topolology del sombreador. Esto no es necesariamente el mismo que la topología de la llamada a Draw asociada.

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IPipeLineStagesCallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 

---
description: Devolución de llamada que notifica al host el número de subprocesos y grupos del sombreador de cálculo en la solicitud asociada.
MS-HAID: vspixengine.IPipeLineStagesCallback2\_ThreadDataDimensionCallback\_ThreadData3D\_ThreadData3D
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback2:: ThreadDataDimensionCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E8765C14-0A55-468D-BCA8-3E28E5476DFB
api_name:
- IPipeLineStagesCallback2.ThreadDataDimensionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 93a8ee64c863128513563f3ce50dd2bfcdd77714
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423088"
---
# <a name="span-idvspixengineipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3dspanipipelinestagescallback2threaddatadimensioncallback-method"></a><span id="vspixengine.ipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3d"></span>IPipeLineStagesCallback2:: ThreadDataDimensionCallback (método)

Devolución de llamada que notifica al host el número de subprocesos y grupos del sombreador de cálculo en la solicitud asociada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ThreadDataDimensionCallback(
   ThreadData3D threadGroupCount,
   ThreadData3D threadGroupSize
);
```

## <a name="parameters"></a>Parámetros

*threadGroupCount*   
Recuento multidimensional de grupos de subprocesos.

*threadGroupSize*   
Tamaño multidimensional de cada grupo de subprocesos.

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IPipeLineStagesCallback2**](/windows/desktop/direct3dtools/ipipelinestagescallback2)

 

 

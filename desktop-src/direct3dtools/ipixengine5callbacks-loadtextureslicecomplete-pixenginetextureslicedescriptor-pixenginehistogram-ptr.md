---
description: Función de devolución de llamada que se usa para notificar al host cuando se ha completado una carga de segmento de textura.
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadTextureSliceComplete\_PixEngineTextureSliceDescriptor\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5Callbacks::LoadTextureSliceComplete (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CEEAB77F-0856-4DEC-991A-7CEB921C84BB
api_name:
- IPixEngine5Callbacks.LoadTextureSliceComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 93ad2b73c1d139aeacd23bb62df63b8393e6e695
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627111"
---
# <a name="span-idvspixengineipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptrspanipixengine5callbacksloadtextureslicecomplete-method"></a><span id="vspixengine.ipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptr"></span>IPixEngine5Callbacks::LoadTextureSliceComplete (método)

Función de devolución de llamada que se usa para notificar al host cuando se ha completado una carga de segmento de textura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LoadTextureSliceComplete(
   PixEngineTextureSliceDescriptor sliceDesc,
   PixEngineHistogram*             histogram
);
```

## <a name="parameters"></a>Parámetros

*sliceDesc*   
Descriptor del segmento cargado.

*Histograma*   
Dirección de los datos del histograma para el segmento cargado.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IPixEngine5Callbacks**](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 

---
description: Solicita que inicie una sesión de depuración de sombreador para la fase de canalización especificada, píxel/vértice, si corresponde, evento y marco.
MS-HAID: vspixengine.IDebugShaderRequest\_BeginDebugShader\_IPixErrorCallback\_ptr\_EventID\_DWORD\_DWORD\_Point2D\_PipeLineStages\_PixelHistoryOperation\_ptr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IDebugShaderRequest:: BeginDebugShader (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC93D31C-8593-4B03-B974-87B886B9431D
api_name:
- IDebugShaderRequest.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b6512dc8aa67b3f4d128be3cd2dcd2b622ba2035
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152373"
---
# <a name="span-idvspixengineidebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptrspanidebugshaderrequestbegindebugshader-method"></a><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>IDebugShaderRequest:: BeginDebugShader (método)

Solicita que inicie una sesión de depuración de sombreador para la fase de canalización especificada, píxel/vértice, si corresponde, evento y marco.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback *     errorCallback,
   EventID                 eventID,
   DWORD                   frameNumber,
   DWORD                   vertex,
   Point2D                 pixel,
   PipeLineStages          stage,
   PixelHistoryOperation * pPixelHistory,
   DWORD *                 pDevice
);
```

## <a name="parameters"></a>Parámetros

*errorCallback*   
Dirección de una devolución de llamada para los errores que pueden producirse durante la depuración.

*eventID*   
El evento especificado.

*Númeromarco*   
Marco especificado.

*vértice*   
El vértice especificado. Solo se aplica al depurar un sombreador de vértices.

*píxel*   
Píxel especificado. Solo se aplica al depurar un sombreador de píxeles.

*media*   
La fase de canalización especificada.

*pPixelHistory*   
Dirección de los resultados del historial de píxeles utilizados para buscar el píxel asociado que se va a depurar. Solo se aplica al depurar un sombreador de píxeles.

*pDevice*   
Dirección que se va a pasar al motor de depuración para comunicarse con esta sesión de depuración (motor de depuración readprocessmemory en esta dirección).

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IDebugShaderRequest**](/windows/desktop/direct3dtools/idebugshaderrequest)

 

 

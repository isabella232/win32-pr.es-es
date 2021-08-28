---
description: Solicita iniciar una sesión de depuración del sombreador para la fase de canalización, el píxel o el vértice especificados, si procede, el evento y el marco.
MS-HAID: vspixengine.IDebugShaderRequest\_BeginDebugShader\_IPixErrorCallback\_ptr\_EventID\_DWORD\_DWORD\_Point2D\_PipeLineStages\_PixelHistoryOperation\_ptr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IDebugShaderRequest::BeginDebugShader (Método)
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
ms.openlocfilehash: 20e9667ba0c0d4d36175cd9694c2e6b57d192fab
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629859"
---
# <a name="span-idvspixengineidebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptrspanidebugshaderrequestbegindebugshader-method"></a><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>IDebugShaderRequest::BeginDebugShader (Método)

Solicita iniciar una sesión de depuración del sombreador para la fase de canalización, el píxel o el vértice especificados, si procede, el evento y el marco.

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

*Eventid*   
Evento especificado.

*frameNumber*   
Marco especificado.

*Vértice*   
Vértice especificado. Solo se aplica al depurar un sombreador de vértices.

*Pixel*   
Píxel especificado. Solo se aplica al depurar un sombreador de píxeles.

*Etapa*   
Fase de canalización especificada.

*pPixelHistory*   
Dirección de los resultados del historial de píxeles que se usan para buscar el píxel asociado que se depurará. Solo se aplica al depurar un sombreador de píxeles.

*pDevice*   
Dirección que se va a pasar al motor de depuración para comunicarse con esta sesión de depuración (readprocessmemory del motor de depuración en esta dirección).

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IDebugShaderRequest**](/windows/desktop/direct3dtools/idebugshaderrequest)

 

 

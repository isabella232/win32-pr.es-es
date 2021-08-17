---
description: Solicitudes para generar instrucciones de seguimiento del sombreador en una solicitud de depuración. La depuración basada en seguimiento se produce en la CPU (distorsión) en lugar de en la GPU.
MS-HAID: vspixengine.IDebugShaderRequest2\_GenerateInstructions\_IPixErrorCallback\_ptr\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr\_IDebugShaderCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IDebugShaderRequest2::GenerateInstructions (Método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50685D38-AA85-43D7-9199-12B3776708C2
api_name:
- IDebugShaderRequest2.GenerateInstructions
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 08005bd777f8835f60615c61dfc6ae763f2a5a8345bb8309e0923941eeacf2dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094875"
---
# <a name="span-idvspixengineidebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptrspanidebugshaderrequest2generateinstructions-method"></a><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>IDebugShaderRequest2::GenerateInstructions (Método)

Solicitudes para generar instrucciones de seguimiento del sombreador en una solicitud de depuración. La depuración basada en seguimiento se produce en la CPU (distorsión) en lugar de en la GPU.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GenerateInstructions(
   IPixErrorCallback *      errorCallback,
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory,
   IDebugShaderCallback *   pCallback
);
```

## <a name="parameters"></a>Parámetros

*errorCallback*   
Dirección de una devolución de llamada para los errores que pueden producirse al generar instrucciones de seguimiento del sombreador.

*requestInfo*   
Dirección de una estructura DebugShaderRequestInfo que describe el evento, vértice o píxel solicitado.

*pPixelHistory*   
Dirección de los resultados del historial de píxeles que se usan para buscar el píxel asociado que se debe depurar. Solo se aplica al depurar un sombreador de píxeles.

*pCallback*   
Dirección de una devolución de llamada utilizada para notificar al host de resultados.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IDebugShaderRequest2**](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 

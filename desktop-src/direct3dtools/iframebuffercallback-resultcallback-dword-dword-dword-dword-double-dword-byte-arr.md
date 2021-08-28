---
description: Devolución de llamada que notifica al host la información del búfer de fotogramas devuelta por la solicitud asociada.
MS-HAID: vspixengine.IFrameBufferCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_double\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameBufferCallback::ResultCallback (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F0276125-2DA9-45BC-A295-BD67C21EE601
api_name:
- IFrameBufferCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2308ec5355da8f8fda7eeccf31d1cbe19e8a8247
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626681"
---
# <a name="span-idvspixengineiframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arrspaniframebuffercallbackresultcallback-method"></a><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>IFrameBufferCallback::ResultCallback (método)

Devolución de llamada que notifica al host la información del búfer de fotogramas devuelta por la solicitud asociada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ResultCallback(
   DWORD   frameNumber,
   DWORD   width,
   DWORD   height,
   DWORD   renderTargetPtr,
   double  frameDuraction,
   DWORD   size,
   BYTE [] count5_buffer
);
```

## <a name="parameters"></a>Parámetros

*frameNumber*   
Número de fotograma.

*Ancho*   
Ancho del marco.

*Altura*   
Alto del marco.

*renderTargetPtr*   
Destino de representación del que proceden los resultados. Siempre es una ranura especificada por la solicitud de búfer de fotogramas, o si no es una llamada a draw, el primer RTV salta al origen de salida.

*frameDuraction*   
No se utiliza.

*Tamaño*   
Tamaño del búfer de salida en bytes.

*búfer \_ count5*   
Contenido del destino de representación en formato R8G8B8A8 \_ UNORM.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IFrameBufferCallback**](/windows/desktop/direct3dtools/iframebuffercallback)

 

 

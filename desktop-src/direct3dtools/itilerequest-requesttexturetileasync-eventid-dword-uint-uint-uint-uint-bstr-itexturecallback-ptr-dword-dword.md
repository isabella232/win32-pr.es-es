---
description: Solicita obtener el contenido de una textura en mosaico como . Archivo DDS (DirectDraw Surface).
MS-HAID: vspixengine.ITileRequest\_RequestTextureTileAsync\_EventID\_DWORD\_UINT\_UINT\_UINT\_UINT\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ITileRequest::RequestTextureTileAsync (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E3F4FAC2-E7D9-4FDF-BE64-73D3EA175A8F
api_name:
- ITileRequest.RequestTextureTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 20e67b9cd6d05e32488246306edb80d35fc8c6379fe4054f2cb1d7858f8e7402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119469"
---
# <a name="span-idvspixengineitilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dwordspanitilerequestrequesttexturetileasync-method"></a><span id="vspixengine.itilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dword"></span>ITileRequest::RequestTextureTileAsync (método)

Solicita obtener el contenido de una textura en mosaico como . Archivo DDS (DirectDraw Surface).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RequestTextureTileAsync(
   EventID            eventID,
   DWORD              textureFileptr,
   UINT               tileSubresource,
   UINT               tileX,
   UINT               tileY,
   UINT               tileZ,
   BSTR               ddsFilename,
   ITextureCallback * pRequestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a>Parámetros

*Eventid*   
Evento especificado con el que se va a hacer coincidir el contenido del búfer (por ejemplo, un destino de representación podría cambiar con el tiempo).

*textureFileptr*   
Dirección del objeto de textura especificado.

*tileSubresource*   
El subrecurso especificado del icono.

*tileX*   
Posición X del icono especificado.

*tileY*   
Posición Y del icono especificado.

*tileZ*   
Posición Z del icono especificado.

*ddsFilename*   
Cadena COM que contiene el nombre de ruta de acceso del archivo .dds donde se escriben los resultados.

*pRequestCallback*   
Dirección de devolución de llamada utilizada para notificar al host de resultados.

*requestCookie*   
Cookie que identifica de forma única la solicitud y se puede usar para indicar que se cancele.

*progressIntervalMsecs*   
No se usa.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**ITileRequest**](/windows/desktop/direct3dtools/itilerequest)

 

 

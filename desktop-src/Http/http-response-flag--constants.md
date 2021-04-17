---
title: Constantes de HTTP_RESPONSE_FLAG_ (http. h)
description: Defina las opciones para configurar las respuestas en la API del servidor HTTP.
ms.assetid: bcb59457-fd22-4166-8a72-ba85209ec8c7
topic_type:
- apiref
api_name:
- HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96b7c34d453c1b9bbe45cf2c85ad268b414f3439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665959"
---
# <a name="http_response_flag_-constants"></a>Constantes de la \_ marca de respuesta HTTP \_ \_

Las constantes de la **\_ \_ \_ marca de respuesta http** definen las opciones para configurar las respuestas en la API del servidor http.

Estas constantes se utilizan en el miembro **Flags** de la estructura [**http \_ Response \_ v1**](/windows/desktop/api/Http/ns-http-http_response_v1) .

<dl> <dt>

<span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**\_marca de respuesta HTTP \_ \_ varias \_ codificaciones \_ disponibles**
</dt> <dd> <dl> <dt>



Las codificaciones que no sean el formulario de identidad están disponibles para este recurso. Esta marca se omite si la aplicación no ha solicitado que se almacene en caché la respuesta. Se usa como una sugerencia a la API del servidor HTTP para la negociación de contenido cuando atiende desde la caché de respuesta del kernel.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Http. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[API del servidor HTTP versión 2,0 constantes](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**\_Respuesta HTTP \_ v1**](/windows/desktop/api/Http/ns-http-http_response_v1)
</dt> </dl>

 

 






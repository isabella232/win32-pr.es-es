---
title: HTTP_RESPONSE_FLAG_ constantes (Http.h)
description: Defina opciones para configurar respuestas en la API del servidor HTTP.
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
ms.openlocfilehash: 3099012df5be9ed4a53d3072319be6dc47ede32b71567749c4668cd7870fee29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394413"
---
# <a name="http_response_flag_-constants"></a>Constantes \_ HTTP RESPONSE \_ FLAG \_

Las **constantes HTTP RESPONSE \_ \_ FLAG \_** definen opciones para configurar respuestas en la API del servidor HTTP.

Estas constantes se usan en el miembro **Flags** de la [**estructura HTTP RESPONSE \_ \_ V1.**](/windows/desktop/api/Http/ns-http-http_response_v1)

<dl> <dt>

<span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**MARCAS DE RESPUESTA HTTP \_ \_ CON VARIAS \_ \_ \_ CODIFICACIONES DISPONIBLES**
</dt> <dd> <dl> <dt>



Hay codificaciones distintas del formulario de identidad disponibles para este recurso. Esta marca se omite si la aplicación no ha solicitado que la respuesta se almacene en caché. Se usa como sugerencia para la API del servidor HTTP para la negociación de contenido al servir desde la caché de respuestas del kernel.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                           |
| Header<br/>                   | <dl> <dt>Http.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes de API de servidor HTTP versión 2.0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**RESPUESTA \_ HTTP \_ V1**](/windows/desktop/api/Http/ns-http-http_response_v1)
</dt> </dl>

 

 






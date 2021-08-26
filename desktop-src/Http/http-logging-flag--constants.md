---
title: HTTP_LOGGING_FLAG_ constantes (Http.h)
description: Defina las opciones para configurar el registro en la API del servidor HTTP.
ms.assetid: b6afef7a-5426-4ccd-9785-169e83812c07
topic_type:
- apiref
api_name:
- HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER
- HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION
- HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY
- HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ae84697d84295d137f929bcf0d65c2e49fc6754aa7c1110d3b341bb471cbcb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981445"
---
# <a name="http_logging_flag_-constants"></a>Constantes \_ DE MARCA DE \_ REGISTRO \_ HTTP

Las **constantes HTTP \_ LOGGING \_ FLAG \_** definen las opciones para configurar el registro en la API del servidor HTTP.

Estas constantes se usan en la estructura [**HTTP \_ LOGGING \_ INFO.**](/windows/desktop/api/Http/ns-http-http_logging_info)

<dl> <dt>

<span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**SUVERSIÓN \_ DE LA HORA LOCAL DE LA MARCA DE REGISTRO \_ \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



La suversión del archivo de registro se basa en la hora local. De forma predeterminada, las subaciones de archivos de registro se basan en la hora universal coordinada (UTC).


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span>**HTTP \_ MARCA DE \_ REGISTRO \_ USAR CONVERSIÓN \_ \_ UTF8**
</dt> <dd> <dl> <dt>



Los campos Unicode se convierten en multibyte UTF8 al escribir en los archivos de registro. De forma predeterminada, los archivos de registro se escriben con la conversión de página de códigos local.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**SOLO \_ ERRORES DE REGISTRO DE MARCA DE REGISTRO \_ \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



Los archivos de registro solo incluyen información de error. De forma predeterminada, se registran las respuestas de error y correctas. Si no se **establece http \_ LOGGING FLAG LOG \_ ERRORS \_ \_ \_ ONLY** o **HTTP \_ LOGGING FLAG LOG SUCCESS \_ \_ \_ \_ ONLY,** se registra tanto la información de error como de acierto.

Esta marca no se puede establecer si la marca **HTTP \_ LOGGING \_ FLAG LOG \_ \_ SUCCESS \_ ONLY** también está establecida. Estas dos marcas son mutuamente excluyentes.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span>**HTTP \_ SOLO SE HA \_ CORRECTO EL REGISTRO DE LA MARCA DE \_ \_ \_ REGISTRO**
</dt> <dd> <dl> <dt>



Los archivos de registro solo incluyen información de éxito. De forma predeterminada, se registran los errores y las transacciones correctas. Si no se **establece http \_ LOGGING FLAG LOG \_ ERRORS \_ \_ \_ ONLY** o **HTTP \_ LOGGING FLAG LOG SUCCESS \_ \_ \_ \_ ONLY,** se registra tanto la información de error como de acierto.

Esta marca no se puede establecer si la marca **HTTP \_ LOGGING \_ FLAG LOG \_ ERRORS \_ \_ ONLY** también está establecida. Estas dos marcas son mutuamente excluyentes.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                              |
| Header<br/>                   | <dl> <dt>Http.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de API de servidor HTTP versión 2.0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**INFORMACIÓN \_ DE REGISTRO \_ HTTP**](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 






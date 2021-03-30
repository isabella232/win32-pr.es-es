---
title: Constantes de HTTP_LOGGING_FLAG_ (http. h)
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
ms.openlocfilehash: c501fc3ab646ab65fa039a5ff5e7d2dc0578002a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803026"
---
# <a name="http_logging_flag_-constants"></a>\_Constantes de \_ marca de registro http \_

Las constantes de la **\_ \_ \_ marca de registro http** definen las opciones para configurar el registro en la API del servidor http.

Estas constantes se utilizan en la estructura [**de \_ \_ información de registro http**](/windows/desktop/api/Http/ns-http-http_logging_info) .

<dl> <dt>

<span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**\_sustitución de \_ la \_ \_ hora local \_ de la marca de registro http**
</dt> <dd> <dl> <dt>



La sustitución del archivo de registro se basa en la hora local. De forma predeterminada, la sustitución del archivo de registro se basa en la hora universal coordinada (UTC).


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span>**Http \_ Marca de registro \_ \_ usar \_ \_ conversión UTF8**
</dt> <dd> <dl> <dt>



Los campos Unicode se convierten en UTF8 multibyte cuando se escriben en los archivos de registro. De forma predeterminada, los archivos de registro se escriben con la conversión de página de códigos local.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**\_ \_ \_ solo errores de registro de marca \_ de registro http \_**
</dt> <dd> <dl> <dt>



Los archivos de registro solo incluyen información de errores. De forma predeterminada, se registran las respuestas de error y de éxito. Si no se establecen los errores de registro de marcas de registro **http \_ \_ \_ \_ \_ solamente** o se establece la marca de registro **http \_ \_ \_ \_ Success Success \_ Only** , se registra la información de error y de éxito.

No se puede establecer esta marca si también se establece la marca **http \_ Logging \_ Flag \_ log \_ Success \_ Only** . Estas dos marcas son mutuamente excluyentes.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span>**Http \_ \_ \_ Registro \_ correcto \_** de la marca de registro
</dt> <dd> <dl> <dt>



Los archivos de registro solo incluyen información de éxito. De forma predeterminada, se registran los errores y las transacciones correctas. Si no se establecen los errores de registro de marcas de registro **http \_ \_ \_ \_ \_ solamente** o se establece la marca de registro **http \_ \_ \_ \_ Success Success \_ Only** , se registra la información de error y de éxito.

No se puede establecer esta marca si también se ha establecido la marca de **\_ registro de marcas de registro \_ \_ \_ \_ http** . Estas dos marcas son mutuamente excluyentes.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Http. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[API del servidor HTTP versión 2,0 constantes](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**\_información de registro http \_**](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 






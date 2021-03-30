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
# <a name="http_logging_flag_-constants"></a><span data-ttu-id="15efb-103">\_Constantes de \_ marca de registro http \_</span><span class="sxs-lookup"><span data-stu-id="15efb-103">HTTP\_LOGGING\_FLAG\_ Constants</span></span>

<span data-ttu-id="15efb-104">Las constantes de la **\_ \_ \_ marca de registro http** definen las opciones para configurar el registro en la API del servidor http.</span><span class="sxs-lookup"><span data-stu-id="15efb-104">The **HTTP\_LOGGING\_FLAG\_** constants define the options to configure logging on the HTTP Server API.</span></span>

<span data-ttu-id="15efb-105">Estas constantes se utilizan en la estructura [**de \_ \_ información de registro http**](/windows/desktop/api/Http/ns-http-http_logging_info) .</span><span class="sxs-lookup"><span data-stu-id="15efb-105">These constants are used in the [**HTTP\_LOGGING\_INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="15efb-106"><span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**\_sustitución de \_ la \_ \_ hora local \_ de la marca de registro http**</span><span class="sxs-lookup"><span data-stu-id="15efb-106"><span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**HTTP\_LOGGING\_FLAG\_LOCAL\_TIME\_ROLLOVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="15efb-107">La sustitución del archivo de registro se basa en la hora local.</span><span class="sxs-lookup"><span data-stu-id="15efb-107">The log file rollover is based on local time.</span></span> <span data-ttu-id="15efb-108">De forma predeterminada, la sustitución del archivo de registro se basa en la hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="15efb-108">By default, log file rollovers is based on coordinated universal time (UTC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="15efb-109"><span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span>**Http \_ Marca de registro \_ \_ usar \_ \_ conversión UTF8**</span><span class="sxs-lookup"><span data-stu-id="15efb-109"><span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span> **HTTP\_LOGGING\_FLAG\_USE\_UTF8\_CONVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="15efb-110">Los campos Unicode se convierten en UTF8 multibyte cuando se escriben en los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="15efb-110">The unicode fields are converted to UTF8 multibytes when writting to the log files.</span></span> <span data-ttu-id="15efb-111">De forma predeterminada, los archivos de registro se escriben con la conversión de página de códigos local.</span><span class="sxs-lookup"><span data-stu-id="15efb-111">By default, the log files are written with the local code page conversion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="15efb-112"><span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**\_ \_ \_ solo errores de registro de marca \_ de registro http \_**</span><span class="sxs-lookup"><span data-stu-id="15efb-112"><span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="15efb-113">Los archivos de registro solo incluyen información de errores.</span><span class="sxs-lookup"><span data-stu-id="15efb-113">The log files include error information only.</span></span> <span data-ttu-id="15efb-114">De forma predeterminada, se registran las respuestas de error y de éxito.</span><span class="sxs-lookup"><span data-stu-id="15efb-114">By default, both error and success responses are logged.</span></span> <span data-ttu-id="15efb-115">Si no se establecen los errores de registro de marcas de registro **http \_ \_ \_ \_ \_ solamente** o se establece la marca de registro **http \_ \_ \_ \_ Success Success \_ Only** , se registra la información de error y de éxito.</span><span class="sxs-lookup"><span data-stu-id="15efb-115">If neither the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** or the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** is set, both error and success information is logged.</span></span>

<span data-ttu-id="15efb-116">No se puede establecer esta marca si también se establece la marca **http \_ Logging \_ Flag \_ log \_ Success \_ Only** .</span><span class="sxs-lookup"><span data-stu-id="15efb-116">This flag cannot be set if the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** flag is also set.</span></span> <span data-ttu-id="15efb-117">Estas dos marcas son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="15efb-117">These two flags are mutually exclusive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="15efb-118"><span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span>**Http \_ \_ \_ Registro \_ correcto \_** de la marca de registro</span><span class="sxs-lookup"><span data-stu-id="15efb-118"><span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span> **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="15efb-119">Los archivos de registro solo incluyen información de éxito.</span><span class="sxs-lookup"><span data-stu-id="15efb-119">The log files include success information only.</span></span> <span data-ttu-id="15efb-120">De forma predeterminada, se registran los errores y las transacciones correctas.</span><span class="sxs-lookup"><span data-stu-id="15efb-120">By default, both errors and success transactions are logged.</span></span> <span data-ttu-id="15efb-121">Si no se establecen los errores de registro de marcas de registro **http \_ \_ \_ \_ \_ solamente** o se establece la marca de registro **http \_ \_ \_ \_ Success Success \_ Only** , se registra la información de error y de éxito.</span><span class="sxs-lookup"><span data-stu-id="15efb-121">If neither the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** or the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** is set, both error and success information is logged.</span></span>

<span data-ttu-id="15efb-122">No se puede establecer esta marca si también se ha establecido la marca de **\_ registro de marcas de registro \_ \_ \_ \_ http** .</span><span class="sxs-lookup"><span data-stu-id="15efb-122">This flag cannot be set if the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** flag is also set.</span></span> <span data-ttu-id="15efb-123">Estas dos marcas son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="15efb-123">These two flags are mutually exclusive.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15efb-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15efb-124">Requirements</span></span>



| <span data-ttu-id="15efb-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="15efb-125">Requirement</span></span> | <span data-ttu-id="15efb-126">Value</span><span class="sxs-lookup"><span data-stu-id="15efb-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="15efb-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15efb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="15efb-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="15efb-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="15efb-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15efb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="15efb-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="15efb-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="15efb-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15efb-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="15efb-132"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="15efb-132"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15efb-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="15efb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15efb-134">API del servidor HTTP versión 2,0 constantes</span><span class="sxs-lookup"><span data-stu-id="15efb-134">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="15efb-135">**\_información de registro http \_**</span><span class="sxs-lookup"><span data-stu-id="15efb-135">**HTTP\_LOGGING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[<span data-ttu-id="15efb-136">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="15efb-136">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="15efb-137">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="15efb-137">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="15efb-138">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="15efb-138">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="15efb-139">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="15efb-139">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 






---
title: Constantes de HTTP_AUTH_ENABLE_ (http. h)
description: Defina los esquemas de autenticación que pueden habilitarse en un grupo de direcciones URL.
ms.assetid: db22645f-c9e4-427e-b3d5-91d568aec7c5
topic_type:
- apiref
api_name:
- HTTP_AUTH_ENABLE_BASIC
- HTTP_AUTH_ENABLE_DIGEST
- HTTP_AUTH_ENABLE_KERBEROS
- HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING
- HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL
- HTTP_AUTH_ENABLE_NTLM
- HTTP_AUTH_ENABLE_NEGOTIATE
- HTTP_AUTH_ENABLE_ALL
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6462a4f9d884244f460c4bf7714b45d3e17600c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492832"
---
# <a name="http_auth_enable_-constants"></a><span data-ttu-id="80a1b-103">\_ \_ Habilitación de las constantes de autenticación HTTP \_</span><span class="sxs-lookup"><span data-stu-id="80a1b-103">HTTP\_AUTH\_ENABLE\_ Constants</span></span>

<span data-ttu-id="80a1b-104">Las constantes de **\_ \_ habilitación** de la autenticación http definen los esquemas de autenticación que se pueden habilitar en un grupo de direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="80a1b-104">The **HTTP\_AUTH\_ENABLE** constants define authentication schemes that can be enabled on a URL Group.</span></span>

<span data-ttu-id="80a1b-105">Estas constantes se utilizan en la estructura [**de \_ \_ \_ información de autenticación del servidor http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) .</span><span class="sxs-lookup"><span data-stu-id="80a1b-105">These constants are used in the [**HTTP\_SERVER\_AUTHENTICATION\_INFO**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="80a1b-106"><span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**\_autenticación HTTP \_ habilitada \_ básica**</span><span class="sxs-lookup"><span data-stu-id="80a1b-106"><span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**HTTP\_AUTH\_ENABLE\_BASIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="80a1b-107">El esquema de autenticación básica está habilitado.</span><span class="sxs-lookup"><span data-stu-id="80a1b-107">The Basic authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="80a1b-108"><span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**\_autenticación HTTP \_ habilitar \_ Resumen**</span><span class="sxs-lookup"><span data-stu-id="80a1b-108"><span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**HTTP\_AUTH\_ENABLE\_DIGEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="80a1b-109">El esquema de autenticación implícita está habilitado.</span><span class="sxs-lookup"><span data-stu-id="80a1b-109">The Digest authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="80a1b-110"><span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**\_autenticación HTTP \_ habilitar \_ Kerberos**</span><span class="sxs-lookup"><span data-stu-id="80a1b-110"><span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**HTTP\_AUTH\_ENABLE\_KERBEROS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="80a1b-111">El esquema de autenticación Kerberos está habilitado.</span><span class="sxs-lookup"><span data-stu-id="80a1b-111">The Kerberos authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="80a1b-112"><span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**\_marca http auth \_ ex habilitar el \_ \_ \_ \_ \_ almacenamiento en caché de credenciales de Kerberos**</span><span class="sxs-lookup"><span data-stu-id="80a1b-112"><span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**HTTP\_AUTH\_EX\_FLAG\_ENABLE\_KERBEROS\_CREDENTIAL\_CACHING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="80a1b-113">El almacenamiento en caché de credenciales de Kerberos está habilitado.</span><span class="sxs-lookup"><span data-stu-id="80a1b-113">Kerberos credential caching is enabled.</span></span>

<span data-ttu-id="80a1b-114">**Windows Server 2003 y anteriores:** No disponible.</span><span class="sxs-lookup"><span data-stu-id="80a1b-114">**Windows Server 2003 and before:** Not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="80a1b-115"><span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**\_credencial de \_ \_ captura de \_ marca \_ de autenticación http**</span><span class="sxs-lookup"><span data-stu-id="80a1b-115"><span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**HTTP\_AUTH\_EX\_FLAG\_CAPTURE\_CREDENTIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="80a1b-116">La API del servidor HTTP captura la identidad del autor de la llamada y la usa solo para la autenticación para los esquemas Negotiate y Kerberos.</span><span class="sxs-lookup"><span data-stu-id="80a1b-116">The HTTP Server API captures the caller identity and uses it for authentication for Negotiate and Kerberos schemes only.</span></span>

<span data-ttu-id="80a1b-117">**Windows Server 2003 y anteriores:** No disponible.</span><span class="sxs-lookup"><span data-stu-id="80a1b-117">**Windows Server 2003 and before:** Not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="80a1b-118"><span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**\_autenticación HTTP \_ habilitar \_ NTLM**</span><span class="sxs-lookup"><span data-stu-id="80a1b-118"><span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**HTTP\_AUTH\_ENABLE\_NTLM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="80a1b-119">El esquema de autenticación NTLM está habilitado.</span><span class="sxs-lookup"><span data-stu-id="80a1b-119">The NTLM authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="80a1b-120"><span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**\_autenticación HTTP \_ habilitar \_ Negotiate**</span><span class="sxs-lookup"><span data-stu-id="80a1b-120"><span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**HTTP\_AUTH\_ENABLE\_NEGOTIATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="80a1b-121">El esquema de autenticación Negotiate está habilitado.</span><span class="sxs-lookup"><span data-stu-id="80a1b-121">The Negotiate authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="80a1b-122"><span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**\_habilitación de autenticación HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="80a1b-122"><span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**HTTP\_AUTH\_ENABLE\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="80a1b-123">Están habilitados todos los esquemas de autenticación.</span><span class="sxs-lookup"><span data-stu-id="80a1b-123">All authentication schemes are enabled.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80a1b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80a1b-124">Requirements</span></span>



| <span data-ttu-id="80a1b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="80a1b-125">Requirement</span></span> | <span data-ttu-id="80a1b-126">Value</span><span class="sxs-lookup"><span data-stu-id="80a1b-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="80a1b-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80a1b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="80a1b-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="80a1b-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="80a1b-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80a1b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="80a1b-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="80a1b-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="80a1b-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80a1b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="80a1b-132"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="80a1b-132"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80a1b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="80a1b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80a1b-134">API del servidor HTTP versión 2,0 constantes</span><span class="sxs-lookup"><span data-stu-id="80a1b-134">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="80a1b-135">**\_información de \_ autenticación del servidor HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="80a1b-135">**HTTP\_SERVER\_AUTHENTICATION\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_server_authentication_info)
</dt> <dt>

[<span data-ttu-id="80a1b-136">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="80a1b-136">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="80a1b-137">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="80a1b-137">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="80a1b-138">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="80a1b-138">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="80a1b-139">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="80a1b-139">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 






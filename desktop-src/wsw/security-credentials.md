---
title: Credenciales de seguridad
description: Las credenciales de seguridad son un fragmento de evidencia que posee una entidad de comunicación que se puede usar para crear u obtener un token de seguridad.
ms.assetid: 70e260ce-9e45-436f-b6d1-b650a5c9c0e9
keywords:
- Servicios Web de credenciales de seguridad para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0611e6e54fd83e09f811ffddcda4785cef162685
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "105705078"
---
# <a name="security-credentials"></a><span data-ttu-id="15c3a-106">Credenciales de seguridad</span><span class="sxs-lookup"><span data-stu-id="15c3a-106">Security Credentials</span></span>

<span data-ttu-id="15c3a-107">Las credenciales de seguridad son un fragmento de evidencia que posee una entidad de comunicación que se puede usar para crear u obtener un token de seguridad.</span><span class="sxs-lookup"><span data-stu-id="15c3a-107">Security credentials are a piece of evidence that a communicating party possesses that can be used to create or obtain a security token.</span></span> <span data-ttu-id="15c3a-108">Por lo tanto, las credenciales suelen durar más que los tokens de seguridad, y un token de seguridad se puede ver como la manifestación en tiempo de ejecución de las credenciales de seguridad.</span><span class="sxs-lookup"><span data-stu-id="15c3a-108">Thus, credentials are typically longer-lived than security tokens, and a security token can be viewed as the runtime manifestation of the security credentials.</span></span> <span data-ttu-id="15c3a-109">Un ejemplo de credenciales incluye un certificado de equipo (que se puede convertir en un token de seguridad X. 509 en tiempo de ejecución) o un par de nombre de usuario/contraseña para un dominio (que se puede usar para obtener un token de seguridad de Kerberos).</span><span class="sxs-lookup"><span data-stu-id="15c3a-109">Example of credentials include a machine certificate (which can be converted into an X.509 security token at runtime) or a username/password pair for a domain (which can be used to obtain a Kerberos security token).</span></span>


<span data-ttu-id="15c3a-110">Las credenciales se especifican como parte de los [enlaces de seguridad](security-bindings.md).</span><span class="sxs-lookup"><span data-stu-id="15c3a-110">Credentials are specified as part of the [security bindings](security-bindings.md).</span></span>

<span data-ttu-id="15c3a-111">Los siguientes elementos de API se usan con las credenciales de seguridad.</span><span class="sxs-lookup"><span data-stu-id="15c3a-111">The following API elements are used with security credentials.</span></span>

| <span data-ttu-id="15c3a-112">Devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="15c3a-112">Callback</span></span>                                                                  | <span data-ttu-id="15c3a-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="15c3a-113">Description</span></span>                                              |
|---------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="15c3a-114">**devolución de llamada de WS \_ Get \_ CERT \_**</span><span class="sxs-lookup"><span data-stu-id="15c3a-114">**WS\_GET\_CERT\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)                   | <span data-ttu-id="15c3a-115">Proporciona un certificado para el tiempo de ejecución de seguridad.</span><span class="sxs-lookup"><span data-stu-id="15c3a-115">Provides a certificate to the security runtime.</span></span>          |
| [<span data-ttu-id="15c3a-116">**devolución de llamada de validación de contraseña de WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="15c3a-116">**WS\_VALIDATE\_PASSWORD\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback) | <span data-ttu-id="15c3a-117">Valida un par de nombre de usuario y contraseña en el lado receptor.</span><span class="sxs-lookup"><span data-stu-id="15c3a-117">Validates a username/password pair on the receiver side.</span></span> |



 



| <span data-ttu-id="15c3a-118">Enumeración</span><span class="sxs-lookup"><span data-stu-id="15c3a-118">Enumeration</span></span>                                                                                           | <span data-ttu-id="15c3a-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="15c3a-119">Description</span></span>                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="15c3a-120">**\_tipo de \_ credencial de certificado WS \_**</span><span class="sxs-lookup"><span data-stu-id="15c3a-120">**WS\_CERT\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_cert_credential_type)                                         | <span data-ttu-id="15c3a-121">El tipo de la credencial de certificado.</span><span class="sxs-lookup"><span data-stu-id="15c3a-121">The type of the certificate credential.</span></span>                       |
| [<span data-ttu-id="15c3a-122">**tipo de credencial de WS \_ username \_ \_**</span><span class="sxs-lookup"><span data-stu-id="15c3a-122">**WS\_USERNAME\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_username_credential_type)                                 | <span data-ttu-id="15c3a-123">Tipo de la credencial de nombre de usuario/contraseña.</span><span class="sxs-lookup"><span data-stu-id="15c3a-123">The type of the username/password credential.</span></span>                 |
| [<span data-ttu-id="15c3a-124">**\_tipo de \_ \_ credencial de autenticación integrada \_ \_ de WS Windows**</span><span class="sxs-lookup"><span data-stu-id="15c3a-124">**WS\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_credential_type) | <span data-ttu-id="15c3a-125">El tipo de credencial de autenticación integrada de Windows.</span><span class="sxs-lookup"><span data-stu-id="15c3a-125">The type of the Windows Integrated Authentication credential.</span></span> |



 



| <span data-ttu-id="15c3a-126">Estructura</span><span class="sxs-lookup"><span data-stu-id="15c3a-126">Structure</span></span>                                                                                                   | <span data-ttu-id="15c3a-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="15c3a-127">Description</span></span>                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15c3a-128">**\_credencial de certificado WS \_**</span><span class="sxs-lookup"><span data-stu-id="15c3a-128">**WS\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential)                                                          | <span data-ttu-id="15c3a-129">El tipo base abstracto para todos los tipos de credenciales de certificado.</span><span class="sxs-lookup"><span data-stu-id="15c3a-129">The abstract base type for all certificate credential types.</span></span>                                                          |
| [<span data-ttu-id="15c3a-130">**\_credencial de \_ certificado \_ personalizado de WS**</span><span class="sxs-lookup"><span data-stu-id="15c3a-130">**WS\_CUSTOM\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_cert_credential)                                           | <span data-ttu-id="15c3a-131">Tipo para especificar una credencial de certificado que se va a proporcionar mediante una devolución de llamada a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="15c3a-131">The type for specifying a certificate credential that is to be supplied by a callback to the application.</span></span>             |
| [<span data-ttu-id="15c3a-132">**\_credencial de \_ \_ autenticación integrada \_ de \_ Windows de WS predeterminada**</span><span class="sxs-lookup"><span data-stu-id="15c3a-132">**WS\_DEFAULT\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_default_windows_integrated_auth_credential) | <span data-ttu-id="15c3a-133">Tipo para proporcionar una credencial de autenticación integrada de Windows basada en el token de subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="15c3a-133">Type for supplying a Windows Integrated Authentication credential based on the current thread token.</span></span>                  |
| [<span data-ttu-id="15c3a-134">**\_credencial de \_ autenticación de Windows \_ integrada \_ \_ de WS opaco**</span><span class="sxs-lookup"><span data-stu-id="15c3a-134">**WS\_OPAQUE\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_opaque_windows_integrated_auth_credential)   | <span data-ttu-id="15c3a-135">Escriba para proporcionar una credencial de autenticación integrada de Windows.</span><span class="sxs-lookup"><span data-stu-id="15c3a-135">Type for supplying a Windows Integrated Authentication credential.</span></span>                                                    |
| [<span data-ttu-id="15c3a-136">**\_credencial de \_ nombre de usuario de WS String \_**</span><span class="sxs-lookup"><span data-stu-id="15c3a-136">**WS\_STRING\_USERNAME\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_username_credential)                                   | <span data-ttu-id="15c3a-137">Tipo para proporcionar un par de nombre de usuario y contraseña como cadenas.</span><span class="sxs-lookup"><span data-stu-id="15c3a-137">The type for supplying a username/password pair as strings.</span></span>                                                           |
| [<span data-ttu-id="15c3a-138">**\_credencial de \_ \_ autenticación integrada \_ de Windows de cadena WS \_**</span><span class="sxs-lookup"><span data-stu-id="15c3a-138">**WS\_STRING\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_windows_integrated_auth_credential)   | <span data-ttu-id="15c3a-139">Escriba para proporcionar una credencial de Windows como nombre de usuario, contraseña y cadenas de dominio.</span><span class="sxs-lookup"><span data-stu-id="15c3a-139">Type for supplying a Windows credential as username, password, domain strings.</span></span>                                        |
| [<span data-ttu-id="15c3a-140">**\_credencial de \_ certificado de nombre de firmante de WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="15c3a-140">**WS\_SUBJECT\_NAME\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_subject_name_cert_credential)                              | <span data-ttu-id="15c3a-141">El tipo para especificar una credencial de certificado con el nombre de sujeto del certificado, la ubicación del almacén y el nombre de almacén.</span><span class="sxs-lookup"><span data-stu-id="15c3a-141">The type for specifying a certificate credential using the certificate's subject name, store location and store name.</span></span> |
| [<span data-ttu-id="15c3a-142">**\_credencial de certificado de huella digital de WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="15c3a-142">**WS\_THUMBPRINT\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_thumbprint_cert_credential)                                   | <span data-ttu-id="15c3a-143">Tipo para especificar una credencial de certificado utilizando la huella digital del certificado, la ubicación del almacén y el nombre de almacén.</span><span class="sxs-lookup"><span data-stu-id="15c3a-143">The type for specifying a certificate credential using the certificate's thumbprint, store location and store name.</span></span>   |
| [<span data-ttu-id="15c3a-144">**credencial de WS \_ username \_**</span><span class="sxs-lookup"><span data-stu-id="15c3a-144">**WS\_USERNAME\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)                                                  | <span data-ttu-id="15c3a-145">El tipo base abstracto para todas las credenciales de nombre de usuario y contraseña.</span><span class="sxs-lookup"><span data-stu-id="15c3a-145">The abstract base type for all username/password credentials.</span></span>                                                         |
| [<span data-ttu-id="15c3a-146">**\_credencial de \_ \_ autenticación integrada \_ de WS Windows**</span><span class="sxs-lookup"><span data-stu-id="15c3a-146">**WS\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)                  | <span data-ttu-id="15c3a-147">El tipo base abstracto para todos los tipos de credenciales que se usan con la autenticación integrada de Windows.</span><span class="sxs-lookup"><span data-stu-id="15c3a-147">The abstract base type for all credential types used with Windows Integrated Authentication.</span></span>                          |



 

 

 





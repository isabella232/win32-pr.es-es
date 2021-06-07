---
Description: Las marcas de opción siguientes son compatibles con WinHttpQueryOption y WinHttpSetOption.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Marcas de opción (Winhttp.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: f9ca6b7c74d484a6bcac235b2396b2005c8c3260
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386684"
---
# <a name="option-flags"></a><span data-ttu-id="4b829-103">Marcas de opción</span><span class="sxs-lookup"><span data-stu-id="4b829-103">Option Flags</span></span>

<span data-ttu-id="4b829-104">Las siguientes marcas de opción son compatibles [**con WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) y [**WinHttpSetOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)</span><span class="sxs-lookup"><span data-stu-id="4b829-104">The following option flags are supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span>

<dl> <dt>

<span data-ttu-id="4b829-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**OPCIÓN WINHTTP \_ QUE GARANTIZA DEVOLUCIONES DE LLAMADA SIN \_ \_ \_ \_ BLOQUEO**</span><span class="sxs-lookup"><span data-stu-id="4b829-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-106">El valor predeterminado es FALSE.</span><span class="sxs-lookup"><span data-stu-id="4b829-106">The default is FALSE.</span></span> <span data-ttu-id="4b829-107">Si se establece en TRUE, WinHTTP no garantiza el progreso si la aplicación cliente bloquea las devoluciones de llamada de estado.</span><span class="sxs-lookup"><span data-stu-id="4b829-107">If set to TRUE, WinHTTP does not guarantee progress if status callbacks are blocked by the client application.</span></span>

<span data-ttu-id="4b829-108">La aplicación cliente debe tener especial cuidado para realizar operaciones mínimas dentro de la devolución de llamada sin bloqueo, devolviendo lo antes posible y, en concreto, no debe esperar ninguna llamada WinHTTP posterior.</span><span class="sxs-lookup"><span data-stu-id="4b829-108">The client application must take special care to perform minimal operations within the callback without blocking, returning as quickly as possible, and in particular must not wait for any subsequent WinHTTP calls.</span></span> <span data-ttu-id="4b829-109">Si no sigue estas directrices, es probable que haya un impacto negativo en el rendimiento o que una posible aplicación se desasoye.</span><span class="sxs-lookup"><span data-stu-id="4b829-109">If it does not follow these guidelines, there is likely to be a negative performance impact or a potential application hang.</span></span> <span data-ttu-id="4b829-110">Si se usa de la manera prescrita, esta opción puede mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="4b829-110">If used in the prescribed manner, this option may improve performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**DIRECTIVA DE \_ INICIO DE SESIÓN AUTOMÁTICO DE LA OPCIÓN \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-112">Establece un valor entero largo sin signo que especifica la directiva [de inicio](authentication-in-winhttp.md) de sesión automático con uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4b829-112">Sets an unsigned long integer value that specifies the [Automatic Logon Policy](authentication-in-winhttp.md) with one of the following values.</span></span>

| <span data-ttu-id="4b829-113">Término</span><span class="sxs-lookup"><span data-stu-id="4b829-113">Term</span></span> | <span data-ttu-id="4b829-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b829-114">Description</span></span> |
|-|-|
| <span data-ttu-id="4b829-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>NIVEL DE \_ SEGURIDAD ALTO DE WINHTTP AUTOLOGON \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="4b829-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH</span></span> | <span data-ttu-id="4b829-116">No se usan credenciales predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="4b829-116">Default credentials are not used.</span></span> <span data-ttu-id="4b829-117">Tenga en cuenta que esta marca solo tiene efecto si especifica el servidor por el nombre real de la máquina.</span><span class="sxs-lookup"><span data-stu-id="4b829-117">Note that this flag takes effect only if you specify the server by the actual machine name.</span></span> <span data-ttu-id="4b829-118">No tendrá efecto si especifica el servidor por "localhost" o dirección IP.</span><span class="sxs-lookup"><span data-stu-id="4b829-118">It will not take effect, if you specify the server by "localhost" or IP address.</span></span> |
| <span data-ttu-id="4b829-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>NIVEL DE \_ SEGURIDAD BAJO DE WINHTTP AUTOLOGON \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="4b829-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW</span></span> | <span data-ttu-id="4b829-120">Se realiza un inicio de sesión autenticado con las credenciales predeterminadas para todas las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="4b829-120">An authenticated log on using the default credentials is performed for all requests.</span></span> |
| <span data-ttu-id="4b829-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>MEDIO DE \_ NIVEL DE SEGURIDAD DE WINHTTP AUTOLOGON \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="4b829-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM</span></span> | <span data-ttu-id="4b829-122">Un inicio de sesión autenticado con las credenciales predeterminadas solo se realiza para las solicitudes en la intranet local.</span><span class="sxs-lookup"><span data-stu-id="4b829-122">An authenticated log on using the default credentials is performed only for requests on the local Intranet.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="4b829-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**DEVOLUCIÓN DE LLAMADA \_ DE \_ LA OPCIÓN WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-124">Recupera el puntero al conjunto de funciones de devolución de llamada [**con WinHttpSetStatusCallback.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)</span><span class="sxs-lookup"><span data-stu-id="4b829-124">Retrieves the pointer to the callback function set with [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**CONTEXTO DE CERTIFICADO \_ DE CLIENTE DE LA OPCIÓN \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-126">Establece el contexto del certificado de cliente.</span><span class="sxs-lookup"><span data-stu-id="4b829-126">Sets the client certificate context.</span></span> <span data-ttu-id="4b829-127">Si una aplicación recibe [**ERROR \_ WINHTTP \_ CLIENT \_ AUTH CERT \_ \_ NEEDED**](error-messages.md), debe llamar a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para proporcionar un certificado antes de reintentar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b829-127">If an application receives [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md), it must call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="4b829-128">Como parte del procesamiento de esta opción, WinHttp llama a [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) en el contexto de certificado proporcionado por el autor de la llamada para que el autor de la llamada pueda liberar el contexto del certificado de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="4b829-128">As a part of processing this option, WinHttp calls [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) on the caller-provided certificate context so that the certificate context can be independently released by the caller.</span></span>

> [!Note]
> <span data-ttu-id="4b829-129">La aplicación no debe intentar cerrar el almacén de certificados con la marca CERT CLOSE STORE FORCE FLAG en la llamada a \_ \_ \_ \_ [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) en el almacén de certificados del que se recuperó el contexto del certificado.</span><span class="sxs-lookup"><span data-stu-id="4b829-129">The application should not attempt to close the certificate store with the CERT\_CLOSE\_STORE\_FORCE\_FLAG flag in the call to [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) on the certificate store from which the certificate context was retrieved.</span></span> <span data-ttu-id="4b829-130">Puede producirse una infracción de acceso.</span><span class="sxs-lookup"><span data-stu-id="4b829-130">An access violation may occur.</span></span>

<span data-ttu-id="4b829-131">Cuando el servidor solicita un certificado de cliente, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) devuelve un [**error ERROR \_ WINHTTP CLIENT \_ \_ AUTH CERT \_ \_ NEEDED.**](error-messages.md)</span><span class="sxs-lookup"><span data-stu-id="4b829-131">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md) error.</span></span> <span data-ttu-id="4b829-132">Si el servidor solicita el certificado pero no lo requiere, la aplicación puede especificar esta opción para indicar que no tiene un certificado.</span><span class="sxs-lookup"><span data-stu-id="4b829-132">If the server requests the certificate but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="4b829-133">El servidor puede elegir otro esquema de autenticación o permitir el acceso anónimo al servidor.</span><span class="sxs-lookup"><span data-stu-id="4b829-133">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="4b829-134">La aplicación proporciona la macro **WINHTTP \_ NO CLIENT \_ CERT \_ \_ CONTEXT** en el parámetro *lpBuffer* de [**WinHttpSetOption,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="4b829-134">The application provides the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

<span data-ttu-id="4b829-135">Si el servidor requiere un certificado de cliente, puede enviar un código de estado HTTP 403 en respuesta.</span><span class="sxs-lookup"><span data-stu-id="4b829-135">If the server requires a client certificate, it may send a 403 HTTP status code in response.</span></span> <span data-ttu-id="4b829-136">Para obtener más información, vea la **opción WINHTTP \_ OPTION CLIENT \_ CERT \_ \_ ISSUER \_ LIST.**</span><span class="sxs-lookup"><span data-stu-id="4b829-136">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**LISTA DE \_ \_ EMISORES DE \_ CERTIFICADOS DE CLIENTE DE LA \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-138">Recupera una [**estructura \_ IssuerListInfoEx de SecPkgContext**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) cuando el error de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) es **ERROR \_ WINHTTP CLIENT \_ \_ AUTH CERT \_ \_ NEEDED**.</span><span class="sxs-lookup"><span data-stu-id="4b829-138">Retrieves a [**SecPkgContext\_IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure when the error from [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) is **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="4b829-139">La lista de emisores de la estructura contiene una lista de las autoridades de certificación (CA) aceptables del servidor.</span><span class="sxs-lookup"><span data-stu-id="4b829-139">The issuer list in the structure contains a list of acceptable Certificate Authorities (CA) from the server.</span></span> <span data-ttu-id="4b829-140">La aplicación cliente puede filtrar la lista de ca para recuperar el certificado de cliente para la autenticación SSL.</span><span class="sxs-lookup"><span data-stu-id="4b829-140">The client application can filter the CA list to retrieve the client certificate for SSL authentication.</span></span>

<span data-ttu-id="4b829-141">Como alternativa, si el servidor solicita el certificado de cliente, pero no lo requiere, la aplicación puede llamar a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con la opción **\_ WINHTTP OPTION \_ CLIENT CERT \_ \_ CONTEXT.**</span><span class="sxs-lookup"><span data-stu-id="4b829-141">Alternately, if the server requests the client certificate, but does not require it, the application can call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="4b829-142">Para obtener más información, vea la **opción WINHTTP \_ OPTION CLIENT \_ CERT \_ \_ CONTEXT.**</span><span class="sxs-lookup"><span data-stu-id="4b829-142">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**PÁGINA DE CÓDIGOS \_ DE \_ LA OPCIÓN WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-144">Establece la [*página de códigos*](glossary.md) que se usa para procesar la dirección URL (es decir, cadena de consulta).</span><span class="sxs-lookup"><span data-stu-id="4b829-144">Sets the [*code page*](glossary.md) that is used to process the URL (that is, query string).</span></span> <span data-ttu-id="4b829-145">El valor predeterminado es UTF8.</span><span class="sxs-lookup"><span data-stu-id="4b829-145">The default is UTF8.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**OPCIÓN WINHTTP \_ \_ CONFIGURAR LA \_ \_ AUTENTICACIÓN DE PASSPORT**</span><span class="sxs-lookup"><span data-stu-id="4b829-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-147">Establece un valor entero largo sin signo que especifica si está habilitada la autenticación [de Passport en la autenticación WinHTTP.](passport-authentication-in-winhttp.md)</span><span class="sxs-lookup"><span data-stu-id="4b829-147">Sets an unsigned long integer value that specifies whether [Passport Authentication in WinHTTP](passport-authentication-in-winhttp.md) authentication is enabled.</span></span> <span data-ttu-id="4b829-148">El valor puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="4b829-148">The value can be one of the following:</span></span>

| <span data-ttu-id="4b829-149">Término</span><span class="sxs-lookup"><span data-stu-id="4b829-149">Term</span></span> | <span data-ttu-id="4b829-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b829-150">Description</span></span> |
|-|-|
| <span data-ttu-id="4b829-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP \_ DISABLE \_ PASSPORT \_ AUTH</span><span class="sxs-lookup"><span data-stu-id="4b829-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP\_DISABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="4b829-152">Microsoft Passport autenticación está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="4b829-152">Microsoft Passport authentication is disabled.</span></span> <span data-ttu-id="4b829-153">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4b829-153">This is the default.</span></span> |
| <span data-ttu-id="4b829-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ DISABLE \_ PASSPORT \_ KEYRING</span><span class="sxs-lookup"><span data-stu-id="4b829-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP\_DISABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="4b829-155">El llavero de Passport está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="4b829-155">The Passport keyring is disabled.</span></span> <span data-ttu-id="4b829-156">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4b829-156">This is the default.</span></span> |
| <span data-ttu-id="4b829-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>HABILITACIÓN \_ DE \_ LA AUTENTICACIÓN DE PASSPORT EN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP\_ENABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="4b829-158">La autenticación de Passport está habilitada.</span><span class="sxs-lookup"><span data-stu-id="4b829-158">Passport authentication is enabled.</span></span> |
| <span data-ttu-id="4b829-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ ENABLE \_ PASSPORT \_ KEYRING</span><span class="sxs-lookup"><span data-stu-id="4b829-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP\_ENABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="4b829-160">El llavero de Passport está habilitado.</span><span class="sxs-lookup"><span data-stu-id="4b829-160">The Passport keyring is enabled.</span></span> |

</dl> </dd> <dt>

<span data-ttu-id="4b829-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**REINTENTOS DE \_ CONEXIÓN DE LA OPCIÓN \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-162">Establece o recupera un valor entero largo sin signo que contiene el número de veces queWinHTTP intenta conectarse a un host.</span><span class="sxs-lookup"><span data-stu-id="4b829-162">Sets or retrieves an unsigned long integer value that contains the number of timesWinHTTP attempts to connect to a host.</span></span> <span data-ttu-id="4b829-163">Servicios HTTP de Microsoft Windows (WinHTTP) solo intenta una vez por dirección ip (Protocolo de Internet).</span><span class="sxs-lookup"><span data-stu-id="4b829-163">Microsoft Windows HTTP Services (WinHTTP) only attempts once per Internet Protocol (IP) address.</span></span> <span data-ttu-id="4b829-164">Por ejemplo, si intenta conectarse a un host multihome que tiene 10 direcciones IP y **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** se establece en 7, WinHTTP solo intenta conectarse a las siete primeras direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="4b829-164">For example, if you attempt to connect to a multihomed host that has 10 IP addresses and **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 7, then WinHTTP only attempts to connect to the first seven IP address.</span></span> <span data-ttu-id="4b829-165">Dado el mismo conjunto de 10 direcciones IP, si **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** está establecido en 20, WinHTTP intenta cada una de las 10 solo una vez.</span><span class="sxs-lookup"><span data-stu-id="4b829-165">Given the same set of 10 IP addresses, if **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 20, WinHTTP attempts each of the 10 only once.</span></span> <span data-ttu-id="4b829-166">Si un intento de conexión sigue generando un error después del número especificado de intentos, o si el tiempo de espera de conexión expiró antes, se cancela la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b829-166">If a connection attempt still fails after the specified number of attempts, or if the connect timeout expired before then, the request is canceled.</span></span> <span data-ttu-id="4b829-167">El valor predeterminado de **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** es de cinco intentos.</span><span class="sxs-lookup"><span data-stu-id="4b829-167">The default value for **WINHTTP\_OPTION\_CONNECT\_RETRIES** is five attempts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**TIEMPO DE ESPERA \_ DE CONEXIÓN DE LA OPCIÓN \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-169">Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="4b829-169">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds.</span></span> <span data-ttu-id="4b829-170">Al establecer esta opción en infinito (0xFFFFFFFF) se deshabilitará este temporizador.</span><span class="sxs-lookup"><span data-stu-id="4b829-170">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="4b829-171">Si una solicitud de conexión TCP tarda más tiempo que este valor de tiempo de espera, se cancela la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b829-171">If a TCP connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="4b829-172">El tiempo de espera predeterminado es de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="4b829-172">The default timeout is 60 seconds.</span></span> <span data-ttu-id="4b829-173">Cuando intenta conectarse a varias direcciones IP para un único host (un host de varios locales), el límite de tiempo de espera es para cada conexión individual.</span><span class="sxs-lookup"><span data-stu-id="4b829-173">When you are attempting to connect to multiple IP addresses for a single host (a multihomed host), the timeout limit is for each individual connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**INFORMACIÓN DE CONEXIÓN \_ DE \_ LA OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP\_OPTION\_CONNECTION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-175">Recupera la dirección IP de origen y destino y el puerto de la solicitud que generó la respuesta cuando [**winHttpReceiveResponse vuelve.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)</span><span class="sxs-lookup"><span data-stu-id="4b829-175">Retrieves the source and destination IP address, and port of the request that generated the response when [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns.</span></span> <span data-ttu-id="4b829-176">La aplicación llama [**a WinHttpQueryOption con**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) la opción **WINHTTP OPTION CONNECTION \_ \_ \_ INFO** y proporciona la estructura DE INFORMACIÓN DE CONEXIÓN [**WINHTTP \_ \_**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) en el *parámetro lpBuffer.*</span><span class="sxs-lookup"><span data-stu-id="4b829-176">The application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CONNECTION\_INFO** option, and provides the [**WINHTTP\_CONNECTION\_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) structure in the *lpBuffer* parameter.</span></span> <span data-ttu-id="4b829-177">Para obtener más información, **vea WINHTTP \_ CONNECTION \_ INFO**.</span><span class="sxs-lookup"><span data-stu-id="4b829-177">For more information, see **WINHTTP\_CONNECTION\_INFO**.</span></span>

<span data-ttu-id="4b829-178">**Windows Server 2003 con SP1 y Windows XP con SP2:** Esta marca está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="4b829-178">**Windows Server 2003 with SP1 and Windows XP with SP2:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V0**</span><span class="sxs-lookup"><span data-stu-id="4b829-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V0**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-180">Reenvía la [**estructura TCP \_ INFO \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) para la conexión subyacente utilizada por la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b829-180">Retreives the [**TCP\_INFO\_v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="4b829-181">La estructura devuelta puede contener estadísticas de solicitudes anteriores enviadas a través de la misma conexión.</span><span class="sxs-lookup"><span data-stu-id="4b829-181">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>

> [!Note]
> <span data-ttu-id="4b829-182">Esta opción se ha reemplazado por **WINHTTP \_ OPTION CONNECTION \_ STATS \_ \_ V1**.</span><span class="sxs-lookup"><span data-stu-id="4b829-182">This option has been superseded by **WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1**</span><span class="sxs-lookup"><span data-stu-id="4b829-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-184">Reenvía la [**estructura TCP \_ INFO \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) para la conexión subyacente utilizada por la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b829-184">Retreives the [**TCP\_INFO\_v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="4b829-185">La estructura devuelta puede contener estadísticas de solicitudes anteriores enviadas a través de la misma conexión.</span><span class="sxs-lookup"><span data-stu-id="4b829-185">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**VALOR DE CONTEXTO \_ DE \_ LA OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-187">Establece o recupera un **DWORD \_ PTR** que contiene un puntero al valor de contexto asociado a este [identificador HINTERNET.](hinternet-handles-in-winhttp.md)</span><span class="sxs-lookup"><span data-stu-id="4b829-187">Sets or retrieves a **DWORD\_PTR** that contains a pointer to the context value associated with this [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span> <span data-ttu-id="4b829-188">Se usa el valor almacenado en el búfer y se asigna un nuevo valor a la marca de opción **WINHTTP \_ OPTION CONTEXT \_ \_ VALUE.**</span><span class="sxs-lookup"><span data-stu-id="4b829-188">The value stored in the buffer is used and the **WINHTTP\_OPTION\_CONTEXT\_VALUE** option flag is assigned a new value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**DESCOMPRESIÓN DE \_ LA OPCIÓN WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="4b829-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP\_OPTION\_DECOMPRESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-190">Establece un DWORD de marcas que determinan si WinHTTP descomprime automáticamente los cuerpos de respuesta con codificaciones de contenido comprimidas.</span><span class="sxs-lookup"><span data-stu-id="4b829-190">Sets a DWORD of flags which determine whether WinHTTP will automatically decompress response bodies with compressed Content-Encodings.</span></span> <span data-ttu-id="4b829-191">WinHTTP también establecerá un encabezado de Accept-Encoding adecuado, reemplazando los proporcionados por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="4b829-191">WinHTTP will also set an appropriate Accept-Encoding header, overriding any supplied by the caller.</span></span> <span data-ttu-id="4b829-192">Los valores admitidos son:</span><span class="sxs-lookup"><span data-stu-id="4b829-192">Supported values are:</span></span>

| <span data-ttu-id="4b829-193">Término</span><span class="sxs-lookup"><span data-stu-id="4b829-193">Term</span></span> | <span data-ttu-id="4b829-194">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b829-194">Description</span></span> |
|-|-|
| <span data-ttu-id="4b829-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>MARCA \_ DE DESCOMPRESIÓN \_ \_ WINHTTP GZIP</span><span class="sxs-lookup"><span data-stu-id="4b829-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP\_DECOMPRESSION\_FLAG\_GZIP</span></span> | <span data-ttu-id="4b829-196">Descomprimir Content-Encoding: respuestas gzip.</span><span class="sxs-lookup"><span data-stu-id="4b829-196">Decompress Content-Encoding: gzip responses.</span></span> |
| <span data-ttu-id="4b829-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>DEFLATE DE LA \_ \_ MARCA DE DESCOMPRESIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP\_DECOMPRESSION\_FLAG\_DEFLATE</span></span> | <span data-ttu-id="4b829-198">Descomprimir Content-Encoding: deflate las respuestas.</span><span class="sxs-lookup"><span data-stu-id="4b829-198">Decompress Content-Encoding: deflate responses.</span></span> |
| <span data-ttu-id="4b829-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>MARCA \_ DE DESCOMPRESIÓN WINHTTP \_ \_ ALL</span><span class="sxs-lookup"><span data-stu-id="4b829-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP\_DECOMPRESSION\_FLAG\_ALL</span></span> | <span data-ttu-id="4b829-200">Descomprime las respuestas con cualquier codificación de contenido compatible.</span><span class="sxs-lookup"><span data-stu-id="4b829-200">Decompress responses with any supported Content-Encoding.</span></span> |

<span data-ttu-id="4b829-201">De forma predeterminada, WinHTTP entregará respuestas comprimidas al autor de la llamada sin modificar.</span><span class="sxs-lookup"><span data-stu-id="4b829-201">By default, WinHTTP will deliver compressed responses to the caller unmodified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**CARACTERÍSTICA DESHABILITAR OPCIÓN WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4b829-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP\_OPTION\_DISABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-203">Establece un valor entero largo sin signo que especifica qué características están deshabilitadas con una o varias de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="4b829-203">Sets an unsigned long integer value that specifies which features are disabled with one or more of the following flags.</span></span> <span data-ttu-id="4b829-204">Tenga en cuenta que esta característica solo debe pasarse a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) en los identificadores de solicitud después de crear el identificador de solicitud con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)y antes de que la solicitud se envíe [**con WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="4b829-204">Be aware that this feature should only be passed to [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) on request handles after the request handle is created with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), and before the request is sent with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

| <span data-ttu-id="4b829-205">Término</span><span class="sxs-lookup"><span data-stu-id="4b829-205">Term</span></span> | <span data-ttu-id="4b829-206">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b829-206">Description</span></span> |
|-|-|
| <span data-ttu-id="4b829-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>AUTENTICACIÓN \_ DESHABILITADA DE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP\_DISABLE\_AUTHENTICATION</span></span> | <span data-ttu-id="4b829-208">La autenticación automática está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="4b829-208">Automatic authentication is disabled.</span></span> |
| <span data-ttu-id="4b829-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP \_ DISABLE \_ COOKIES</span><span class="sxs-lookup"><span data-stu-id="4b829-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP\_DISABLE\_COOKIES</span></span> | <span data-ttu-id="4b829-210">La adición automática de encabezados de cookie a las solicitudes está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="4b829-210">Automatic addition of cookie headers to requests is disabled.</span></span> <span data-ttu-id="4b829-211">Además, las cookies devueltas no se agregan automáticamente a la base de datos de cookies.</span><span class="sxs-lookup"><span data-stu-id="4b829-211">Also, returned cookies are not automatically added to the cookie database.</span></span> <span data-ttu-id="4b829-212">Deshabilitar las cookies puede provocar un rendimiento deficiente para la autenticación de Passport.</span><span class="sxs-lookup"><span data-stu-id="4b829-212">Disabling cookies can result in poor performance for Passport authentication.</span></span> |
| <span data-ttu-id="4b829-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP \_ DISABLE \_ KEEP \_ ALIVE</span><span class="sxs-lookup"><span data-stu-id="4b829-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP\_DISABLE\_KEEP\_ALIVE</span></span> | <span data-ttu-id="4b829-214">Deshabilita la semántica de conexión keep-alive para la conexión.</span><span class="sxs-lookup"><span data-stu-id="4b829-214">Disables keep-alive semantics for the connection.</span></span> <span data-ttu-id="4b829-215">La semántica de conexión continua es necesaria para MSN, NTLM y otros tipos de autenticación.</span><span class="sxs-lookup"><span data-stu-id="4b829-215">Keep-alive semantics are required for MSN, NTLM, and other types of authentication.</span></span> |
| <span data-ttu-id="4b829-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>REDIRECCIONAMIENTOS \_ DE DESHABILITACIÓN DE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="4b829-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP\_DISABLE\_REDIRECTS</span></span> | <span data-ttu-id="4b829-217">El redireccionamiento automático está deshabilitado al enviar solicitudes [**con WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="4b829-217">Automatic redirection is disabled when sending requests with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="4b829-218">Si el redireccionamiento automático está deshabilitado, una aplicación debe registrar una función de devolución de llamada para que la autenticación de Passport se haga correctamente.</span><span class="sxs-lookup"><span data-stu-id="4b829-218">If automatic redirection is disabled, an application must register a callback function in order for Passport authentication to succeed.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="4b829-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**OPCIÓN WINHTTP \_ DESHABILITAR LA RESERVA DE PROTOCOLO \_ \_ \_ \_ SEGURO**</span><span class="sxs-lookup"><span data-stu-id="4b829-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-220">Impide que WinHTTP vuelva a intentar una conexión con una versión inferior del protocolo de seguridad cuando se produce un error en la negociación inicial del protocolo.</span><span class="sxs-lookup"><span data-stu-id="4b829-220">Prevents WinHTTP from retrying a connection with a lower version of the security protocol when the initial protocol negotiation fails.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**OPCIÓN WINHTTP \_ DISABLE \_ STREAM \_ \_ QUEUE**</span><span class="sxs-lookup"><span data-stu-id="4b829-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-222">Permite que las nuevas solicitudes abran una conexión HTTP/2 adicional cuando se alcanza el límite máximo de secuencias simultáneas, en lugar de esperar a la siguiente secuencia disponible en una conexión existente.</span><span class="sxs-lookup"><span data-stu-id="4b829-222">Allows new requests to open an additional HTTP/2 connection when the maximum concurrent stream limit is reached, rather than waiting for the next available stream on an existing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**CARACTERÍSTICA HABILITAR OPCIÓN WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4b829-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP\_OPTION\_ENABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-224">Establece un valor entero largo sin signo que especifica las características habilitadas actualmente.</span><span class="sxs-lookup"><span data-stu-id="4b829-224">Sets an unsigned long integer value that specifies the features currently enabled.</span></span> <span data-ttu-id="4b829-225">Puede ser uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="4b829-225">Can be one of the following values.</span></span>

| <span data-ttu-id="4b829-226">Término</span><span class="sxs-lookup"><span data-stu-id="4b829-226">Term</span></span> | <span data-ttu-id="4b829-227">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b829-227">Description</span></span> |
|-|-|
| <span data-ttu-id="4b829-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVERT \_ IMPERSONATION</span><span class="sxs-lookup"><span data-stu-id="4b829-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP\_ENABLE\_SSL\_REVERT\_IMPERSONATION</span></span> | <span data-ttu-id="4b829-229">Si está habilitada, WinHTTP revierte temporalmente la suplantación de cliente mientras duren las operaciones de autenticación de certificados SSL.</span><span class="sxs-lookup"><span data-stu-id="4b829-229">If enabled, WinHTTP temporarily reverts client impersonation for the duration of SSL certificate authentication operations.</span></span> <span data-ttu-id="4b829-230">Este valor solo se puede establecer en el identificador de sesión.</span><span class="sxs-lookup"><span data-stu-id="4b829-230">This value can be set only on the session handle.</span></span> |
| <span data-ttu-id="4b829-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVOCATION</span><span class="sxs-lookup"><span data-stu-id="4b829-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP\_ENABLE\_SSL\_REVOCATION</span></span> | <span data-ttu-id="4b829-232">Si está habilitado, WinHTTP permite la revocación SSL.</span><span class="sxs-lookup"><span data-stu-id="4b829-232">If enabled, WinHTTP allows SSL revocation.</span></span> <span data-ttu-id="4b829-233">Este valor solo se puede establecer en el identificador de solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b829-233">This value can be set only on the request handle.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**OPCIÓN WINHTTP \_ HABILITAR \_ PROTOCOLO \_ \_ HTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-235">Establece una máscara de bits DWORD de versiones HTTP avanzadas aceptables.</span><span class="sxs-lookup"><span data-stu-id="4b829-235">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="4b829-236">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="4b829-236">Possible values are:</span></span>

| <span data-ttu-id="4b829-237">Término</span><span class="sxs-lookup"><span data-stu-id="4b829-237">Term</span></span> | <span data-ttu-id="4b829-238">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b829-238">Description</span></span> |
|-|-|
| <span data-ttu-id="4b829-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>MARCA DE PROTOCOLO WINHTTP \_ \_ \_ HTTP2 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4b829-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP\_PROTOCOL\_FLAG\_HTTP2 (0x1)</span></span> | <span data-ttu-id="4b829-240">Habilita HTTP/2 para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b829-240">Enables HTTP/2 for the request.</span></span> |
| <span data-ttu-id="4b829-241">Ninguno (0x0)</span><span class="sxs-lookup"><span data-stu-id="4b829-241">None (0x0)</span></span> | <span data-ttu-id="4b829-242">Restringe la solicitud a HTTP/1.1 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="4b829-242">Restricts the request to HTTP/1.1 and prior.</span></span> |

<span data-ttu-id="4b829-243">Las versiones heredadas de HTTP (1.1 y anteriores) no se pueden deshabilitar con esta opción.</span><span class="sxs-lookup"><span data-stu-id="4b829-243">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="4b829-244">El valor predeterminado es 0x0.</span><span class="sxs-lookup"><span data-stu-id="4b829-244">The default is 0x0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-245"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**OPCIÓN WINHTTP \_ \_ ENABLETRACING**</span><span class="sxs-lookup"><span data-stu-id="4b829-245"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP\_OPTION\_ENABLETRACING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-246">Establece un **valor BOOL** que especifica si el seguimiento está habilitado actualmente.</span><span class="sxs-lookup"><span data-stu-id="4b829-246">Sets a **BOOL** value that specifies whether tracing is currently enabled.</span></span> <span data-ttu-id="4b829-247">Para obtener más información sobre la instalación de seguimiento en WinHTTP, vea [Instalación de seguimiento winHTTP](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="4b829-247">For more information about the trace facility in WinHTTP, see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span> <span data-ttu-id="4b829-248">Esta opción solo se puede establecer en un **identificador NULL** **HINTERNET.**</span><span class="sxs-lookup"><span data-stu-id="4b829-248">This option can only be set on a **NULL** **HINTERNET** handle.</span></span>


</dt> </dl> </dd>

<dt>

<span data-ttu-id="4b829-249"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**CODIFICACIÓN \_ ADICIONAL DE LA \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-249"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-250">Habilita la codificación de porcentaje de dirección URL para la ruta de acceso y la cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="4b829-250">Enables URL percent encoding for path and query string.</span></span>

<span data-ttu-id="4b829-251">Como alternativa, puede codificar por porcentaje antes de llamar a WinHttp.</span><span class="sxs-lookup"><span data-stu-id="4b829-251">Alternatively, you can percent encode before calling WinHttp.</span></span>

</dt> </dl> </dd>

<dt>

<span data-ttu-id="4b829-252"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**LA OPCIÓN WINHTTP \_ \_ EXPIRA LA \_ CONEXIÓN**</span><span class="sxs-lookup"><span data-stu-id="4b829-252"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP\_OPTION\_EXPIRE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-253">Esta opción solo se puede establecer en un identificador de solicitud que sigue activo (enviando o recibiendo).</span><span class="sxs-lookup"><span data-stu-id="4b829-253">This option can only be set on a request handle which is still active (sending or receiving).</span></span> <span data-ttu-id="4b829-254">Al establecer esta opción se le pedirá a WinHttp que deje de atender solicitudes en la conexión asociada con el identificador de solicitud pasado.</span><span class="sxs-lookup"><span data-stu-id="4b829-254">Setting this option will tell WinHttp to stop serving requests on the connection associated with the request handle passed in.</span></span> <span data-ttu-id="4b829-255">La conexión se cerrará una vez completado el identificador de solicitud con el que se llama a esta opción.</span><span class="sxs-lookup"><span data-stu-id="4b829-255">The connection will be closed after the request handle this option is called with is completed.</span></span> <span data-ttu-id="4b829-256">Esta opción no toma ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="4b829-256">This option does not take any parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-257"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**ERROR EXTENDIDO DE LA OPCIÓN WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4b829-257"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-258">Recupera un valor entero largo sin signo que contiene un código de error de Microsoft Windows Sockets que se asignó a los mensajes de error ERROR WINHTTP devueltos por última vez en este \_ \_ \* contexto de subproceso.</span><span class="sxs-lookup"><span data-stu-id="4b829-258">Retrieves an unsigned long integer value that contains a Microsoft Windows Sockets error code that was mapped to the ERROR\_WINHTTP\_\* error messages last returned in this thread context.</span></span> <span data-ttu-id="4b829-259">Puede pasar **NULL como** valor de identificador.</span><span class="sxs-lookup"><span data-stu-id="4b829-259">You can pass **NULL** as the handle value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-260"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**\_CREDS DE PROXY GLOBAL DE LA OPCIÓN \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-260"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-261">Toma un puntero a una [**estructura DE WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) con el parámetro de función *hInternet* establecido en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="4b829-261">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="4b829-262">Esta opción requiere la clave del Registro **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="4b829-262">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="4b829-263">Si no se establece esta clave del Registro, WinHTTP devolverá **el error ERROR \_ WINHTTP INVALID \_ \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="4b829-263">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="4b829-264">Esta clave del Registro no está presente de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4b829-264">This registry key is not present by default.</span></span> <span data-ttu-id="4b829-265">Cuando se establece, WinINet enviará las credenciales a WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="4b829-265">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="4b829-266">Cada vez que WinHttp obtiene un desafío de autenticación y no hay ninguna credencial establecida en el identificador actual, usará las credenciales proporcionadas por WinINet.</span><span class="sxs-lookup"><span data-stu-id="4b829-266">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="4b829-267">Para compartir las credenciales del servidor además de las credenciales de proxy, los usuarios deben establecer **LA OPCIÓN WINHTTP \_ USAR CREDENCIALES DE SERVIDOR \_ \_ \_ \_ GLOBAL** .</span><span class="sxs-lookup"><span data-stu-id="4b829-267">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-268"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**\_CREDS DE SERVIDOR GLOBAL DE LA OPCIÓN \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-268"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-269">Toma un puntero a una [**estructura DE WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) con el parámetro de función *hInternet* establecido en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="4b829-269">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="4b829-270">Esta opción requiere la clave del Registro **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="4b829-270">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="4b829-271">Si no se establece esta clave del Registro, WinHTTP devolverá **el error ERROR \_ WINHTTP INVALID \_ \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="4b829-271">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="4b829-272">Esta clave del Registro no está presente de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4b829-272">This registry key is not present by default.</span></span> <span data-ttu-id="4b829-273">Cuando se establece, WinINet enviará las credenciales a WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="4b829-273">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="4b829-274">Cada vez que WinHttp obtiene un desafío de autenticación y no hay ninguna credencial establecida en el identificador actual, usará las credenciales proporcionadas por WinINet.</span><span class="sxs-lookup"><span data-stu-id="4b829-274">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="4b829-275">Para compartir las credenciales del servidor además de las credenciales de proxy, los usuarios deben establecer **LA OPCIÓN WINHTTP \_ USAR CREDENCIALES DE SERVIDOR \_ \_ \_ \_ GLOBAL** .</span><span class="sxs-lookup"><span data-stu-id="4b829-275">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-276"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**TIPO DE IDENTIFICADOR \_ DE \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-276"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-277">Recupera un valor entero largo sin signo que contiene el tipo del identificador [HINTERNET](hinternet-handles-in-winhttp.md) pasado.</span><span class="sxs-lookup"><span data-stu-id="4b829-277">Retrieves an unsigned long integer value that contains the type of the [HINTERNET](hinternet-handles-in-winhttp.md) handle passed in.</span></span> <span data-ttu-id="4b829-278">El valor devuelto puede ser cualquiera de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="4b829-278">The return value can be one of the following:</span></span>

| <span data-ttu-id="4b829-279">Término</span><span class="sxs-lookup"><span data-stu-id="4b829-279">Term</span></span> | <span data-ttu-id="4b829-280">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b829-280">Description</span></span> |
|-|-|
| <span data-ttu-id="4b829-281"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP \_ HANDLE \_ TYPE \_ CONNECT</span><span class="sxs-lookup"><span data-stu-id="4b829-281"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP\_HANDLE\_TYPE\_CONNECT</span></span> | <span data-ttu-id="4b829-282">El identificador es un identificador de conexión.</span><span class="sxs-lookup"><span data-stu-id="4b829-282">The handle is a connection handle.</span></span> |
| <span data-ttu-id="4b829-283"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>SOLICITUD DE TIPO \_ DE \_ IDENTIFICADOR \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-283"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP\_HANDLE\_TYPE\_REQUEST</span></span> | <span data-ttu-id="4b829-284">El identificador es un identificador de solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b829-284">The handle is a request handle.</span></span> |
| <span data-ttu-id="4b829-285"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>SESIÓN DE TIPO \_ DE \_ IDENTIFICADOR \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-285"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP\_HANDLE\_TYPE\_SESSION</span></span> | <span data-ttu-id="4b829-286">El identificador es un identificador de sesión.</span><span class="sxs-lookup"><span data-stu-id="4b829-286">The handle is a session handle.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="4b829-287"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**SE REQUIERE EL PROTOCOLO HTTP DE \_ \_ LA OPCIÓN \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-287"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-288">Impide que se utilicen versiones de protocolo distintas de las habilitadas **por WINHTTP \_ OPTION ENABLE \_ HTTP \_ \_ PROTOCOL** para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b829-288">Prevents protocol versions other than those enabled by **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL** from being used for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-289"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**OPCIÓN WINHTTP \_ \_ PROTOCOLO HTTP \_ \_ USADO**</span><span class="sxs-lookup"><span data-stu-id="4b829-289"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-290">Obtiene un DWORD que indica qué versión avanzada de HTTP se usó en una solicitud determinada.</span><span class="sxs-lookup"><span data-stu-id="4b829-290">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="4b829-291">Para obtener una lista de los valores posibles, **vea WINHTTP \_ OPTION ENABLE \_ HTTP \_ \_ PROTOCOL**.</span><span class="sxs-lookup"><span data-stu-id="4b829-291">For a list of possible values, see **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-292"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**VERSIÓN HTTP DE \_ LA OPCIÓN \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-292"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-293">Establece o recupera una estructura [**HTTP \_ VERSION \_ INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) que contiene la versión HTTP que se admite.</span><span class="sxs-lookup"><span data-stu-id="4b829-293">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) structure that contains the HTTP version being supported.</span></span> <span data-ttu-id="4b829-294">Se trata de una opción para todo el proceso; use **NULL** para el identificador.</span><span class="sxs-lookup"><span data-stu-id="4b829-294">This is a process-wide option; use **NULL** for the handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-295"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**OPCIÓN WINHTTP \_ OMITIR \_ \_ REVOCACIÓN \_ DE CERTIFICADOS \_ SIN CONEXIÓN**</span><span class="sxs-lookup"><span data-stu-id="4b829-295"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-296">Permite que las conexiones seguras usen certificados de seguridad para los que no se pudo descargar la lista de revocación de certificados.</span><span class="sxs-lookup"><span data-stu-id="4b829-296">Allows secure connections to use security certificates for which the certificate revocation list could not be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-297"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**OPCIÓN WINHTTP \_ \_ IPV6 \_ FAST \_ FALLBACK**</span><span class="sxs-lookup"><span data-stu-id="4b829-297"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-298">Habilita la reserva rápida IPv6 (eyeballs desapedachas) para la conexión.</span><span class="sxs-lookup"><span data-stu-id="4b829-298">Enables IPv6 fast fallback (Happier Eyeballs) for the connection.</span></span> <span data-ttu-id="4b829-299">Este comportamiento es similar al comportamiento de Happy Eyeballs descrito en [RFC 6555](https://tools.ietf.org/html/rfc6555) para mejorar los tiempos de conexión en redes donde IPv6 no es confiable.</span><span class="sxs-lookup"><span data-stu-id="4b829-299">This behavior is similar to the Happy Eyeballs behavior described in [RFC 6555](https://tools.ietf.org/html/rfc6555) for improving connection times on networks where IPv6 is unreliable.</span></span>
- <span data-ttu-id="4b829-300">Si las direcciones IPv6 e IPv4 se resuelven para un host determinado, WinHttp comenzará conectándose a la primera dirección IPv6 resuelta con un tiempo de espera corto (300 ms).</span><span class="sxs-lookup"><span data-stu-id="4b829-300">If both IPv6 and IPv4 addresses are resolved for a given host, WinHttp will begin by connecting to the first resolved IPv6 address with a short (300ms) timeout.</span></span>
- <span data-ttu-id="4b829-301">Si se producirá un error en la conexión, WinHttp intentará conectarse a la primera dirección IPv4 resuelta con el tiempo de espera estándar.</span><span class="sxs-lookup"><span data-stu-id="4b829-301">Should that connection fail, WinHttp will attempt to connect to the first resolved IPv4 address with the standard timeout.</span></span>
- <span data-ttu-id="4b829-302">Si se producirá un error en la segunda conexión, WinHttp volverá a intentar la primera dirección IPv6 resuelta con el tiempo de espera estándar.</span><span class="sxs-lookup"><span data-stu-id="4b829-302">Should the second connection fail, WinHttp will retry the first resolved IPv6 address with the standard timeout.</span></span>
- <span data-ttu-id="4b829-303">Si se producirá un error en la tercera conexión, WinHttp revertirá al comportamiento predeterminado de las direcciones restantes, intentando una conexión a cada una con el tiempo de espera estándar hasta que se establece una conexión o no quedan direcciones.</span><span class="sxs-lookup"><span data-stu-id="4b829-303">Should the third connection fail, WinHttp will revert to the default behavior for any remaining addresses, attempting a connection to each one with the standard timeout until a connection is made or no addresses remain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-304"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**LA OPCIÓN WINHTTP \_ ES RESPUESTA DE CONEXIÓN DE \_ \_ \_ \_ PROXY**</span><span class="sxs-lookup"><span data-stu-id="4b829-304"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-305">Obtiene si se puede recuperar o no una respuesta de conexión de devolución de proxy.</span><span class="sxs-lookup"><span data-stu-id="4b829-305">Gets whether or not a Proxy Return Connect Response can be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-306"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**OPCIÓN WINHTTP \_ \_ NÚMERO MÁXIMO DE \_ CONN POR \_ \_ 1 \_ SERVIDOR 0 \_**</span><span class="sxs-lookup"><span data-stu-id="4b829-306"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-307">Establece o recupera un valor entero largo sin signo que contiene el número máximo de conexiones permitidas por servidor HTTP/1.0.</span><span class="sxs-lookup"><span data-stu-id="4b829-307">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="4b829-308">El valor predeterminado es **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="4b829-308">The default value is **INFINITE**.</span></span>

<span data-ttu-id="4b829-309">**Windows Vista con SP1 y Windows Server 2008:** Esta marca está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="4b829-309">**Windows Vista with SP1 and Windows Server 2008:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-310"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**OPCIÓN WINHTTP \_ \_ NÚMERO MÁXIMO DE \_ CONN POR \_ \_ SERVIDOR**</span><span class="sxs-lookup"><span data-stu-id="4b829-310"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-311">Establece o recupera un valor entero largo sin signo que contiene el número máximo de conexiones permitidas por servidor.</span><span class="sxs-lookup"><span data-stu-id="4b829-311">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="4b829-312">El valor predeterminado es **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="4b829-312">The default value is **INFINITE**.</span></span>

<span data-ttu-id="4b829-313">Cuando esta opción se establece en cero, WinHTTP establece el límite en el número de conexiones en 2.</span><span class="sxs-lookup"><span data-stu-id="4b829-313">When this option is set to zero, WinHTTP sets the limit on the number of connections to 2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-314"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**OPCIÓN WINHTTP \_ \_ MAX HTTP AUTOMATIC \_ \_ \_ REDIRECTS**</span><span class="sxs-lookup"><span data-stu-id="4b829-314"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-315">Establece el número máximo de redirecciones que sigue WinHTTP; el valor predeterminado es 10.</span><span class="sxs-lookup"><span data-stu-id="4b829-315">Sets the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="4b829-316">Este límite impide que sitios no autorizados haga que el cliente WinHTTP se ponga en pausa después de un gran número de redirecciones.</span><span class="sxs-lookup"><span data-stu-id="4b829-316">This limit prevents unauthorized sites from making the WinHTTP client pause following a large number of redirects.</span></span>

<span data-ttu-id="4b829-317">**Windows XP con SP1 y Windows 2000 con SP3:** Esta marca está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="4b829-317">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-318"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**OPCIÓN WINHTTP \_ \_ MAX HTTP STATUS \_ \_ \_ CONTINUE**</span><span class="sxs-lookup"><span data-stu-id="4b829-318"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-319">Número máximo de respuestas de código de estado informativo 100-199 omitido antes de devolver el código de estado final al cliente WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="4b829-319">The maximum number of Informational 100-199 status code responses ignored before returning the final status code to the WinHTTP client.</span></span> <span data-ttu-id="4b829-320">El servidor puede enviar códigos de estado informativos 100-199 antes del código de estado final y se describen en la especificación de HTTP/1.1 (para obtener más información, vea [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span><span class="sxs-lookup"><span data-stu-id="4b829-320">Informational 100-199 status codes can be sent by the server before the final status code, and are described in the specification for HTTP/1.1 (for more information, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span></span> <span data-ttu-id="4b829-321">El valor predeterminado es 10.</span><span class="sxs-lookup"><span data-stu-id="4b829-321">The default is 10.</span></span>

<span data-ttu-id="4b829-322">**Windows XP con SP1 y Windows 2000 con SP3:** Esta marca está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="4b829-322">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-323"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**TAMAÑO MÁXIMO DE PURGA DE RESPUESTA DE LA \_ \_ \_ \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-323"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-324">Enlazado a la cantidad de datos que se purgan de las respuestas para reutilizar una conexión, especificada en bytes.</span><span class="sxs-lookup"><span data-stu-id="4b829-324">A bound on the amount of data drained from responses in order to reuse a connection, specified in bytes.</span></span> <span data-ttu-id="4b829-325">El valor predeterminado es 1 MB.</span><span class="sxs-lookup"><span data-stu-id="4b829-325">The default is 1MB.</span></span>

<span data-ttu-id="4b829-326">**Windows XP con SP1 y Windows 2000 con SP3:** Esta marca está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="4b829-326">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-327"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**TAMAÑO MÁXIMO \_ DE ENCABEZADO DE RESPUESTA DE LA \_ \_ \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-327"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-328">Un conjunto enlazado en el tamaño máximo de la parte de encabezado de la respuesta del servidor, especificado en bytes.</span><span class="sxs-lookup"><span data-stu-id="4b829-328">A bound set on the maximum size of the header portion of the server response, specified in bytes.</span></span> <span data-ttu-id="4b829-329">Este límite protege al cliente de un servidor no autorizado que intenta detener el cliente mediante el envío de una respuesta con una cantidad infinita de datos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="4b829-329">This bound protects the client from an unauthorized server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="4b829-330">El valor predeterminado es 64 KB.</span><span class="sxs-lookup"><span data-stu-id="4b829-330">The default value is 64KB.</span></span>

<span data-ttu-id="4b829-331">**Windows XP con SP1 y Windows 2000 con SP3:** Esta marca está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="4b829-331">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-332"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**IDENTIFICADOR PRIMARIO DE \_ LA \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-332"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-333">Recupera el identificador primario de este identificador.</span><span class="sxs-lookup"><span data-stu-id="4b829-333">Retrieves the parent handle to this handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-334"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**TEXTO DE MARCA DE PASSPORT DE LA \_ \_ \_ OPCIÓN WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="4b829-334"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-335">Recupera una cadena que contiene el texto [*de marca*](glossary.md) de marca proporcionado por el servidor de inicio de sesión de Passport.</span><span class="sxs-lookup"><span data-stu-id="4b829-335">Retrieves a string that contains the [*cobranding*](glossary.md) text provided by the Passport logon server.</span></span> <span data-ttu-id="4b829-336">Esta opción debe recuperarse inmediatamente después de que el servidor de inicio de sesión responda con un código de estado 401.</span><span class="sxs-lookup"><span data-stu-id="4b829-336">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="4b829-337">Una aplicación debe pasar un tamaño de búfer, en bytes, lo suficientemente grande como para contener la cadena devuelta.</span><span class="sxs-lookup"><span data-stu-id="4b829-337">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-338"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**DIRECCIÓN URL DE \_ \_ COBRANDING DE LA OPCIÓN WINHTTP PASSPORT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4b829-338"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-339">Recupera una cadena que contiene una dirección URL para un [*gráfico de marca*](glossary.md) de marca proporcionado por el servidor de inicio de sesión de Passport.</span><span class="sxs-lookup"><span data-stu-id="4b829-339">Retrieves a string that contains a URL for a [*cobranding*](glossary.md) graphic provided by the Passport logon server.</span></span> <span data-ttu-id="4b829-340">Esta opción debe recuperarse inmediatamente después de que el servidor de inicio de sesión responda con un código de estado 401.</span><span class="sxs-lookup"><span data-stu-id="4b829-340">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="4b829-341">Una aplicación debe pasar un tamaño de búfer, en bytes, lo suficientemente grande como para contener la cadena devuelta.</span><span class="sxs-lookup"><span data-stu-id="4b829-341">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-342"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**DIRECCIÓN URL DE \_ RETORNO DE PASSPORT DE LA \_ OPCIÓN WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4b829-342"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-343">Establece una opción de solo lectura en un identificador de solicitud que recupera la dirección URL de devolución de Passport.</span><span class="sxs-lookup"><span data-stu-id="4b829-343">Sets a read-only option on a request handle that retrieves the Passport return URL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-344"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**OPCIÓN WINHTTP \_ \_ PASSPORT SIGN \_ \_ OUT**</span><span class="sxs-lookup"><span data-stu-id="4b829-344"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-345">Establece la opción en un identificador de sesión para cerrar la sesión de los inicios de sesión de Passport.</span><span class="sxs-lookup"><span data-stu-id="4b829-345">Sets the option on a session handle to sign out of any Passport logins.</span></span> <span data-ttu-id="4b829-346">Una aplicación debe pasar la dirección URL de devolución de Passport que se recuperó con **WINHTTP \_ OPTION PASSPORT RETURN \_ \_ \_ URL**.</span><span class="sxs-lookup"><span data-stu-id="4b829-346">An application should pass in the Passport return URL that was retrieved with **WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**.</span></span> <span data-ttu-id="4b829-347">Se borran todas las cookies relacionadas con la dirección URL de devolución.</span><span class="sxs-lookup"><span data-stu-id="4b829-347">All cookies related to the return URL are cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-348"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**CONTRASEÑA DE LA OPCIÓN WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4b829-348"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-349">Establece o recupera un valor de cadena que contiene la contraseña asociada a un identificador de solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b829-349">Sets or retrieves a string value that contains the password associated with a request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-350"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**PROXY DE \_ OPCIÓN WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="4b829-350"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-351">Establece o recupera una estructura [**DE INFORMACIÓN DE \_ PROXY \_ WINHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) que contiene los datos de proxy en un identificador de sesión o identificador de solicitud existente.</span><span class="sxs-lookup"><span data-stu-id="4b829-351">Sets or retrieves an [**WINHTTP\_PROXY\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) structure that contains the proxy data on an existing session handle or request handle.</span></span> <span data-ttu-id="4b829-352">Al recuperar datos de proxy, una aplicación debe liberar las **cadenas lpszProxy** y **lpszProxyBypass** contenidas en esta estructura (si no son **NULL)** mediante la [**función GlobalFree.**](/windows/desktop/api/winbase/nf-winbase-globalfree)</span><span class="sxs-lookup"><span data-stu-id="4b829-352">When retrieving proxy data, an application must free the **lpszProxy** and **lpszProxyBypass** strings contained in this structure (if they are non-**NULL**) using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="4b829-353">Una aplicación puede consultar los datos del proxy global (el proxy predeterminado) pasando un **identificador NULL.**</span><span class="sxs-lookup"><span data-stu-id="4b829-353">An application can query for the global proxy data (the default proxy) by passing a **NULL** handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-354"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**CONTRASEÑA DE \_ PROXY DE \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-354"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-355">Establece o recupera un valor de cadena que contiene la contraseña usada para acceder al proxy.</span><span class="sxs-lookup"><span data-stu-id="4b829-355">Sets or retrieves a string value that contains the password used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-356"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**SPN DE \_ \_ PROXY DE OPCIÓN \_ WINHTTP \_ USADO**</span><span class="sxs-lookup"><span data-stu-id="4b829-356"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**WINHTTP\_OPTION\_PROXY\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-357">Obtiene el nombre principal del servidor proxy que WinHTTP proporcionó a SSPI durante la autenticación.</span><span class="sxs-lookup"><span data-stu-id="4b829-357">Gets the proxy Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="4b829-358">Este valor de cadena se usa para pasar a [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) después de un error de autenticación.</span><span class="sxs-lookup"><span data-stu-id="4b829-358">This string value is usefor passing to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-359"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**NOMBRE DE USUARIO \_ DEL PROXY DE OPCIÓN \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-359"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-360">Establece o recupera un valor de cadena que contiene el nombre de usuario utilizado para acceder al proxy.</span><span class="sxs-lookup"><span data-stu-id="4b829-360">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-361"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**TAMAÑO DEL BÚFER \_ DE LECTURA DE LA \_ \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-361"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-362">Esta opción está en desuso; no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="4b829-362">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-363"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**RESPUESTA DE \_ CONEXIÓN DEL PROXY DE RECEPCIÓN DE LA OPCIÓN \_ \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-363"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-364">Establece si se puede recuperar o no la entidad de respuesta del proxy.</span><span class="sxs-lookup"><span data-stu-id="4b829-364">Sets whether or not the proxy response entity can be retrieved.</span></span> <span data-ttu-id="4b829-365">Esta opción está deshabilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4b829-365">This option is disabled by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-366"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**TIEMPO DE ESPERA \_ DE RESPUESTA DE RECEPCIÓN DE LA OPCIÓN \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-366"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-367">Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, para esperar a recibir todos los encabezados de respuesta a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b829-367">Sets or retrieves an unsigned long integer value that contains the timeout value, in milliseconds, to wait to receive all response headers to a request.</span></span> <span data-ttu-id="4b829-368">Si WinHTTP no recibe todos los encabezados dentro de este período de tiempo de espera, se cancela la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b829-368">If WinHTTP fails to receive all the headers within this timeout period, the request is canceled.</span></span> <span data-ttu-id="4b829-369">El valor de tiempo de espera predeterminado es de 90 segundos.</span><span class="sxs-lookup"><span data-stu-id="4b829-369">The default timeout value is 90 seconds.</span></span>

<span data-ttu-id="4b829-370">Este tiempo de espera solo se comprueba cuando se reciben datos del socket.</span><span class="sxs-lookup"><span data-stu-id="4b829-370">This timeout is checked only when data is received from the socket.</span></span> <span data-ttu-id="4b829-371">Como resultado, cuando expira el tiempo de espera, la aplicación cliente no se notifica hasta que llegan más datos del servidor.</span><span class="sxs-lookup"><span data-stu-id="4b829-371">As a result, when the timeout expires the client application is not notified until more data arrives from the server.</span></span> <span data-ttu-id="4b829-372">Si no llegan datos del servidor, el retraso entre la expiración del tiempo de espera y la notificación de la aplicación cliente podría ser tan grande como el valor de tiempo de espera establecido mediante el parámetro *dwReceiveTimeout* de la función [**WinHttpSetTimeouts.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)</span><span class="sxs-lookup"><span data-stu-id="4b829-372">If no data arrives from the server, the delay between the timeout expiration and notification of the client application could be as large as the timeout value set using the *dwReceiveTimeout* parameter of the [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-373"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**TIEMPO DE ESPERA \_ DE RECEPCIÓN DE LA OPCIÓN \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-373"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-374">Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, para recibir una respuesta parcial a una solicitud o leer algunos datos.</span><span class="sxs-lookup"><span data-stu-id="4b829-374">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a partial response to a request or read some data.</span></span> <span data-ttu-id="4b829-375">Si la respuesta tarda más tiempo que este valor de tiempo de espera, se cancela la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b829-375">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="4b829-376">El valor predeterminado del tiempo de espera es de 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="4b829-376">The default timeout value is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-377"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**DIRECTIVA DE REDIRECCIÓN \_ DE \_ OPCIONES \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-377"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP\_OPTION\_REDIRECT\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-378">Establece el comportamiento de WinHTTP con respecto al control de un código de estado de redireccionamiento HTTP 30 veces mayor.</span><span class="sxs-lookup"><span data-stu-id="4b829-378">Sets the behavior of WinHTTP regarding the handling of a 30x HTTP redirect status code.</span></span> <span data-ttu-id="4b829-379">Esta opción se puede establecer en un identificador de sesión o solicitud en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="4b829-379">This option can be set on a session or request handle to one of the following values:</span></span>

| <span data-ttu-id="4b829-380">Término</span><span class="sxs-lookup"><span data-stu-id="4b829-380">Term</span></span> | <span data-ttu-id="4b829-381">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b829-381">Description</span></span> |
|-|-|
| <span data-ttu-id="4b829-382"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>DIRECTIVA DE REDIRECCIÓN \_ DE \_ OPCIONES WINHTTP \_ \_ SIEMPRE</span><span class="sxs-lookup"><span data-stu-id="4b829-382"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_ALWAYS</span></span> | <span data-ttu-id="4b829-383">Todas las redirecciones se siguen automáticamente.</span><span class="sxs-lookup"><span data-stu-id="4b829-383">All redirects are followed automatically.</span></span> |
| <span data-ttu-id="4b829-384"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>DIRECTIVA DE REDIRECCIÓN \_ DE \_ OPCIONES WINHTTP NO PERMITE HTTPS \_ A \_ \_ \_ \_ HTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-384"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_DISALLOW\_HTTPS\_TO\_HTTP</span></span> | <span data-ttu-id="4b829-385">Se siguen todas las redirecciones, excepto las que se originan desde una dirección URL segura (https) a una dirección URL no segura (http).</span><span class="sxs-lookup"><span data-stu-id="4b829-385">All redirects are followed, except those that originate from a secure (https) URL to an unsecure (http) URL.</span></span> <span data-ttu-id="4b829-386">Esta es la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4b829-386">This is the default setting.</span></span> |
| <span data-ttu-id="4b829-387"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>DIRECTIVA DE REDIRECCIÓN \_ DE \_ OPCIONES WINHTTP \_ \_ NUNCA</span><span class="sxs-lookup"><span data-stu-id="4b829-387"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_NEVER</span></span> | <span data-ttu-id="4b829-388">Los redireccionamientos nunca se siguen.</span><span class="sxs-lookup"><span data-stu-id="4b829-388">Redirects are never followed.</span></span> <span data-ttu-id="4b829-389">El estado 30x se devuelve a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b829-389">The 30x status is returned to the application.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-390"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**OPCIÓN WINHTTP \_ \_ REJECT \_ USERPWD \_ IN \_ URL**</span><span class="sxs-lookup"><span data-stu-id="4b829-390"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-391">Rechaza las direcciones URL que contienen un nombre de usuario y una contraseña.</span><span class="sxs-lookup"><span data-stu-id="4b829-391">Rejects URLs that contain a username and password.</span></span> <span data-ttu-id="4b829-392">Esta opción también rechaza las direcciones URL que contienen semántica *username:password,* incluso si no se especifica ningún nombre de usuario o contraseña.</span><span class="sxs-lookup"><span data-stu-id="4b829-392">This option also rejects URLs that contain *username:password* semantics, even if no username or password is specified.</span></span> <span data-ttu-id="4b829-393">Por ejemplo, " u:p@hostname ", " ", " " " y :@hostname " " " se u:@hostname :p@hostname marcarán como no válidos.</span><span class="sxs-lookup"><span data-stu-id="4b829-393">For example, "u:p@hostname", ":@hostname", "u:@hostname", and ":p@hostname" would all be flagged as invalid.</span></span> <span data-ttu-id="4b829-394">Si se pasa una dirección URL no válida a la función, devuelve [ERROR \_ WINHTTP \_ INVALID \_ URL](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="4b829-394">If an invalid URL is passed to the function, it returns [ERROR\_WINHTTP\_INVALID\_URL](error-messages.md).</span></span> <span data-ttu-id="4b829-395">Esta opción está desactivada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4b829-395">This option is turned off by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-396"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**PRIORIDAD DE \_ SOLICITUD DE LA OPCIÓN \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-396"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-397">Esta opción está en desuso; no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="4b829-397">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-398"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**ESTADÍSTICAS DE \_ SOLICITUD DE LA OPCIÓN \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-398"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP\_OPTION\_REQUEST\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-399">Retraive las estadísticas de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b829-399">Retreives statistics for the request.</span></span>  <span data-ttu-id="4b829-400">Para obtener una lista de las estadísticas disponibles, [**vea \_ ESTADÍSTICAS DE SOLICITUDES \_ WINHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span><span class="sxs-lookup"><span data-stu-id="4b829-400">For a list of the available statistics, see [**WINHTTP\_REQUEST\_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-401"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**TIEMPOS DE SOLICITUD \_ DE \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-401"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP\_OPTION\_REQUEST\_TIMES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-402">Retraive la información de tiempo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b829-402">Retreives timing information for the request.</span></span> <span data-ttu-id="4b829-403">Para obtener una lista de los intervalos disponibles, [**vea WINHTTP \_ REQUEST \_ TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span><span class="sxs-lookup"><span data-stu-id="4b829-403">For a list of the available timings, see [**WINHTTP\_REQUEST\_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-404"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**OPCIÓN WINHTTP \_ RESOLVER \_ TIEMPO DE \_ ESPERA**</span><span class="sxs-lookup"><span data-stu-id="4b829-404"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP\_OPTION\_RESOLVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-405">Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, para resolver un nombre de host.</span><span class="sxs-lookup"><span data-stu-id="4b829-405">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to resolve a host name.</span></span> <span data-ttu-id="4b829-406">El valor de tiempo de espera predeterminado **es INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="4b829-406">The default timeout value is **INFINITE**.</span></span> <span data-ttu-id="4b829-407">Si se especifica un valor no predeterminado, hay una sobrecarga de una creación de subprocesos por resolución de nombre.</span><span class="sxs-lookup"><span data-stu-id="4b829-407">If a non-default value is specified, there is an overhead of one thread-creation per name resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-408"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**PROTOCOLOS SEGUROS \_ DE \_ LA OPCIÓN WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="4b829-408"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP\_OPTION\_SECURE\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-409">Establece un valor entero largo sin signo que especifica qué protocolos seguros son aceptables.</span><span class="sxs-lookup"><span data-stu-id="4b829-409">Sets an unsigned long integer value that specifies which secure protocols are acceptable.</span></span> <span data-ttu-id="4b829-410">De forma predeterminada, solo SSL3 y TLS1 están habilitados en Windows 7 y Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4b829-410">By default only SSL3 and TLS1 are enabled in Windows 7 and Windows 8.</span></span> <span data-ttu-id="4b829-411">De forma predeterminada, solo SSL3, TLS1.0, TLS1.1 y TLS1.2 están habilitados en Windows 8.1 y Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4b829-411">By default only SSL3, TLS1.0, TLS1.1, and TLS1.2 are enabled in Windows 8.1 and Windows 10.</span></span> <span data-ttu-id="4b829-412">El valor puede ser una combinación de uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4b829-412">The value can be a combination of one or more of the following values.</span></span>

| <span data-ttu-id="4b829-413">Término</span><span class="sxs-lookup"><span data-stu-id="4b829-413">Term</span></span> | <span data-ttu-id="4b829-414">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b829-414">Description</span></span> |
|-|-|
| <span data-ttu-id="4b829-415"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>PROTOCOLO SEGURO DE MARCA WINHTTP \_ \_ \_ \_ ALL</span><span class="sxs-lookup"><span data-stu-id="4b829-415"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_ALL</span></span> | <span data-ttu-id="4b829-416">Se pueden Capa de sockets seguros (SSL) 2.0, SSL 3.0 y seguridad de la capa de transporte (TLS) 1.0.</span><span class="sxs-lookup"><span data-stu-id="4b829-416">The Secure Sockets Layer (SSL) 2.0, SSL 3.0, and Transport Layer Security (TLS) 1.0 protocols can be used.</span></span> |
| <span data-ttu-id="4b829-417"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>PROTOCOLO SEGURO \_ \_ DE MARCA \_ \_ WINHTTP SSL2</span><span class="sxs-lookup"><span data-stu-id="4b829-417"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL2</span></span> | <span data-ttu-id="4b829-418">Se puede usar el protocolo SSL 2.0.</span><span class="sxs-lookup"><span data-stu-id="4b829-418">The SSL 2.0 protocol can be used.</span></span> |
| <span data-ttu-id="4b829-419"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>PROTOCOLO SEGURO \_ \_ DE MARCA \_ \_ WINHTTP SSL3</span><span class="sxs-lookup"><span data-stu-id="4b829-419"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL3</span></span> | <span data-ttu-id="4b829-420">Se puede usar el protocolo SSL 3.0.</span><span class="sxs-lookup"><span data-stu-id="4b829-420">The SSL 3.0 protocol can be used.</span></span> |
| <span data-ttu-id="4b829-421"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>PROTOCOLO SEGURO \_ \_ DE MARCA \_ \_ WINHTTP TLS1</span><span class="sxs-lookup"><span data-stu-id="4b829-421"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1</span></span> | <span data-ttu-id="4b829-422">Se puede usar el protocolo TLS 1.0.</span><span class="sxs-lookup"><span data-stu-id="4b829-422">The TLS 1.0 protocol can be used.</span></span> |
| <span data-ttu-id="4b829-423"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>PROTOCOLO SEGURO \_ \_ DE MARCA \_ \_ WINHTTP TLS1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="4b829-423"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_1</span></span> | <span data-ttu-id="4b829-424">Se puede usar el protocolo TLS 1.1.</span><span class="sxs-lookup"><span data-stu-id="4b829-424">The TLS 1.1 protocol can be used.</span></span> |
| <span data-ttu-id="4b829-425"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>PROTOCOLO SEGURO \_ \_ DE MARCA \_ \_ WINHTTP TLS1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="4b829-425"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_2</span></span> | <span data-ttu-id="4b829-426">Se puede usar el protocolo TLS 1.2.</span><span class="sxs-lookup"><span data-stu-id="4b829-426">The TLS 1.2 protocol can be used.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="4b829-427"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**ESTRUCTURA DE CERTIFICADO \_ DE SEGURIDAD DE LA OPCIÓN \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-427"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-428">Recupera el certificado de un servidor SSL/TLS en la [**estructura WINHTTP \_ CERTIFICATE \_ INFO.**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)</span><span class="sxs-lookup"><span data-stu-id="4b829-428">Retrieves the certificate for a SSL/TLS server into the [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="4b829-429">La aplicación debe liberar los **miembros lpszSubjectInfo** y **lpszIssuerInfo** con [**LocalFree.**](/windows/desktop/api/winbase/nf-winbase-localfree)</span><span class="sxs-lookup"><span data-stu-id="4b829-429">The application must free the **lpszSubjectInfo** and **lpszIssuerInfo** members with [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-430"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**MARCAS DE \_ SEGURIDAD DE \_ LA \_ OPCIÓN WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-430"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-431">Establece o recupera un valor entero largo sin signo que contiene las marcas de seguridad de un identificador.</span><span class="sxs-lookup"><span data-stu-id="4b829-431">Sets or retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="4b829-432">Puede ser una combinación de estos valores:</span><span class="sxs-lookup"><span data-stu-id="4b829-432">It can be a combination of these values:</span></span>

| <span data-ttu-id="4b829-433">Término</span><span class="sxs-lookup"><span data-stu-id="4b829-433">Term</span></span> | <span data-ttu-id="4b829-434">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b829-434">Description</span></span> |
|-|-|
| <span data-ttu-id="4b829-435"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>LA MARCA \_ DE SEGURIDAD OMITIR CN DE CERTIFICADO NO ES \_ \_ \_ \_ VÁLIDA</span><span class="sxs-lookup"><span data-stu-id="4b829-435"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span> |<span data-ttu-id="4b829-436">Permite un nombre común no válido en un certificado; es decir, el nombre de servidor especificado por la aplicación no coincide con el nombre común del certificado.</span><span class="sxs-lookup"><span data-stu-id="4b829-436">Allows an invalid common name in a certificate; that is, the server name specified by the application does not match the common name in the certificate.</span></span> <span data-ttu-id="4b829-437">Si se establece esta marca, la aplicación no recibe una devolución de llamada **WINHTTP \_ CALLBACK \_ STATUS FLAG CERT CN \_ \_ \_ \_ INVALID.**</span><span class="sxs-lookup"><span data-stu-id="4b829-437">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_CN\_INVALID** callback.</span></span> |
| <span data-ttu-id="4b829-438"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>MARCA DE \_ SEGURIDAD OMITIR LA FECHA DE CERTIFICADO NO \_ \_ \_ \_ VÁLIDA</span><span class="sxs-lookup"><span data-stu-id="4b829-438"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span> |<span data-ttu-id="4b829-439">Permite una fecha de certificado no válida, es decir, un certificado expirado o no efectivo.</span><span class="sxs-lookup"><span data-stu-id="4b829-439">Allows an invalid certificate date, that is, an expired or not-yet-effective certificate.</span></span> <span data-ttu-id="4b829-440">Si se establece esta marca, la aplicación no recibe una devolución de llamada **CERT \_ DATE \_ \_ \_ \_ \_ INVALID** DE LA MARCA DE ESTADO DE DEVOLUCIÓN DE LLAMADA WINHTTP.</span><span class="sxs-lookup"><span data-stu-id="4b829-440">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_DATE\_INVALID** callback.</span></span> |
| <span data-ttu-id="4b829-441"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>MARCA DE \_ SEGURIDAD \_ OMITIR CA \_ \_ DESCONOCIDA</span><span class="sxs-lookup"><span data-stu-id="4b829-441"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span> | <span data-ttu-id="4b829-442">Permite una entidad de certificación no válida.</span><span class="sxs-lookup"><span data-stu-id="4b829-442">Allows an invalid certificate authority.</span></span> <span data-ttu-id="4b829-443">Si se establece esta marca, la aplicación no recibe una devolución de llamada DE CA NO VÁLIDA DE LA MARCA DE ESTADO DE DEVOLUCIÓN DE LLAMADA **WINHTTP. \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4b829-443">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_INVALID\_CA** callback.</span></span> |
| <span data-ttu-id="4b829-444"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>MARCA DE \_ SEGURIDAD OMITIR EL USO INCORRECTO DEL \_ \_ \_ \_ CERTIFICADO</span><span class="sxs-lookup"><span data-stu-id="4b829-444"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_CERT\_WRONG\_USAGE</span></span> | <span data-ttu-id="4b829-445">Permite establecer la identidad de un servidor con un certificado que no es de servidor (por ejemplo, un certificado de cliente).</span><span class="sxs-lookup"><span data-stu-id="4b829-445">Allows the identity of a server to be established with a non-server certificate (for example, a client certificate).</span></span> |
| <span data-ttu-id="4b829-446"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>MARCA DE \_ SEGURIDAD \_ OMITIR FIRMA \_ \_ DÉBIL</span><span class="sxs-lookup"><span data-stu-id="4b829-446"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span> | <span data-ttu-id="4b829-447">Permite omitir una firma débil.</span><span class="sxs-lookup"><span data-stu-id="4b829-447">Allows a weak signature to be ignored.</span></span><br/><span data-ttu-id="4b829-448">Esta marca está disponible en la actualización de acumulación para cada sistema operativo a partir de Windows 7 y Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="4b829-448">This flag is available in the rollup update for each OS starting with Windows 7 and Windows Server 2008 R2.</span></span> |
| <span data-ttu-id="4b829-449"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>MARCA \_ DE SEGURIDAD \_ SEGURA</span><span class="sxs-lookup"><span data-stu-id="4b829-449"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span> | <span data-ttu-id="4b829-450">Usa transferencias seguras.</span><span class="sxs-lookup"><span data-stu-id="4b829-450">Uses secure transfers.</span></span> <span data-ttu-id="4b829-451">Esto solo se devuelve en una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="4b829-451">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="4b829-452"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>MEDIO \_ DE INTENSIDAD DE LA MARCA DE \_ \_ SEGURIDAD</span><span class="sxs-lookup"><span data-stu-id="4b829-452"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span> | <span data-ttu-id="4b829-453">Usa cifrado medio (56 bits).</span><span class="sxs-lookup"><span data-stu-id="4b829-453">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="4b829-454">Esto solo se devuelve en una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="4b829-454">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="4b829-455"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SEGURIDAD \_ FUERTE DE LA \_ MARCA \_</span><span class="sxs-lookup"><span data-stu-id="4b829-455"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span> | <span data-ttu-id="4b829-456">Usa un cifrado seguro (de 128 bits).</span><span class="sxs-lookup"><span data-stu-id="4b829-456">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="4b829-457">Esto solo se devuelve en una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="4b829-457">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="4b829-458"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SEGURIDAD \_ DÉBIL DE LA INTENSIDAD DE LA \_ \_ MARCA</span><span class="sxs-lookup"><span data-stu-id="4b829-458"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span> | <span data-ttu-id="4b829-459">Usa un cifrado débil (de 40 bits).</span><span class="sxs-lookup"><span data-stu-id="4b829-459">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="4b829-460">Esto solo se devuelve en una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="4b829-460">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="4b829-461"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**INFORMACIÓN DE SEGURIDAD \_ DE LA \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-461"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP\_OPTION\_SECURITY\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-462">Retraive la conexión de SChannel y la información de cifrado de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="4b829-462">Retreives the SChannel connection and cipher information for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-463"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**VALOR DE BITS \_ DE CLAVE DE SEGURIDAD DE LA OPCIÓN \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-463"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-464">Recupera un valor entero largo sin signo que contiene la intensidad de cifrado de la clave de cifrado.</span><span class="sxs-lookup"><span data-stu-id="4b829-464">Retrieves an unsigned long integer value that contains the cipher strength of the encryption key.</span></span> <span data-ttu-id="4b829-465">Un número mayor indica un cifrado más seguro de la intensidad del cifrado.</span><span class="sxs-lookup"><span data-stu-id="4b829-465">A larger number indicates stronger cipher strength encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-466"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**OPCIÓN WINHTTP \_ ENVIAR TIEMPO DE \_ \_ ESPERA**</span><span class="sxs-lookup"><span data-stu-id="4b829-466"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-467">Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, para enviar una solicitud o escribir algunos datos.</span><span class="sxs-lookup"><span data-stu-id="4b829-467">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to send a request or write some data.</span></span> <span data-ttu-id="4b829-468">Si el envío de la solicitud tarda más tiempo que el tiempo de espera, se cancela la operación de envío.</span><span class="sxs-lookup"><span data-stu-id="4b829-468">If sending the request takes longer than the timeout, the send operation is canceled.</span></span> <span data-ttu-id="4b829-469">El tiempo de expiración predeterminado es de 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="4b829-469">The default timeout is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-470"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP \_ OPTION \_ SERVER \_ CBT**</span><span class="sxs-lookup"><span data-stu-id="4b829-470"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP\_OPTION\_SERVER\_CBT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-471">Obtiene un puntero a [**la estructura Enlaces SecPkgContext \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) que especifica un token de enlace de canal (CBT).</span><span class="sxs-lookup"><span data-stu-id="4b829-471">Gets a pointer to [**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) structure that specifies a Channel Binding Token (CBT).</span></span>

<span data-ttu-id="4b829-472">Un token de enlace de canal es una propiedad de un canal de transporte seguro y se usa para enlazar un canal de autenticación al canal de transporte seguro.</span><span class="sxs-lookup"><span data-stu-id="4b829-472">A Channel Binding Token is a property of a secure transport channel and is used to bind an authentication channel to the secure transport channel.</span></span> <span data-ttu-id="4b829-473">Este token solo se puede obtener con esta opción una vez establecida una conexión SSL.</span><span class="sxs-lookup"><span data-stu-id="4b829-473">This token can only be obtained by this option after an SSL connection has been established.</span></span>

> [!Note]
> <span data-ttu-id="4b829-474">Si se pasa esta opción y un valor **NULL** para *lpBuffer* a [**WinHttpQueryOption,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) se devolverá ERROR INSUFFICIENT BUFFER y el tamaño de byte necesario para el búfer en el parámetro \_ \_ *lpdwBufferLength.*</span><span class="sxs-lookup"><span data-stu-id="4b829-474">Passing this option and a **null** value for *lpBuffer* to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) will return ERROR\_INSUFFICIENT\_BUFFER and the required byte size for the buffer in the *lpdwBufferLength* parameter.</span></span> <span data-ttu-id="4b829-475">Este valor de tamaño de búfer devuelto se puede pasar en una llamada posterior para consultar el token de enlace de canal.</span><span class="sxs-lookup"><span data-stu-id="4b829-475">This returned buffer size value can be passed in a subsequent call to query for the Channel Binding Token.</span></span> <span data-ttu-id="4b829-476">Estos pasos son necesarios al controlar LA SOLICITUD DE ESTADO DE DEVOLUCIÓN DE LLAMADA DE WINHTTP si desea modificar los encabezados de solicitud \_ en función del token de enlace de \_ \_ canal.</span><span class="sxs-lookup"><span data-stu-id="4b829-476">These steps are necessary when handling WINHTTP\_CALLBACK\_STATUS\_REQUEST if you want to modify request headers based on the Channel Binding Token.</span></span> <span data-ttu-id="4b829-477">Tenga en cuenta que Windows XP y Vista no admiten la modificación de encabezados de solicitud durante esta devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="4b829-477">Note that Windows XP and Vista do not support modifying request headers during this callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-478"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**CONTEXTO DE CADENA \_ DE CERTIFICADOS DE SERVIDOR DE \_ \_ OPCIÓN \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-478"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-479">Recupera el contexto de la cadena de certificación del servidor.</span><span class="sxs-lookup"><span data-stu-id="4b829-479">Retrieves the server certification chain context.</span></span> <span data-ttu-id="4b829-480">**WINHTTP \_ OPTION \_ SERVER CERT CHAIN \_ \_ \_ CONTEXT** se puede pasar para obtener un puntero duplicado a **CERT CHAIN \_ \_ CONTEXT** para una cadena de certificados de servidor recibida durante una conexión SSL negociada.</span><span class="sxs-lookup"><span data-stu-id="4b829-480">**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT** can be passed to obtain a duplicated pointer to the **CERT\_CHAIN\_CONTEXT** for a server certificate chain received during a negotiated SSL connection.</span></span> <span data-ttu-id="4b829-481">El cliente debe llamar [**a CertFreeCertificateContext en**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) el puntero DE CONTEXTO DE PCCERT \_ devuelto que se rellena en el búfer.</span><span class="sxs-lookup"><span data-stu-id="4b829-481">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-482"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**CONTEXTO DE CERTIFICADO \_ DE SERVIDOR DE LA OPCIÓN \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-482"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-483">Recupera el contexto de certificación del servidor.</span><span class="sxs-lookup"><span data-stu-id="4b829-483">Retrieves the server certification context.</span></span> <span data-ttu-id="4b829-484">**WINHTTP \_ OPTION \_ SERVER CERT CONTEXT \_ \_ se** puede pasar para obtener un puntero duplicado al [**CONTEXTO DE CERT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) para un certificado de servidor recibido durante una conexión SSL negociada.</span><span class="sxs-lookup"><span data-stu-id="4b829-484">**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT** can be passed to obtain a duplicated pointer to the [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) for a server certificate received during a negotiated SSL connection.</span></span> <span data-ttu-id="4b829-485">El cliente debe llamar [**a CertFreeCertificateContext en**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) el puntero DE CONTEXTO DE PCCERT \_ devuelto que se rellena en el búfer.</span><span class="sxs-lookup"><span data-stu-id="4b829-485">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-486"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**OPCIÓN WINHTTP \_ \_ SERVIDOR \_ SPN \_ USADO**</span><span class="sxs-lookup"><span data-stu-id="4b829-486"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**WINHTTP\_OPTION\_SERVER\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-487">Obtiene el nombre principal del servidor que WinHTTP proporcionó a SSPI durante la autenticación.</span><span class="sxs-lookup"><span data-stu-id="4b829-487">Gets the server Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="4b829-488">Este valor de cadena se puede pasar a [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) después de un error de autenticación.</span><span class="sxs-lookup"><span data-stu-id="4b829-488">This string value can be passed to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-489"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**SPN DE \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-489"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP\_OPTION\_SPN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-490">Incluye o quita el número de puerto del servidor cuando se ha creado el SPN (nombre principal de servicio) para la autenticación Kerberos o Negotiate Kerberos.</span><span class="sxs-lookup"><span data-stu-id="4b829-490">Includes or removes the server port number when the SPN (service principal name) is built for Kerberos or Negotiate Kerberos authentication.</span></span> <span data-ttu-id="4b829-491">Esta marca es uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="4b829-491">This flag is one of the following values:</span></span>

| <span data-ttu-id="4b829-492">Término</span><span class="sxs-lookup"><span data-stu-id="4b829-492">Term</span></span> | <span data-ttu-id="4b829-493">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b829-493">Description</span></span> |
|-|-|
| <span data-ttu-id="4b829-494"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP \_ DISABLE \_ SPN \_ SERVER \_ PORT</span><span class="sxs-lookup"><span data-stu-id="4b829-494"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP\_DISABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="4b829-495">Quita el número de puerto del servidor.</span><span class="sxs-lookup"><span data-stu-id="4b829-495">Removes the server port number.</span></span> |
| <span data-ttu-id="4b829-496"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP \_ ENABLE \_ SPN \_ SERVER \_ PORT</span><span class="sxs-lookup"><span data-stu-id="4b829-496"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP\_ENABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="4b829-497">Incluye el número de puerto del servidor.</span><span class="sxs-lookup"><span data-stu-id="4b829-497">Includes the server port number.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="4b829-498"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**OPCIÓN WINHTTP \_ \_ TCP FAST \_ \_ OPEN**</span><span class="sxs-lookup"><span data-stu-id="4b829-498"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP\_OPTION\_TCP\_FAST\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-499">Habilita TCP Fast Open para la conexión.</span><span class="sxs-lookup"><span data-stu-id="4b829-499">Enables TCP Fast Open for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-500"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**OPCIÓN WINHTTP \_ \_ TCP \_ KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="4b829-500"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**WINHTTP\_OPTION\_TCP\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-501">Esta opción se puede establecer en un identificador de sesión WinHttp para habilitar el comportamiento de conexión de TCP en el socket subyacente.</span><span class="sxs-lookup"><span data-stu-id="4b829-501">This option can be set on a WinHttp session handle to enable TCP keep-alive behavior on the underlying socket.</span></span> <span data-ttu-id="4b829-502">Toma una [**estructura \_ tcp keepalive.**](/windows/win32/winsock/sio-keepalive-vals)</span><span class="sxs-lookup"><span data-stu-id="4b829-502">Takes a [**tcp\_keepalive**](/windows/win32/winsock/sio-keepalive-vals) struct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-503"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**OPCIÓN WINHTTP \_ \_ TLS FALSE \_ \_ START**</span><span class="sxs-lookup"><span data-stu-id="4b829-503"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP\_OPTION\_TLS\_FALSE\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-504">Habilita TLS False Start para la conexión.</span><span class="sxs-lookup"><span data-stu-id="4b829-504">Enables TLS False Start for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-505"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**EVENTO DE NOTIFICACIÓN DE \_ DESCARGA DE LA OPCIÓN \_ WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4b829-505"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-506">Toma un evento que se establecerá cuando se haya completado la última devolución de llamada para una sesión determinada.</span><span class="sxs-lookup"><span data-stu-id="4b829-506">Takes an event that will be set when the last callback has completed for a particular session.</span></span> <span data-ttu-id="4b829-507">Esta marca debe usarse en un identificador de sesión.</span><span class="sxs-lookup"><span data-stu-id="4b829-507">This flag must be must be used on a session handle.</span></span> <span data-ttu-id="4b829-508">El evento no se puede cerrar hasta que WinHTTP lo haya establecido.</span><span class="sxs-lookup"><span data-stu-id="4b829-508">The event cannot be closed until after it has been set by WinHTTP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-509"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**ANÁLISIS DE ENCABEZADOS NO SEGUROS DE LA \_ \_ \_ \_ OPCIÓN WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-509"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-510">Esta opción está reservada para uso interno y no se debe llamar a .</span><span class="sxs-lookup"><span data-stu-id="4b829-510">This option is reserved for internal use and should not be called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-511"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**ACTUALIZACIÓN DE LA OPCIÓN WINHTTP \_ \_ AL SOCKET \_ \_ \_ WEB**</span><span class="sxs-lookup"><span data-stu-id="4b829-511"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-512">Indica a la pila que inicie un proceso de protocolo de enlace de WebSocket [**con WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="4b829-512">Instructs the stack to start a WebSocket handshake process with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="4b829-513">Esta opción no toma ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="4b829-513">This option takes no parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-514"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**DIRECCIÓN URL DE LA OPCIÓN WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4b829-514"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-515">Recupera un valor de cadena que contiene la dirección URL completa de un recurso descargado.</span><span class="sxs-lookup"><span data-stu-id="4b829-515">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="4b829-516">Si la dirección URL original contenía datos adicionales, como cadenas de búsqueda o delimitadores, o si la llamada se redirija, la dirección URL devuelta difiere de la original.</span><span class="sxs-lookup"><span data-stu-id="4b829-516">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="4b829-517">La aplicación debe pasar un búfer, con un tamaño en bytes, lo suficientemente grande como para contener la dirección URL devuelta en caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="4b829-517">The application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-518"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**OPCIÓN WINHTTP \_ USAR CREDENCIALES DE SERVIDOR \_ \_ \_ \_ GLOBAL**</span><span class="sxs-lookup"><span data-stu-id="4b829-518"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-519">Toma un **valor BOOL** y solo se puede establecer un identificador de sesión.</span><span class="sxs-lookup"><span data-stu-id="4b829-519">Takes a **BOOL** and can be set only a session handle.</span></span> <span data-ttu-id="4b829-520">Solo se propagará hacia abajo a los identificadores creados a partir del identificador de sesión una vez establecida la opción.</span><span class="sxs-lookup"><span data-stu-id="4b829-520">It will only propagate down to handles created from the session handle after the option has been set.</span></span> <span data-ttu-id="4b829-521">Si **es TRUE,** esta opción provoca como último recurso el uso de credenciales de servidor global que se insertaron desde WinInet.</span><span class="sxs-lookup"><span data-stu-id="4b829-521">If **TRUE**, this option causes as a last resort the use of global server credentials that were pushed down from WinInet.</span></span> <span data-ttu-id="4b829-522">El valor predeterminado de esta opción es **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="4b829-522">The default for this option is **FALSE**.</span></span> <span data-ttu-id="4b829-523">Esta opción requiere la clave del Registro **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="4b829-523">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="4b829-524">Esta clave del Registro no está presente de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4b829-524">This registry key is not present by default.</span></span> <span data-ttu-id="4b829-525">Cuando se establece, WinINet enviará las credenciales a WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="4b829-525">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="4b829-526">Cada vez que WinHttp obtiene un desafío de autenticación y no hay ninguna credencial establecida en el identificador actual, usará las credenciales proporcionadas por WinINet.</span><span class="sxs-lookup"><span data-stu-id="4b829-526">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-527"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**AGENTE DE USUARIO \_ DE LA \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-527"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-528">Establece o recupera [](glossary.md) la cadena del agente de usuario en los identificadores proporcionados por [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) y usados en funciones [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) posteriores, siempre que no se invalide por un encabezado agregado por [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) **o WinHttpSendRequest**.</span><span class="sxs-lookup"><span data-stu-id="4b829-528">Sets or retrieves the [*user agent*](glossary.md) string on handles supplied by [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) and used in subsequent [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) functions, as long as it is not overridden by a header added by [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) or **WinHttpSendRequest**.</span></span> <span data-ttu-id="4b829-529">Al recuperar un agente de usuario, la aplicación debe pasar un búfer, con un tamaño en bytes, lo suficientemente grande como para contener la dirección URL devuelta en caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="4b829-529">When retrieving a user agent, the application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span> <span data-ttu-id="4b829-530">Al establecer el agente de usuario, el tamaño del búfer es la longitud de la cadena, en caracteres, más el **terminador NULL.**</span><span class="sxs-lookup"><span data-stu-id="4b829-530">When setting the user agent, the buffer size is the length of the string, in characters, plus the **NULL** terminator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-531"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**NOMBRE DE USUARIO DE LA OPCIÓN WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4b829-531"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-532">Establece o recupera una cadena que contiene el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="4b829-532">Sets or retrieves a string that contains the user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-533"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**TIEMPO DE ESPERA \_ DE CIERRE DE SOCKET WEB DE LA \_ \_ \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-533"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-534">Establece el tiempo, en milisegundos, que [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) debe esperar para completar el protocolo de enlace de cierre.</span><span class="sxs-lookup"><span data-stu-id="4b829-534">Sets the time, in milliseconds, that [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) should wait to complete the close handshake.</span></span> <span data-ttu-id="4b829-535">El valor predeterminado es 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="4b829-535">The default is 10 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-536"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**OPCIÓN WINHTTP \_ \_ WEB SOCKET \_ \_ \_ KEEPALIVE INTERVAL**</span><span class="sxs-lookup"><span data-stu-id="4b829-536"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-537">Establece el intervalo, en milisegundos, para enviar un paquete keep-alive a través de la conexión.</span><span class="sxs-lookup"><span data-stu-id="4b829-537">Sets the interval, in milliseconds, to send a keep-alive packet over the connection.</span></span> <span data-ttu-id="4b829-538">El intervalo predeterminado es 30 000 (30 segundos).</span><span class="sxs-lookup"><span data-stu-id="4b829-538">The default interval is 30000 (30 seconds).</span></span> <span data-ttu-id="4b829-539">El intervalo mínimo es 15 000 (15 segundos).</span><span class="sxs-lookup"><span data-stu-id="4b829-539">The minimum interval is 15000 (15 seconds).</span></span> <span data-ttu-id="4b829-540">El [**uso de WinHttpSetOption para**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) establecer un valor inferior a 15000 devolverá con ERROR INVALID **\_ \_ PARAMETER**.</span><span class="sxs-lookup"><span data-stu-id="4b829-540">Using [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to set a value lower than 15000 will return with **ERROR\_INVALID\_PARAMETER**.</span></span>

> [!Note]
> <span data-ttu-id="4b829-541">El valor predeterminado de **WINHTTP \_ OPTION WEB SOCKET \_ \_ \_ KEEPALIVE \_ INTERVAL** se lee de **HKLM: \\ SOFTWARE Microsoft \\ \\ WebSocket \\ KeepaliveInterval**.</span><span class="sxs-lookup"><span data-stu-id="4b829-541">The default value for **WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL** is read from **HKLM:\\SOFTWARE\\Microsoft\\WebSocket\\KeepaliveInterval**.</span></span> <span data-ttu-id="4b829-542">Si no se establece un valor, se usará el valor predeterminado de 30000.</span><span class="sxs-lookup"><span data-stu-id="4b829-542">If a value is not set, the default value of 30000 will be used.</span></span> <span data-ttu-id="4b829-543">No es posible tener un intervalo de keepalive inferior a 15 000 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="4b829-543">It is not possible to have a lower keepalive interval than 15000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-544"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**TAMAÑO DEL BÚFER DE RECEPCIÓN DE LA OPCIÓN WINHTTP \_ \_ WEB \_ SOCKET \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4b829-544"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-545">Establece o recupera un DWORD que especifica el tamaño del búfer de recepción que se va a usar en las conexiones de WebSocket.</span><span class="sxs-lookup"><span data-stu-id="4b829-545">Sets or retrieves a DWORD which specifies the receive buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-546"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**TAMAÑO DEL BÚFER DE ENVÍO DE SOCKET WEB DE LA \_ \_ \_ \_ \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-546"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-547">Establece o recupera un DWORD que especifica el tamaño del búfer de envío que se usará en las conexiones webSocket.</span><span class="sxs-lookup"><span data-stu-id="4b829-547">Sets or retrieves a DWORD which specifies the send buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-548"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**RECUENTO DE \_ SUBPROCESOS \_ DE TRABAJO DE LA \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-548"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-549">Establece un valor entero largo sin signo que especifica el número de subprocesos de trabajo que el grupo de subprocesos debe usar para las finalizaciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="4b829-549">Sets an unsigned long integer value that specifies the number of worker threads the thread pool should use for asynchronous completions.</span></span> <span data-ttu-id="4b829-550">El valor predeterminado de esta opción es cero, que especifica que el número de subprocesos de trabajo es igual al número de CPU del sistema.</span><span class="sxs-lookup"><span data-stu-id="4b829-550">The default value of this option is zero, which specifies that the number of worker threads is equal to the number of CPUs on the system.</span></span> <span data-ttu-id="4b829-551">Esta opción solo se puede establecer en un **identificador NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) antes de que se haya producido una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="4b829-551">This option can only be set on a **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) handle before an asynchronous operation has occurred.</span></span> <span data-ttu-id="4b829-552">Esta opción solo se puede establecer una vez.</span><span class="sxs-lookup"><span data-stu-id="4b829-552">This option can only be set once.</span></span>

<span data-ttu-id="4b829-553">**Windows Server 2008 R2 y Windows 7:** Esta marca está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="4b829-553">**Windows Server 2008 R2 and Windows 7:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4b829-554"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**TAMAÑO DEL BÚFER \_ DE ESCRITURA DE LA \_ \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-554"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4b829-555">Esta opción ha quedado en desuso; no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="4b829-555">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b829-556">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4b829-556">Remarks</span></span>

<span data-ttu-id="4b829-557">En la tabla siguiente se enumeran las marcas de opción especificando los identificadores sobre los que pueden actuar, si se pueden consultar y establecer, y el tipo de datos utilizado.</span><span class="sxs-lookup"><span data-stu-id="4b829-557">The following table lists the option flags by specifying which handles they can act upon, whether they can be queried and set, and the data type used.</span></span> <span data-ttu-id="4b829-558">Una "X" indica que la marca de opción es válida para su uso con la función o el identificador, mientras que "-" especifica que la marca de opción no es válida.</span><span class="sxs-lookup"><span data-stu-id="4b829-558">An "X" indicates that the option flag is valid for use with the function or handle, while a "-" specifies that the option flag is invalid.</span></span>

<span data-ttu-id="4b829-559">Al intentar establecer o consultar una marca de opción en una versión de Windows en la que no se admite, se producirá **el error \_ WINHTTP INVALID \_ \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="4b829-559">Attempting to set or query an option flag on a Windows version where it is not supported will result in **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span>

| <span data-ttu-id="4b829-560">Marca de opción y tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4b829-560">Option flag, and data type</span></span> | <span data-ttu-id="4b829-561">Identificador de sesión</span><span class="sxs-lookup"><span data-stu-id="4b829-561">Session handle</span></span> | <span data-ttu-id="4b829-562">Identificador de solicitud</span><span class="sxs-lookup"><span data-stu-id="4b829-562">Request handle</span></span> | <span data-ttu-id="4b829-563">Opción de consulta</span><span class="sxs-lookup"><span data-stu-id="4b829-563">Query option</span></span> | <span data-ttu-id="4b829-564">Opción SET</span><span class="sxs-lookup"><span data-stu-id="4b829-564">Set option</span></span> | <span data-ttu-id="4b829-565">Versión mínima de Windows</span><span class="sxs-lookup"><span data-stu-id="4b829-565">Minimum Windows Version</span></span> |
|-|-|-|-|-|-|
| <span data-ttu-id="4b829-566">OPCIÓN WINHTTP \_ QUE GARANTIZA DEVOLUCIONES DE LLAMADA SIN \_ \_ \_ \_ BLOQUEO</span><span class="sxs-lookup"><span data-stu-id="4b829-566">WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS</span></span><br/><span data-ttu-id="4b829-567">**Bool**</span><span class="sxs-lookup"><span data-stu-id="4b829-567">**BOOL**</span></span> | <span data-ttu-id="4b829-568">X</span><span class="sxs-lookup"><span data-stu-id="4b829-568">X</span></span> | \- | \- | <span data-ttu-id="4b829-569">X</span><span class="sxs-lookup"><span data-stu-id="4b829-569">X</span></span> | \- |
| <span data-ttu-id="4b829-570">DIRECTIVA DE \_ INICIO DE SESIÓN AUTOMÁTICO DE LA OPCIÓN \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-570">WINHTTP\_OPTION\_AUTOLOGON\_POLICY</span></span><br/><span data-ttu-id="4b829-571">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-571">**DWORD**</span></span> | \- | <span data-ttu-id="4b829-572">X</span><span class="sxs-lookup"><span data-stu-id="4b829-572">X</span></span> | \- | <span data-ttu-id="4b829-573">X</span><span class="sxs-lookup"><span data-stu-id="4b829-573">X</span></span> | \- |
| <span data-ttu-id="4b829-574">DEVOLUCIÓN DE LLAMADA \_ DE LA \_ OPCIÓN WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-574">WINHTTP\_OPTION\_CALLBACK</span></span><br/><span data-ttu-id="4b829-575">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="4b829-575">**LPVOID**</span></span> | <span data-ttu-id="4b829-576">X</span><span class="sxs-lookup"><span data-stu-id="4b829-576">X</span></span> | <span data-ttu-id="4b829-577">X</span><span class="sxs-lookup"><span data-stu-id="4b829-577">X</span></span> | <span data-ttu-id="4b829-578">X</span><span class="sxs-lookup"><span data-stu-id="4b829-578">X</span></span> | <span data-ttu-id="4b829-579">X</span><span class="sxs-lookup"><span data-stu-id="4b829-579">X</span></span> | \- |
| <span data-ttu-id="4b829-580">CONTEXTO DE CERTIFICADO \_ DE CLIENTE DE LA OPCIÓN \_ \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-580">WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="4b829-581">**CONTEXTO \_ DE CERT**</span><span class="sxs-lookup"><span data-stu-id="4b829-581">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="4b829-582">X</span><span class="sxs-lookup"><span data-stu-id="4b829-582">X</span></span> | \- | <span data-ttu-id="4b829-583">X</span><span class="sxs-lookup"><span data-stu-id="4b829-583">X</span></span> | <span data-ttu-id="4b829-584">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b829-584">Windows Vista</span></span> |
| <span data-ttu-id="4b829-585">LISTA DE \_ \_ EMISORES DE \_ CERTIFICADOS DE CLIENTE DE LA \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-585">WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST</span></span><br/>[<span data-ttu-id="4b829-586">**SecPkgContext \_ IssuerListInfoEx**</span><span class="sxs-lookup"><span data-stu-id="4b829-586">**SecPkgContext\_IssuerListInfoEx**</span></span>](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | <span data-ttu-id="4b829-587">X</span><span class="sxs-lookup"><span data-stu-id="4b829-587">X</span></span> | <span data-ttu-id="4b829-588">X</span><span class="sxs-lookup"><span data-stu-id="4b829-588">X</span></span> | \- | <span data-ttu-id="4b829-589">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b829-589">Windows Vista</span></span> |
| <span data-ttu-id="4b829-590">PÁGINA DE CÓDIGOS \_ DE LA \_ OPCIÓN WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-590">WINHTTP\_OPTION\_CODEPAGE</span></span><br/><span data-ttu-id="4b829-591">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-591">**DWORD**</span></span> | <span data-ttu-id="4b829-592">X</span><span class="sxs-lookup"><span data-stu-id="4b829-592">X</span></span> | \- | \- | <span data-ttu-id="4b829-593">X</span><span class="sxs-lookup"><span data-stu-id="4b829-593">X</span></span> | \- |
| <span data-ttu-id="4b829-594">OPCIÓN WINHTTP \_ CONFIGURAR \_ LA \_ AUTENTICACIÓN DE PASSPORT \_</span><span class="sxs-lookup"><span data-stu-id="4b829-594">WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH</span></span><br/><span data-ttu-id="4b829-595">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-595">**DWORD**</span></span> | <span data-ttu-id="4b829-596">X</span><span class="sxs-lookup"><span data-stu-id="4b829-596">X</span></span> | \- | \- | <span data-ttu-id="4b829-597">X</span><span class="sxs-lookup"><span data-stu-id="4b829-597">X</span></span> | \- |
| <span data-ttu-id="4b829-598">REINTENTOS DE \_ CONEXIÓN DE LA OPCIÓN \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-598">WINHTTP\_OPTION\_CONNECT\_RETRIES</span></span><br/><span data-ttu-id="4b829-599">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-599">**DWORD**</span></span> | <span data-ttu-id="4b829-600">X</span><span class="sxs-lookup"><span data-stu-id="4b829-600">X</span></span> | <span data-ttu-id="4b829-601">X</span><span class="sxs-lookup"><span data-stu-id="4b829-601">X</span></span> | <span data-ttu-id="4b829-602">X</span><span class="sxs-lookup"><span data-stu-id="4b829-602">X</span></span> | <span data-ttu-id="4b829-603">X</span><span class="sxs-lookup"><span data-stu-id="4b829-603">X</span></span> | \- |
| <span data-ttu-id="4b829-604">TIEMPO DE ESPERA \_ DE CONEXIÓN DE LA OPCIÓN \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-604">WINHTTP\_OPTION\_CONNECT\_TIMEOUT</span></span><br/><span data-ttu-id="4b829-605">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-605">**DWORD**</span></span> | <span data-ttu-id="4b829-606">X</span><span class="sxs-lookup"><span data-stu-id="4b829-606">X</span></span> | <span data-ttu-id="4b829-607">X</span><span class="sxs-lookup"><span data-stu-id="4b829-607">X</span></span> | <span data-ttu-id="4b829-608">X</span><span class="sxs-lookup"><span data-stu-id="4b829-608">X</span></span> | <span data-ttu-id="4b829-609">X</span><span class="sxs-lookup"><span data-stu-id="4b829-609">X</span></span> | \- |
| <span data-ttu-id="4b829-610">INFORMACIÓN DE CONEXIÓN \_ DE \_ LA OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-610">WINHTTP\_OPTION\_CONNECTION\_INFO</span></span><br/>[<span data-ttu-id="4b829-611">**INFORMACIÓN DE CONEXIÓN \_ WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="4b829-611">**WINHTTP\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | <span data-ttu-id="4b829-612">X</span><span class="sxs-lookup"><span data-stu-id="4b829-612">X</span></span> | <span data-ttu-id="4b829-613">X</span><span class="sxs-lookup"><span data-stu-id="4b829-613">X</span></span> | \- | \- |
| <span data-ttu-id="4b829-614">WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V0</span><span class="sxs-lookup"><span data-stu-id="4b829-614">WINHTTP\_OPTION\_CONNECTION\_STATS\_V0</span></span><br/>[<span data-ttu-id="4b829-615">**TCP \_ INFO \_ v0**</span><span class="sxs-lookup"><span data-stu-id="4b829-615">**TCP\_INFO\_v0**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | <span data-ttu-id="4b829-616">X</span><span class="sxs-lookup"><span data-stu-id="4b829-616">X</span></span> | <span data-ttu-id="4b829-617">X</span><span class="sxs-lookup"><span data-stu-id="4b829-617">X</span></span> | \- | <span data-ttu-id="4b829-618">Windows 10 versión 1903</span><span class="sxs-lookup"><span data-stu-id="4b829-618">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="4b829-619">WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1</span><span class="sxs-lookup"><span data-stu-id="4b829-619">WINHTTP\_OPTION\_CONNECTION\_STATS\_V1</span></span><br/>[<span data-ttu-id="4b829-620">**TCP \_ INFO \_ v1**</span><span class="sxs-lookup"><span data-stu-id="4b829-620">**TCP\_INFO\_v1**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | <span data-ttu-id="4b829-621">X</span><span class="sxs-lookup"><span data-stu-id="4b829-621">X</span></span> | <span data-ttu-id="4b829-622">X</span><span class="sxs-lookup"><span data-stu-id="4b829-622">X</span></span> | \- | <span data-ttu-id="4b829-623">Windows 10 versión 2004</span><span class="sxs-lookup"><span data-stu-id="4b829-623">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="4b829-624">VALOR DE CONTEXTO \_ DE \_ LA OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-624">WINHTTP\_OPTION\_CONTEXT\_VALUE</span></span><br/><span data-ttu-id="4b829-625">**DWORD \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="4b829-625">**DWORD\_PTR**</span></span> | <span data-ttu-id="4b829-626">X</span><span class="sxs-lookup"><span data-stu-id="4b829-626">X</span></span> | <span data-ttu-id="4b829-627">X</span><span class="sxs-lookup"><span data-stu-id="4b829-627">X</span></span> | <span data-ttu-id="4b829-628">X</span><span class="sxs-lookup"><span data-stu-id="4b829-628">X</span></span> | <span data-ttu-id="4b829-629">X</span><span class="sxs-lookup"><span data-stu-id="4b829-629">X</span></span> | \- |
| <span data-ttu-id="4b829-630">DESCOMPRESIÓN DE \_ LA OPCIÓN WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="4b829-630">WINHTTP\_OPTION\_DECOMPRESSION</span></span><br/><span data-ttu-id="4b829-631">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-631">**DWORD**</span></span> | <span data-ttu-id="4b829-632">X</span><span class="sxs-lookup"><span data-stu-id="4b829-632">X</span></span> | <span data-ttu-id="4b829-633">X</span><span class="sxs-lookup"><span data-stu-id="4b829-633">X</span></span> | \- | <span data-ttu-id="4b829-634">X</span><span class="sxs-lookup"><span data-stu-id="4b829-634">X</span></span> | <span data-ttu-id="4b829-635">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4b829-635">Windows 8.1</span></span> |
| <span data-ttu-id="4b829-636">CARACTERÍSTICA DESHABILITAR OPCIÓN WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="4b829-636">WINHTTP\_OPTION\_DISABLE\_FEATURE</span></span><br/><span data-ttu-id="4b829-637">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-637">**DWORD**</span></span> | \- | <span data-ttu-id="4b829-638">X</span><span class="sxs-lookup"><span data-stu-id="4b829-638">X</span></span> | \- | <span data-ttu-id="4b829-639">X</span><span class="sxs-lookup"><span data-stu-id="4b829-639">X</span></span> | \- |
| <span data-ttu-id="4b829-640">OPCIÓN WINHTTP \_ DESHABILITAR LA RESERVA DE \_ \_ \_ \_ PROTOCOLOS SEGUROS</span><span class="sxs-lookup"><span data-stu-id="4b829-640">WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK</span></span><br/><span data-ttu-id="4b829-641">**Bool**</span><span class="sxs-lookup"><span data-stu-id="4b829-641">**BOOL**</span></span> | <span data-ttu-id="4b829-642">X</span><span class="sxs-lookup"><span data-stu-id="4b829-642">X</span></span> | \- | \- | <span data-ttu-id="4b829-643">X</span><span class="sxs-lookup"><span data-stu-id="4b829-643">X</span></span> | <span data-ttu-id="4b829-644">Windows 10 versión 1903</span><span class="sxs-lookup"><span data-stu-id="4b829-644">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="4b829-645">OPCIÓN WINHTTP \_ DISABLE \_ STREAM \_ \_ QUEUE</span><span class="sxs-lookup"><span data-stu-id="4b829-645">WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE</span></span><br/><span data-ttu-id="4b829-646">**Bool**</span><span class="sxs-lookup"><span data-stu-id="4b829-646">**BOOL**</span></span> | <span data-ttu-id="4b829-647">X</span><span class="sxs-lookup"><span data-stu-id="4b829-647">X</span></span> | <span data-ttu-id="4b829-648">X</span><span class="sxs-lookup"><span data-stu-id="4b829-648">X</span></span> | \- | <span data-ttu-id="4b829-649">X</span><span class="sxs-lookup"><span data-stu-id="4b829-649">X</span></span> | <span data-ttu-id="4b829-650">Windows 10 versión 1809</span><span class="sxs-lookup"><span data-stu-id="4b829-650">Windows 10 Version 1809</span></span> |
| <span data-ttu-id="4b829-651">CARACTERÍSTICA HABILITAR OPCIÓN WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="4b829-651">WINHTTP\_OPTION\_ENABLE\_FEATURE</span></span><br/><span data-ttu-id="4b829-652">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-652">**DWORD**</span></span> | \* | \* | \- | <span data-ttu-id="4b829-653">X</span><span class="sxs-lookup"><span data-stu-id="4b829-653">X</span></span> | \- |
| <span data-ttu-id="4b829-654">OPCIÓN WINHTTP \_ HABILITAR \_ PROTOCOLO \_ \_ HTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-654">WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL</span></span><br/><span data-ttu-id="4b829-655">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-655">**DWORD**</span></span> | <span data-ttu-id="4b829-656">X</span><span class="sxs-lookup"><span data-stu-id="4b829-656">X</span></span> | <span data-ttu-id="4b829-657">X</span><span class="sxs-lookup"><span data-stu-id="4b829-657">X</span></span> | \- | <span data-ttu-id="4b829-658">X</span><span class="sxs-lookup"><span data-stu-id="4b829-658">X</span></span> | <span data-ttu-id="4b829-659">Windows 10 Versión 1607</span><span class="sxs-lookup"><span data-stu-id="4b829-659">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="4b829-660">HABILITACIÓN \_ DE LA OPCIÓN \_ WINHTTPTRACING</span><span class="sxs-lookup"><span data-stu-id="4b829-660">WINHTTP\_OPTION\_ENABLETRACING</span></span><br/><span data-ttu-id="4b829-661">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-661">**DWORD**</span></span> | \- | \- | <span data-ttu-id="4b829-662">X</span><span class="sxs-lookup"><span data-stu-id="4b829-662">X</span></span> | <span data-ttu-id="4b829-663">X</span><span class="sxs-lookup"><span data-stu-id="4b829-663">X</span></span> | \- |
| <span data-ttu-id="4b829-664">CODIFICACIÓN \_ ADICIONAL DE LA \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-664">WINHTTP\_OPTION\_ENCODE\_EXTRA</span></span><br/><span data-ttu-id="4b829-665">**Bool**</span><span class="sxs-lookup"><span data-stu-id="4b829-665">**BOOL**</span></span> | <span data-ttu-id="4b829-666">X</span><span class="sxs-lookup"><span data-stu-id="4b829-666">X</span></span> | <span data-ttu-id="4b829-667">X</span><span class="sxs-lookup"><span data-stu-id="4b829-667">X</span></span> | \- | <span data-ttu-id="4b829-668">X</span><span class="sxs-lookup"><span data-stu-id="4b829-668">X</span></span> | <span data-ttu-id="4b829-669">Windows 10 versión 1803</span><span class="sxs-lookup"><span data-stu-id="4b829-669">Windows 10 Version 1803</span></span> |
| <span data-ttu-id="4b829-670">LA OPCIÓN WINHTTP \_ \_ EXPIRA LA \_ CONEXIÓN</span><span class="sxs-lookup"><span data-stu-id="4b829-670">WINHTTP\_OPTION\_EXPIRE\_CONNECTION</span></span><br/><span data-ttu-id="4b829-671">N/D</span><span class="sxs-lookup"><span data-stu-id="4b829-671">N/A</span></span> | \- | <span data-ttu-id="4b829-672">X</span><span class="sxs-lookup"><span data-stu-id="4b829-672">X</span></span> | \- | <span data-ttu-id="4b829-673">X</span><span class="sxs-lookup"><span data-stu-id="4b829-673">X</span></span> | <span data-ttu-id="4b829-674">Windows 10 versión 1903</span><span class="sxs-lookup"><span data-stu-id="4b829-674">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="4b829-675">ERROR EXTENDIDO DE LA OPCIÓN WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="4b829-675">WINHTTP\_OPTION\_EXTENDED\_ERROR</span></span><br/><span data-ttu-id="4b829-676">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-676">**DWORD**</span></span> | <span data-ttu-id="4b829-677">X</span><span class="sxs-lookup"><span data-stu-id="4b829-677">X</span></span> | <span data-ttu-id="4b829-678">X</span><span class="sxs-lookup"><span data-stu-id="4b829-678">X</span></span> | <span data-ttu-id="4b829-679">X</span><span class="sxs-lookup"><span data-stu-id="4b829-679">X</span></span> | \- | \- |
| <span data-ttu-id="4b829-680">\_CREDS DE PROXY GLOBAL DE LA OPCIÓN \_ \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-680">WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS</span></span><br/>[<span data-ttu-id="4b829-681">**CREDS DE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="4b829-681">**WINHTTP\_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | <span data-ttu-id="4b829-682">X</span><span class="sxs-lookup"><span data-stu-id="4b829-682">X</span></span> | <span data-ttu-id="4b829-683">X</span><span class="sxs-lookup"><span data-stu-id="4b829-683">X</span></span> | \- | <span data-ttu-id="4b829-684">X</span><span class="sxs-lookup"><span data-stu-id="4b829-684">X</span></span> | \- |
| <span data-ttu-id="4b829-685">\_CREDS DE SERVIDOR GLOBAL DE LA OPCIÓN \_ \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-685">WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS</span></span><br/>[<span data-ttu-id="4b829-686">**WINHTTP \_ CREDS \_ EX**</span><span class="sxs-lookup"><span data-stu-id="4b829-686">**WINHTTP\_CREDS\_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | <span data-ttu-id="4b829-687">X</span><span class="sxs-lookup"><span data-stu-id="4b829-687">X</span></span> | <span data-ttu-id="4b829-688">X</span><span class="sxs-lookup"><span data-stu-id="4b829-688">X</span></span> | \- | <span data-ttu-id="4b829-689">X</span><span class="sxs-lookup"><span data-stu-id="4b829-689">X</span></span> | \- |
| <span data-ttu-id="4b829-690">TIPO DE IDENTIFICADOR \_ DE \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-690">WINHTTP\_OPTION\_HANDLE\_TYPE</span></span><br/><span data-ttu-id="4b829-691">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-691">**DWORD**</span></span> | <span data-ttu-id="4b829-692">X</span><span class="sxs-lookup"><span data-stu-id="4b829-692">X</span></span> | <span data-ttu-id="4b829-693">X</span><span class="sxs-lookup"><span data-stu-id="4b829-693">X</span></span> | <span data-ttu-id="4b829-694">X</span><span class="sxs-lookup"><span data-stu-id="4b829-694">X</span></span> | \- | \- |
| <span data-ttu-id="4b829-695">SE REQUIERE EL \_ PROTOCOLO HTTP DE LA OPCIÓN \_ \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-695">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED</span></span><br/><span data-ttu-id="4b829-696">**Bool**</span><span class="sxs-lookup"><span data-stu-id="4b829-696">**BOOL**</span></span> | <span data-ttu-id="4b829-697">X</span><span class="sxs-lookup"><span data-stu-id="4b829-697">X</span></span> | <span data-ttu-id="4b829-698">X</span><span class="sxs-lookup"><span data-stu-id="4b829-698">X</span></span> | \- | <span data-ttu-id="4b829-699">X</span><span class="sxs-lookup"><span data-stu-id="4b829-699">X</span></span> | <span data-ttu-id="4b829-700">Windows 10 versión 1903</span><span class="sxs-lookup"><span data-stu-id="4b829-700">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="4b829-701">OPCIÓN WINHTTP \_ \_ PROTOCOLO HTTP \_ \_ USADO</span><span class="sxs-lookup"><span data-stu-id="4b829-701">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED</span></span><br/><span data-ttu-id="4b829-702">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-702">**DWORD**</span></span> | \- | <span data-ttu-id="4b829-703">X</span><span class="sxs-lookup"><span data-stu-id="4b829-703">X</span></span> | <span data-ttu-id="4b829-704">X</span><span class="sxs-lookup"><span data-stu-id="4b829-704">X</span></span> | \- | <span data-ttu-id="4b829-705">Windows 10 Versión 1607</span><span class="sxs-lookup"><span data-stu-id="4b829-705">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="4b829-706">VERSIÓN HTTP DE \_ LA OPCIÓN \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-706">WINHTTP\_OPTION\_HTTP\_VERSION</span></span><br/>[<span data-ttu-id="4b829-707">**INFORMACIÓN \_ DE VERSIÓN \_ HTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-707">**HTTP\_VERSION\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | <span data-ttu-id="4b829-708">X</span><span class="sxs-lookup"><span data-stu-id="4b829-708">X</span></span> | <span data-ttu-id="4b829-709">X</span><span class="sxs-lookup"><span data-stu-id="4b829-709">X</span></span> | <span data-ttu-id="4b829-710">X</span><span class="sxs-lookup"><span data-stu-id="4b829-710">X</span></span> | <span data-ttu-id="4b829-711">X</span><span class="sxs-lookup"><span data-stu-id="4b829-711">X</span></span> | \- |
| <span data-ttu-id="4b829-712">OPCIÓN WINHTTP \_ OMITIR \_ \_ REVOCACIÓN \_ DE CERTIFICADOS \_ SIN CONEXIÓN</span><span class="sxs-lookup"><span data-stu-id="4b829-712">WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE</span></span><br/><span data-ttu-id="4b829-713">**Bool**</span><span class="sxs-lookup"><span data-stu-id="4b829-713">**BOOL**</span></span> | \- | <span data-ttu-id="4b829-714">X</span><span class="sxs-lookup"><span data-stu-id="4b829-714">X</span></span> | \- | <span data-ttu-id="4b829-715">X</span><span class="sxs-lookup"><span data-stu-id="4b829-715">X</span></span> | <span data-ttu-id="4b829-716">Windows 10 versión 2004</span><span class="sxs-lookup"><span data-stu-id="4b829-716">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="4b829-717">OPCIÓN WINHTTP \_ \_ IPV6 \_ FAST \_ FALLBACK</span><span class="sxs-lookup"><span data-stu-id="4b829-717">WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK</span></span><br/><span data-ttu-id="4b829-718">**Bool**</span><span class="sxs-lookup"><span data-stu-id="4b829-718">**BOOL**</span></span> | <span data-ttu-id="4b829-719">X</span><span class="sxs-lookup"><span data-stu-id="4b829-719">X</span></span> | \- | \- | <span data-ttu-id="4b829-720">X</span><span class="sxs-lookup"><span data-stu-id="4b829-720">X</span></span> | <span data-ttu-id="4b829-721">Windows 10 versión 1903</span><span class="sxs-lookup"><span data-stu-id="4b829-721">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="4b829-722">LA OPCIÓN WINHTTP \_ ES RESPUESTA DE CONEXIÓN DE \_ \_ \_ \_ PROXY</span><span class="sxs-lookup"><span data-stu-id="4b829-722">WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="4b829-723">**Bool**</span><span class="sxs-lookup"><span data-stu-id="4b829-723">**BOOL**</span></span> | <span data-ttu-id="4b829-724">X</span><span class="sxs-lookup"><span data-stu-id="4b829-724">X</span></span> | <span data-ttu-id="4b829-725">X</span><span class="sxs-lookup"><span data-stu-id="4b829-725">X</span></span> | <span data-ttu-id="4b829-726">X</span><span class="sxs-lookup"><span data-stu-id="4b829-726">X</span></span> | \- | \- |
| <span data-ttu-id="4b829-727">OPCIÓN WINHTTP \_ \_ NÚMERO MÁXIMO DE \_ CONN POR \_ \_ 1 \_ SERVIDOR 0 \_</span><span class="sxs-lookup"><span data-stu-id="4b829-727">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER</span></span><br/><span data-ttu-id="4b829-728">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-728">**DWORD**</span></span> | <span data-ttu-id="4b829-729">X</span><span class="sxs-lookup"><span data-stu-id="4b829-729">X</span></span> | \- | <span data-ttu-id="4b829-730">X</span><span class="sxs-lookup"><span data-stu-id="4b829-730">X</span></span> | <span data-ttu-id="4b829-731">X</span><span class="sxs-lookup"><span data-stu-id="4b829-731">X</span></span> | \- |
| <span data-ttu-id="4b829-732">OPCIÓN WINHTTP \_ \_ NÚMERO MÁXIMO DE \_ CONN POR \_ \_ SERVIDOR</span><span class="sxs-lookup"><span data-stu-id="4b829-732">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER</span></span><br/><span data-ttu-id="4b829-733">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-733">**DWORD**</span></span> | <span data-ttu-id="4b829-734">X</span><span class="sxs-lookup"><span data-stu-id="4b829-734">X</span></span> | \- | <span data-ttu-id="4b829-735">X</span><span class="sxs-lookup"><span data-stu-id="4b829-735">X</span></span> | <span data-ttu-id="4b829-736">X</span><span class="sxs-lookup"><span data-stu-id="4b829-736">X</span></span> | \- |
| <span data-ttu-id="4b829-737">OPCIÓN WINHTTP \_ \_ MAX HTTP AUTOMATIC \_ \_ \_ REDIRECTS</span><span class="sxs-lookup"><span data-stu-id="4b829-737">WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS</span></span><br/><span data-ttu-id="4b829-738">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-738">**DWORD**</span></span> | <span data-ttu-id="4b829-739">X</span><span class="sxs-lookup"><span data-stu-id="4b829-739">X</span></span> | <span data-ttu-id="4b829-740">X</span><span class="sxs-lookup"><span data-stu-id="4b829-740">X</span></span> | <span data-ttu-id="4b829-741">X</span><span class="sxs-lookup"><span data-stu-id="4b829-741">X</span></span> | <span data-ttu-id="4b829-742">X</span><span class="sxs-lookup"><span data-stu-id="4b829-742">X</span></span> | \- |
| <span data-ttu-id="4b829-743">OPCIÓN WINHTTP \_ \_ MAX HTTP STATUS \_ \_ \_ CONTINUE</span><span class="sxs-lookup"><span data-stu-id="4b829-743">WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE</span></span><br/><span data-ttu-id="4b829-744">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-744">**DWORD**</span></span> | <span data-ttu-id="4b829-745">X</span><span class="sxs-lookup"><span data-stu-id="4b829-745">X</span></span> | <span data-ttu-id="4b829-746">X</span><span class="sxs-lookup"><span data-stu-id="4b829-746">X</span></span> | <span data-ttu-id="4b829-747">X</span><span class="sxs-lookup"><span data-stu-id="4b829-747">X</span></span> | <span data-ttu-id="4b829-748">X</span><span class="sxs-lookup"><span data-stu-id="4b829-748">X</span></span> | \- |
| <span data-ttu-id="4b829-749">TAMAÑO MÁXIMO DE PURGA DE RESPUESTA DE LA \_ \_ \_ \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-749">WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE</span></span><br/><span data-ttu-id="4b829-750">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-750">**DWORD**</span></span> | <span data-ttu-id="4b829-751">X</span><span class="sxs-lookup"><span data-stu-id="4b829-751">X</span></span> | <span data-ttu-id="4b829-752">X</span><span class="sxs-lookup"><span data-stu-id="4b829-752">X</span></span> | <span data-ttu-id="4b829-753">X</span><span class="sxs-lookup"><span data-stu-id="4b829-753">X</span></span> | <span data-ttu-id="4b829-754">X</span><span class="sxs-lookup"><span data-stu-id="4b829-754">X</span></span> | \- |
| <span data-ttu-id="4b829-755">TAMAÑO MÁXIMO \_ DE ENCABEZADO DE RESPUESTA DE LA \_ \_ \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-755">WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE</span></span><br/><span data-ttu-id="4b829-756">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-756">**DWORD**</span></span> | <span data-ttu-id="4b829-757">X</span><span class="sxs-lookup"><span data-stu-id="4b829-757">X</span></span> | <span data-ttu-id="4b829-758">X</span><span class="sxs-lookup"><span data-stu-id="4b829-758">X</span></span> | <span data-ttu-id="4b829-759">X</span><span class="sxs-lookup"><span data-stu-id="4b829-759">X</span></span> | <span data-ttu-id="4b829-760">X</span><span class="sxs-lookup"><span data-stu-id="4b829-760">X</span></span> | \- |
| <span data-ttu-id="4b829-761">IDENTIFICADOR PRIMARIO DE \_ LA \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-761">WINHTTP\_OPTION\_PARENT\_HANDLE</span></span><br/>[<span data-ttu-id="4b829-762">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="4b829-762">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="4b829-763">X</span><span class="sxs-lookup"><span data-stu-id="4b829-763">X</span></span> | <span data-ttu-id="4b829-764">X</span><span class="sxs-lookup"><span data-stu-id="4b829-764">X</span></span> | <span data-ttu-id="4b829-765">X</span><span class="sxs-lookup"><span data-stu-id="4b829-765">X</span></span> | \- | \- |
| <span data-ttu-id="4b829-766">TEXTO DE MARCA DE PASSPORT DE LA \_ \_ \_ OPCIÓN WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="4b829-766">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT</span></span><br/><span data-ttu-id="4b829-767">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="4b829-767">**LPWSTR**</span></span> | \- | <span data-ttu-id="4b829-768">X</span><span class="sxs-lookup"><span data-stu-id="4b829-768">X</span></span> | <span data-ttu-id="4b829-769">X</span><span class="sxs-lookup"><span data-stu-id="4b829-769">X</span></span> | \- | \- |
| <span data-ttu-id="4b829-770">DIRECCIÓN URL DE \_ \_ COBRANDING DE LA OPCIÓN WINHTTP PASSPORT \_ \_</span><span class="sxs-lookup"><span data-stu-id="4b829-770">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL</span></span><br/><span data-ttu-id="4b829-771">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="4b829-771">**LPWSTR**</span></span> | \- | <span data-ttu-id="4b829-772">X</span><span class="sxs-lookup"><span data-stu-id="4b829-772">X</span></span> | <span data-ttu-id="4b829-773">X</span><span class="sxs-lookup"><span data-stu-id="4b829-773">X</span></span> | \- | \- |
| <span data-ttu-id="4b829-774">DIRECCIÓN URL DE \_ RETORNO DE PASSPORT DE LA \_ OPCIÓN WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="4b829-774">WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL</span></span><br/><span data-ttu-id="4b829-775">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="4b829-775">**LPVOID**</span></span> | \- | <span data-ttu-id="4b829-776">X</span><span class="sxs-lookup"><span data-stu-id="4b829-776">X</span></span> | <span data-ttu-id="4b829-777">X</span><span class="sxs-lookup"><span data-stu-id="4b829-777">X</span></span> | \- | \- |
| <span data-ttu-id="4b829-778">OPCIÓN WINHTTP \_ \_ PASSPORT SIGN \_ \_ OUT</span><span class="sxs-lookup"><span data-stu-id="4b829-778">WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT</span></span><br/><span data-ttu-id="4b829-779">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="4b829-779">**LPVOID**</span></span> | <span data-ttu-id="4b829-780">X</span><span class="sxs-lookup"><span data-stu-id="4b829-780">X</span></span> | \- | \- | <span data-ttu-id="4b829-781">X</span><span class="sxs-lookup"><span data-stu-id="4b829-781">X</span></span> | \- |
| <span data-ttu-id="4b829-782">CONTRASEÑA DE LA OPCIÓN WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="4b829-782">WINHTTP\_OPTION\_PASSWORD</span></span><br/><span data-ttu-id="4b829-783">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="4b829-783">**LPWSTR**</span></span> | \- | <span data-ttu-id="4b829-784">X</span><span class="sxs-lookup"><span data-stu-id="4b829-784">X</span></span> | <span data-ttu-id="4b829-785">X</span><span class="sxs-lookup"><span data-stu-id="4b829-785">X</span></span> | <span data-ttu-id="4b829-786">X</span><span class="sxs-lookup"><span data-stu-id="4b829-786">X</span></span> | \- |
| <span data-ttu-id="4b829-787">PROXY DE \_ OPCIÓN WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="4b829-787">WINHTTP\_OPTION\_PROXY</span></span><br/>[<span data-ttu-id="4b829-788">**INFORMACIÓN DEL \_ PROXY \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-788">**WINHTTP\_PROXY\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | <span data-ttu-id="4b829-789">X</span><span class="sxs-lookup"><span data-stu-id="4b829-789">X</span></span> | <span data-ttu-id="4b829-790">X</span><span class="sxs-lookup"><span data-stu-id="4b829-790">X</span></span> | <span data-ttu-id="4b829-791">X</span><span class="sxs-lookup"><span data-stu-id="4b829-791">X</span></span> | <span data-ttu-id="4b829-792">X</span><span class="sxs-lookup"><span data-stu-id="4b829-792">X</span></span> | \- |
| <span data-ttu-id="4b829-793">CONTRASEÑA DE \_ PROXY DE \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-793">WINHTTP\_OPTION\_PROXY\_PASSWORD</span></span><br/><span data-ttu-id="4b829-794">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="4b829-794">**LPWSTR**</span></span> | \- | <span data-ttu-id="4b829-795">X</span><span class="sxs-lookup"><span data-stu-id="4b829-795">X</span></span> | <span data-ttu-id="4b829-796">X</span><span class="sxs-lookup"><span data-stu-id="4b829-796">X</span></span> | <span data-ttu-id="4b829-797">X</span><span class="sxs-lookup"><span data-stu-id="4b829-797">X</span></span> | \- |
| <span data-ttu-id="4b829-798">SPN DE \_ \_ PROXY DE OPCIÓN \_ WINHTTP \_ USADO</span><span class="sxs-lookup"><span data-stu-id="4b829-798">WINHTTP\_OPTION\_PROXY\_SPN\_USED</span></span><br/><span data-ttu-id="4b829-799">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="4b829-799">**LPWSTR**</span></span> | \- | <span data-ttu-id="4b829-800">X</span><span class="sxs-lookup"><span data-stu-id="4b829-800">X</span></span> | <span data-ttu-id="4b829-801">X</span><span class="sxs-lookup"><span data-stu-id="4b829-801">X</span></span> | \- | \- |
| <span data-ttu-id="4b829-802">NOMBRE DE USUARIO \_ DEL PROXY DE OPCIÓN \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-802">WINHTTP\_OPTION\_PROXY\_USERNAME</span></span><br/><span data-ttu-id="4b829-803">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="4b829-803">**LPWSTR**</span></span> | \- | <span data-ttu-id="4b829-804">X</span><span class="sxs-lookup"><span data-stu-id="4b829-804">X</span></span> | <span data-ttu-id="4b829-805">X</span><span class="sxs-lookup"><span data-stu-id="4b829-805">X</span></span> | <span data-ttu-id="4b829-806">X</span><span class="sxs-lookup"><span data-stu-id="4b829-806">X</span></span> | \- |
| <span data-ttu-id="4b829-807">TAMAÑO DEL BÚFER \_ DE LECTURA DE LA \_ \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-807">WINHTTP\_OPTION\_READ\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="4b829-808">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-808">**DWORD**</span></span> | \- | <span data-ttu-id="4b829-809">X</span><span class="sxs-lookup"><span data-stu-id="4b829-809">X</span></span> | <span data-ttu-id="4b829-810">X</span><span class="sxs-lookup"><span data-stu-id="4b829-810">X</span></span> | <span data-ttu-id="4b829-811">X</span><span class="sxs-lookup"><span data-stu-id="4b829-811">X</span></span> | \- |
| <span data-ttu-id="4b829-812">RESPUESTA DE CONEXIÓN DE \_ PROXY DE RECEPCIÓN DE LA OPCIÓN \_ \_ \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-812">WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="4b829-813">**Bool**</span><span class="sxs-lookup"><span data-stu-id="4b829-813">**BOOL**</span></span> | <span data-ttu-id="4b829-814">X</span><span class="sxs-lookup"><span data-stu-id="4b829-814">X</span></span> | <span data-ttu-id="4b829-815">X</span><span class="sxs-lookup"><span data-stu-id="4b829-815">X</span></span> | \- | <span data-ttu-id="4b829-816">X</span><span class="sxs-lookup"><span data-stu-id="4b829-816">X</span></span> | \- |
| <span data-ttu-id="4b829-817">TIEMPO DE ESPERA \_ DE RESPUESTA DE RECEPCIÓN DE LA OPCIÓN \_ \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-817">WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT</span></span><br/><span data-ttu-id="4b829-818">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-818">**DWORD**</span></span> | <span data-ttu-id="4b829-819">X</span><span class="sxs-lookup"><span data-stu-id="4b829-819">X</span></span> | <span data-ttu-id="4b829-820">X</span><span class="sxs-lookup"><span data-stu-id="4b829-820">X</span></span> | <span data-ttu-id="4b829-821">X</span><span class="sxs-lookup"><span data-stu-id="4b829-821">X</span></span> | <span data-ttu-id="4b829-822">X</span><span class="sxs-lookup"><span data-stu-id="4b829-822">X</span></span> | \- |
| <span data-ttu-id="4b829-823">TIEMPO DE ESPERA \_ DE RECEPCIÓN DE LA OPCIÓN \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-823">WINHTTP\_OPTION\_RECEIVE\_TIMEOUT</span></span><br/><span data-ttu-id="4b829-824">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-824">**DWORD**</span></span> | <span data-ttu-id="4b829-825">X</span><span class="sxs-lookup"><span data-stu-id="4b829-825">X</span></span> | <span data-ttu-id="4b829-826">X</span><span class="sxs-lookup"><span data-stu-id="4b829-826">X</span></span> | <span data-ttu-id="4b829-827">X</span><span class="sxs-lookup"><span data-stu-id="4b829-827">X</span></span> | <span data-ttu-id="4b829-828">X</span><span class="sxs-lookup"><span data-stu-id="4b829-828">X</span></span> | \- |
| <span data-ttu-id="4b829-829">DIRECTIVA DE REDIRECCIÓN \_ DE \_ OPCIONES \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-829">WINHTTP\_OPTION\_REDIRECT\_POLICY</span></span><br/><span data-ttu-id="4b829-830">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-830">**DWORD**</span></span> | <span data-ttu-id="4b829-831">X</span><span class="sxs-lookup"><span data-stu-id="4b829-831">X</span></span> | <span data-ttu-id="4b829-832">X</span><span class="sxs-lookup"><span data-stu-id="4b829-832">X</span></span> | <span data-ttu-id="4b829-833">X</span><span class="sxs-lookup"><span data-stu-id="4b829-833">X</span></span> | <span data-ttu-id="4b829-834">X</span><span class="sxs-lookup"><span data-stu-id="4b829-834">X</span></span> | \- |
| <span data-ttu-id="4b829-835">OPCIÓN WINHTTP \_ \_ RECHAZAR \_ USERPWD \_ EN LA DIRECCIÓN \_ URL</span><span class="sxs-lookup"><span data-stu-id="4b829-835">WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL</span></span><br/><span data-ttu-id="4b829-836">**Bool**</span><span class="sxs-lookup"><span data-stu-id="4b829-836">**BOOL**</span></span> | \- | <span data-ttu-id="4b829-837">X</span><span class="sxs-lookup"><span data-stu-id="4b829-837">X</span></span> | \- | <span data-ttu-id="4b829-838">X</span><span class="sxs-lookup"><span data-stu-id="4b829-838">X</span></span> | \- |
| <span data-ttu-id="4b829-839">PRIORIDAD DE \_ SOLICITUD DE LA OPCIÓN \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-839">WINHTTP\_OPTION\_REQUEST\_PRIORITY</span></span><br/><span data-ttu-id="4b829-840">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-840">**DWORD**</span></span> | \- | <span data-ttu-id="4b829-841">X</span><span class="sxs-lookup"><span data-stu-id="4b829-841">X</span></span> | <span data-ttu-id="4b829-842">X</span><span class="sxs-lookup"><span data-stu-id="4b829-842">X</span></span> | <span data-ttu-id="4b829-843">X</span><span class="sxs-lookup"><span data-stu-id="4b829-843">X</span></span> | \- |
| <span data-ttu-id="4b829-844">ESTADÍSTICAS DE \_ SOLICITUD DE LA OPCIÓN \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-844">WINHTTP\_OPTION\_REQUEST\_STATS</span></span><br/>[<span data-ttu-id="4b829-845">**ESTADÍSTICAS DE \_ SOLICITUDES \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-845">**WINHTTP\_REQUEST\_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | <span data-ttu-id="4b829-846">X</span><span class="sxs-lookup"><span data-stu-id="4b829-846">X</span></span> | <span data-ttu-id="4b829-847">X</span><span class="sxs-lookup"><span data-stu-id="4b829-847">X</span></span> | \- | <span data-ttu-id="4b829-848">Windows 10 versión 1903</span><span class="sxs-lookup"><span data-stu-id="4b829-848">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="4b829-849">TIEMPOS DE SOLICITUD \_ DE \_ LA OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-849">WINHTTP\_OPTION\_REQUEST\_TIMES</span></span><br/>[<span data-ttu-id="4b829-850">**TIEMPOS DE \_ SOLICITUD \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-850">**WINHTTP\_REQUEST\_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | <span data-ttu-id="4b829-851">X</span><span class="sxs-lookup"><span data-stu-id="4b829-851">X</span></span> | <span data-ttu-id="4b829-852">X</span><span class="sxs-lookup"><span data-stu-id="4b829-852">X</span></span> | \- | <span data-ttu-id="4b829-853">Windows 10 versión 1903</span><span class="sxs-lookup"><span data-stu-id="4b829-853">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="4b829-854">OPCIÓN WINHTTP \_ RESOLVER \_ TIEMPO DE \_ ESPERA</span><span class="sxs-lookup"><span data-stu-id="4b829-854">WINHTTP\_OPTION\_RESOLVE\_TIMEOUT</span></span><br/><span data-ttu-id="4b829-855">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-855">**DWORD**</span></span> | <span data-ttu-id="4b829-856">X</span><span class="sxs-lookup"><span data-stu-id="4b829-856">X</span></span> | <span data-ttu-id="4b829-857">X</span><span class="sxs-lookup"><span data-stu-id="4b829-857">X</span></span> | <span data-ttu-id="4b829-858">X</span><span class="sxs-lookup"><span data-stu-id="4b829-858">X</span></span> | <span data-ttu-id="4b829-859">X</span><span class="sxs-lookup"><span data-stu-id="4b829-859">X</span></span> | \- |
| <span data-ttu-id="4b829-860">PROTOCOLOS SEGUROS \_ DE \_ LA OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-860">WINHTTP\_OPTION\_SECURE\_PROTOCOLS</span></span><br/><span data-ttu-id="4b829-861">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-861">**DWORD**</span></span> | <span data-ttu-id="4b829-862">X</span><span class="sxs-lookup"><span data-stu-id="4b829-862">X</span></span> | \- | \- | <span data-ttu-id="4b829-863">X</span><span class="sxs-lookup"><span data-stu-id="4b829-863">X</span></span> | \- |
| <span data-ttu-id="4b829-864">ESTRUCTURA DE \_ CERTIFICADO DE SEGURIDAD DE LA OPCIÓN \_ \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-864">WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT</span></span><br/>[<span data-ttu-id="4b829-865">**INFORMACIÓN DEL \_ CERTIFICADO \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="4b829-865">**WINHTTP\_CERTIFICATE\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | <span data-ttu-id="4b829-866">X</span><span class="sxs-lookup"><span data-stu-id="4b829-866">X</span></span> | <span data-ttu-id="4b829-867">X</span><span class="sxs-lookup"><span data-stu-id="4b829-867">X</span></span> | \- | \- |
| <span data-ttu-id="4b829-868">MARCAS DE \_ SEGURIDAD DE \_ LA \_ OPCIÓN WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-868">WINHTTP\_OPTION\_SECURITY\_FLAGS</span></span><br/><span data-ttu-id="4b829-869">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-869">**DWORD**</span></span> | \- | <span data-ttu-id="4b829-870">X</span><span class="sxs-lookup"><span data-stu-id="4b829-870">X</span></span> | <span data-ttu-id="4b829-871">X</span><span class="sxs-lookup"><span data-stu-id="4b829-871">X</span></span> | <span data-ttu-id="4b829-872">X</span><span class="sxs-lookup"><span data-stu-id="4b829-872">X</span></span> | \- |
| <span data-ttu-id="4b829-873">INFORMACIÓN DE \_ SEGURIDAD DE LA OPCIÓN \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-873">WINHTTP\_OPTION\_SECURITY\_INFO</span></span><br/>[<span data-ttu-id="4b829-874">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="4b829-874">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | <span data-ttu-id="4b829-875">X</span><span class="sxs-lookup"><span data-stu-id="4b829-875">X</span></span> | <span data-ttu-id="4b829-876">X</span><span class="sxs-lookup"><span data-stu-id="4b829-876">X</span></span> | \- | <span data-ttu-id="4b829-877">Windows 10 versión 2004</span><span class="sxs-lookup"><span data-stu-id="4b829-877">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="4b829-878">VALOR DE BITS \_ DE CLAVE DE SEGURIDAD DE LA OPCIÓN \_ \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-878">WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS</span></span><br/><span data-ttu-id="4b829-879">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-879">**DWORD**</span></span> | \- | <span data-ttu-id="4b829-880">X</span><span class="sxs-lookup"><span data-stu-id="4b829-880">X</span></span> | <span data-ttu-id="4b829-881">X</span><span class="sxs-lookup"><span data-stu-id="4b829-881">X</span></span> | \- | \- |
| <span data-ttu-id="4b829-882">TIEMPO DE ESPERA \_ DE ENVÍO DE LA OPCIÓN \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-882">WINHTTP\_OPTION\_SEND\_TIMEOUT</span></span><br/><span data-ttu-id="4b829-883">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-883">**DWORD**</span></span> | <span data-ttu-id="4b829-884">X</span><span class="sxs-lookup"><span data-stu-id="4b829-884">X</span></span> | <span data-ttu-id="4b829-885">X</span><span class="sxs-lookup"><span data-stu-id="4b829-885">X</span></span> | <span data-ttu-id="4b829-886">X</span><span class="sxs-lookup"><span data-stu-id="4b829-886">X</span></span> | <span data-ttu-id="4b829-887">X</span><span class="sxs-lookup"><span data-stu-id="4b829-887">X</span></span> | \- |
| <span data-ttu-id="4b829-888">WINHTTP \_ OPTION \_ SERVER \_ CBT</span><span class="sxs-lookup"><span data-stu-id="4b829-888">WINHTTP\_OPTION\_SERVER\_CBT</span></span><br/><span data-ttu-id="4b829-889">[**Enlaces \_ SecPkgContext**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span><span class="sxs-lookup"><span data-stu-id="4b829-889">[**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span></span> | \- | <span data-ttu-id="4b829-890">X</span><span class="sxs-lookup"><span data-stu-id="4b829-890">X</span></span> | <span data-ttu-id="4b829-891">X</span><span class="sxs-lookup"><span data-stu-id="4b829-891">X</span></span> | \- | \- |
| <span data-ttu-id="4b829-892">CONTEXTO DE CADENA \_ DE CERTIFICADOS DE SERVIDOR DE OPCIÓN \_ \_ \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-892">WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT</span></span><br/>[<span data-ttu-id="4b829-893">**CERT_CHAIN_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="4b829-893">**CERT_CHAIN_CONTEXT**</span></span>](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | <span data-ttu-id="4b829-894">X</span><span class="sxs-lookup"><span data-stu-id="4b829-894">X</span></span> | <span data-ttu-id="4b829-895">X</span><span class="sxs-lookup"><span data-stu-id="4b829-895">X</span></span> | \- | <span data-ttu-id="4b829-896">Windows 10 versión 2004</span><span class="sxs-lookup"><span data-stu-id="4b829-896">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="4b829-897">CONTEXTO DE \_ CERTIFICADO DE SERVIDOR DE LA OPCIÓN \_ \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-897">WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="4b829-898">**CONTEXTO DE CERTIFICADO**</span><span class="sxs-lookup"><span data-stu-id="4b829-898">**CERT CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="4b829-899">X</span><span class="sxs-lookup"><span data-stu-id="4b829-899">X</span></span> | <span data-ttu-id="4b829-900">X</span><span class="sxs-lookup"><span data-stu-id="4b829-900">X</span></span> | \- | \- |
| <span data-ttu-id="4b829-901">OPCIÓN WINHTTP \_ \_ SERVIDOR \_ SPN \_ USADO</span><span class="sxs-lookup"><span data-stu-id="4b829-901">WINHTTP\_OPTION\_SERVER\_SPN\_USED</span></span><br/><span data-ttu-id="4b829-902">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="4b829-902">**LPWSTR**</span></span> | \- | <span data-ttu-id="4b829-903">X</span><span class="sxs-lookup"><span data-stu-id="4b829-903">X</span></span> | <span data-ttu-id="4b829-904">X</span><span class="sxs-lookup"><span data-stu-id="4b829-904">X</span></span> | \- | \- |
| <span data-ttu-id="4b829-905">SPN DE \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-905">WINHTTP\_OPTION\_SPN</span></span><br/><span data-ttu-id="4b829-906">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-906">**DWORD**</span></span> | \- | <span data-ttu-id="4b829-907">X</span><span class="sxs-lookup"><span data-stu-id="4b829-907">X</span></span> | \- | <span data-ttu-id="4b829-908">X</span><span class="sxs-lookup"><span data-stu-id="4b829-908">X</span></span> | \- |
| <span data-ttu-id="4b829-909">OPCIÓN WINHTTP \_ \_ TCP FAST \_ \_ OPEN</span><span class="sxs-lookup"><span data-stu-id="4b829-909">WINHTTP\_OPTION\_TCP\_FAST\_OPEN</span></span><br/><span data-ttu-id="4b829-910">**Bool**</span><span class="sxs-lookup"><span data-stu-id="4b829-910">**BOOL**</span></span> | <span data-ttu-id="4b829-911">X</span><span class="sxs-lookup"><span data-stu-id="4b829-911">X</span></span> | \- | \- | <span data-ttu-id="4b829-912">X</span><span class="sxs-lookup"><span data-stu-id="4b829-912">X</span></span> | <span data-ttu-id="4b829-913">Windows 10 versión 2004</span><span class="sxs-lookup"><span data-stu-id="4b829-913">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="4b829-914">OPCIÓN WINHTTP \_ \_ TCP \_ KEEPALIVE</span><span class="sxs-lookup"><span data-stu-id="4b829-914">WINHTTP\_OPTION\_TCP\_KEEPALIVE</span></span><br/>[<span data-ttu-id="4b829-915">**tcp \_ keepalive**</span><span class="sxs-lookup"><span data-stu-id="4b829-915">**tcp\_keepalive**</span></span>](/windows/win32/winsock/sio-keepalive-vals) | <span data-ttu-id="4b829-916">X</span><span class="sxs-lookup"><span data-stu-id="4b829-916">X</span></span> | \- | \- | <span data-ttu-id="4b829-917">X</span><span class="sxs-lookup"><span data-stu-id="4b829-917">X</span></span> | <span data-ttu-id="4b829-918">Windows 10 versión 2004</span><span class="sxs-lookup"><span data-stu-id="4b829-918">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="4b829-919">OPCIÓN WINHTTP \_ \_ TLS FALSE \_ \_ START</span><span class="sxs-lookup"><span data-stu-id="4b829-919">WINHTTP\_OPTION\_TLS\_FALSE\_START</span></span><br/><span data-ttu-id="4b829-920">**Bool**</span><span class="sxs-lookup"><span data-stu-id="4b829-920">**BOOL**</span></span> | <span data-ttu-id="4b829-921">X</span><span class="sxs-lookup"><span data-stu-id="4b829-921">X</span></span> | \- | \- | <span data-ttu-id="4b829-922">X</span><span class="sxs-lookup"><span data-stu-id="4b829-922">X</span></span> | <span data-ttu-id="4b829-923">Windows 10 versión 2004</span><span class="sxs-lookup"><span data-stu-id="4b829-923">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="4b829-924">EVENTO DE NOTIFICACIÓN DE \_ DESCARGA DE LA OPCIÓN \_ WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="4b829-924">WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT</span></span><br/>[<span data-ttu-id="4b829-925">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="4b829-925">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="4b829-926">X</span><span class="sxs-lookup"><span data-stu-id="4b829-926">X</span></span> | \- | \- | <span data-ttu-id="4b829-927">X</span><span class="sxs-lookup"><span data-stu-id="4b829-927">X</span></span> | \- |
| <span data-ttu-id="4b829-928">ANÁLISIS DE ENCABEZADOS NO SEGUROS DE LA \_ \_ \_ \_ OPCIÓN WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-928">WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING</span></span><br/><span data-ttu-id="4b829-929">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-929">**DWORD**</span></span> | \- | <span data-ttu-id="4b829-930">X</span><span class="sxs-lookup"><span data-stu-id="4b829-930">X</span></span> | \- | <span data-ttu-id="4b829-931">X</span><span class="sxs-lookup"><span data-stu-id="4b829-931">X</span></span> | \- |
| <span data-ttu-id="4b829-932">ACTUALIZACIÓN DE LA OPCIÓN WINHTTP \_ \_ AL SOCKET \_ \_ \_ WEB</span><span class="sxs-lookup"><span data-stu-id="4b829-932">WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET</span></span><br/><span data-ttu-id="4b829-933">N/D</span><span class="sxs-lookup"><span data-stu-id="4b829-933">N/A</span></span> | \- | <span data-ttu-id="4b829-934">X</span><span class="sxs-lookup"><span data-stu-id="4b829-934">X</span></span> | \- | <span data-ttu-id="4b829-935">X</span><span class="sxs-lookup"><span data-stu-id="4b829-935">X</span></span> | \- |
| <span data-ttu-id="4b829-936">DIRECCIÓN URL DE LA OPCIÓN WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="4b829-936">WINHTTP\_OPTION\_URL</span></span><br/><span data-ttu-id="4b829-937">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="4b829-937">**LPWSTR**</span></span> | \- | <span data-ttu-id="4b829-938">X</span><span class="sxs-lookup"><span data-stu-id="4b829-938">X</span></span> | <span data-ttu-id="4b829-939">X</span><span class="sxs-lookup"><span data-stu-id="4b829-939">X</span></span> | \- | \- |
| <span data-ttu-id="4b829-940">OPCIÓN WINHTTP \_ USAR CREDENCIALES DE SERVIDOR \_ \_ \_ \_ GLOBAL</span><span class="sxs-lookup"><span data-stu-id="4b829-940">WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS</span></span><br/><span data-ttu-id="4b829-941">**Bool**</span><span class="sxs-lookup"><span data-stu-id="4b829-941">**BOOL**</span></span> | <span data-ttu-id="4b829-942">X</span><span class="sxs-lookup"><span data-stu-id="4b829-942">X</span></span> | <span data-ttu-id="4b829-943">X</span><span class="sxs-lookup"><span data-stu-id="4b829-943">X</span></span> | \- | <span data-ttu-id="4b829-944">X</span><span class="sxs-lookup"><span data-stu-id="4b829-944">X</span></span> | \- |
| <span data-ttu-id="4b829-945">AGENTE DE USUARIO \_ DE LA \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-945">WINHTTP\_OPTION\_USER\_AGENT</span></span><br/><span data-ttu-id="4b829-946">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="4b829-946">**LPWSTR**</span></span> | <span data-ttu-id="4b829-947">X</span><span class="sxs-lookup"><span data-stu-id="4b829-947">X</span></span> | \- | <span data-ttu-id="4b829-948">X</span><span class="sxs-lookup"><span data-stu-id="4b829-948">X</span></span> | <span data-ttu-id="4b829-949">X</span><span class="sxs-lookup"><span data-stu-id="4b829-949">X</span></span> | \- |
| <span data-ttu-id="4b829-950">NOMBRE DE USUARIO DE LA OPCIÓN WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="4b829-950">WINHTTP\_OPTION\_USERNAME</span></span><br/><span data-ttu-id="4b829-951">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="4b829-951">**LPWSTR**</span></span> | \- | <span data-ttu-id="4b829-952">X</span><span class="sxs-lookup"><span data-stu-id="4b829-952">X</span></span> | <span data-ttu-id="4b829-953">X</span><span class="sxs-lookup"><span data-stu-id="4b829-953">X</span></span> | <span data-ttu-id="4b829-954">X</span><span class="sxs-lookup"><span data-stu-id="4b829-954">X</span></span> | \- |
| <span data-ttu-id="4b829-955">TIEMPO DE ESPERA \_ DE CIERRE DE SOCKET WEB DE LA \_ \_ \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-955">WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT</span></span><br/><span data-ttu-id="4b829-956">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-956">**DWORD**</span></span> | \- | \- | <span data-ttu-id="4b829-957">X</span><span class="sxs-lookup"><span data-stu-id="4b829-957">X</span></span> | <span data-ttu-id="4b829-958">X</span><span class="sxs-lookup"><span data-stu-id="4b829-958">X</span></span> | \- |
| <span data-ttu-id="4b829-959">OPCIÓN WINHTTP \_ \_ WEB SOCKET \_ \_ \_ KEEPALIVE INTERVAL</span><span class="sxs-lookup"><span data-stu-id="4b829-959">WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL</span></span><br/><span data-ttu-id="4b829-960">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-960">**DWORD**</span></span> | \- | \- | <span data-ttu-id="4b829-961">X</span><span class="sxs-lookup"><span data-stu-id="4b829-961">X</span></span> | <span data-ttu-id="4b829-962">X</span><span class="sxs-lookup"><span data-stu-id="4b829-962">X</span></span> | \- |
| <span data-ttu-id="4b829-963">TAMAÑO DEL BÚFER DE RECEPCIÓN DE LA OPCIÓN WINHTTP \_ \_ WEB \_ SOCKET \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="4b829-963">WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="4b829-964">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-964">**DWORD**</span></span> | <span data-ttu-id="4b829-965">X</span><span class="sxs-lookup"><span data-stu-id="4b829-965">X</span></span> | <span data-ttu-id="4b829-966">X</span><span class="sxs-lookup"><span data-stu-id="4b829-966">X</span></span> | <span data-ttu-id="4b829-967">X</span><span class="sxs-lookup"><span data-stu-id="4b829-967">X</span></span> | <span data-ttu-id="4b829-968">X</span><span class="sxs-lookup"><span data-stu-id="4b829-968">X</span></span> | <span data-ttu-id="4b829-969">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4b829-969">Windows 8.1</span></span> |
| <span data-ttu-id="4b829-970">TAMAÑO DEL BÚFER DE ENVÍO DE SOCKET WEB DE LA \_ \_ \_ \_ \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-970">WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="4b829-971">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-971">**DWORD**</span></span> | <span data-ttu-id="4b829-972">X</span><span class="sxs-lookup"><span data-stu-id="4b829-972">X</span></span> | <span data-ttu-id="4b829-973">X</span><span class="sxs-lookup"><span data-stu-id="4b829-973">X</span></span> | <span data-ttu-id="4b829-974">X</span><span class="sxs-lookup"><span data-stu-id="4b829-974">X</span></span> | <span data-ttu-id="4b829-975">X</span><span class="sxs-lookup"><span data-stu-id="4b829-975">X</span></span> | <span data-ttu-id="4b829-976">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4b829-976">Windows 8.1</span></span> |
| <span data-ttu-id="4b829-977">RECUENTO DE \_ SUBPROCESOS \_ DE TRABAJO DE LA \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-977">WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT</span></span><br/><span data-ttu-id="4b829-978">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-978">**DWORD**</span></span> | \- | \- | \- | <span data-ttu-id="4b829-979">X</span><span class="sxs-lookup"><span data-stu-id="4b829-979">X</span></span> | \- |
| <span data-ttu-id="4b829-980">TAMAÑO DEL BÚFER \_ DE ESCRITURA DE LA \_ \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-980">WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="4b829-981">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="4b829-981">**DWORD**</span></span> | \- | <span data-ttu-id="4b829-982">X</span><span class="sxs-lookup"><span data-stu-id="4b829-982">X</span></span> | <span data-ttu-id="4b829-983">X</span><span class="sxs-lookup"><span data-stu-id="4b829-983">X</span></span> | <span data-ttu-id="4b829-984">X</span><span class="sxs-lookup"><span data-stu-id="4b829-984">X</span></span> | \- |

> [!Note]
> <span data-ttu-id="4b829-985">Para Windows XP y Windows 2000, consulte [Requisitos en tiempo de ejecución.](winhttp-start-page.md)</span><span class="sxs-lookup"><span data-stu-id="4b829-985">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b829-986">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b829-986">Requirements</span></span>

| <span data-ttu-id="4b829-987">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b829-987">Requirement</span></span> | <span data-ttu-id="4b829-988">Valor</span><span class="sxs-lookup"><span data-stu-id="4b829-988">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4b829-989">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b829-989">Minimum supported client</span></span> | <span data-ttu-id="4b829-990">Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio sp3 \[\]</span><span class="sxs-lookup"><span data-stu-id="4b829-990">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>            |
| <span data-ttu-id="4b829-991">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b829-991">Minimum supported server</span></span> | <span data-ttu-id="4b829-992">Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="4b829-992">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>         |
| <span data-ttu-id="4b829-993">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="4b829-993">Redistributable</span></span>          | <span data-ttu-id="4b829-994">WinHTTP 5.0 y Internet Explorer 5.01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4b829-994">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span> |
| <span data-ttu-id="4b829-995">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b829-995">Header</span></span>                   | <span data-ttu-id="4b829-996">Winhttp.h</span><span class="sxs-lookup"><span data-stu-id="4b829-996">Winhttp.h</span></span>                                                                       |

## <a name="see-also"></a><span data-ttu-id="4b829-997">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b829-997">See also</span></span>

[<span data-ttu-id="4b829-998">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4b829-998">WinHTTP Versions</span></span>](winhttp-versions.md)

---
Description: Las marcas de opción siguientes son compatibles con WinHttpQueryOption y WinHttpSetOption.
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: Marcas de opción (Winhttp.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: 25049ee11c59c6b320b794c07bd65e5ec9b930c9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395420"
---
# <a name="option-flags"></a><span data-ttu-id="49ba8-103">Marcas de opción</span><span class="sxs-lookup"><span data-stu-id="49ba8-103">Option Flags</span></span>

<span data-ttu-id="49ba8-104">Las marcas de opción siguientes son compatibles [**con WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) y [**WinHttpSetOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)</span><span class="sxs-lookup"><span data-stu-id="49ba8-104">The following option flags are supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span>

<dl> <dt>

<span data-ttu-id="49ba8-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**OPCIÓN WINHTTP \_ QUE GARANTIZA DEVOLUCIONES DE LLAMADA SIN \_ \_ \_ \_ BLOQUEO**</span><span class="sxs-lookup"><span data-stu-id="49ba8-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-106">El valor predeterminado es FALSE.</span><span class="sxs-lookup"><span data-stu-id="49ba8-106">The default is FALSE.</span></span> <span data-ttu-id="49ba8-107">Si se establece en TRUE, WinHTTP no garantiza el progreso si la aplicación cliente bloquea las devoluciones de llamada de estado.</span><span class="sxs-lookup"><span data-stu-id="49ba8-107">If set to TRUE, WinHTTP does not guarantee progress if status callbacks are blocked by the client application.</span></span>

<span data-ttu-id="49ba8-108">La aplicación cliente debe tener especial cuidado para realizar operaciones mínimas dentro de la devolución de llamada sin bloqueo, devolviendo lo antes posible y, en concreto, no debe esperar ninguna llamada WinHTTP posterior.</span><span class="sxs-lookup"><span data-stu-id="49ba8-108">The client application must take special care to perform minimal operations within the callback without blocking, returning as quickly as possible, and in particular must not wait for any subsequent WinHTTP calls.</span></span> <span data-ttu-id="49ba8-109">Si no sigue estas directrices, es probable que haya un impacto negativo en el rendimiento o que una posible aplicación se desasoye.</span><span class="sxs-lookup"><span data-stu-id="49ba8-109">If it does not follow these guidelines, there is likely to be a negative performance impact or a potential application hang.</span></span> <span data-ttu-id="49ba8-110">Si se usa de la manera prescrita, esta opción puede mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="49ba8-110">If used in the prescribed manner, this option may improve performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**DIRECTIVA DE \_ INICIO DE SESIÓN AUTOMÁTICO DE LA OPCIÓN \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-112">Establece un valor entero largo sin signo que especifica la directiva [de inicio](authentication-in-winhttp.md) de sesión automático con uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="49ba8-112">Sets an unsigned long integer value that specifies the [Automatic Logon Policy](authentication-in-winhttp.md) with one of the following values.</span></span>

| <span data-ttu-id="49ba8-113">Término</span><span class="sxs-lookup"><span data-stu-id="49ba8-113">Term</span></span> | <span data-ttu-id="49ba8-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="49ba8-114">Description</span></span> |
|-|-|
| <span data-ttu-id="49ba8-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>NIVEL DE \_ SEGURIDAD ALTO DE WINHTTP AUTOLOGON \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH</span></span> | <span data-ttu-id="49ba8-116">No se usan credenciales predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="49ba8-116">Default credentials are not used.</span></span> <span data-ttu-id="49ba8-117">Tenga en cuenta que esta marca solo tiene efecto si especifica el servidor por el nombre real de la máquina.</span><span class="sxs-lookup"><span data-stu-id="49ba8-117">Note that this flag takes effect only if you specify the server by the actual machine name.</span></span> <span data-ttu-id="49ba8-118">No tendrá efecto si especifica el servidor por "localhost" o dirección IP.</span><span class="sxs-lookup"><span data-stu-id="49ba8-118">It will not take effect, if you specify the server by "localhost" or IP address.</span></span> |
| <span data-ttu-id="49ba8-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>NIVEL DE \_ SEGURIDAD BAJO DE WINHTTP AUTOLOGON \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW</span></span> | <span data-ttu-id="49ba8-120">Se realiza un inicio de sesión autenticado con las credenciales predeterminadas para todas las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="49ba8-120">An authenticated log on using the default credentials is performed for all requests.</span></span> |
| <span data-ttu-id="49ba8-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>MEDIO DE \_ NIVEL DE SEGURIDAD DE WINHTTP AUTOLOGON \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM</span></span> | <span data-ttu-id="49ba8-122">Un inicio de sesión autenticado con las credenciales predeterminadas solo se realiza para las solicitudes en la intranet local.</span><span class="sxs-lookup"><span data-stu-id="49ba8-122">An authenticated log on using the default credentials is performed only for requests on the local Intranet.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="49ba8-123"><span id="WINHTTP_OPTION_BACKGROUND_CONNECTIONS"></span><span id="winhttp_option_background_connections"></span>**CONEXIONES EN \_ SEGUNDO PLANO DE LA OPCIÓN \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-123"><span id="WINHTTP_OPTION_BACKGROUND_CONNECTIONS"></span><span id="winhttp_option_background_connections"></span>**WINHTTP\_OPTION\_BACKGROUND\_CONNECTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49ba8-124">Al establecer esta opción en un identificador de sesión, debe pasar el número de conexiones que desea abrir.</span><span class="sxs-lookup"><span data-stu-id="49ba8-124">When you set this option on a session handle, you must pass the number of connections you wish to open.</span></span> <span data-ttu-id="49ba8-125">Después, al enviar primero una solicitud, en lugar de abrir una sola conexión, WinHttp abre varias conexiones en paralelo.</span><span class="sxs-lookup"><span data-stu-id="49ba8-125">Then, upon first sending a request, rather than opening only a single connection, WinHttp opens a number of connections in parallel.</span></span> <span data-ttu-id="49ba8-126">Esto puede mejorar el rendimiento de las solicitudes posteriores al mismo destino, lo que no tendrá la sobrecarga del establecimiento de la conexión.</span><span class="sxs-lookup"><span data-stu-id="49ba8-126">This can improve the performance of subsequent requests to the same destination, which won't have the overhead of connection establishment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-127"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**DEVOLUCIÓN DE LLAMADA \_ DE \_ LA OPCIÓN WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-127"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-128">Recupera el puntero al conjunto de funciones de devolución de llamada [**con WinHttpSetStatusCallback.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)</span><span class="sxs-lookup"><span data-stu-id="49ba8-128">Retrieves the pointer to the callback function set with [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-129"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**CONTEXTO DE CERTIFICADO \_ DE CLIENTE DE LA OPCIÓN \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-129"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-130">Establece el contexto del certificado de cliente.</span><span class="sxs-lookup"><span data-stu-id="49ba8-130">Sets the client certificate context.</span></span> <span data-ttu-id="49ba8-131">Si una aplicación recibe [**ERROR \_ WINHTTP \_ CLIENT \_ AUTH CERT \_ \_ NEEDED**](error-messages.md), debe llamar a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) para proporcionar un certificado antes de reintentar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="49ba8-131">If an application receives [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md), it must call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="49ba8-132">Como parte del procesamiento de esta opción, WinHttp llama a [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) en el contexto de certificado proporcionado por el autor de la llamada para que el autor de la llamada pueda liberar el contexto del certificado de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="49ba8-132">As a part of processing this option, WinHttp calls [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) on the caller-provided certificate context so that the certificate context can be independently released by the caller.</span></span>

> [!Note]
> <span data-ttu-id="49ba8-133">La aplicación no debe intentar cerrar el almacén de certificados con la marca CERT CLOSE STORE FORCE FLAG en la llamada a \_ \_ \_ \_ [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) en el almacén de certificados del que se recuperó el contexto del certificado.</span><span class="sxs-lookup"><span data-stu-id="49ba8-133">The application should not attempt to close the certificate store with the CERT\_CLOSE\_STORE\_FORCE\_FLAG flag in the call to [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) on the certificate store from which the certificate context was retrieved.</span></span> <span data-ttu-id="49ba8-134">Puede producirse una infracción de acceso.</span><span class="sxs-lookup"><span data-stu-id="49ba8-134">An access violation may occur.</span></span>

<span data-ttu-id="49ba8-135">Cuando el servidor solicita un certificado de cliente, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) devuelve un [**error ERROR \_ WINHTTP CLIENT \_ \_ AUTH CERT \_ \_ NEEDED.**](error-messages.md)</span><span class="sxs-lookup"><span data-stu-id="49ba8-135">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md) error.</span></span> <span data-ttu-id="49ba8-136">Si el servidor solicita el certificado pero no lo requiere, la aplicación puede especificar esta opción para indicar que no tiene un certificado.</span><span class="sxs-lookup"><span data-stu-id="49ba8-136">If the server requests the certificate but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="49ba8-137">El servidor puede elegir otro esquema de autenticación o permitir el acceso anónimo al servidor.</span><span class="sxs-lookup"><span data-stu-id="49ba8-137">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="49ba8-138">La aplicación proporciona la macro **WINHTTP \_ NO CLIENT \_ CERT \_ \_ CONTEXT** en el parámetro *lpBuffer* de [**WinHttpSetOption,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="49ba8-138">The application provides the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

<span data-ttu-id="49ba8-139">Si el servidor requiere un certificado de cliente, puede enviar un código de estado HTTP 403 en respuesta.</span><span class="sxs-lookup"><span data-stu-id="49ba8-139">If the server requires a client certificate, it may send a 403 HTTP status code in response.</span></span> <span data-ttu-id="49ba8-140">Para obtener más información, vea la **opción WINHTTP \_ OPTION CLIENT \_ CERT \_ \_ ISSUER \_ LIST.**</span><span class="sxs-lookup"><span data-stu-id="49ba8-140">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-141"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**LISTA DE \_ \_ EMISORES DE \_ CERTIFICADOS DE CLIENTE DE LA \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-141"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-142">Recupera una estructura [**\_ IssuerListInfoEx de SecPkgContext**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) cuando el error de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) es **ERROR \_ WINHTTP CLIENT \_ \_ AUTH CERT \_ \_ NEEDED**.</span><span class="sxs-lookup"><span data-stu-id="49ba8-142">Retrieves a [**SecPkgContext\_IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure when the error from [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) is **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="49ba8-143">La lista de emisores de la estructura contiene una lista de las autoridades de certificación (CA) aceptables del servidor.</span><span class="sxs-lookup"><span data-stu-id="49ba8-143">The issuer list in the structure contains a list of acceptable Certificate Authorities (CA) from the server.</span></span> <span data-ttu-id="49ba8-144">La aplicación cliente puede filtrar la lista de ca para recuperar el certificado de cliente para la autenticación SSL.</span><span class="sxs-lookup"><span data-stu-id="49ba8-144">The client application can filter the CA list to retrieve the client certificate for SSL authentication.</span></span>

<span data-ttu-id="49ba8-145">Como alternativa, si el servidor solicita el certificado de cliente, pero no lo requiere, la aplicación puede llamar a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con la opción **\_ WINHTTP OPTION \_ CLIENT CERT \_ \_ CONTEXT.**</span><span class="sxs-lookup"><span data-stu-id="49ba8-145">Alternately, if the server requests the client certificate, but does not require it, the application can call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="49ba8-146">Para obtener más información, vea la **opción WINHTTP \_ OPTION CLIENT \_ CERT \_ \_ CONTEXT.**</span><span class="sxs-lookup"><span data-stu-id="49ba8-146">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-147"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**PÁGINA DE CÓDIGOS \_ DE \_ LA OPCIÓN WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-147"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-148">Establece la [*página de códigos*](glossary.md) que se usa para procesar la dirección URL (es decir, cadena de consulta).</span><span class="sxs-lookup"><span data-stu-id="49ba8-148">Sets the [*code page*](glossary.md) that is used to process the URL (that is, query string).</span></span> <span data-ttu-id="49ba8-149">El valor predeterminado es UTF8.</span><span class="sxs-lookup"><span data-stu-id="49ba8-149">The default is UTF8.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-150"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**OPCIÓN WINHTTP \_ \_ CONFIGURAR LA \_ \_ AUTENTICACIÓN DE PASSPORT**</span><span class="sxs-lookup"><span data-stu-id="49ba8-150"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-151">Establece un valor entero largo sin signo que especifica si la autenticación de Passport en la [autenticación WinHTTP](passport-authentication-in-winhttp.md) está habilitada.</span><span class="sxs-lookup"><span data-stu-id="49ba8-151">Sets an unsigned long integer value that specifies whether [Passport Authentication in WinHTTP](passport-authentication-in-winhttp.md) authentication is enabled.</span></span> <span data-ttu-id="49ba8-152">El valor puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="49ba8-152">The value can be one of the following:</span></span>

| <span data-ttu-id="49ba8-153">Término</span><span class="sxs-lookup"><span data-stu-id="49ba8-153">Term</span></span> | <span data-ttu-id="49ba8-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="49ba8-154">Description</span></span> |
|-|-|
| <span data-ttu-id="49ba8-155"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP \_ DISABLE \_ PASSPORT \_ AUTH</span><span class="sxs-lookup"><span data-stu-id="49ba8-155"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP\_DISABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="49ba8-156">Microsoft Passport autenticación está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="49ba8-156">Microsoft Passport authentication is disabled.</span></span> <span data-ttu-id="49ba8-157">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="49ba8-157">This is the default.</span></span> |
| <span data-ttu-id="49ba8-158"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ DISABLE \_ PASSPORT \_ KEYRING</span><span class="sxs-lookup"><span data-stu-id="49ba8-158"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP\_DISABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="49ba8-159">El llavero de Passport está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="49ba8-159">The Passport keyring is disabled.</span></span> <span data-ttu-id="49ba8-160">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="49ba8-160">This is the default.</span></span> |
| <span data-ttu-id="49ba8-161"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>HABILITACIÓN \_ DE \_ LA AUTENTICACIÓN DE PASSPORT EN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-161"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP\_ENABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="49ba8-162">La autenticación de Passport está habilitada.</span><span class="sxs-lookup"><span data-stu-id="49ba8-162">Passport authentication is enabled.</span></span> |
| <span data-ttu-id="49ba8-163"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ ENABLE \_ PASSPORT \_ KEYRING</span><span class="sxs-lookup"><span data-stu-id="49ba8-163"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP\_ENABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="49ba8-164">El llavero de Passport está habilitado.</span><span class="sxs-lookup"><span data-stu-id="49ba8-164">The Passport keyring is enabled.</span></span> |

</dl> </dd> <dt>

<span data-ttu-id="49ba8-165"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**REINTENTOS DE \_ CONEXIÓN DE LA OPCIÓN \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-165"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-166">Establece o recupera un valor entero largo sin signo que contiene el número de veces queWinHTTP intenta conectarse a un host.</span><span class="sxs-lookup"><span data-stu-id="49ba8-166">Sets or retrieves an unsigned long integer value that contains the number of timesWinHTTP attempts to connect to a host.</span></span> <span data-ttu-id="49ba8-167">Servicios HTTP de Microsoft Windows (WinHTTP) solo intenta una vez por dirección ip (Protocolo de Internet).</span><span class="sxs-lookup"><span data-stu-id="49ba8-167">Microsoft Windows HTTP Services (WinHTTP) only attempts once per Internet Protocol (IP) address.</span></span> <span data-ttu-id="49ba8-168">Por ejemplo, si intenta conectarse a un host multihome que tiene 10 direcciones IP y **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** se establece en 7, WinHTTP solo intenta conectarse a las siete primeras direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="49ba8-168">For example, if you attempt to connect to a multihomed host that has 10 IP addresses and **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 7, then WinHTTP only attempts to connect to the first seven IP address.</span></span> <span data-ttu-id="49ba8-169">Dado el mismo conjunto de 10 direcciones IP, si **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** está establecido en 20, WinHTTP intenta cada una de las 10 solo una vez.</span><span class="sxs-lookup"><span data-stu-id="49ba8-169">Given the same set of 10 IP addresses, if **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 20, WinHTTP attempts each of the 10 only once.</span></span> <span data-ttu-id="49ba8-170">Si un intento de conexión sigue generando un error después del número especificado de intentos, o si el tiempo de espera de conexión expiró antes, se cancela la solicitud.</span><span class="sxs-lookup"><span data-stu-id="49ba8-170">If a connection attempt still fails after the specified number of attempts, or if the connect timeout expired before then, the request is canceled.</span></span> <span data-ttu-id="49ba8-171">El valor predeterminado de **WINHTTP \_ OPTION CONNECT \_ \_ RETRIES** es de cinco intentos.</span><span class="sxs-lookup"><span data-stu-id="49ba8-171">The default value for **WINHTTP\_OPTION\_CONNECT\_RETRIES** is five attempts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-172"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**TIEMPO DE ESPERA \_ DE CONEXIÓN DE LA OPCIÓN \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-172"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-173">Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="49ba8-173">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds.</span></span> <span data-ttu-id="49ba8-174">Al establecer esta opción en infinito (0xFFFFFFFF) se deshabilitará este temporizador.</span><span class="sxs-lookup"><span data-stu-id="49ba8-174">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="49ba8-175">Si una solicitud de conexión TCP tarda más tiempo que este valor de tiempo de espera, se cancela la solicitud.</span><span class="sxs-lookup"><span data-stu-id="49ba8-175">If a TCP connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="49ba8-176">El tiempo de espera predeterminado es de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="49ba8-176">The default timeout is 60 seconds.</span></span> <span data-ttu-id="49ba8-177">Cuando intenta conectarse a varias direcciones IP para un único host (un host de varios locales), el límite de tiempo de espera es para cada conexión individual.</span><span class="sxs-lookup"><span data-stu-id="49ba8-177">When you are attempting to connect to multiple IP addresses for a single host (a multihomed host), the timeout limit is for each individual connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-178"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**INFORMACIÓN DE CONEXIÓN \_ DE \_ LA OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-178"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP\_OPTION\_CONNECTION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-179">Recupera la dirección IP de origen y destino y el puerto de la solicitud que generó la respuesta cuando [**winHttpReceiveResponse vuelve.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)</span><span class="sxs-lookup"><span data-stu-id="49ba8-179">Retrieves the source and destination IP address, and port of the request that generated the response when [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns.</span></span> <span data-ttu-id="49ba8-180">La aplicación llama [**a WinHttpQueryOption con**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) la opción **WINHTTP OPTION CONNECTION \_ \_ \_ INFO** y proporciona la estructura DE INFORMACIÓN DE CONEXIÓN [**WINHTTP \_ \_**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) en el *parámetro lpBuffer.*</span><span class="sxs-lookup"><span data-stu-id="49ba8-180">The application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CONNECTION\_INFO** option, and provides the [**WINHTTP\_CONNECTION\_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) structure in the *lpBuffer* parameter.</span></span> <span data-ttu-id="49ba8-181">Para obtener más información, **vea WINHTTP \_ CONNECTION \_ INFO**.</span><span class="sxs-lookup"><span data-stu-id="49ba8-181">For more information, see **WINHTTP\_CONNECTION\_INFO**.</span></span>

<span data-ttu-id="49ba8-182">**Windows Server 2003 con SP1 y Windows XP con SP2:** Esta marca está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="49ba8-182">**Windows Server 2003 with SP1 and Windows XP with SP2:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V0**</span><span class="sxs-lookup"><span data-stu-id="49ba8-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V0**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-184">Reenvía la [**estructura TCP \_ INFO \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) para la conexión subyacente utilizada por la solicitud.</span><span class="sxs-lookup"><span data-stu-id="49ba8-184">Retreives the [**TCP\_INFO\_v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="49ba8-185">La estructura devuelta puede contener estadísticas de solicitudes anteriores enviadas a través de la misma conexión.</span><span class="sxs-lookup"><span data-stu-id="49ba8-185">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>

> [!Note]
> <span data-ttu-id="49ba8-186">Esta opción se ha reemplazado por **WINHTTP \_ OPTION CONNECTION \_ STATS \_ \_ V1**.</span><span class="sxs-lookup"><span data-stu-id="49ba8-186">This option has been superseded by **WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-187"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V1**</span><span class="sxs-lookup"><span data-stu-id="49ba8-187"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-188">Reenvía la [**estructura TCP \_ INFO \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) para la conexión subyacente utilizada por la solicitud.</span><span class="sxs-lookup"><span data-stu-id="49ba8-188">Retreives the [**TCP\_INFO\_v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="49ba8-189">La estructura devuelta puede contener estadísticas de solicitudes anteriores enviadas a través de la misma conexión.</span><span class="sxs-lookup"><span data-stu-id="49ba8-189">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-190"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**VALOR DE CONTEXTO \_ DE \_ LA OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-190"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-191">Establece o recupera un **\_ PTR DWORD** que contiene un puntero al valor de contexto asociado a este [identificador HINTERNET.](hinternet-handles-in-winhttp.md)</span><span class="sxs-lookup"><span data-stu-id="49ba8-191">Sets or retrieves a **DWORD\_PTR** that contains a pointer to the context value associated with this [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span> <span data-ttu-id="49ba8-192">Se usa el valor almacenado en el búfer y se asigna un nuevo valor a la marca de opción **WINHTTP \_ OPTION CONTEXT \_ \_ VALUE.**</span><span class="sxs-lookup"><span data-stu-id="49ba8-192">The value stored in the buffer is used and the **WINHTTP\_OPTION\_CONTEXT\_VALUE** option flag is assigned a new value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-193"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**DESCOMPRESIÓN DE \_ LA OPCIÓN WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-193"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP\_OPTION\_DECOMPRESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-194">Establece un DWORD de marcas que determinan si WinHTTP descomprime automáticamente los cuerpos de respuesta con codificaciones de contenido comprimidas.</span><span class="sxs-lookup"><span data-stu-id="49ba8-194">Sets a DWORD of flags which determine whether WinHTTP will automatically decompress response bodies with compressed Content-Encodings.</span></span> <span data-ttu-id="49ba8-195">WinHTTP también establecerá un encabezado Accept-Encoding, reemplazando los proporcionados por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="49ba8-195">WinHTTP will also set an appropriate Accept-Encoding header, overriding any supplied by the caller.</span></span> <span data-ttu-id="49ba8-196">Los valores admitidos son:</span><span class="sxs-lookup"><span data-stu-id="49ba8-196">Supported values are:</span></span>

| <span data-ttu-id="49ba8-197">Término</span><span class="sxs-lookup"><span data-stu-id="49ba8-197">Term</span></span> | <span data-ttu-id="49ba8-198">Descripción</span><span class="sxs-lookup"><span data-stu-id="49ba8-198">Description</span></span> |
|-|-|
| <span data-ttu-id="49ba8-199"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>MARCA \_ DE DESCOMPRESIÓN \_ \_ WINHTTP GZIP</span><span class="sxs-lookup"><span data-stu-id="49ba8-199"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP\_DECOMPRESSION\_FLAG\_GZIP</span></span> | <span data-ttu-id="49ba8-200">Descomprimir Content-Encoding: respuestas gzip.</span><span class="sxs-lookup"><span data-stu-id="49ba8-200">Decompress Content-Encoding: gzip responses.</span></span> |
| <span data-ttu-id="49ba8-201"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>DEFLATE \_ DE LA MARCA DE \_ DESCOMPRESIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-201"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP\_DECOMPRESSION\_FLAG\_DEFLATE</span></span> | <span data-ttu-id="49ba8-202">Descomprimir codificación de contenido: desinfla las respuestas.</span><span class="sxs-lookup"><span data-stu-id="49ba8-202">Decompress Content-Encoding: deflate responses.</span></span> |
| <span data-ttu-id="49ba8-203"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>MARCA DE \_ DESCOMPRESIÓN WINHTTP \_ \_ ALL</span><span class="sxs-lookup"><span data-stu-id="49ba8-203"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP\_DECOMPRESSION\_FLAG\_ALL</span></span> | <span data-ttu-id="49ba8-204">Descomprima las respuestas con cualquier codificación de contenido compatible.</span><span class="sxs-lookup"><span data-stu-id="49ba8-204">Decompress responses with any supported Content-Encoding.</span></span> |

<span data-ttu-id="49ba8-205">De forma predeterminada, WinHTTP entregará respuestas comprimidas al autor de la llamada sin modificar.</span><span class="sxs-lookup"><span data-stu-id="49ba8-205">By default, WinHTTP will deliver compressed responses to the caller unmodified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-206"><span id="WINHTTP_OPTION_DISABLE_CERT_CHAIN_BUILDING"></span><span id="winhttp_option_disable_cert_chain_building"></span>**OPCIÓN WINHTTP \_ DESHABILITAR LA CREACIÓN DE CADENA DE \_ \_ \_ \_ CERTIFICADOS**</span><span class="sxs-lookup"><span data-stu-id="49ba8-206"><span id="WINHTTP_OPTION_DISABLE_CERT_CHAIN_BUILDING"></span><span id="winhttp_option_disable_cert_chain_building"></span>**WINHTTP\_OPTION\_DISABLE\_CERT\_CHAIN\_BUILDING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="49ba8-207">Establecer esta opción en un identificador de sesión WinHttp permite habilitar o deshabilitar si se ha creado la cadena de certificados de servidor.</span><span class="sxs-lookup"><span data-stu-id="49ba8-207">Setting this option on a WinHttp session handle allows you to enable/disable whether the server certificate chain is built.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-208"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**CARACTERÍSTICA DESHABILITAR OPCIÓN WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-208"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP\_OPTION\_DISABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-209">Establece un valor entero largo sin signo que especifica qué características están deshabilitadas con una o varias de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="49ba8-209">Sets an unsigned long integer value that specifies which features are disabled with one or more of the following flags.</span></span> <span data-ttu-id="49ba8-210">Tenga en cuenta que esta característica solo se debe pasar a [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) en los identificadores de solicitud después de crear el identificador de solicitud [**con WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)y antes de que la solicitud se [**envíe con WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="49ba8-210">Be aware that this feature should only be passed to [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) on request handles after the request handle is created with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), and before the request is sent with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

| <span data-ttu-id="49ba8-211">Término</span><span class="sxs-lookup"><span data-stu-id="49ba8-211">Term</span></span> | <span data-ttu-id="49ba8-212">Descripción</span><span class="sxs-lookup"><span data-stu-id="49ba8-212">Description</span></span> |
|-|-|
| <span data-ttu-id="49ba8-213"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>AUTENTICACIÓN DE \_ DESHABILITACIÓN DE \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-213"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP\_DISABLE\_AUTHENTICATION</span></span> | <span data-ttu-id="49ba8-214">La autenticación automática está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="49ba8-214">Automatic authentication is disabled.</span></span> |
| <span data-ttu-id="49ba8-215"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>DESHABILITACIÓN \_ DE COOKIES DE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-215"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP\_DISABLE\_COOKIES</span></span> | <span data-ttu-id="49ba8-216">La adición automática de encabezados de cookie a las solicitudes está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="49ba8-216">Automatic addition of cookie headers to requests is disabled.</span></span> <span data-ttu-id="49ba8-217">Además, las cookies devueltas no se agregan automáticamente a la base de datos de cookies.</span><span class="sxs-lookup"><span data-stu-id="49ba8-217">Also, returned cookies are not automatically added to the cookie database.</span></span> <span data-ttu-id="49ba8-218">Deshabilitar las cookies puede provocar un rendimiento deficiente para la autenticación de Passport.</span><span class="sxs-lookup"><span data-stu-id="49ba8-218">Disabling cookies can result in poor performance for Passport authentication.</span></span> |
| <span data-ttu-id="49ba8-219"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP \_ DISABLE \_ KEEP \_ ALIVE</span><span class="sxs-lookup"><span data-stu-id="49ba8-219"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP\_DISABLE\_KEEP\_ALIVE</span></span> | <span data-ttu-id="49ba8-220">Deshabilita la semántica de conexión keep-alive para la conexión.</span><span class="sxs-lookup"><span data-stu-id="49ba8-220">Disables keep-alive semantics for the connection.</span></span> <span data-ttu-id="49ba8-221">La semántica de conexión continua es necesaria para MSN, NTLM y otros tipos de autenticación.</span><span class="sxs-lookup"><span data-stu-id="49ba8-221">Keep-alive semantics are required for MSN, NTLM, and other types of authentication.</span></span> |
| <span data-ttu-id="49ba8-222"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>REDIRECCIONAMIENTOS \_ DE DESHABILITACIÓN DE WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-222"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP\_DISABLE\_REDIRECTS</span></span> | <span data-ttu-id="49ba8-223">El redireccionamiento automático está deshabilitado al enviar solicitudes [**con WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="49ba8-223">Automatic redirection is disabled when sending requests with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="49ba8-224">Si el redireccionamiento automático está deshabilitado, una aplicación debe registrar una función de devolución de llamada para que la autenticación de Passport se haga correctamente.</span><span class="sxs-lookup"><span data-stu-id="49ba8-224">If automatic redirection is disabled, an application must register a callback function in order for Passport authentication to succeed.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="49ba8-225"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**OPCIÓN WINHTTP \_ DESHABILITAR RESERVA DE PROTOCOLO \_ \_ \_ \_ SEGURO**</span><span class="sxs-lookup"><span data-stu-id="49ba8-225"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-226">Impide que WinHTTP vuelva a intentar una conexión con una versión inferior del protocolo de seguridad cuando se produce un error en la negociación del protocolo inicial.</span><span class="sxs-lookup"><span data-stu-id="49ba8-226">Prevents WinHTTP from retrying a connection with a lower version of the security protocol when the initial protocol negotiation fails.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-227"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**OPCIÓN WINHTTP \_ DESHABILITAR \_ COLA DE \_ \_ TRANSMISIONES**</span><span class="sxs-lookup"><span data-stu-id="49ba8-227"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-228">Permite que las nuevas solicitudes abran una conexión HTTP/2 adicional cuando se alcanza el límite máximo de flujos simultáneos, en lugar de esperar a la siguiente secuencia disponible en una conexión existente.</span><span class="sxs-lookup"><span data-stu-id="49ba8-228">Allows new requests to open an additional HTTP/2 connection when the maximum concurrent stream limit is reached, rather than waiting for the next available stream on an existing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-229"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**CARACTERÍSTICA HABILITAR OPCIÓN WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-229"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP\_OPTION\_ENABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-230">Establece un valor entero largo sin signo que especifica las características habilitadas actualmente.</span><span class="sxs-lookup"><span data-stu-id="49ba8-230">Sets an unsigned long integer value that specifies the features currently enabled.</span></span> <span data-ttu-id="49ba8-231">Puede ser uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="49ba8-231">Can be one of the following values.</span></span>

| <span data-ttu-id="49ba8-232">Término</span><span class="sxs-lookup"><span data-stu-id="49ba8-232">Term</span></span> | <span data-ttu-id="49ba8-233">Descripción</span><span class="sxs-lookup"><span data-stu-id="49ba8-233">Description</span></span> |
|-|-|
| <span data-ttu-id="49ba8-234"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVERT \_ IMPERSONATION</span><span class="sxs-lookup"><span data-stu-id="49ba8-234"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP\_ENABLE\_SSL\_REVERT\_IMPERSONATION</span></span> | <span data-ttu-id="49ba8-235">Si está habilitado, WinHTTP revierte temporalmente la suplantación de cliente mientras duren las operaciones de autenticación de certificados SSL.</span><span class="sxs-lookup"><span data-stu-id="49ba8-235">If enabled, WinHTTP temporarily reverts client impersonation for the duration of SSL certificate authentication operations.</span></span> <span data-ttu-id="49ba8-236">Este valor solo se puede establecer en el identificador de sesión.</span><span class="sxs-lookup"><span data-stu-id="49ba8-236">This value can be set only on the session handle.</span></span> |
| <span data-ttu-id="49ba8-237"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ ENABLE \_ SSL \_ REVOCATION</span><span class="sxs-lookup"><span data-stu-id="49ba8-237"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP\_ENABLE\_SSL\_REVOCATION</span></span> | <span data-ttu-id="49ba8-238">Si está habilitado, WinHTTP permite la revocación SSL.</span><span class="sxs-lookup"><span data-stu-id="49ba8-238">If enabled, WinHTTP allows SSL revocation.</span></span> <span data-ttu-id="49ba8-239">Este valor solo se puede establecer en el identificador de solicitud.</span><span class="sxs-lookup"><span data-stu-id="49ba8-239">This value can be set only on the request handle.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-240"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**OPCIÓN WINHTTP \_ HABILITAR \_ PROTOCOLO \_ HTTP \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-240"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-241">Establece una máscara de bits DWORD de versiones HTTP avanzadas aceptables.</span><span class="sxs-lookup"><span data-stu-id="49ba8-241">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="49ba8-242">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="49ba8-242">Possible values are:</span></span>

| <span data-ttu-id="49ba8-243">Término</span><span class="sxs-lookup"><span data-stu-id="49ba8-243">Term</span></span> | <span data-ttu-id="49ba8-244">Descripción</span><span class="sxs-lookup"><span data-stu-id="49ba8-244">Description</span></span> |
|-|-|
| <span data-ttu-id="49ba8-245"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>MARCA DE PROTOCOLO WINHTTP \_ \_ \_ HTTP2 (0x1)</span><span class="sxs-lookup"><span data-stu-id="49ba8-245"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP\_PROTOCOL\_FLAG\_HTTP2 (0x1)</span></span> | <span data-ttu-id="49ba8-246">Habilita HTTP/2 para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="49ba8-246">Enables HTTP/2 for the request.</span></span> |
| <span data-ttu-id="49ba8-247">Ninguno (0x0)</span><span class="sxs-lookup"><span data-stu-id="49ba8-247">None (0x0)</span></span> | <span data-ttu-id="49ba8-248">Restringe la solicitud a HTTP/1.1 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="49ba8-248">Restricts the request to HTTP/1.1 and prior.</span></span> |

<span data-ttu-id="49ba8-249">Las versiones heredadas de HTTP (1.1 y anteriores) no se pueden deshabilitar con esta opción.</span><span class="sxs-lookup"><span data-stu-id="49ba8-249">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="49ba8-250">El valor predeterminado es 0x0.</span><span class="sxs-lookup"><span data-stu-id="49ba8-250">The default is 0x0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-251"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**OPCIÓN WINHTTP \_ \_ HABILITAR \_ HTTP2 MÁS EL CERTIFICADO DE \_ \_ \_ CLIENTE**</span><span class="sxs-lookup"><span data-stu-id="49ba8-251"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="49ba8-252">Esta opción se puede establecer en un identificador de sesión WinHttp para permitir que WinHttp use el contexto de certificado de cliente proporcionado por el autor de la llamada cuando se usa HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="49ba8-252">This option can be set on a WinHttp session handle to allow WinHttp to use the caller-provided client certificate context when HTTP/2 is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-253"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**HABILITACIÓN \_ DE LA OPCIÓN \_ WINHTTPTRACING**</span><span class="sxs-lookup"><span data-stu-id="49ba8-253"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP\_OPTION\_ENABLETRACING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-254">Establece un **valor BOOL** que especifica si el seguimiento está habilitado actualmente.</span><span class="sxs-lookup"><span data-stu-id="49ba8-254">Sets a **BOOL** value that specifies whether tracing is currently enabled.</span></span> <span data-ttu-id="49ba8-255">Para obtener más información sobre la instalación de seguimiento en WinHTTP, vea [Instalación de seguimiento winHTTP](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="49ba8-255">For more information about the trace facility in WinHTTP, see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span> <span data-ttu-id="49ba8-256">Esta opción solo se puede establecer en un **identificador** **HINTERNET** NULL.</span><span class="sxs-lookup"><span data-stu-id="49ba8-256">This option can only be set on a **NULL** **HINTERNET** handle.</span></span>


</dt> </dl> </dd>

<dt>

<span data-ttu-id="49ba8-257"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**CODIFICACIÓN \_ ADICIONAL DE LA \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-257"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-258">Habilita la codificación de porcentaje de dirección URL para la ruta de acceso y la cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="49ba8-258">Enables URL percent encoding for path and query string.</span></span>

<span data-ttu-id="49ba8-259">Como alternativa, puede codificar por porcentaje antes de llamar a WinHttp.</span><span class="sxs-lookup"><span data-stu-id="49ba8-259">Alternatively, you can percent encode before calling WinHttp.</span></span>

</dt> </dl> </dd>

<dt>

<span data-ttu-id="49ba8-260"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**OPCIÓN WINHTTP \_ \_ EXPIRE \_ CONNECTION**</span><span class="sxs-lookup"><span data-stu-id="49ba8-260"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP\_OPTION\_EXPIRE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-261">Esta opción solo se puede establecer en un identificador de solicitud que sigue activo (envío o recepción).</span><span class="sxs-lookup"><span data-stu-id="49ba8-261">This option can only be set on a request handle which is still active (sending or receiving).</span></span> <span data-ttu-id="49ba8-262">Al establecer esta opción se le pedirá a WinHttp que deje de atender solicitudes en la conexión asociada con el identificador de solicitud pasado.</span><span class="sxs-lookup"><span data-stu-id="49ba8-262">Setting this option will tell WinHttp to stop serving requests on the connection associated with the request handle passed in.</span></span> <span data-ttu-id="49ba8-263">La conexión se cerrará una vez completado el identificador de solicitud con el que se llama a esta opción.</span><span class="sxs-lookup"><span data-stu-id="49ba8-263">The connection will be closed after the request handle this option is called with is completed.</span></span> <span data-ttu-id="49ba8-264">Esta opción no toma ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="49ba8-264">This option does not take any parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-265"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**ERROR EXTENDIDO DE LA OPCIÓN WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-265"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-266">Recupera un valor entero largo sin signo que contiene un código de error de Microsoft Windows Sockets que se asignó a los mensajes de error DE ERROR WINHTTP devueltos por última vez en este \_ \_ \* contexto de subproceso.</span><span class="sxs-lookup"><span data-stu-id="49ba8-266">Retrieves an unsigned long integer value that contains a Microsoft Windows Sockets error code that was mapped to the ERROR\_WINHTTP\_\* error messages last returned in this thread context.</span></span> <span data-ttu-id="49ba8-267">Puede pasar **NULL como** valor de identificador.</span><span class="sxs-lookup"><span data-stu-id="49ba8-267">You can pass **NULL** as the handle value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-268"><span id="WINHTTP_OPTION_FIRST_AVAILABLE_CONNECTION"></span><span id="winhttp_option_first_available_connection"></span>**PRIMERA CONEXIÓN DISPONIBLE \_ DE LA \_ OPCIÓN \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-268"><span id="WINHTTP_OPTION_FIRST_AVAILABLE_CONNECTION"></span><span id="winhttp_option_first_available_connection"></span>**WINHTTP\_OPTION\_FIRST\_AVAILABLE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="49ba8-269">De forma predeterminada, cuando WinHttp envía una solicitud, si no hay conexiones disponibles para atender la solicitud, WinHttp intentará establecer una nueva conexión y la solicitud se enlazará a esta nueva conexión.</span><span class="sxs-lookup"><span data-stu-id="49ba8-269">By default, when WinHttp sends a request, if there are no available connections to serve the request, WinHttp will attempt to establish a new connection, and the request will be bound to this new connection.</span></span> <span data-ttu-id="49ba8-270">Cuando se establece esta opción, dicha solicitud se sirve en su lugar en la primera conexión que está disponible y no necesariamente en la que se establece.</span><span class="sxs-lookup"><span data-stu-id="49ba8-270">When you set this option, such a request will instead be served on the first connection that becomes available, and not necessarily the one being established.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-271"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**CREDS DE PROXY GLOBAL DE \_ \_ LA OPCIÓN \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-271"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-272">Toma un puntero a una [**estructura DE WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) con el parámetro de función *hInternet* establecido en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="49ba8-272">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="49ba8-273">Esta opción requiere la clave del Registro **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="49ba8-273">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="49ba8-274">Si no se establece esta clave del Registro, WinHTTP devolverá el **error ERROR \_ WINHTTP INVALID \_ \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="49ba8-274">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="49ba8-275">Esta clave del Registro no está presente de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="49ba8-275">This registry key is not present by default.</span></span> <span data-ttu-id="49ba8-276">Cuando se establece, WinINet enviará las credenciales a WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="49ba8-276">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="49ba8-277">Cada vez que WinHttp obtiene un desafío de autenticación y no hay ninguna credencial establecida en el identificador actual, usará las credenciales proporcionadas por WinINet.</span><span class="sxs-lookup"><span data-stu-id="49ba8-277">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="49ba8-278">Para compartir las credenciales del servidor además de las credenciales de proxy, los usuarios deben establecer **LA OPCIÓN WINHTTP \_ USE GLOBAL SERVER \_ \_ \_ \_ CREDENTIALS** .</span><span class="sxs-lookup"><span data-stu-id="49ba8-278">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-279"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP \_ OPTION \_ GLOBAL \_ SERVER \_ CREDS**</span><span class="sxs-lookup"><span data-stu-id="49ba8-279"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-280">Toma un puntero a una [**estructura DE WINHTTP \_ CREDS \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) con el parámetro de función *hInternet* establecido en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="49ba8-280">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="49ba8-281">Esta opción requiere la clave del Registro **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="49ba8-281">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="49ba8-282">Si no se establece esta clave del Registro, WinHTTP devolverá el **error ERROR \_ WINHTTP INVALID \_ \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="49ba8-282">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="49ba8-283">Esta clave del Registro no está presente de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="49ba8-283">This registry key is not present by default.</span></span> <span data-ttu-id="49ba8-284">Cuando se establece, WinINet enviará las credenciales a WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="49ba8-284">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="49ba8-285">Cada vez que WinHttp obtiene un desafío de autenticación y no hay ninguna credencial establecida en el identificador actual, usará las credenciales proporcionadas por WinINet.</span><span class="sxs-lookup"><span data-stu-id="49ba8-285">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="49ba8-286">Para compartir las credenciales del servidor además de las credenciales de proxy, los usuarios deben establecer **LA OPCIÓN WINHTTP \_ USE GLOBAL SERVER \_ \_ \_ \_ CREDENTIALS** .</span><span class="sxs-lookup"><span data-stu-id="49ba8-286">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-287"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**TIPO DE IDENTIFICADOR \_ DE OPCIÓN \_ WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-287"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-288">Recupera un valor entero largo sin signo que contiene el tipo del identificador [HINTERNET](hinternet-handles-in-winhttp.md) pasado.</span><span class="sxs-lookup"><span data-stu-id="49ba8-288">Retrieves an unsigned long integer value that contains the type of the [HINTERNET](hinternet-handles-in-winhttp.md) handle passed in.</span></span> <span data-ttu-id="49ba8-289">El valor devuelto puede ser cualquiera de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="49ba8-289">The return value can be one of the following:</span></span>

| <span data-ttu-id="49ba8-290">Término</span><span class="sxs-lookup"><span data-stu-id="49ba8-290">Term</span></span> | <span data-ttu-id="49ba8-291">Descripción</span><span class="sxs-lookup"><span data-stu-id="49ba8-291">Description</span></span> |
|-|-|
| <span data-ttu-id="49ba8-292"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP \_ HANDLE \_ TYPE \_ CONNECT</span><span class="sxs-lookup"><span data-stu-id="49ba8-292"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP\_HANDLE\_TYPE\_CONNECT</span></span> | <span data-ttu-id="49ba8-293">El identificador es un identificador de conexión.</span><span class="sxs-lookup"><span data-stu-id="49ba8-293">The handle is a connection handle.</span></span> |
| <span data-ttu-id="49ba8-294"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>SOLICITUD DE TIPO \_ DE \_ IDENTIFICADOR \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-294"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP\_HANDLE\_TYPE\_REQUEST</span></span> | <span data-ttu-id="49ba8-295">El identificador es un identificador de solicitud.</span><span class="sxs-lookup"><span data-stu-id="49ba8-295">The handle is a request handle.</span></span> |
| <span data-ttu-id="49ba8-296"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>SESIÓN DE TIPO DE IDENTIFICADOR WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-296"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP\_HANDLE\_TYPE\_SESSION</span></span> | <span data-ttu-id="49ba8-297">El identificador es un identificador de sesión.</span><span class="sxs-lookup"><span data-stu-id="49ba8-297">The handle is a session handle.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="49ba8-298"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**SE REQUIERE \_ EL PROTOCOLO HTTP DE LA OPCIÓN \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-298"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-299">Impide que se utilicen versiones de protocolo distintas de las habilitadas por **WINHTTP \_ OPTION ENABLE HTTP \_ \_ \_ PROTOCOL** para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="49ba8-299">Prevents protocol versions other than those enabled by **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL** from being used for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-300"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**SE USA EL PROTOCOLO HTTP DE \_ \_ LA OPCIÓN WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-300"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-301">Obtiene un DWORD que indica qué versión avanzada de HTTP se usó en una solicitud determinada.</span><span class="sxs-lookup"><span data-stu-id="49ba8-301">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="49ba8-302">Para obtener una lista de los valores posibles, **vea WINHTTP \_ OPTION ENABLE \_ HTTP \_ \_ PROTOCOL**.</span><span class="sxs-lookup"><span data-stu-id="49ba8-302">For a list of possible values, see **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-303"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**VERSIÓN HTTP DE \_ LA OPCIÓN \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-303"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-304">Establece o recupera una estructura [**HTTP \_ VERSION \_ INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) que contiene la versión HTTP que se admite.</span><span class="sxs-lookup"><span data-stu-id="49ba8-304">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) structure that contains the HTTP version being supported.</span></span> <span data-ttu-id="49ba8-305">Se trata de una opción para todo el proceso; use **NULL** para el identificador.</span><span class="sxs-lookup"><span data-stu-id="49ba8-305">This is a process-wide option; use **NULL** for the handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-306"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**OPCIÓN WINHTTP \_ \_ HTTP2 \_ KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="49ba8-306"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**WINHTTP\_OPTION\_HTTP2\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="49ba8-307">Esta opción se puede establecer en un identificador de sesión para que WinHttp use marcos PING HTTP/2 como mecanismo keepalive.</span><span class="sxs-lookup"><span data-stu-id="49ba8-307">This option can be set on a session handle to have WinHttp use HTTP/2 PING frames as a keepalive mechanism.</span></span> <span data-ttu-id="49ba8-308">Los llamadores especifican un tiempo de espera en milisegundos y, después de que no haya ninguna actividad en una conexión durante ese período de tiempo de espera, WinHttp comenzará a enviar fotogramas PING HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="49ba8-308">Callers specify a timeout in milliseconds, and after there is no activity on a connection for that timeout period, WinHttp will begin to send HTTP/2 PING frames.</span></span> <span data-ttu-id="49ba8-309">Los llamadores no pueden establecer un valor de tiempo de espera inferior a 5000 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="49ba8-309">Callers cannot set a timeout value less than 5000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-310"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**OPCIÓN WINHTTP \_ \_ HTTP2 \_ MÁS \_ CODIFICACIÓN DE \_ TRANSFERENCIA**</span><span class="sxs-lookup"><span data-stu-id="49ba8-310"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="49ba8-311">Esta opción se puede establecer en un identificador de solicitud WinHttp para controlar cómo se comporta WinHttp cuando una respuesta HTTP/2 contiene un encabezado "Transfer-Encoding".</span><span class="sxs-lookup"><span data-stu-id="49ba8-311">This option can be set on a WinHttp request handle to control how WinHttp behaves when an HTTP/2 response contains a "Transfer-Encoding" header.</span></span> <span data-ttu-id="49ba8-312">En tal caso, WinHttp devolverá un error si esta opción está establecida en **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="49ba8-312">In such a case, WinHttp will return an error if this option is set to **FALSE**.</span></span>


</dt> </dl> </dd> <dt>


<span data-ttu-id="49ba8-313"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**OPCIÓN WINHTTP \_ OMITIR \_ \_ REVOCACIÓN \_ DE CERTIFICADOS SIN \_ CONEXIÓN**</span><span class="sxs-lookup"><span data-stu-id="49ba8-313"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-314">Permite que las conexiones seguras usen certificados de seguridad para los que no se pudo descargar la lista de revocación de certificados.</span><span class="sxs-lookup"><span data-stu-id="49ba8-314">Allows secure connections to use security certificates for which the certificate revocation list could not be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-315"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**OPCIÓN WINHTTP \_ \_ IPV6 \_ FAST \_ FALLBACK**</span><span class="sxs-lookup"><span data-stu-id="49ba8-315"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-316">Habilita la reserva rápida de IPv6 (globos oculares inertes) para la conexión.</span><span class="sxs-lookup"><span data-stu-id="49ba8-316">Enables IPv6 fast fallback (Happier Eyeballs) for the connection.</span></span> <span data-ttu-id="49ba8-317">Este comportamiento es similar al comportamiento de Happy Eyeballs descrito en [RFC 6555](https://tools.ietf.org/html/rfc6555) para mejorar los tiempos de conexión en redes en las que IPv6 no es confiable.</span><span class="sxs-lookup"><span data-stu-id="49ba8-317">This behavior is similar to the Happy Eyeballs behavior described in [RFC 6555](https://tools.ietf.org/html/rfc6555) for improving connection times on networks where IPv6 is unreliable.</span></span>
- <span data-ttu-id="49ba8-318">Si las direcciones IPv6 e IPv4 se resuelven para un host determinado, WinHttp comenzará conectándose a la primera dirección IPv6 resuelta con un tiempo de espera corto (300 ms).</span><span class="sxs-lookup"><span data-stu-id="49ba8-318">If both IPv6 and IPv4 addresses are resolved for a given host, WinHttp will begin by connecting to the first resolved IPv6 address with a short (300ms) timeout.</span></span>
- <span data-ttu-id="49ba8-319">Si se producirá un error en la conexión, WinHttp intentará conectarse a la primera dirección IPv4 resuelta con el tiempo de espera estándar.</span><span class="sxs-lookup"><span data-stu-id="49ba8-319">Should that connection fail, WinHttp will attempt to connect to the first resolved IPv4 address with the standard timeout.</span></span>
- <span data-ttu-id="49ba8-320">Si se producirá un error en la segunda conexión, WinHttp volverá a intentar la primera dirección IPv6 resuelta con el tiempo de espera estándar.</span><span class="sxs-lookup"><span data-stu-id="49ba8-320">Should the second connection fail, WinHttp will retry the first resolved IPv6 address with the standard timeout.</span></span>
- <span data-ttu-id="49ba8-321">Si se producirá un error en la tercera conexión, WinHttp revertirá al comportamiento predeterminado de las direcciones restantes, intentando una conexión a cada una con el tiempo de espera estándar hasta que se establece una conexión o no quedan direcciones.</span><span class="sxs-lookup"><span data-stu-id="49ba8-321">Should the third connection fail, WinHttp will revert to the default behavior for any remaining addresses, attempting a connection to each one with the standard timeout until a connection is made or no addresses remain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-322"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**LA OPCIÓN WINHTTP \_ ES RESPUESTA DE CONEXIÓN DE \_ \_ \_ \_ PROXY**</span><span class="sxs-lookup"><span data-stu-id="49ba8-322"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-323">Obtiene si se puede recuperar o no una respuesta de conexión de devolución de proxy.</span><span class="sxs-lookup"><span data-stu-id="49ba8-323">Gets whether or not a Proxy Return Connect Response can be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-324"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**OPCIÓN WINHTTP \_ \_ NÚMERO MÁXIMO DE \_ CONNS \_ POR \_ 1 \_ 0 \_ SERVIDOR**</span><span class="sxs-lookup"><span data-stu-id="49ba8-324"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-325">Establece o recupera un valor entero largo sin signo que contiene el número máximo de conexiones permitidas por servidor HTTP/1.0.</span><span class="sxs-lookup"><span data-stu-id="49ba8-325">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="49ba8-326">El valor predeterminado es **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="49ba8-326">The default value is **INFINITE**.</span></span>

<span data-ttu-id="49ba8-327">**Windows Vista con SP1 y Windows Server 2008:** Esta marca está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="49ba8-327">**Windows Vista with SP1 and Windows Server 2008:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-328"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**OPCIÓN WINHTTP \_ \_ NÚMERO MÁXIMO DE \_ \_ CONNS POR \_ SERVIDOR**</span><span class="sxs-lookup"><span data-stu-id="49ba8-328"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-329">Establece o recupera un valor entero largo sin signo que contiene el número máximo de conexiones permitidas por servidor.</span><span class="sxs-lookup"><span data-stu-id="49ba8-329">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="49ba8-330">El valor predeterminado es **INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="49ba8-330">The default value is **INFINITE**.</span></span>

<span data-ttu-id="49ba8-331">Cuando esta opción se establece en cero, WinHTTP establece el límite en el número de conexiones en 2.</span><span class="sxs-lookup"><span data-stu-id="49ba8-331">When this option is set to zero, WinHTTP sets the limit on the number of connections to 2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-332"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**OPCIÓN WINHTTP \_ \_ MAX HTTP AUTOMATIC \_ \_ \_ REDIRECTS**</span><span class="sxs-lookup"><span data-stu-id="49ba8-332"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-333">Establece el número máximo de redirecciones que sigue WinHTTP; el valor predeterminado es 10.</span><span class="sxs-lookup"><span data-stu-id="49ba8-333">Sets the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="49ba8-334">Este límite impide que sitios no autorizados haga que el cliente WinHTTP se detenga después de un gran número de redirecciones.</span><span class="sxs-lookup"><span data-stu-id="49ba8-334">This limit prevents unauthorized sites from making the WinHTTP client pause following a large number of redirects.</span></span>

<span data-ttu-id="49ba8-335">**Windows XP con SP1 y Windows 2000 con SP3:** Esta marca está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="49ba8-335">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-336"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**OPCIÓN WINHTTP \_ \_ MAX HTTP STATUS \_ \_ \_ CONTINUE**</span><span class="sxs-lookup"><span data-stu-id="49ba8-336"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-337">Número máximo de respuestas de código de estado informativo 100-199 omitido antes de devolver el código de estado final al cliente WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="49ba8-337">The maximum number of Informational 100-199 status code responses ignored before returning the final status code to the WinHTTP client.</span></span> <span data-ttu-id="49ba8-338">El servidor puede enviar códigos de estado informativos 100-199 antes del código de estado final y se describen en la especificación de HTTP/1.1 (para obtener más información, vea [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span><span class="sxs-lookup"><span data-stu-id="49ba8-338">Informational 100-199 status codes can be sent by the server before the final status code, and are described in the specification for HTTP/1.1 (for more information, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span></span> <span data-ttu-id="49ba8-339">El valor predeterminado es 10.</span><span class="sxs-lookup"><span data-stu-id="49ba8-339">The default is 10.</span></span>

<span data-ttu-id="49ba8-340">**Windows XP con SP1 y Windows 2000 con SP3:** Esta marca está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="49ba8-340">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-341"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**TAMAÑO MÁXIMO DE PURGA DE RESPUESTA DE LA \_ \_ OPCIÓN \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-341"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-342">Enlazado a la cantidad de datos purgados de las respuestas para reutilizar una conexión, especificada en bytes.</span><span class="sxs-lookup"><span data-stu-id="49ba8-342">A bound on the amount of data drained from responses in order to reuse a connection, specified in bytes.</span></span> <span data-ttu-id="49ba8-343">El valor predeterminado es 1 MB.</span><span class="sxs-lookup"><span data-stu-id="49ba8-343">The default is 1MB.</span></span>

<span data-ttu-id="49ba8-344">**Windows XP con SP1 y Windows 2000 con SP3:** Esta marca está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="49ba8-344">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-345"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**TAMAÑO MÁXIMO DE ENCABEZADO DE RESPUESTA DE LA \_ \_ \_ \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-345"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-346">Un conjunto enlazado en el tamaño máximo de la parte de encabezado de la respuesta del servidor, especificado en bytes.</span><span class="sxs-lookup"><span data-stu-id="49ba8-346">A bound set on the maximum size of the header portion of the server response, specified in bytes.</span></span> <span data-ttu-id="49ba8-347">Este límite protege al cliente de un servidor no autorizado que intenta detener el cliente mediante el envío de una respuesta con una cantidad infinita de datos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="49ba8-347">This bound protects the client from an unauthorized server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="49ba8-348">El valor predeterminado es 64 KB.</span><span class="sxs-lookup"><span data-stu-id="49ba8-348">The default value is 64KB.</span></span>

<span data-ttu-id="49ba8-349">**Windows XP con SP1 y Windows 2000 con SP3:** Esta marca está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="49ba8-349">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-350"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**IDENTIFICADOR PRIMARIO DE LA OPCIÓN WINHTTP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-350"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-351">Recupera el identificador primario de este identificador.</span><span class="sxs-lookup"><span data-stu-id="49ba8-351">Retrieves the parent handle to this handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-352"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**TEXTO DE MARCA DE PASSPORT DE LA \_ \_ \_ OPCIÓN WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-352"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-353">Recupera una cadena que contiene el texto [*de marca*](glossary.md) que proporciona el servidor de inicio de sesión de Passport.</span><span class="sxs-lookup"><span data-stu-id="49ba8-353">Retrieves a string that contains the [*cobranding*](glossary.md) text provided by the Passport logon server.</span></span> <span data-ttu-id="49ba8-354">Esta opción debe recuperarse inmediatamente después de que el servidor de inicio de sesión responda con un código de estado 401.</span><span class="sxs-lookup"><span data-stu-id="49ba8-354">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="49ba8-355">Una aplicación debe pasar un tamaño de búfer, en bytes, lo suficientemente grande como para contener la cadena devuelta.</span><span class="sxs-lookup"><span data-stu-id="49ba8-355">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-356"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**DIRECCIÓN URL DE COBRANDING DE \_ \_ LA OPCIÓN WINHTTP PASSPORT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-356"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-357">Recupera una cadena que contiene una dirección URL para un [*gráfico de marca*](glossary.md) de marca proporcionado por el servidor de inicio de sesión de Passport.</span><span class="sxs-lookup"><span data-stu-id="49ba8-357">Retrieves a string that contains a URL for a [*cobranding*](glossary.md) graphic provided by the Passport logon server.</span></span> <span data-ttu-id="49ba8-358">Esta opción debe recuperarse inmediatamente después de que el servidor de inicio de sesión responda con un código de estado 401.</span><span class="sxs-lookup"><span data-stu-id="49ba8-358">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="49ba8-359">Una aplicación debe pasar un tamaño de búfer, en bytes, lo suficientemente grande como para contener la cadena devuelta.</span><span class="sxs-lookup"><span data-stu-id="49ba8-359">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-360"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**DIRECCIÓN URL DE RETORNO DE PASSPORT DE LA \_ \_ OPCIÓN WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-360"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-361">Establece una opción de solo lectura en un identificador de solicitud que recupera la dirección URL de devolución de Passport.</span><span class="sxs-lookup"><span data-stu-id="49ba8-361">Sets a read-only option on a request handle that retrieves the Passport return URL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-362"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**OPCIÓN WINHTTP \_ \_ PASSPORT SIGN \_ \_ OUT**</span><span class="sxs-lookup"><span data-stu-id="49ba8-362"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-363">Establece la opción en un identificador de sesión para cerrar la sesión de los inicios de sesión de Passport.</span><span class="sxs-lookup"><span data-stu-id="49ba8-363">Sets the option on a session handle to sign out of any Passport logins.</span></span> <span data-ttu-id="49ba8-364">Una aplicación debe pasar la dirección URL de devolución de Passport que se recuperó con **WINHTTP \_ OPTION PASSPORT RETURN \_ \_ \_ URL**.</span><span class="sxs-lookup"><span data-stu-id="49ba8-364">An application should pass in the Passport return URL that was retrieved with **WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**.</span></span> <span data-ttu-id="49ba8-365">Se borran todas las cookies relacionadas con la dirección URL de devolución.</span><span class="sxs-lookup"><span data-stu-id="49ba8-365">All cookies related to the return URL are cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-366"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**CONTRASEÑA DE LA OPCIÓN WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-366"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-367">Establece o recupera un valor de cadena que contiene la contraseña asociada a un identificador de solicitud.</span><span class="sxs-lookup"><span data-stu-id="49ba8-367">Sets or retrieves a string value that contains the password associated with a request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-368"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**PROXY DE OPCIÓN WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-368"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-369">Establece o recupera una estructura [**DE INFORMACIÓN DE \_ PROXY \_ WINHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) que contiene los datos de proxy en un identificador de sesión o identificador de solicitud existente.</span><span class="sxs-lookup"><span data-stu-id="49ba8-369">Sets or retrieves an [**WINHTTP\_PROXY\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) structure that contains the proxy data on an existing session handle or request handle.</span></span> <span data-ttu-id="49ba8-370">Al recuperar datos de proxy, una aplicación debe liberar las cadenas **lpszProxy** y **lpszProxyBypass** contenidas en esta estructura (si no son **NULL)** mediante la [**función GlobalFree.**](/windows/desktop/api/winbase/nf-winbase-globalfree)</span><span class="sxs-lookup"><span data-stu-id="49ba8-370">When retrieving proxy data, an application must free the **lpszProxy** and **lpszProxyBypass** strings contained in this structure (if they are non-**NULL**) using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="49ba8-371">Una aplicación puede consultar los datos de proxy global (el proxy predeterminado) pasando un **identificador NULL.**</span><span class="sxs-lookup"><span data-stu-id="49ba8-371">An application can query for the global proxy data (the default proxy) by passing a **NULL** handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-372"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**CONTRASEÑA DE \_ PROXY DE OPCIÓN \_ WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-372"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-373">Establece o recupera un valor de cadena que contiene la contraseña usada para acceder al proxy.</span><span class="sxs-lookup"><span data-stu-id="49ba8-373">Sets or retrieves a string value that contains the password used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-374"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**SPN DE \_ \_ PROXY DE OPCIÓN \_ WINHTTP \_ USADO**</span><span class="sxs-lookup"><span data-stu-id="49ba8-374"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**WINHTTP\_OPTION\_PROXY\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-375">Obtiene el nombre principal del servidor proxy que WinHTTP proporcionó a SSPI durante la autenticación.</span><span class="sxs-lookup"><span data-stu-id="49ba8-375">Gets the proxy Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="49ba8-376">Este valor de cadena se usa para pasar a [**SspiPromptForCredentials después**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) de un error de autenticación.</span><span class="sxs-lookup"><span data-stu-id="49ba8-376">This string value is usefor passing to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-377"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**NOMBRE DE USUARIO \_ DEL PROXY DE OPCIÓN \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-377"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-378">Establece o recupera un valor de cadena que contiene el nombre de usuario utilizado para acceder al proxy.</span><span class="sxs-lookup"><span data-stu-id="49ba8-378">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-379"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**TAMAÑO DEL BÚFER \_ DE LECTURA DE LA OPCIÓN \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-379"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-380">Esta opción está en desuso; no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="49ba8-380">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-381"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**RESPUESTA DE CONEXIÓN \_ DEL PROXY DE RECEPCIÓN DE LA OPCIÓN \_ \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-381"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-382">Establece si se puede recuperar o no la entidad de respuesta del proxy.</span><span class="sxs-lookup"><span data-stu-id="49ba8-382">Sets whether or not the proxy response entity can be retrieved.</span></span> <span data-ttu-id="49ba8-383">Esta opción está deshabilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="49ba8-383">This option is disabled by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-384"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**TIEMPO DE ESPERA \_ DE RESPUESTA DE RECEPCIÓN DE LA OPCIÓN \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-384"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-385">Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, para esperar a recibir todos los encabezados de respuesta a una solicitud.</span><span class="sxs-lookup"><span data-stu-id="49ba8-385">Sets or retrieves an unsigned long integer value that contains the timeout value, in milliseconds, to wait to receive all response headers to a request.</span></span> <span data-ttu-id="49ba8-386">Si WinHTTP no recibe todos los encabezados dentro de este período de tiempo de espera, se cancela la solicitud.</span><span class="sxs-lookup"><span data-stu-id="49ba8-386">If WinHTTP fails to receive all the headers within this timeout period, the request is canceled.</span></span> <span data-ttu-id="49ba8-387">El valor de tiempo de espera predeterminado es de 90 segundos.</span><span class="sxs-lookup"><span data-stu-id="49ba8-387">The default timeout value is 90 seconds.</span></span>

<span data-ttu-id="49ba8-388">Este tiempo de espera solo se comprueba cuando se reciben datos del socket.</span><span class="sxs-lookup"><span data-stu-id="49ba8-388">This timeout is checked only when data is received from the socket.</span></span> <span data-ttu-id="49ba8-389">Como resultado, cuando expira el tiempo de espera, la aplicación cliente no se notifica hasta que llegan más datos del servidor.</span><span class="sxs-lookup"><span data-stu-id="49ba8-389">As a result, when the timeout expires the client application is not notified until more data arrives from the server.</span></span> <span data-ttu-id="49ba8-390">Si no llegan datos del servidor, el retraso entre la expiración del tiempo de espera y la notificación de la aplicación cliente podría ser tan grande como el valor de tiempo de espera establecido mediante el parámetro *dwReceiveTimeout* de la función [**WinHttpSetTimeouts.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)</span><span class="sxs-lookup"><span data-stu-id="49ba8-390">If no data arrives from the server, the delay between the timeout expiration and notification of the client application could be as large as the timeout value set using the *dwReceiveTimeout* parameter of the [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-391"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**TIEMPO DE ESPERA \_ DE RECEPCIÓN DE LA OPCIÓN \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-391"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-392">Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, para recibir una respuesta parcial a una solicitud o leer algunos datos.</span><span class="sxs-lookup"><span data-stu-id="49ba8-392">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a partial response to a request or read some data.</span></span> <span data-ttu-id="49ba8-393">Si la respuesta tarda más que este valor de tiempo de espera, se cancela la solicitud.</span><span class="sxs-lookup"><span data-stu-id="49ba8-393">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="49ba8-394">El valor predeterminado del tiempo de espera es de 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="49ba8-394">The default timeout value is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-395"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**DIRECTIVA DE REDIRECCIÓN \_ DE \_ OPCIONES WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-395"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP\_OPTION\_REDIRECT\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-396">Establece el comportamiento de WinHTTP con respecto al control de un código de estado de redirección HTTP 30x.</span><span class="sxs-lookup"><span data-stu-id="49ba8-396">Sets the behavior of WinHTTP regarding the handling of a 30x HTTP redirect status code.</span></span> <span data-ttu-id="49ba8-397">Esta opción se puede establecer en un identificador de sesión o solicitud en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="49ba8-397">This option can be set on a session or request handle to one of the following values:</span></span>

| <span data-ttu-id="49ba8-398">Término</span><span class="sxs-lookup"><span data-stu-id="49ba8-398">Term</span></span> | <span data-ttu-id="49ba8-399">Descripción</span><span class="sxs-lookup"><span data-stu-id="49ba8-399">Description</span></span> |
|-|-|
| <span data-ttu-id="49ba8-400"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>DIRECTIVA DE REDIRECCIÓN \_ DE \_ OPCIONES WINHTTP \_ \_ SIEMPRE</span><span class="sxs-lookup"><span data-stu-id="49ba8-400"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_ALWAYS</span></span> | <span data-ttu-id="49ba8-401">Todas las redirecciones se siguen automáticamente.</span><span class="sxs-lookup"><span data-stu-id="49ba8-401">All redirects are followed automatically.</span></span> |
| <span data-ttu-id="49ba8-402"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>DIRECTIVA DE REDIRECCIÓN \_ DE \_ OPCIONES WINHTTP NO PERMITE HTTPS \_ A \_ \_ \_ \_ HTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-402"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_DISALLOW\_HTTPS\_TO\_HTTP</span></span> | <span data-ttu-id="49ba8-403">Se siguen todas las redirecciones, excepto las que se originan desde una dirección URL segura (https) a una dirección URL no segura (http).</span><span class="sxs-lookup"><span data-stu-id="49ba8-403">All redirects are followed, except those that originate from a secure (https) URL to an unsecure (http) URL.</span></span> <span data-ttu-id="49ba8-404">Esta es la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="49ba8-404">This is the default setting.</span></span> |
| <span data-ttu-id="49ba8-405"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>DIRECTIVA DE REDIRECCIÓN \_ DE \_ OPCIONES WINHTTP \_ \_ NUNCA</span><span class="sxs-lookup"><span data-stu-id="49ba8-405"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_NEVER</span></span> | <span data-ttu-id="49ba8-406">Las redirecciones nunca se siguen.</span><span class="sxs-lookup"><span data-stu-id="49ba8-406">Redirects are never followed.</span></span> <span data-ttu-id="49ba8-407">El estado 30x se devuelve a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="49ba8-407">The 30x status is returned to the application.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-408"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**OPCIÓN WINHTTP \_ \_ RECHAZAR \_ USERPWD \_ EN \_ URL**</span><span class="sxs-lookup"><span data-stu-id="49ba8-408"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-409">Rechaza las direcciones URL que contienen un nombre de usuario y una contraseña.</span><span class="sxs-lookup"><span data-stu-id="49ba8-409">Rejects URLs that contain a username and password.</span></span> <span data-ttu-id="49ba8-410">Esta opción también rechaza las direcciones URL que contienen la semántica *username:password,* incluso si no se especifica ningún nombre de usuario o contraseña.</span><span class="sxs-lookup"><span data-stu-id="49ba8-410">This option also rejects URLs that contain *username:password* semantics, even if no username or password is specified.</span></span> <span data-ttu-id="49ba8-411">Por ejemplo, " ", " ", " " " y " " se marcaría u:p@hostname :@hostname como no u:@hostname :p@hostname válido.</span><span class="sxs-lookup"><span data-stu-id="49ba8-411">For example, "u:p@hostname", ":@hostname", "u:@hostname", and ":p@hostname" would all be flagged as invalid.</span></span> <span data-ttu-id="49ba8-412">Si se pasa una dirección URL no válida a la función, devuelve [ERROR \_ WINHTTP \_ INVALID \_ URL](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="49ba8-412">If an invalid URL is passed to the function, it returns [ERROR\_WINHTTP\_INVALID\_URL](error-messages.md).</span></span> <span data-ttu-id="49ba8-413">Esta opción está desactivada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="49ba8-413">This option is turned off by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-414"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**PRIORIDAD DE SOLICITUD \_ DE \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-414"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-415">Esta opción ha quedado en desuso; no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="49ba8-415">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-416"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**ESTADÍSTICAS DE SOLICITUD \_ DE \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-416"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP\_OPTION\_REQUEST\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-417">Retraives statistics for the request.</span><span class="sxs-lookup"><span data-stu-id="49ba8-417">Retreives statistics for the request.</span></span>  <span data-ttu-id="49ba8-418">Para obtener una lista de las estadísticas disponibles, vea [**ESTADÍSTICAS DE SOLICITUDES WINHTTP \_ \_**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span><span class="sxs-lookup"><span data-stu-id="49ba8-418">For a list of the available statistics, see [**WINHTTP\_REQUEST\_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-419"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**TIEMPOS DE SOLICITUD \_ DE \_ LA OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-419"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP\_OPTION\_REQUEST\_TIMES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-420">Retraive la información de tiempo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="49ba8-420">Retreives timing information for the request.</span></span> <span data-ttu-id="49ba8-421">Para obtener una lista de los intervalos disponibles, vea [**WINHTTP \_ REQUEST \_ TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span><span class="sxs-lookup"><span data-stu-id="49ba8-421">For a list of the available timings, see [**WINHTTP\_REQUEST\_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-422"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**OPCIÓN WINHTTP \_ REQUERIR \_ STREAM \_ \_ END**</span><span class="sxs-lookup"><span data-stu-id="49ba8-422"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**WINHTTP\_OPTION\_REQUIRE\_STREAM\_END**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="49ba8-423">Esta opción indica a WinHttp que ignore los encabezados de respuesta "Content-Length" y que siga recibiendo en una secuencia hasta que END_STREAM la marca.</span><span class="sxs-lookup"><span data-stu-id="49ba8-423">This option tells WinHttp to ignore "Content-Length" response headers, and continue receiving on a stream until the END_STREAM flag is received.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-424"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**NOMBRE DE HOST DE \_ RESOLUCIÓN \_ DE OPCIONES WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-424"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="49ba8-425">Esta opción se puede establecer en un identificador de solicitud WinHttp antes de que se haya enviado.</span><span class="sxs-lookup"><span data-stu-id="49ba8-425">This option can be set on a WinHttp request handle before it has been sent.</span></span> <span data-ttu-id="49ba8-426">Si se establece, WinHttp usará la cadena proporcionada por el autor de la llamada como nombre de host para la resolución DNS.</span><span class="sxs-lookup"><span data-stu-id="49ba8-426">If set, WinHttp will use the caller-provided string as the hostname for DNS resolution.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-427"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**OPCIÓN WINHTTP \_ RESOLVER \_ TIEMPO DE \_ ESPERA**</span><span class="sxs-lookup"><span data-stu-id="49ba8-427"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP\_OPTION\_RESOLVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-428">Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, para resolver un nombre de host.</span><span class="sxs-lookup"><span data-stu-id="49ba8-428">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to resolve a host name.</span></span> <span data-ttu-id="49ba8-429">El valor de tiempo de espera predeterminado **es INFINITE.**</span><span class="sxs-lookup"><span data-stu-id="49ba8-429">The default timeout value is **INFINITE**.</span></span> <span data-ttu-id="49ba8-430">Si se especifica un valor no predeterminado, hay una sobrecarga de una creación de subprocesos por resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="49ba8-430">If a non-default value is specified, there is an overhead of one thread-creation per name resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-431"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**PROTOCOLOS SEGUROS \_ DE \_ LA OPCIÓN WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-431"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP\_OPTION\_SECURE\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-432">Establece un valor entero largo sin signo que especifica qué protocolos seguros son aceptables.</span><span class="sxs-lookup"><span data-stu-id="49ba8-432">Sets an unsigned long integer value that specifies which secure protocols are acceptable.</span></span> <span data-ttu-id="49ba8-433">De forma predeterminada, solo SSL3 y TLS1 están habilitados en Windows 7 y Windows 8.</span><span class="sxs-lookup"><span data-stu-id="49ba8-433">By default only SSL3 and TLS1 are enabled in Windows 7 and Windows 8.</span></span> <span data-ttu-id="49ba8-434">De forma predeterminada, solo SSL3, TLS1.0, TLS1.1 y TLS1.2 están habilitados en Windows 8.1 y Windows 10.</span><span class="sxs-lookup"><span data-stu-id="49ba8-434">By default only SSL3, TLS1.0, TLS1.1, and TLS1.2 are enabled in Windows 8.1 and Windows 10.</span></span> <span data-ttu-id="49ba8-435">El valor puede ser una combinación de uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="49ba8-435">The value can be a combination of one or more of the following values.</span></span>

| <span data-ttu-id="49ba8-436">Término</span><span class="sxs-lookup"><span data-stu-id="49ba8-436">Term</span></span> | <span data-ttu-id="49ba8-437">Descripción</span><span class="sxs-lookup"><span data-stu-id="49ba8-437">Description</span></span> |
|-|-|
| <span data-ttu-id="49ba8-438"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>PROTOCOLO SEGURO DE MARCA WINHTTP \_ \_ \_ \_ ALL</span><span class="sxs-lookup"><span data-stu-id="49ba8-438"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_ALL</span></span> | <span data-ttu-id="49ba8-439">Se pueden Capa de sockets seguros (SSL) 2.0, SSL 3.0 y seguridad de la capa de transporte (TLS) 1.0.</span><span class="sxs-lookup"><span data-stu-id="49ba8-439">The Secure Sockets Layer (SSL) 2.0, SSL 3.0, and Transport Layer Security (TLS) 1.0 protocols can be used.</span></span> |
| <span data-ttu-id="49ba8-440"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>PROTOCOLO SEGURO \_ \_ DE MARCA \_ \_ WINHTTP SSL2</span><span class="sxs-lookup"><span data-stu-id="49ba8-440"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL2</span></span> | <span data-ttu-id="49ba8-441">Se puede usar el protocolo SSL 2.0.</span><span class="sxs-lookup"><span data-stu-id="49ba8-441">The SSL 2.0 protocol can be used.</span></span> |
| <span data-ttu-id="49ba8-442"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>PROTOCOLO SEGURO \_ \_ DE MARCA \_ \_ WINHTTP SSL3</span><span class="sxs-lookup"><span data-stu-id="49ba8-442"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL3</span></span> | <span data-ttu-id="49ba8-443">Se puede usar el protocolo SSL 3.0.</span><span class="sxs-lookup"><span data-stu-id="49ba8-443">The SSL 3.0 protocol can be used.</span></span> |
| <span data-ttu-id="49ba8-444"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>PROTOCOLO SEGURO \_ \_ DE MARCA \_ \_ WINHTTP TLS1</span><span class="sxs-lookup"><span data-stu-id="49ba8-444"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1</span></span> | <span data-ttu-id="49ba8-445">Se puede usar el protocolo TLS 1.0.</span><span class="sxs-lookup"><span data-stu-id="49ba8-445">The TLS 1.0 protocol can be used.</span></span> |
| <span data-ttu-id="49ba8-446"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>PROTOCOLO SEGURO \_ \_ DE MARCA \_ \_ WINHTTP TLS1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="49ba8-446"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_1</span></span> | <span data-ttu-id="49ba8-447">Se puede usar el protocolo TLS 1.1.</span><span class="sxs-lookup"><span data-stu-id="49ba8-447">The TLS 1.1 protocol can be used.</span></span> |
| <span data-ttu-id="49ba8-448"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>PROTOCOLO SEGURO \_ \_ DE MARCA \_ \_ WINHTTP TLS1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="49ba8-448"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_2</span></span> | <span data-ttu-id="49ba8-449">Se puede usar el protocolo TLS 1.2.</span><span class="sxs-lookup"><span data-stu-id="49ba8-449">The TLS 1.2 protocol can be used.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="49ba8-450"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**ESTRUCTURA DE CERTIFICADO \_ DE SEGURIDAD DE LA OPCIÓN \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-450"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-451">Recupera el certificado de un servidor SSL/TLS en la [**estructura WINHTTP \_ CERTIFICATE \_ INFO.**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)</span><span class="sxs-lookup"><span data-stu-id="49ba8-451">Retrieves the certificate for a SSL/TLS server into the [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="49ba8-452">La aplicación debe liberar los **miembros lpszSubjectInfo** y **lpszIssuerInfo** con [**LocalFree.**](/windows/desktop/api/winbase/nf-winbase-localfree)</span><span class="sxs-lookup"><span data-stu-id="49ba8-452">The application must free the **lpszSubjectInfo** and **lpszIssuerInfo** members with [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-453"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**MARCAS DE \_ SEGURIDAD DE \_ LA \_ OPCIÓN WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-453"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-454">Establece o recupera un valor entero largo sin signo que contiene las marcas de seguridad de un identificador.</span><span class="sxs-lookup"><span data-stu-id="49ba8-454">Sets or retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="49ba8-455">Puede ser una combinación de estos valores:</span><span class="sxs-lookup"><span data-stu-id="49ba8-455">It can be a combination of these values:</span></span>

| <span data-ttu-id="49ba8-456">Término</span><span class="sxs-lookup"><span data-stu-id="49ba8-456">Term</span></span> | <span data-ttu-id="49ba8-457">Descripción</span><span class="sxs-lookup"><span data-stu-id="49ba8-457">Description</span></span> |
|-|-|
| <span data-ttu-id="49ba8-458"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>LA MARCA \_ DE SEGURIDAD OMITIR CN DE CERTIFICADO NO ES \_ \_ \_ \_ VÁLIDA</span><span class="sxs-lookup"><span data-stu-id="49ba8-458"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span> |<span data-ttu-id="49ba8-459">Permite un nombre común no válido en un certificado; es decir, el nombre de servidor especificado por la aplicación no coincide con el nombre común del certificado.</span><span class="sxs-lookup"><span data-stu-id="49ba8-459">Allows an invalid common name in a certificate; that is, the server name specified by the application does not match the common name in the certificate.</span></span> <span data-ttu-id="49ba8-460">Si se establece esta marca, la aplicación no recibe una devolución de llamada **WINHTTP \_ CALLBACK \_ STATUS FLAG CERT CN \_ \_ \_ \_ INVALID.**</span><span class="sxs-lookup"><span data-stu-id="49ba8-460">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_CN\_INVALID** callback.</span></span> |
| <span data-ttu-id="49ba8-461"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>LA MARCA \_ DE SEGURIDAD OMITIR LA FECHA DE CERTIFICADO NO ES \_ \_ \_ \_ VÁLIDA</span><span class="sxs-lookup"><span data-stu-id="49ba8-461"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span> |<span data-ttu-id="49ba8-462">Permite una fecha de certificado no válida, es decir, un certificado expirado o aún no efectivo.</span><span class="sxs-lookup"><span data-stu-id="49ba8-462">Allows an invalid certificate date, that is, an expired or not-yet-effective certificate.</span></span> <span data-ttu-id="49ba8-463">Si se establece esta marca, la aplicación no recibe una devolución de llamada **CERT \_ DATE \_ \_ \_ \_ \_ INVALID** DE MARCA DE ESTADO DE DEVOLUCIÓN DE LLAMADA WINHTTP.</span><span class="sxs-lookup"><span data-stu-id="49ba8-463">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_DATE\_INVALID** callback.</span></span> |
| <span data-ttu-id="49ba8-464"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>MARCA DE \_ SEGURIDAD \_ OMITIR CA \_ \_ DESCONOCIDA</span><span class="sxs-lookup"><span data-stu-id="49ba8-464"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span> | <span data-ttu-id="49ba8-465">Permite una entidad de certificación no válida.</span><span class="sxs-lookup"><span data-stu-id="49ba8-465">Allows an invalid certificate authority.</span></span> <span data-ttu-id="49ba8-466">Si se establece esta marca, la aplicación no recibe una devolución de llamada DE CA NO VÁLIDA DE LA MARCA DE ESTADO DE DEVOLUCIÓN DE LLAMADA **WINHTTP. \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-466">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_INVALID\_CA** callback.</span></span> |
| <span data-ttu-id="49ba8-467"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>LA MARCA \_ DE SEGURIDAD OMITE EL USO INCORRECTO DEL \_ \_ \_ \_ CERTIFICADO</span><span class="sxs-lookup"><span data-stu-id="49ba8-467"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_CERT\_WRONG\_USAGE</span></span> | <span data-ttu-id="49ba8-468">Permite establecer la identidad de un servidor con un certificado que no es de servidor (por ejemplo, un certificado de cliente).</span><span class="sxs-lookup"><span data-stu-id="49ba8-468">Allows the identity of a server to be established with a non-server certificate (for example, a client certificate).</span></span> |
| <span data-ttu-id="49ba8-469"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>MARCA DE \_ SEGURIDAD \_ OMITIR FIRMA \_ \_ DÉBIL</span><span class="sxs-lookup"><span data-stu-id="49ba8-469"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span> | <span data-ttu-id="49ba8-470">Permite omitir una firma débil.</span><span class="sxs-lookup"><span data-stu-id="49ba8-470">Allows a weak signature to be ignored.</span></span><br/><span data-ttu-id="49ba8-471">Esta marca está disponible en la actualización de acumulación para cada sistema operativo a partir de Windows 7 y Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="49ba8-471">This flag is available in the rollup update for each OS starting with Windows 7 and Windows Server 2008 R2.</span></span> |
| <span data-ttu-id="49ba8-472"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>MARCA \_ DE SEGURIDAD \_ SEGURA</span><span class="sxs-lookup"><span data-stu-id="49ba8-472"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span> | <span data-ttu-id="49ba8-473">Usa transferencias seguras.</span><span class="sxs-lookup"><span data-stu-id="49ba8-473">Uses secure transfers.</span></span> <span data-ttu-id="49ba8-474">Esto solo se devuelve en una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="49ba8-474">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="49ba8-475"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>MEDIO \_ DE INTENSIDAD DE LA MARCA DE \_ \_ SEGURIDAD</span><span class="sxs-lookup"><span data-stu-id="49ba8-475"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span> | <span data-ttu-id="49ba8-476">Usa cifrado medio (56 bits).</span><span class="sxs-lookup"><span data-stu-id="49ba8-476">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="49ba8-477">Esto solo se devuelve en una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="49ba8-477">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="49ba8-478"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SEGURIDAD \_ FUERTE DE LA \_ MARCA \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-478"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span> | <span data-ttu-id="49ba8-479">Usa un cifrado seguro (de 128 bits).</span><span class="sxs-lookup"><span data-stu-id="49ba8-479">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="49ba8-480">Esto solo se devuelve en una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="49ba8-480">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="49ba8-481"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SEGURIDAD \_ DÉBIL DE LA INTENSIDAD DE LA \_ \_ MARCA</span><span class="sxs-lookup"><span data-stu-id="49ba8-481"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span> | <span data-ttu-id="49ba8-482">Usa cifrado débil (de 40 bits).</span><span class="sxs-lookup"><span data-stu-id="49ba8-482">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="49ba8-483">Esto solo se devuelve en una llamada a [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span><span class="sxs-lookup"><span data-stu-id="49ba8-483">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="49ba8-484"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**INFORMACIÓN DE SEGURIDAD \_ DE LA \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-484"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP\_OPTION\_SECURITY\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-485">Retraive la conexión de SChannel y la información de cifrado de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="49ba8-485">Retreives the SChannel connection and cipher information for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-486"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**VALOR DE BITS \_ DE CLAVE DE SEGURIDAD DE LA OPCIÓN \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-486"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-487">Recupera un valor entero largo sin signo que contiene la intensidad de cifrado de la clave de cifrado.</span><span class="sxs-lookup"><span data-stu-id="49ba8-487">Retrieves an unsigned long integer value that contains the cipher strength of the encryption key.</span></span> <span data-ttu-id="49ba8-488">Un número mayor indica un cifrado más seguro de la intensidad del cifrado.</span><span class="sxs-lookup"><span data-stu-id="49ba8-488">A larger number indicates stronger cipher strength encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-489"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**OPCIÓN WINHTTP \_ ENVIAR TIEMPO DE \_ \_ ESPERA**</span><span class="sxs-lookup"><span data-stu-id="49ba8-489"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-490">Establece o recupera un valor entero largo sin signo que contiene el valor de tiempo de espera, en milisegundos, para enviar una solicitud o escribir algunos datos.</span><span class="sxs-lookup"><span data-stu-id="49ba8-490">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to send a request or write some data.</span></span> <span data-ttu-id="49ba8-491">Si el envío de la solicitud tarda más tiempo que el tiempo de espera, se cancela la operación de envío.</span><span class="sxs-lookup"><span data-stu-id="49ba8-491">If sending the request takes longer than the timeout, the send operation is canceled.</span></span> <span data-ttu-id="49ba8-492">El tiempo de expiración predeterminado es de 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="49ba8-492">The default timeout is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-493"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP \_ OPTION \_ SERVER \_ CBT**</span><span class="sxs-lookup"><span data-stu-id="49ba8-493"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP\_OPTION\_SERVER\_CBT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-494">Obtiene un puntero a [**la estructura Enlaces SecPkgContext \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) que especifica un token de enlace de canal (CBT).</span><span class="sxs-lookup"><span data-stu-id="49ba8-494">Gets a pointer to [**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) structure that specifies a Channel Binding Token (CBT).</span></span>

<span data-ttu-id="49ba8-495">Un token de enlace de canal es una propiedad de un canal de transporte seguro y se usa para enlazar un canal de autenticación al canal de transporte seguro.</span><span class="sxs-lookup"><span data-stu-id="49ba8-495">A Channel Binding Token is a property of a secure transport channel and is used to bind an authentication channel to the secure transport channel.</span></span> <span data-ttu-id="49ba8-496">Este token solo se puede obtener con esta opción una vez establecida una conexión SSL.</span><span class="sxs-lookup"><span data-stu-id="49ba8-496">This token can only be obtained by this option after an SSL connection has been established.</span></span>

> [!Note]
> <span data-ttu-id="49ba8-497">Si se pasa esta opción y un valor **NULL** para *lpBuffer* a [**WinHttpQueryOption,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) se devolverá ERROR INSUFFICIENT BUFFER y el tamaño de byte necesario para el búfer en el parámetro \_ \_ *lpdwBufferLength.*</span><span class="sxs-lookup"><span data-stu-id="49ba8-497">Passing this option and a **null** value for *lpBuffer* to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) will return ERROR\_INSUFFICIENT\_BUFFER and the required byte size for the buffer in the *lpdwBufferLength* parameter.</span></span> <span data-ttu-id="49ba8-498">Este valor de tamaño de búfer devuelto se puede pasar en una llamada posterior para consultar el token de enlace de canal.</span><span class="sxs-lookup"><span data-stu-id="49ba8-498">This returned buffer size value can be passed in a subsequent call to query for the Channel Binding Token.</span></span> <span data-ttu-id="49ba8-499">Estos pasos son necesarios al controlar LA SOLICITUD DE ESTADO DE DEVOLUCIÓN DE LLAMADA DE WINHTTP si desea modificar los encabezados de solicitud \_ en función del token de enlace de \_ \_ canal.</span><span class="sxs-lookup"><span data-stu-id="49ba8-499">These steps are necessary when handling WINHTTP\_CALLBACK\_STATUS\_REQUEST if you want to modify request headers based on the Channel Binding Token.</span></span> <span data-ttu-id="49ba8-500">Tenga en cuenta que Windows XP y Vista no admiten la modificación de encabezados de solicitud durante esta devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="49ba8-500">Note that Windows XP and Vista do not support modifying request headers during this callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-501"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**CONTEXTO DE CADENA \_ DE CERTIFICADOS DE SERVIDOR DE OPCIÓN \_ \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-501"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-502">Recupera el contexto de la cadena de certificación del servidor.</span><span class="sxs-lookup"><span data-stu-id="49ba8-502">Retrieves the server certification chain context.</span></span> <span data-ttu-id="49ba8-503">**WINHTTP \_ OPTION \_ SERVER CERT CHAIN \_ \_ \_ CONTEXT** se puede pasar para obtener un puntero duplicado a **CERT CHAIN \_ \_ CONTEXT** para una cadena de certificados de servidor recibida durante una conexión SSL negociada.</span><span class="sxs-lookup"><span data-stu-id="49ba8-503">**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT** can be passed to obtain a duplicated pointer to the **CERT\_CHAIN\_CONTEXT** for a server certificate chain received during a negotiated SSL connection.</span></span> <span data-ttu-id="49ba8-504">El cliente debe llamar [**a CertFreeCertificateContext en**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) el puntero DE CONTEXTO DE PCCERT \_ devuelto que se rellena en el búfer.</span><span class="sxs-lookup"><span data-stu-id="49ba8-504">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-505"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**CONTEXTO DE CERTIFICADO \_ DE SERVIDOR DE LA OPCIÓN \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-505"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-506">Recupera el contexto de certificación del servidor.</span><span class="sxs-lookup"><span data-stu-id="49ba8-506">Retrieves the server certification context.</span></span> <span data-ttu-id="49ba8-507">**WINHTTP \_ OPTION \_ SERVER CERT CONTEXT \_ \_ se** puede pasar para obtener un puntero duplicado al [**CONTEXTO DE CERT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) para un certificado de servidor recibido durante una conexión SSL negociada.</span><span class="sxs-lookup"><span data-stu-id="49ba8-507">**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT** can be passed to obtain a duplicated pointer to the [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) for a server certificate received during a negotiated SSL connection.</span></span> <span data-ttu-id="49ba8-508">El cliente debe llamar [**a CertFreeCertificateContext en**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) el puntero DE CONTEXTO DE PCCERT \_ devuelto que se rellena en el búfer.</span><span class="sxs-lookup"><span data-stu-id="49ba8-508">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-509"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**OPCIÓN WINHTTP \_ SERVIDOR \_ \_ SPN \_ USADO**</span><span class="sxs-lookup"><span data-stu-id="49ba8-509"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**WINHTTP\_OPTION\_SERVER\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-510">Obtiene el nombre principal del servidor que WinHTTP proporcionó a SSPI durante la autenticación.</span><span class="sxs-lookup"><span data-stu-id="49ba8-510">Gets the server Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="49ba8-511">Este valor de cadena se puede pasar a [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) después de un error de autenticación.</span><span class="sxs-lookup"><span data-stu-id="49ba8-511">This string value can be passed to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-512"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**SPN DE \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-512"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP\_OPTION\_SPN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-513">Incluye o quita el número de puerto del servidor cuando se ha creado el SPN (nombre principal de servicio) para la autenticación Kerberos o Negotiate Kerberos.</span><span class="sxs-lookup"><span data-stu-id="49ba8-513">Includes or removes the server port number when the SPN (service principal name) is built for Kerberos or Negotiate Kerberos authentication.</span></span> <span data-ttu-id="49ba8-514">Esta marca es uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="49ba8-514">This flag is one of the following values:</span></span>

| <span data-ttu-id="49ba8-515">Término</span><span class="sxs-lookup"><span data-stu-id="49ba8-515">Term</span></span> | <span data-ttu-id="49ba8-516">Descripción</span><span class="sxs-lookup"><span data-stu-id="49ba8-516">Description</span></span> |
|-|-|
| <span data-ttu-id="49ba8-517"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP \_ DISABLE \_ SPN \_ SERVER \_ PORT</span><span class="sxs-lookup"><span data-stu-id="49ba8-517"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP\_DISABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="49ba8-518">Quita el número de puerto del servidor.</span><span class="sxs-lookup"><span data-stu-id="49ba8-518">Removes the server port number.</span></span> |
| <span data-ttu-id="49ba8-519"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP \_ ENABLE \_ SPN \_ SERVER \_ PORT</span><span class="sxs-lookup"><span data-stu-id="49ba8-519"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP\_ENABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="49ba8-520">Incluye el número de puerto del servidor.</span><span class="sxs-lookup"><span data-stu-id="49ba8-520">Includes the server port number.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="49ba8-521"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**CÓDIGO DE ERROR \_ DE SECUENCIA DE LA OPCIÓN \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-521"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**WINHTTP\_OPTION\_STREAM\_ERROR\_CODE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="49ba8-522">Esta opción se puede consultar en un identificador de solicitud WinHttp y devolverá el código de error indicado por un marco de RST_STREAM recibido en una secuencia HTTP.</span><span class="sxs-lookup"><span data-stu-id="49ba8-522">This option can be queried on a WinHttp request handle, and will return the error code indicated by a RST_STREAM frame received on an HTTP stream.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-523"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**OPCIÓN WINHTTP \_ \_ TCP FAST \_ \_ OPEN**</span><span class="sxs-lookup"><span data-stu-id="49ba8-523"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP\_OPTION\_TCP\_FAST\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-524">Habilita TCP Fast Open para la conexión.</span><span class="sxs-lookup"><span data-stu-id="49ba8-524">Enables TCP Fast Open for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-525"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**OPCIÓN WINHTTP \_ \_ TCP \_ KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="49ba8-525"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**WINHTTP\_OPTION\_TCP\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-526">Esta opción se puede establecer en un identificador de sesión WinHttp para habilitar el comportamiento de conexión de TCP en el socket subyacente.</span><span class="sxs-lookup"><span data-stu-id="49ba8-526">This option can be set on a WinHttp session handle to enable TCP keep-alive behavior on the underlying socket.</span></span> <span data-ttu-id="49ba8-527">Toma una [**estructura \_ tcp keepalive.**](/windows/win32/winsock/sio-keepalive-vals)</span><span class="sxs-lookup"><span data-stu-id="49ba8-527">Takes a [**tcp\_keepalive**](/windows/win32/winsock/sio-keepalive-vals) struct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-528"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**OPCIÓN WINHTTP \_ \_ TLS FALSE \_ \_ START**</span><span class="sxs-lookup"><span data-stu-id="49ba8-528"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP\_OPTION\_TLS\_FALSE\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-529">Habilita TLS False Start para la conexión.</span><span class="sxs-lookup"><span data-stu-id="49ba8-529">Enables TLS False Start for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-530"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**RESERVA NO SEGURA DEL PROTOCOLO TLS DE LA OPCIÓN \_ \_ \_ \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-530"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-531">Esta opción se puede establecer en un identificador de sesión WinHttp para controlar si se permite la reserva a TLS 1.0 si se produce un error de protocolo de enlace TLS con una versión de protocolo más reciente.</span><span class="sxs-lookup"><span data-stu-id="49ba8-531">This option can be set on a WinHttp session handle to control whether fallback to TLS 1.0 is allowed if there is a TLS handshake failure with a newer protocol version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-532"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**EVENTO DE \_ NOTIFICACIÓN DE DESCARGA DE LA OPCIÓN \_ WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-532"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-533">Toma un evento que se establecerá cuando se haya completado la última devolución de llamada para una sesión determinada.</span><span class="sxs-lookup"><span data-stu-id="49ba8-533">Takes an event that will be set when the last callback has completed for a particular session.</span></span> <span data-ttu-id="49ba8-534">Esta marca debe usarse en un identificador de sesión.</span><span class="sxs-lookup"><span data-stu-id="49ba8-534">This flag must be must be used on a session handle.</span></span> <span data-ttu-id="49ba8-535">El evento no se puede cerrar hasta que WinHTTP lo haya establecido.</span><span class="sxs-lookup"><span data-stu-id="49ba8-535">The event cannot be closed until after it has been set by WinHTTP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-536"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**ANÁLISIS DE ENCABEZADOS NO SEGUROS DE LA \_ \_ \_ \_ OPCIÓN WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-536"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-537">Esta opción está reservada para uso interno y no se debe llamar a .</span><span class="sxs-lookup"><span data-stu-id="49ba8-537">This option is reserved for internal use and should not be called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-538"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**ACTUALIZACIÓN DE LA OPCIÓN WINHTTP \_ \_ AL SOCKET \_ \_ \_ WEB**</span><span class="sxs-lookup"><span data-stu-id="49ba8-538"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-539">Indica a la pila que inicie un proceso de protocolo de enlace de WebSocket [**con WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="49ba8-539">Instructs the stack to start a WebSocket handshake process with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="49ba8-540">Esta opción no toma ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="49ba8-540">This option takes no parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-541"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**DIRECCIÓN URL DE LA OPCIÓN WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-541"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-542">Recupera un valor de cadena que contiene la dirección URL completa de un recurso descargado.</span><span class="sxs-lookup"><span data-stu-id="49ba8-542">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="49ba8-543">Si la dirección URL original contenía datos adicionales, como cadenas de búsqueda o delimitadores, o si se redirija la llamada, la dirección URL devuelta difiere de la original.</span><span class="sxs-lookup"><span data-stu-id="49ba8-543">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="49ba8-544">La aplicación debe pasar un búfer, con un tamaño en bytes, lo suficientemente grande como para contener la dirección URL devuelta en caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="49ba8-544">The application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-545"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**OPCIÓN WINHTTP \_ USAR CREDENCIALES DE SERVIDOR \_ \_ \_ \_ GLOBAL**</span><span class="sxs-lookup"><span data-stu-id="49ba8-545"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-546">Toma un **valor BOOL** y solo se puede establecer un identificador de sesión.</span><span class="sxs-lookup"><span data-stu-id="49ba8-546">Takes a **BOOL** and can be set only a session handle.</span></span> <span data-ttu-id="49ba8-547">Solo se propagará hacia abajo a los identificadores creados a partir del identificador de sesión una vez establecida la opción.</span><span class="sxs-lookup"><span data-stu-id="49ba8-547">It will only propagate down to handles created from the session handle after the option has been set.</span></span> <span data-ttu-id="49ba8-548">Si **es TRUE,** esta opción provoca como último recurso el uso de credenciales de servidor global que se insertaron desde WinInet.</span><span class="sxs-lookup"><span data-stu-id="49ba8-548">If **TRUE**, this option causes as a last resort the use of global server credentials that were pushed down from WinInet.</span></span> <span data-ttu-id="49ba8-549">El valor predeterminado de esta opción es **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="49ba8-549">The default for this option is **FALSE**.</span></span> <span data-ttu-id="49ba8-550">Esta opción requiere la clave del Registro **HKLM \\ Software Microsoft \\ Windows \\ \\ CurrentVersion Internet \\ Settings! ShareCredsWithWinHttp**.</span><span class="sxs-lookup"><span data-stu-id="49ba8-550">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="49ba8-551">Esta clave del Registro no está presente de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="49ba8-551">This registry key is not present by default.</span></span> <span data-ttu-id="49ba8-552">Cuando se establece, WinINet enviará las credenciales a WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="49ba8-552">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="49ba8-553">Cada vez que WinHttp obtiene un desafío de autenticación y no hay ninguna credencial establecida en el identificador actual, usará las credenciales proporcionadas por WinINet.</span><span class="sxs-lookup"><span data-stu-id="49ba8-553">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-554"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**AGENTE DE USUARIO \_ DE LA \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-554"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-555">Establece o recupera [](glossary.md) la cadena del agente de usuario en los identificadores proporcionados por [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) y usados en funciones [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) posteriores, siempre que no se invalide por un encabezado agregado por [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) **o WinHttpSendRequest**.</span><span class="sxs-lookup"><span data-stu-id="49ba8-555">Sets or retrieves the [*user agent*](glossary.md) string on handles supplied by [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) and used in subsequent [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) functions, as long as it is not overridden by a header added by [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) or **WinHttpSendRequest**.</span></span> <span data-ttu-id="49ba8-556">Al recuperar un agente de usuario, la aplicación debe pasar un búfer, con un tamaño en bytes, lo suficientemente grande como para contener la dirección URL devuelta en caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="49ba8-556">When retrieving a user agent, the application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span> <span data-ttu-id="49ba8-557">Al establecer el agente de usuario, el tamaño del búfer es la longitud de la cadena, en caracteres, más el terminador **NULL.**</span><span class="sxs-lookup"><span data-stu-id="49ba8-557">When setting the user agent, the buffer size is the length of the string, in characters, plus the **NULL** terminator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-558"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**NOMBRE DE USUARIO DE LA OPCIÓN WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-558"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-559">Establece o recupera una cadena que contiene el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="49ba8-559">Sets or retrieves a string that contains the user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-560"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**TIEMPO DE ESPERA \_ DE CIERRE DE SOCKET WEB DE LA \_ \_ \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-560"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-561">Establece el tiempo, en milisegundos, que [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) debe esperar para completar el protocolo de enlace de cierre.</span><span class="sxs-lookup"><span data-stu-id="49ba8-561">Sets the time, in milliseconds, that [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) should wait to complete the close handshake.</span></span> <span data-ttu-id="49ba8-562">El valor predeterminado es 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="49ba8-562">The default is 10 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-563"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**OPCIÓN WINHTTP \_ \_ WEB SOCKET \_ \_ \_ KEEPALIVE INTERVAL**</span><span class="sxs-lookup"><span data-stu-id="49ba8-563"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-564">Establece el intervalo, en milisegundos, para enviar un paquete keep-alive a través de la conexión.</span><span class="sxs-lookup"><span data-stu-id="49ba8-564">Sets the interval, in milliseconds, to send a keep-alive packet over the connection.</span></span> <span data-ttu-id="49ba8-565">El intervalo predeterminado es 30 000 (30 segundos).</span><span class="sxs-lookup"><span data-stu-id="49ba8-565">The default interval is 30000 (30 seconds).</span></span> <span data-ttu-id="49ba8-566">El intervalo mínimo es 15 000 (15 segundos).</span><span class="sxs-lookup"><span data-stu-id="49ba8-566">The minimum interval is 15000 (15 seconds).</span></span> <span data-ttu-id="49ba8-567">El [**uso de WinHttpSetOption para**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) establecer un valor inferior a 15000 devolverá con ERROR INVALID **\_ \_ PARAMETER**.</span><span class="sxs-lookup"><span data-stu-id="49ba8-567">Using [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to set a value lower than 15000 will return with **ERROR\_INVALID\_PARAMETER**.</span></span>

> [!Note]
> <span data-ttu-id="49ba8-568">El valor predeterminado de **WINHTTP \_ OPTION WEB SOCKET \_ \_ \_ KEEPALIVE \_ INTERVAL** se lee de **HKLM: \\ SOFTWARE Microsoft \\ \\ WebSocket \\ KeepaliveInterval**.</span><span class="sxs-lookup"><span data-stu-id="49ba8-568">The default value for **WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL** is read from **HKLM:\\SOFTWARE\\Microsoft\\WebSocket\\KeepaliveInterval**.</span></span> <span data-ttu-id="49ba8-569">Si no se establece un valor, se usará el valor predeterminado de 30000.</span><span class="sxs-lookup"><span data-stu-id="49ba8-569">If a value is not set, the default value of 30000 will be used.</span></span> <span data-ttu-id="49ba8-570">No es posible tener un intervalo de keepalive inferior a 15 000 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="49ba8-570">It is not possible to have a lower keepalive interval than 15000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-571"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**TAMAÑO DEL BÚFER DE RECEPCIÓN DE LA OPCIÓN WINHTTP \_ \_ WEB \_ SOCKET \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-571"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-572">Establece o recupera un DWORD que especifica el tamaño del búfer de recepción que se va a usar en las conexiones de WebSocket.</span><span class="sxs-lookup"><span data-stu-id="49ba8-572">Sets or retrieves a DWORD which specifies the receive buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-573"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**TAMAÑO DEL BÚFER DE ENVÍO DE SOCKET WEB DE LA \_ \_ \_ \_ \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-573"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-574">Establece o recupera un DWORD que especifica el tamaño del búfer de envío que se usará en las conexiones webSocket.</span><span class="sxs-lookup"><span data-stu-id="49ba8-574">Sets or retrieves a DWORD which specifies the send buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-575"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**RECUENTO DE \_ SUBPROCESOS \_ DE TRABAJO DE LA \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-575"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-576">Establece un valor entero largo sin signo que especifica el número de subprocesos de trabajo que el grupo de subprocesos debe usar para las finalizaciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="49ba8-576">Sets an unsigned long integer value that specifies the number of worker threads the thread pool should use for asynchronous completions.</span></span> <span data-ttu-id="49ba8-577">El valor predeterminado de esta opción es cero, que especifica que el número de subprocesos de trabajo es igual al número de CPU del sistema.</span><span class="sxs-lookup"><span data-stu-id="49ba8-577">The default value of this option is zero, which specifies that the number of worker threads is equal to the number of CPUs on the system.</span></span> <span data-ttu-id="49ba8-578">Esta opción solo se puede establecer en un **identificador NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) antes de que se haya producido una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="49ba8-578">This option can only be set on a **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) handle before an asynchronous operation has occurred.</span></span> <span data-ttu-id="49ba8-579">Esta opción solo se puede establecer una vez.</span><span class="sxs-lookup"><span data-stu-id="49ba8-579">This option can only be set once.</span></span>

<span data-ttu-id="49ba8-580">**Windows Server 2008 R2 y Windows 7:** Esta marca está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="49ba8-580">**Windows Server 2008 R2 and Windows 7:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="49ba8-581"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**TAMAÑO DEL BÚFER \_ DE ESCRITURA DE LA \_ \_ OPCIÓN \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-581"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="49ba8-582">Esta opción ha quedado en desuso; no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="49ba8-582">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49ba8-583">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49ba8-583">Remarks</span></span>

<span data-ttu-id="49ba8-584">En la tabla siguiente se enumeran las marcas de opción especificando los identificadores sobre los que pueden actuar, si se pueden consultar y establecer, y el tipo de datos utilizado.</span><span class="sxs-lookup"><span data-stu-id="49ba8-584">The following table lists the option flags by specifying which handles they can act upon, whether they can be queried and set, and the data type used.</span></span> <span data-ttu-id="49ba8-585">Una "X" indica que la marca de opción es válida para su uso con la función o el identificador, mientras que "-" especifica que la marca de opción no es válida.</span><span class="sxs-lookup"><span data-stu-id="49ba8-585">An "X" indicates that the option flag is valid for use with the function or handle, while a "-" specifies that the option flag is invalid.</span></span>

<span data-ttu-id="49ba8-586">Al intentar establecer o consultar una marca de opción en una versión de Windows en la que no se admite, se producirá **el error \_ WINHTTP INVALID \_ \_ OPTION**.</span><span class="sxs-lookup"><span data-stu-id="49ba8-586">Attempting to set or query an option flag on a Windows version where it is not supported will result in **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span>

| <span data-ttu-id="49ba8-587">Marca de opción y tipo de datos</span><span class="sxs-lookup"><span data-stu-id="49ba8-587">Option flag, and data type</span></span> | <span data-ttu-id="49ba8-588">Identificador de sesión</span><span class="sxs-lookup"><span data-stu-id="49ba8-588">Session handle</span></span> | <span data-ttu-id="49ba8-589">Identificador de solicitud</span><span class="sxs-lookup"><span data-stu-id="49ba8-589">Request handle</span></span> | <span data-ttu-id="49ba8-590">Opción de consulta</span><span class="sxs-lookup"><span data-stu-id="49ba8-590">Query option</span></span> | <span data-ttu-id="49ba8-591">Opción SET</span><span class="sxs-lookup"><span data-stu-id="49ba8-591">Set option</span></span> | <span data-ttu-id="49ba8-592">Versión mínima de Windows</span><span class="sxs-lookup"><span data-stu-id="49ba8-592">Minimum Windows Version</span></span> |
|-|-|-|-|-|-|
| <span data-ttu-id="49ba8-593">OPCIÓN WINHTTP \_ QUE GARANTIZA DEVOLUCIONES DE LLAMADA SIN \_ \_ \_ \_ BLOQUEO</span><span class="sxs-lookup"><span data-stu-id="49ba8-593">WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS</span></span><br/><span data-ttu-id="49ba8-594">**Bool**</span><span class="sxs-lookup"><span data-stu-id="49ba8-594">**BOOL**</span></span> | <span data-ttu-id="49ba8-595">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-595">X</span></span> | \- | \- | <span data-ttu-id="49ba8-596">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-596">X</span></span> | \- |
| <span data-ttu-id="49ba8-597">DIRECTIVA DE \_ INICIO DE SESIÓN AUTOMÁTICO DE LA OPCIÓN \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-597">WINHTTP\_OPTION\_AUTOLOGON\_POLICY</span></span><br/><span data-ttu-id="49ba8-598">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-598">**DWORD**</span></span> | \- | <span data-ttu-id="49ba8-599">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-599">X</span></span> | \- | <span data-ttu-id="49ba8-600">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-600">X</span></span> | \- |
| <span data-ttu-id="49ba8-601">CONEXIONES EN \_ SEGUNDO PLANO DE LA \_ OPCIÓN WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-601">WINHTTP\_OPTION\_BACKGROUND\_CONNECTIONS</span></span><br/><span data-ttu-id="49ba8-602">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-602">**DWORD**</span></span> | <span data-ttu-id="49ba8-603">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-603">X</span></span> | \- | \- | <span data-ttu-id="49ba8-604">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-604">X</span></span> | <span data-ttu-id="49ba8-605">Windows 10 versión 21H1</span><span class="sxs-lookup"><span data-stu-id="49ba8-605">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="49ba8-606">DEVOLUCIÓN DE LLAMADA \_ DE LA \_ OPCIÓN WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-606">WINHTTP\_OPTION\_CALLBACK</span></span><br/><span data-ttu-id="49ba8-607">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="49ba8-607">**LPVOID**</span></span> | <span data-ttu-id="49ba8-608">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-608">X</span></span> | <span data-ttu-id="49ba8-609">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-609">X</span></span> | <span data-ttu-id="49ba8-610">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-610">X</span></span> | <span data-ttu-id="49ba8-611">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-611">X</span></span> | \- |
| <span data-ttu-id="49ba8-612">CONTEXTO DE CERTIFICADO \_ DE CLIENTE DE LA OPCIÓN \_ \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-612">WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="49ba8-613">**CONTEXTO \_ DE CERT**</span><span class="sxs-lookup"><span data-stu-id="49ba8-613">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="49ba8-614">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-614">X</span></span> | \- | <span data-ttu-id="49ba8-615">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-615">X</span></span> | <span data-ttu-id="49ba8-616">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49ba8-616">Windows Vista</span></span> |
| <span data-ttu-id="49ba8-617">LISTA DE \_ \_ EMISORES DE \_ CERTIFICADOS DE CLIENTE DE LA \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-617">WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST</span></span><br/>[<span data-ttu-id="49ba8-618">**SecPkgContext \_ IssuerListInfoEx**</span><span class="sxs-lookup"><span data-stu-id="49ba8-618">**SecPkgContext\_IssuerListInfoEx**</span></span>](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | <span data-ttu-id="49ba8-619">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-619">X</span></span> | <span data-ttu-id="49ba8-620">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-620">X</span></span> | \- | <span data-ttu-id="49ba8-621">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49ba8-621">Windows Vista</span></span> |
| <span data-ttu-id="49ba8-622">PÁGINA DE CÓDIGOS \_ DE LA \_ OPCIÓN WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-622">WINHTTP\_OPTION\_CODEPAGE</span></span><br/><span data-ttu-id="49ba8-623">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-623">**DWORD**</span></span> | <span data-ttu-id="49ba8-624">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-624">X</span></span> | \- | \- | <span data-ttu-id="49ba8-625">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-625">X</span></span> | \- |
| <span data-ttu-id="49ba8-626">OPCIÓN WINHTTP \_ CONFIGURAR \_ LA \_ AUTENTICACIÓN DE \_ PASSPORT</span><span class="sxs-lookup"><span data-stu-id="49ba8-626">WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH</span></span><br/><span data-ttu-id="49ba8-627">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-627">**DWORD**</span></span> | <span data-ttu-id="49ba8-628">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-628">X</span></span> | \- | \- | <span data-ttu-id="49ba8-629">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-629">X</span></span> | \- |
| <span data-ttu-id="49ba8-630">REINTENTOS DE \_ CONEXIÓN DE LA OPCIÓN \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-630">WINHTTP\_OPTION\_CONNECT\_RETRIES</span></span><br/><span data-ttu-id="49ba8-631">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-631">**DWORD**</span></span> | <span data-ttu-id="49ba8-632">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-632">X</span></span> | <span data-ttu-id="49ba8-633">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-633">X</span></span> | <span data-ttu-id="49ba8-634">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-634">X</span></span> | <span data-ttu-id="49ba8-635">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-635">X</span></span> | \- |
| <span data-ttu-id="49ba8-636">OPCIÓN WINHTTP \_ CONNECT \_ \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="49ba8-636">WINHTTP\_OPTION\_CONNECT\_TIMEOUT</span></span><br/><span data-ttu-id="49ba8-637">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-637">**DWORD**</span></span> | <span data-ttu-id="49ba8-638">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-638">X</span></span> | <span data-ttu-id="49ba8-639">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-639">X</span></span> | <span data-ttu-id="49ba8-640">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-640">X</span></span> | <span data-ttu-id="49ba8-641">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-641">X</span></span> | \- |
| <span data-ttu-id="49ba8-642">INFORMACIÓN DE CONEXIÓN \_ DE LA \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-642">WINHTTP\_OPTION\_CONNECTION\_INFO</span></span><br/>[<span data-ttu-id="49ba8-643">**INFORMACIÓN DE CONEXIÓN \_ \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-643">**WINHTTP\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | <span data-ttu-id="49ba8-644">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-644">X</span></span> | <span data-ttu-id="49ba8-645">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-645">X</span></span> | \- | \- |
| <span data-ttu-id="49ba8-646">WINHTTP \_ OPTION \_ CONNECTION \_ STATS \_ V0</span><span class="sxs-lookup"><span data-stu-id="49ba8-646">WINHTTP\_OPTION\_CONNECTION\_STATS\_V0</span></span><br/>[<span data-ttu-id="49ba8-647">**TCP \_ INFO \_ v0**</span><span class="sxs-lookup"><span data-stu-id="49ba8-647">**TCP\_INFO\_v0**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | <span data-ttu-id="49ba8-648">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-648">X</span></span> | <span data-ttu-id="49ba8-649">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-649">X</span></span> | \- | <span data-ttu-id="49ba8-650">Windows 10 versión 1903</span><span class="sxs-lookup"><span data-stu-id="49ba8-650">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="49ba8-651">ESTADÍSTICAS DE CONEXIÓN DE LA OPCIÓN WINHTTP \_ \_ \_ \_ V1</span><span class="sxs-lookup"><span data-stu-id="49ba8-651">WINHTTP\_OPTION\_CONNECTION\_STATS\_V1</span></span><br/>[<span data-ttu-id="49ba8-652">**TCP \_ INFO \_ v1**</span><span class="sxs-lookup"><span data-stu-id="49ba8-652">**TCP\_INFO\_v1**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | <span data-ttu-id="49ba8-653">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-653">X</span></span> | <span data-ttu-id="49ba8-654">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-654">X</span></span> | \- | <span data-ttu-id="49ba8-655">Windows 10 versión 2004</span><span class="sxs-lookup"><span data-stu-id="49ba8-655">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="49ba8-656">VALOR DE CONTEXTO \_ DE LA \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-656">WINHTTP\_OPTION\_CONTEXT\_VALUE</span></span><br/><span data-ttu-id="49ba8-657">**DWORD \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="49ba8-657">**DWORD\_PTR**</span></span> | <span data-ttu-id="49ba8-658">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-658">X</span></span> | <span data-ttu-id="49ba8-659">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-659">X</span></span> | <span data-ttu-id="49ba8-660">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-660">X</span></span> | <span data-ttu-id="49ba8-661">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-661">X</span></span> | \- |
| <span data-ttu-id="49ba8-662">\_DESCOMPRESIÓN DE LA OPCIÓN WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-662">WINHTTP\_OPTION\_DECOMPRESSION</span></span><br/><span data-ttu-id="49ba8-663">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-663">**DWORD**</span></span> | <span data-ttu-id="49ba8-664">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-664">X</span></span> | <span data-ttu-id="49ba8-665">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-665">X</span></span> | \- | <span data-ttu-id="49ba8-666">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-666">X</span></span> | <span data-ttu-id="49ba8-667">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="49ba8-667">Windows 8.1</span></span> |
| <span data-ttu-id="49ba8-668">OPCIÓN WINHTTP \_ DESHABILITAR LA CREACIÓN DE CADENA DE \_ \_ \_ \_ CERTIFICADOS</span><span class="sxs-lookup"><span data-stu-id="49ba8-668">WINHTTP\_OPTION\_DISABLE\_CERT\_CHAIN\_BUILDING</span></span><br/><span data-ttu-id="49ba8-669">**Bool**</span><span class="sxs-lookup"><span data-stu-id="49ba8-669">**BOOL**</span></span> | <span data-ttu-id="49ba8-670">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-670">X</span></span> | \- | \- | <span data-ttu-id="49ba8-671">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-671">X</span></span> | <span data-ttu-id="49ba8-672">Windows 10 versión 21H1</span><span class="sxs-lookup"><span data-stu-id="49ba8-672">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="49ba8-673">CARACTERÍSTICA DESHABILITAR OPCIÓN WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-673">WINHTTP\_OPTION\_DISABLE\_FEATURE</span></span><br/><span data-ttu-id="49ba8-674">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-674">**DWORD**</span></span> | \- | <span data-ttu-id="49ba8-675">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-675">X</span></span> | \- | <span data-ttu-id="49ba8-676">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-676">X</span></span> | \- |
| <span data-ttu-id="49ba8-677">OPCIÓN WINHTTP \_ DESHABILITAR RESERVA DE PROTOCOLO \_ \_ \_ \_ SEGURO</span><span class="sxs-lookup"><span data-stu-id="49ba8-677">WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK</span></span><br/><span data-ttu-id="49ba8-678">**Bool**</span><span class="sxs-lookup"><span data-stu-id="49ba8-678">**BOOL**</span></span> | <span data-ttu-id="49ba8-679">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-679">X</span></span> | \- | \- | <span data-ttu-id="49ba8-680">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-680">X</span></span> | <span data-ttu-id="49ba8-681">Windows 10 versión 1903</span><span class="sxs-lookup"><span data-stu-id="49ba8-681">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="49ba8-682">OPCIÓN WINHTTP \_ DESHABILITAR \_ COLA DE \_ \_ TRANSMISIONES</span><span class="sxs-lookup"><span data-stu-id="49ba8-682">WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE</span></span><br/><span data-ttu-id="49ba8-683">**Bool**</span><span class="sxs-lookup"><span data-stu-id="49ba8-683">**BOOL**</span></span> | <span data-ttu-id="49ba8-684">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-684">X</span></span> | <span data-ttu-id="49ba8-685">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-685">X</span></span> | \- | <span data-ttu-id="49ba8-686">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-686">X</span></span> | <span data-ttu-id="49ba8-687">Windows 10 versión 1809</span><span class="sxs-lookup"><span data-stu-id="49ba8-687">Windows 10 Version 1809</span></span> |
| <span data-ttu-id="49ba8-688">CARACTERÍSTICA HABILITAR OPCIÓN WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-688">WINHTTP\_OPTION\_ENABLE\_FEATURE</span></span><br/><span data-ttu-id="49ba8-689">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-689">**DWORD**</span></span> | \* | \* | \- | <span data-ttu-id="49ba8-690">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-690">X</span></span> | \- |
| <span data-ttu-id="49ba8-691">OPCIÓN WINHTTP \_ HABILITAR \_ PROTOCOLO \_ HTTP \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-691">WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL</span></span><br/><span data-ttu-id="49ba8-692">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-692">**DWORD**</span></span> | <span data-ttu-id="49ba8-693">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-693">X</span></span> | <span data-ttu-id="49ba8-694">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-694">X</span></span> | \- | <span data-ttu-id="49ba8-695">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-695">X</span></span> | <span data-ttu-id="49ba8-696">Windows 10 Versión 1607</span><span class="sxs-lookup"><span data-stu-id="49ba8-696">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="49ba8-697">OPCIÓN WINHTTP \_ HABILITAR \_ \_ HTTP2 \_ MÁS EL CONTEXTO DE CERTIFICADO DE \_ \_ \_ CLIENTE</span><span class="sxs-lookup"><span data-stu-id="49ba8-697">WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT\_CONTEXT</span></span><br/><span data-ttu-id="49ba8-698">**Bool**</span><span class="sxs-lookup"><span data-stu-id="49ba8-698">**BOOL**</span></span> | <span data-ttu-id="49ba8-699">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-699">X</span></span> | \- | \- | <span data-ttu-id="49ba8-700">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-700">X</span></span> | <span data-ttu-id="49ba8-701">Windows 10 versión 21H1</span><span class="sxs-lookup"><span data-stu-id="49ba8-701">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="49ba8-702">HABILITACIÓN \_ DE LA OPCIÓN \_ WINHTTPTRACING</span><span class="sxs-lookup"><span data-stu-id="49ba8-702">WINHTTP\_OPTION\_ENABLETRACING</span></span><br/><span data-ttu-id="49ba8-703">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-703">**DWORD**</span></span> | \- | \- | <span data-ttu-id="49ba8-704">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-704">X</span></span> | <span data-ttu-id="49ba8-705">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-705">X</span></span> | \- |
| <span data-ttu-id="49ba8-706">CODIFICACIÓN \_ ADICIONAL DE LA \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-706">WINHTTP\_OPTION\_ENCODE\_EXTRA</span></span><br/><span data-ttu-id="49ba8-707">**Bool**</span><span class="sxs-lookup"><span data-stu-id="49ba8-707">**BOOL**</span></span> | <span data-ttu-id="49ba8-708">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-708">X</span></span> | <span data-ttu-id="49ba8-709">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-709">X</span></span> | \- | <span data-ttu-id="49ba8-710">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-710">X</span></span> | <span data-ttu-id="49ba8-711">Windows 10 versión 1803</span><span class="sxs-lookup"><span data-stu-id="49ba8-711">Windows 10 Version 1803</span></span> |
| <span data-ttu-id="49ba8-712">OPCIÓN WINHTTP \_ \_ EXPIRE \_ CONNECTION</span><span class="sxs-lookup"><span data-stu-id="49ba8-712">WINHTTP\_OPTION\_EXPIRE\_CONNECTION</span></span><br/><span data-ttu-id="49ba8-713">N/D</span><span class="sxs-lookup"><span data-stu-id="49ba8-713">N/A</span></span> | \- | <span data-ttu-id="49ba8-714">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-714">X</span></span> | \- | <span data-ttu-id="49ba8-715">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-715">X</span></span> | <span data-ttu-id="49ba8-716">Windows 10 versión 1903</span><span class="sxs-lookup"><span data-stu-id="49ba8-716">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="49ba8-717">ERROR EXTENDIDO DE LA OPCIÓN WINHTTP \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-717">WINHTTP\_OPTION\_EXTENDED\_ERROR</span></span><br/><span data-ttu-id="49ba8-718">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-718">**DWORD**</span></span> | <span data-ttu-id="49ba8-719">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-719">X</span></span> | <span data-ttu-id="49ba8-720">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-720">X</span></span> | <span data-ttu-id="49ba8-721">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-721">X</span></span> | \- | \- |
| <span data-ttu-id="49ba8-722">PRIMERA CONEXIÓN DISPONIBLE \_ DE LA \_ OPCIÓN \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-722">WINHTTP\_OPTION\_FIRST\_AVAILABLE\_CONNECTION</span></span><br/><span data-ttu-id="49ba8-723">**Bool**</span><span class="sxs-lookup"><span data-stu-id="49ba8-723">**BOOL**</span></span> | <span data-ttu-id="49ba8-724">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-724">X</span></span> | \- | \- | <span data-ttu-id="49ba8-725">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-725">X</span></span> | <span data-ttu-id="49ba8-726">Windows 10 versión 21H1</span><span class="sxs-lookup"><span data-stu-id="49ba8-726">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="49ba8-727">CREDS DE PROXY GLOBAL DE \_ \_ LA OPCIÓN \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-727">WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS</span></span><br/>[<span data-ttu-id="49ba8-728">**CREDS DE WINHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-728">**WINHTTP\_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | <span data-ttu-id="49ba8-729">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-729">X</span></span> | <span data-ttu-id="49ba8-730">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-730">X</span></span> | \- | <span data-ttu-id="49ba8-731">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-731">X</span></span> | \- |
| <span data-ttu-id="49ba8-732">WINHTTP \_ OPTION \_ GLOBAL \_ SERVER \_ CREDS</span><span class="sxs-lookup"><span data-stu-id="49ba8-732">WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS</span></span><br/>[<span data-ttu-id="49ba8-733">**WINHTTP \_ CREDS \_ EX**</span><span class="sxs-lookup"><span data-stu-id="49ba8-733">**WINHTTP\_CREDS\_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | <span data-ttu-id="49ba8-734">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-734">X</span></span> | <span data-ttu-id="49ba8-735">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-735">X</span></span> | \- | <span data-ttu-id="49ba8-736">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-736">X</span></span> | \- |
| <span data-ttu-id="49ba8-737">TIPO DE IDENTIFICADOR \_ DE OPCIÓN \_ WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-737">WINHTTP\_OPTION\_HANDLE\_TYPE</span></span><br/><span data-ttu-id="49ba8-738">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-738">**DWORD**</span></span> | <span data-ttu-id="49ba8-739">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-739">X</span></span> | <span data-ttu-id="49ba8-740">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-740">X</span></span> | <span data-ttu-id="49ba8-741">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-741">X</span></span> | \- | \- |
| <span data-ttu-id="49ba8-742">SE REQUIERE \_ EL PROTOCOLO HTTP DE LA OPCIÓN \_ \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-742">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED</span></span><br/><span data-ttu-id="49ba8-743">**Bool**</span><span class="sxs-lookup"><span data-stu-id="49ba8-743">**BOOL**</span></span> | <span data-ttu-id="49ba8-744">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-744">X</span></span> | <span data-ttu-id="49ba8-745">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-745">X</span></span> | \- | <span data-ttu-id="49ba8-746">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-746">X</span></span> | <span data-ttu-id="49ba8-747">Windows 10 versión 1903</span><span class="sxs-lookup"><span data-stu-id="49ba8-747">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="49ba8-748">SE USA EL PROTOCOLO HTTP DE \_ \_ LA OPCIÓN WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-748">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED</span></span><br/><span data-ttu-id="49ba8-749">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-749">**DWORD**</span></span> | \- | <span data-ttu-id="49ba8-750">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-750">X</span></span> | <span data-ttu-id="49ba8-751">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-751">X</span></span> | \- | <span data-ttu-id="49ba8-752">Windows 10 Versión 1607</span><span class="sxs-lookup"><span data-stu-id="49ba8-752">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="49ba8-753">VERSIÓN HTTP DE \_ LA OPCIÓN \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-753">WINHTTP\_OPTION\_HTTP\_VERSION</span></span><br/>[<span data-ttu-id="49ba8-754">**INFORMACIÓN \_ DE VERSIÓN \_ HTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-754">**HTTP\_VERSION\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | <span data-ttu-id="49ba8-755">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-755">X</span></span> | <span data-ttu-id="49ba8-756">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-756">X</span></span> | <span data-ttu-id="49ba8-757">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-757">X</span></span> | <span data-ttu-id="49ba8-758">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-758">X</span></span> | \- |
| <span data-ttu-id="49ba8-759">OPCIÓN WINHTTP \_ \_ HTTP2 \_ KEEPALIVE</span><span class="sxs-lookup"><span data-stu-id="49ba8-759">WINHTTP\_OPTION\_HTTP2\_KEEPALIVE</span></span><br/><span data-ttu-id="49ba8-760">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-760">**DWORD**</span></span> | <span data-ttu-id="49ba8-761">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-761">X</span></span> | \- | \- | <span data-ttu-id="49ba8-762">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-762">X</span></span> | <span data-ttu-id="49ba8-763">Windows 10 versión 21H1</span><span class="sxs-lookup"><span data-stu-id="49ba8-763">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="49ba8-764">OPCIÓN WINHTTP \_ \_ HTTP2 \_ MÁS \_ CODIFICACIÓN DE \_ TRANSFERENCIA</span><span class="sxs-lookup"><span data-stu-id="49ba8-764">WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING</span></span><br/><span data-ttu-id="49ba8-765">**Bool**</span><span class="sxs-lookup"><span data-stu-id="49ba8-765">**BOOL**</span></span> | <span data-ttu-id="49ba8-766">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-766">X</span></span> | <span data-ttu-id="49ba8-767">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-767">X</span></span> | \- | <span data-ttu-id="49ba8-768">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-768">X</span></span> | <span data-ttu-id="49ba8-769">Windows 10 versión 21H1</span><span class="sxs-lookup"><span data-stu-id="49ba8-769">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="49ba8-770">OPCIÓN WINHTTP \_ OMITIR \_ \_ REVOCACIÓN \_ DE CERTIFICADOS SIN \_ CONEXIÓN</span><span class="sxs-lookup"><span data-stu-id="49ba8-770">WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE</span></span><br/><span data-ttu-id="49ba8-771">**Bool**</span><span class="sxs-lookup"><span data-stu-id="49ba8-771">**BOOL**</span></span> | \- | <span data-ttu-id="49ba8-772">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-772">X</span></span> | \- | <span data-ttu-id="49ba8-773">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-773">X</span></span> | <span data-ttu-id="49ba8-774">Windows 10 versión 2004</span><span class="sxs-lookup"><span data-stu-id="49ba8-774">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="49ba8-775">OPCIÓN WINHTTP \_ \_ IPV6 \_ FAST \_ FALLBACK</span><span class="sxs-lookup"><span data-stu-id="49ba8-775">WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK</span></span><br/><span data-ttu-id="49ba8-776">**Bool**</span><span class="sxs-lookup"><span data-stu-id="49ba8-776">**BOOL**</span></span> | <span data-ttu-id="49ba8-777">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-777">X</span></span> | \- | \- | <span data-ttu-id="49ba8-778">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-778">X</span></span> | <span data-ttu-id="49ba8-779">Windows 10 versión 1903</span><span class="sxs-lookup"><span data-stu-id="49ba8-779">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="49ba8-780">LA OPCIÓN WINHTTP \_ ES RESPUESTA DE CONEXIÓN DE \_ \_ \_ \_ PROXY</span><span class="sxs-lookup"><span data-stu-id="49ba8-780">WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="49ba8-781">**Bool**</span><span class="sxs-lookup"><span data-stu-id="49ba8-781">**BOOL**</span></span> | <span data-ttu-id="49ba8-782">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-782">X</span></span> | <span data-ttu-id="49ba8-783">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-783">X</span></span> | <span data-ttu-id="49ba8-784">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-784">X</span></span> | \- | \- |
| <span data-ttu-id="49ba8-785">OPCIÓN WINHTTP \_ \_ NÚMERO MÁXIMO DE \_ CONNS \_ POR \_ 1 \_ 0 \_ SERVIDOR</span><span class="sxs-lookup"><span data-stu-id="49ba8-785">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER</span></span><br/><span data-ttu-id="49ba8-786">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-786">**DWORD**</span></span> | <span data-ttu-id="49ba8-787">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-787">X</span></span> | \- | <span data-ttu-id="49ba8-788">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-788">X</span></span> | <span data-ttu-id="49ba8-789">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-789">X</span></span> | \- |
| <span data-ttu-id="49ba8-790">OPCIÓN WINHTTP \_ \_ NÚMERO MÁXIMO DE \_ \_ CONNS POR \_ SERVIDOR</span><span class="sxs-lookup"><span data-stu-id="49ba8-790">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER</span></span><br/><span data-ttu-id="49ba8-791">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-791">**DWORD**</span></span> | <span data-ttu-id="49ba8-792">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-792">X</span></span> | \- | <span data-ttu-id="49ba8-793">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-793">X</span></span> | <span data-ttu-id="49ba8-794">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-794">X</span></span> | \- |
| <span data-ttu-id="49ba8-795">OPCIÓN WINHTTP \_ \_ MAX HTTP AUTOMATIC \_ \_ \_ REDIRECTS</span><span class="sxs-lookup"><span data-stu-id="49ba8-795">WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS</span></span><br/><span data-ttu-id="49ba8-796">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-796">**DWORD**</span></span> | <span data-ttu-id="49ba8-797">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-797">X</span></span> | <span data-ttu-id="49ba8-798">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-798">X</span></span> | <span data-ttu-id="49ba8-799">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-799">X</span></span> | <span data-ttu-id="49ba8-800">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-800">X</span></span> | \- |
| <span data-ttu-id="49ba8-801">OPCIÓN WINHTTP \_ \_ MAX HTTP STATUS \_ \_ \_ CONTINUE</span><span class="sxs-lookup"><span data-stu-id="49ba8-801">WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE</span></span><br/><span data-ttu-id="49ba8-802">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-802">**DWORD**</span></span> | <span data-ttu-id="49ba8-803">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-803">X</span></span> | <span data-ttu-id="49ba8-804">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-804">X</span></span> | <span data-ttu-id="49ba8-805">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-805">X</span></span> | <span data-ttu-id="49ba8-806">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-806">X</span></span> | \- |
| <span data-ttu-id="49ba8-807">TAMAÑO MÁXIMO DE PURGA DE RESPUESTA DE LA \_ \_ \_ \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-807">WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE</span></span><br/><span data-ttu-id="49ba8-808">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-808">**DWORD**</span></span> | <span data-ttu-id="49ba8-809">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-809">X</span></span> | <span data-ttu-id="49ba8-810">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-810">X</span></span> | <span data-ttu-id="49ba8-811">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-811">X</span></span> | <span data-ttu-id="49ba8-812">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-812">X</span></span> | \- |
| <span data-ttu-id="49ba8-813">TAMAÑO MÁXIMO \_ DE ENCABEZADO DE RESPUESTA DE LA \_ \_ \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-813">WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE</span></span><br/><span data-ttu-id="49ba8-814">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-814">**DWORD**</span></span> | <span data-ttu-id="49ba8-815">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-815">X</span></span> | <span data-ttu-id="49ba8-816">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-816">X</span></span> | <span data-ttu-id="49ba8-817">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-817">X</span></span> | <span data-ttu-id="49ba8-818">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-818">X</span></span> | \- |
| <span data-ttu-id="49ba8-819">IDENTIFICADOR PRIMARIO DE \_ LA \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-819">WINHTTP\_OPTION\_PARENT\_HANDLE</span></span><br/>[<span data-ttu-id="49ba8-820">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="49ba8-820">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="49ba8-821">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-821">X</span></span> | <span data-ttu-id="49ba8-822">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-822">X</span></span> | <span data-ttu-id="49ba8-823">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-823">X</span></span> | \- | \- |
| <span data-ttu-id="49ba8-824">TEXTO DE MARCA DE PASSPORT DE LA \_ \_ \_ OPCIÓN WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-824">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT</span></span><br/><span data-ttu-id="49ba8-825">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="49ba8-825">**LPWSTR**</span></span> | \- | <span data-ttu-id="49ba8-826">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-826">X</span></span> | <span data-ttu-id="49ba8-827">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-827">X</span></span> | \- | \- |
| <span data-ttu-id="49ba8-828">DIRECCIÓN URL DE \_ \_ COBRANDING DE LA OPCIÓN WINHTTP PASSPORT \_ \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-828">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL</span></span><br/><span data-ttu-id="49ba8-829">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="49ba8-829">**LPWSTR**</span></span> | \- | <span data-ttu-id="49ba8-830">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-830">X</span></span> | <span data-ttu-id="49ba8-831">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-831">X</span></span> | \- | \- |
| <span data-ttu-id="49ba8-832">DIRECCIÓN URL DE \_ RETORNO DE PASSPORT DE LA \_ OPCIÓN WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-832">WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL</span></span><br/><span data-ttu-id="49ba8-833">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="49ba8-833">**LPVOID**</span></span> | \- | <span data-ttu-id="49ba8-834">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-834">X</span></span> | <span data-ttu-id="49ba8-835">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-835">X</span></span> | \- | \- |
| <span data-ttu-id="49ba8-836">OPCIÓN WINHTTP \_ \_ PASSPORT SIGN \_ \_ OUT</span><span class="sxs-lookup"><span data-stu-id="49ba8-836">WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT</span></span><br/><span data-ttu-id="49ba8-837">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="49ba8-837">**LPVOID**</span></span> | <span data-ttu-id="49ba8-838">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-838">X</span></span> | \- | \- | <span data-ttu-id="49ba8-839">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-839">X</span></span> | \- |
| <span data-ttu-id="49ba8-840">CONTRASEÑA DE LA OPCIÓN WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-840">WINHTTP\_OPTION\_PASSWORD</span></span><br/><span data-ttu-id="49ba8-841">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="49ba8-841">**LPWSTR**</span></span> | \- | <span data-ttu-id="49ba8-842">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-842">X</span></span> | <span data-ttu-id="49ba8-843">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-843">X</span></span> | <span data-ttu-id="49ba8-844">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-844">X</span></span> | \- |
| <span data-ttu-id="49ba8-845">PROXY DE \_ OPCIÓN WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-845">WINHTTP\_OPTION\_PROXY</span></span><br/>[<span data-ttu-id="49ba8-846">**INFORMACIÓN DEL PROXY WINHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="49ba8-846">**WINHTTP\_PROXY\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | <span data-ttu-id="49ba8-847">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-847">X</span></span> | <span data-ttu-id="49ba8-848">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-848">X</span></span> | <span data-ttu-id="49ba8-849">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-849">X</span></span> | <span data-ttu-id="49ba8-850">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-850">X</span></span> | \- |
| <span data-ttu-id="49ba8-851">CONTRASEÑA DE \_ PROXY DE \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-851">WINHTTP\_OPTION\_PROXY\_PASSWORD</span></span><br/><span data-ttu-id="49ba8-852">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="49ba8-852">**LPWSTR**</span></span> | \- | <span data-ttu-id="49ba8-853">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-853">X</span></span> | <span data-ttu-id="49ba8-854">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-854">X</span></span> | <span data-ttu-id="49ba8-855">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-855">X</span></span> | \- |
| <span data-ttu-id="49ba8-856">SPN DE \_ \_ PROXY DE OPCIÓN \_ WINHTTP \_ USADO</span><span class="sxs-lookup"><span data-stu-id="49ba8-856">WINHTTP\_OPTION\_PROXY\_SPN\_USED</span></span><br/><span data-ttu-id="49ba8-857">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="49ba8-857">**LPWSTR**</span></span> | \- | <span data-ttu-id="49ba8-858">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-858">X</span></span> | <span data-ttu-id="49ba8-859">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-859">X</span></span> | \- | \- |
| <span data-ttu-id="49ba8-860">NOMBRE DE USUARIO \_ DEL PROXY DE OPCIÓN \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-860">WINHTTP\_OPTION\_PROXY\_USERNAME</span></span><br/><span data-ttu-id="49ba8-861">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="49ba8-861">**LPWSTR**</span></span> | \- | <span data-ttu-id="49ba8-862">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-862">X</span></span> | <span data-ttu-id="49ba8-863">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-863">X</span></span> | <span data-ttu-id="49ba8-864">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-864">X</span></span> | \- |
| <span data-ttu-id="49ba8-865">TAMAÑO DEL BÚFER \_ DE LECTURA DE LA \_ \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-865">WINHTTP\_OPTION\_READ\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="49ba8-866">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-866">**DWORD**</span></span> | \- | <span data-ttu-id="49ba8-867">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-867">X</span></span> | <span data-ttu-id="49ba8-868">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-868">X</span></span> | <span data-ttu-id="49ba8-869">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-869">X</span></span> | \- |
| <span data-ttu-id="49ba8-870">RESPUESTA DE \_ CONEXIÓN DEL PROXY DE RECEPCIÓN DE LA OPCIÓN \_ \_ \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-870">WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="49ba8-871">**Bool**</span><span class="sxs-lookup"><span data-stu-id="49ba8-871">**BOOL**</span></span> | <span data-ttu-id="49ba8-872">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-872">X</span></span> | <span data-ttu-id="49ba8-873">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-873">X</span></span> | \- | <span data-ttu-id="49ba8-874">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-874">X</span></span> | \- |
| <span data-ttu-id="49ba8-875">TIEMPO DE ESPERA \_ DE RESPUESTA DE RECEPCIÓN DE LA OPCIÓN \_ \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-875">WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT</span></span><br/><span data-ttu-id="49ba8-876">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-876">**DWORD**</span></span> | <span data-ttu-id="49ba8-877">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-877">X</span></span> | <span data-ttu-id="49ba8-878">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-878">X</span></span> | <span data-ttu-id="49ba8-879">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-879">X</span></span> | <span data-ttu-id="49ba8-880">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-880">X</span></span> | \- |
| <span data-ttu-id="49ba8-881">TIEMPO DE ESPERA \_ DE RECEPCIÓN DE LA OPCIÓN \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-881">WINHTTP\_OPTION\_RECEIVE\_TIMEOUT</span></span><br/><span data-ttu-id="49ba8-882">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-882">**DWORD**</span></span> | <span data-ttu-id="49ba8-883">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-883">X</span></span> | <span data-ttu-id="49ba8-884">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-884">X</span></span> | <span data-ttu-id="49ba8-885">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-885">X</span></span> | <span data-ttu-id="49ba8-886">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-886">X</span></span> | \- |
| <span data-ttu-id="49ba8-887">DIRECTIVA DE REDIRECCIÓN \_ DE \_ OPCIONES \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-887">WINHTTP\_OPTION\_REDIRECT\_POLICY</span></span><br/><span data-ttu-id="49ba8-888">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-888">**DWORD**</span></span> | <span data-ttu-id="49ba8-889">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-889">X</span></span> | <span data-ttu-id="49ba8-890">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-890">X</span></span> | <span data-ttu-id="49ba8-891">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-891">X</span></span> | <span data-ttu-id="49ba8-892">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-892">X</span></span> | \- |
| <span data-ttu-id="49ba8-893">OPCIÓN WINHTTP \_ \_ RECHAZAR \_ USERPWD \_ EN LA DIRECCIÓN \_ URL</span><span class="sxs-lookup"><span data-stu-id="49ba8-893">WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL</span></span><br/><span data-ttu-id="49ba8-894">**Bool**</span><span class="sxs-lookup"><span data-stu-id="49ba8-894">**BOOL**</span></span> | \- | <span data-ttu-id="49ba8-895">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-895">X</span></span> | \- | <span data-ttu-id="49ba8-896">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-896">X</span></span> | \- |
| <span data-ttu-id="49ba8-897">PRIORIDAD DE \_ SOLICITUD DE LA OPCIÓN \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-897">WINHTTP\_OPTION\_REQUEST\_PRIORITY</span></span><br/><span data-ttu-id="49ba8-898">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-898">**DWORD**</span></span> | \- | <span data-ttu-id="49ba8-899">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-899">X</span></span> | <span data-ttu-id="49ba8-900">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-900">X</span></span> | <span data-ttu-id="49ba8-901">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-901">X</span></span> | \- |
| <span data-ttu-id="49ba8-902">ESTADÍSTICAS DE SOLICITUD \_ DE \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-902">WINHTTP\_OPTION\_REQUEST\_STATS</span></span><br/>[<span data-ttu-id="49ba8-903">**ESTADÍSTICAS DE \_ SOLICITUDES \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-903">**WINHTTP\_REQUEST\_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | <span data-ttu-id="49ba8-904">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-904">X</span></span> | <span data-ttu-id="49ba8-905">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-905">X</span></span> | \- | <span data-ttu-id="49ba8-906">Windows 10 versión 1903</span><span class="sxs-lookup"><span data-stu-id="49ba8-906">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="49ba8-907">TIEMPOS DE SOLICITUD \_ DE \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-907">WINHTTP\_OPTION\_REQUEST\_TIMES</span></span><br/>[<span data-ttu-id="49ba8-908">**TIEMPOS DE \_ SOLICITUD \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-908">**WINHTTP\_REQUEST\_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | <span data-ttu-id="49ba8-909">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-909">X</span></span> | <span data-ttu-id="49ba8-910">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-910">X</span></span> | \- | <span data-ttu-id="49ba8-911">Windows 10 versión 1903</span><span class="sxs-lookup"><span data-stu-id="49ba8-911">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="49ba8-912">OPCIÓN WINHTTP \_ REQUERIR \_ STREAM \_ \_ END</span><span class="sxs-lookup"><span data-stu-id="49ba8-912">WINHTTP\_OPTION\_REQUIRE\_STREAM\_END</span></span><br/><span data-ttu-id="49ba8-913">**Bool**</span><span class="sxs-lookup"><span data-stu-id="49ba8-913">**BOOL**</span></span> | <span data-ttu-id="49ba8-914">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-914">X</span></span> | <span data-ttu-id="49ba8-915">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-915">X</span></span> | \- | <span data-ttu-id="49ba8-916">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-916">X</span></span> | <span data-ttu-id="49ba8-917">Windows 10 versión 21H1</span><span class="sxs-lookup"><span data-stu-id="49ba8-917">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="49ba8-918">NOMBRE DE HOST DE \_ RESOLUCIÓN \_ DE OPCIONES WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-918">WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME</span></span><br/><span data-ttu-id="49ba8-919">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="49ba8-919">**LPWSTR**</span></span> | \- | <span data-ttu-id="49ba8-920">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-920">X</span></span> | \- | <span data-ttu-id="49ba8-921">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-921">X</span></span> | <span data-ttu-id="49ba8-922">Windows 10 versión 21H1</span><span class="sxs-lookup"><span data-stu-id="49ba8-922">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="49ba8-923">OPCIÓN WINHTTP \_ RESOLVER \_ TIEMPO DE \_ ESPERA</span><span class="sxs-lookup"><span data-stu-id="49ba8-923">WINHTTP\_OPTION\_RESOLVE\_TIMEOUT</span></span><br/><span data-ttu-id="49ba8-924">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-924">**DWORD**</span></span> | <span data-ttu-id="49ba8-925">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-925">X</span></span> | <span data-ttu-id="49ba8-926">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-926">X</span></span> | <span data-ttu-id="49ba8-927">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-927">X</span></span> | <span data-ttu-id="49ba8-928">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-928">X</span></span> | \- |
| <span data-ttu-id="49ba8-929">PROTOCOLOS SEGUROS \_ DE \_ LA OPCIÓN WINHTTP \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-929">WINHTTP\_OPTION\_SECURE\_PROTOCOLS</span></span><br/><span data-ttu-id="49ba8-930">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-930">**DWORD**</span></span> | <span data-ttu-id="49ba8-931">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-931">X</span></span> | \- | \- | <span data-ttu-id="49ba8-932">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-932">X</span></span> | \- |
| <span data-ttu-id="49ba8-933">ESTRUCTURA DE CERTIFICADO \_ DE SEGURIDAD DE LA OPCIÓN \_ \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-933">WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT</span></span><br/>[<span data-ttu-id="49ba8-934">**INFORMACIÓN DEL \_ CERTIFICADO \_ WINHTTP**</span><span class="sxs-lookup"><span data-stu-id="49ba8-934">**WINHTTP\_CERTIFICATE\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | <span data-ttu-id="49ba8-935">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-935">X</span></span> | <span data-ttu-id="49ba8-936">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-936">X</span></span> | \- | \- |
| <span data-ttu-id="49ba8-937">MARCAS DE \_ SEGURIDAD DE \_ LA \_ OPCIÓN WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-937">WINHTTP\_OPTION\_SECURITY\_FLAGS</span></span><br/><span data-ttu-id="49ba8-938">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-938">**DWORD**</span></span> | \- | <span data-ttu-id="49ba8-939">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-939">X</span></span> | <span data-ttu-id="49ba8-940">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-940">X</span></span> | <span data-ttu-id="49ba8-941">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-941">X</span></span> | \- |
| <span data-ttu-id="49ba8-942">INFORMACIÓN DE SEGURIDAD \_ DE LA \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-942">WINHTTP\_OPTION\_SECURITY\_INFO</span></span><br/>[<span data-ttu-id="49ba8-943">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="49ba8-943">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | <span data-ttu-id="49ba8-944">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-944">X</span></span> | <span data-ttu-id="49ba8-945">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-945">X</span></span> | \- | <span data-ttu-id="49ba8-946">Windows 10 versión 2004</span><span class="sxs-lookup"><span data-stu-id="49ba8-946">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="49ba8-947">VALOR DE BITS \_ DE CLAVE DE SEGURIDAD DE LA \_ \_ \_ OPCIÓN WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-947">WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS</span></span><br/><span data-ttu-id="49ba8-948">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-948">**DWORD**</span></span> | \- | <span data-ttu-id="49ba8-949">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-949">X</span></span> | <span data-ttu-id="49ba8-950">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-950">X</span></span> | \- | \- |
| <span data-ttu-id="49ba8-951">OPCIÓN WINHTTP \_ ENVIAR \_ TIEMPO DE \_ ESPERA</span><span class="sxs-lookup"><span data-stu-id="49ba8-951">WINHTTP\_OPTION\_SEND\_TIMEOUT</span></span><br/><span data-ttu-id="49ba8-952">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-952">**DWORD**</span></span> | <span data-ttu-id="49ba8-953">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-953">X</span></span> | <span data-ttu-id="49ba8-954">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-954">X</span></span> | <span data-ttu-id="49ba8-955">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-955">X</span></span> | <span data-ttu-id="49ba8-956">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-956">X</span></span> | \- |
| <span data-ttu-id="49ba8-957">WINHTTP \_ OPTION \_ SERVER \_ CBT</span><span class="sxs-lookup"><span data-stu-id="49ba8-957">WINHTTP\_OPTION\_SERVER\_CBT</span></span><br/><span data-ttu-id="49ba8-958">[**Enlaces \_ SecPkgContext**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span><span class="sxs-lookup"><span data-stu-id="49ba8-958">[**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span></span> | \- | <span data-ttu-id="49ba8-959">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-959">X</span></span> | <span data-ttu-id="49ba8-960">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-960">X</span></span> | \- | \- |
| <span data-ttu-id="49ba8-961">CONTEXTO DE CADENA \_ DE CERTIFICADOS DE SERVIDOR DE OPCIÓN \_ \_ \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-961">WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT</span></span><br/>[<span data-ttu-id="49ba8-962">**CERT_CHAIN_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="49ba8-962">**CERT_CHAIN_CONTEXT**</span></span>](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | <span data-ttu-id="49ba8-963">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-963">X</span></span> | <span data-ttu-id="49ba8-964">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-964">X</span></span> | \- | <span data-ttu-id="49ba8-965">Windows 10 versión 2004</span><span class="sxs-lookup"><span data-stu-id="49ba8-965">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="49ba8-966">CONTEXTO DE CERTIFICADO \_ DE SERVIDOR DE LA OPCIÓN \_ \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-966">WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="49ba8-967">**CONTEXTO DE CERT**</span><span class="sxs-lookup"><span data-stu-id="49ba8-967">**CERT CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="49ba8-968">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-968">X</span></span> | <span data-ttu-id="49ba8-969">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-969">X</span></span> | \- | \- |
| <span data-ttu-id="49ba8-970">OPCIÓN WINHTTP \_ SERVIDOR \_ \_ SPN \_ USADO</span><span class="sxs-lookup"><span data-stu-id="49ba8-970">WINHTTP\_OPTION\_SERVER\_SPN\_USED</span></span><br/><span data-ttu-id="49ba8-971">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="49ba8-971">**LPWSTR**</span></span> | \- | <span data-ttu-id="49ba8-972">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-972">X</span></span> | <span data-ttu-id="49ba8-973">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-973">X</span></span> | \- | \- |
| <span data-ttu-id="49ba8-974">SPN DE \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-974">WINHTTP\_OPTION\_SPN</span></span><br/><span data-ttu-id="49ba8-975">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-975">**DWORD**</span></span> | \- | <span data-ttu-id="49ba8-976">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-976">X</span></span> | \- | <span data-ttu-id="49ba8-977">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-977">X</span></span> | \- |
| <span data-ttu-id="49ba8-978">CÓDIGO DE ERROR \_ DE SECUENCIA DE LA OPCIÓN \_ \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-978">WINHTTP\_OPTION\_STREAM\_ERROR\_CODE</span></span><br/><span data-ttu-id="49ba8-979">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-979">**DWORD**</span></span> | \- | <span data-ttu-id="49ba8-980">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-980">X</span></span> | <span data-ttu-id="49ba8-981">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-981">X</span></span> | \- | <span data-ttu-id="49ba8-982">Windows 10 versión 21H1</span><span class="sxs-lookup"><span data-stu-id="49ba8-982">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="49ba8-983">OPCIÓN WINHTTP \_ \_ TCP FAST \_ \_ OPEN</span><span class="sxs-lookup"><span data-stu-id="49ba8-983">WINHTTP\_OPTION\_TCP\_FAST\_OPEN</span></span><br/><span data-ttu-id="49ba8-984">**Bool**</span><span class="sxs-lookup"><span data-stu-id="49ba8-984">**BOOL**</span></span> | <span data-ttu-id="49ba8-985">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-985">X</span></span> | \- | \- | <span data-ttu-id="49ba8-986">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-986">X</span></span> | <span data-ttu-id="49ba8-987">Windows 10 versión 2004</span><span class="sxs-lookup"><span data-stu-id="49ba8-987">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="49ba8-988">OPCIÓN WINHTTP \_ \_ TCP \_ KEEPALIVE</span><span class="sxs-lookup"><span data-stu-id="49ba8-988">WINHTTP\_OPTION\_TCP\_KEEPALIVE</span></span><br/>[<span data-ttu-id="49ba8-989">**tcp \_ keepalive**</span><span class="sxs-lookup"><span data-stu-id="49ba8-989">**tcp\_keepalive**</span></span>](/windows/win32/winsock/sio-keepalive-vals) | <span data-ttu-id="49ba8-990">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-990">X</span></span> | \- | \- | <span data-ttu-id="49ba8-991">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-991">X</span></span> | <span data-ttu-id="49ba8-992">Windows 10 versión 2004</span><span class="sxs-lookup"><span data-stu-id="49ba8-992">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="49ba8-993">OPCIÓN WINHTTP \_ \_ TLS FALSE \_ \_ START</span><span class="sxs-lookup"><span data-stu-id="49ba8-993">WINHTTP\_OPTION\_TLS\_FALSE\_START</span></span><br/><span data-ttu-id="49ba8-994">**Bool**</span><span class="sxs-lookup"><span data-stu-id="49ba8-994">**BOOL**</span></span> | <span data-ttu-id="49ba8-995">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-995">X</span></span> | \- | \- | <span data-ttu-id="49ba8-996">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-996">X</span></span> | <span data-ttu-id="49ba8-997">Windows 10 versión 2004</span><span class="sxs-lookup"><span data-stu-id="49ba8-997">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="49ba8-998">RESERVA NO SEGURA \_ DEL PROTOCOLO TLS DE LA OPCIÓN \_ \_ \_ \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-998">WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK</span></span><br/><span data-ttu-id="49ba8-999">**Bool**</span><span class="sxs-lookup"><span data-stu-id="49ba8-999">**BOOL**</span></span> | <span data-ttu-id="49ba8-1000">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1000">X</span></span> | \- | \- | <span data-ttu-id="49ba8-1001">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1001">X</span></span> | <span data-ttu-id="49ba8-1002">Windows 10 versión 21H1</span><span class="sxs-lookup"><span data-stu-id="49ba8-1002">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="49ba8-1003">EVENTO UNLOAD \_ NOTIFY DE LA OPCIÓN \_ WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-1003">WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT</span></span><br/>[<span data-ttu-id="49ba8-1004">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="49ba8-1004">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="49ba8-1005">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1005">X</span></span> | \- | \- | <span data-ttu-id="49ba8-1006">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1006">X</span></span> | \- |
| <span data-ttu-id="49ba8-1007">ANÁLISIS DE \_ \_ ENCABEZADOS NO \_ SEGUROS DE LA \_ OPCIÓN WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-1007">WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING</span></span><br/><span data-ttu-id="49ba8-1008">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-1008">**DWORD**</span></span> | \- | <span data-ttu-id="49ba8-1009">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1009">X</span></span> | \- | <span data-ttu-id="49ba8-1010">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1010">X</span></span> | \- |
| <span data-ttu-id="49ba8-1011">ACTUALIZACIÓN DE LA OPCIÓN WINHTTP \_ \_ AL SOCKET \_ \_ \_ WEB</span><span class="sxs-lookup"><span data-stu-id="49ba8-1011">WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET</span></span><br/><span data-ttu-id="49ba8-1012">N/D</span><span class="sxs-lookup"><span data-stu-id="49ba8-1012">N/A</span></span> | \- | <span data-ttu-id="49ba8-1013">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1013">X</span></span> | \- | <span data-ttu-id="49ba8-1014">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1014">X</span></span> | \- |
| <span data-ttu-id="49ba8-1015">DIRECCIÓN URL DE LA OPCIÓN WINHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-1015">WINHTTP\_OPTION\_URL</span></span><br/><span data-ttu-id="49ba8-1016">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="49ba8-1016">**LPWSTR**</span></span> | \- | <span data-ttu-id="49ba8-1017">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1017">X</span></span> | <span data-ttu-id="49ba8-1018">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1018">X</span></span> | \- | \- |
| <span data-ttu-id="49ba8-1019">OPCIÓN WINHTTP \_ USAR CREDENCIALES DE SERVIDOR \_ \_ \_ \_ GLOBAL</span><span class="sxs-lookup"><span data-stu-id="49ba8-1019">WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS</span></span><br/><span data-ttu-id="49ba8-1020">**Bool**</span><span class="sxs-lookup"><span data-stu-id="49ba8-1020">**BOOL**</span></span> | <span data-ttu-id="49ba8-1021">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1021">X</span></span> | <span data-ttu-id="49ba8-1022">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1022">X</span></span> | \- | <span data-ttu-id="49ba8-1023">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1023">X</span></span> | \- |
| <span data-ttu-id="49ba8-1024">AGENTE DE USUARIO DE \_ \_ LA OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-1024">WINHTTP\_OPTION\_USER\_AGENT</span></span><br/><span data-ttu-id="49ba8-1025">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="49ba8-1025">**LPWSTR**</span></span> | <span data-ttu-id="49ba8-1026">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1026">X</span></span> | \- | <span data-ttu-id="49ba8-1027">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1027">X</span></span> | <span data-ttu-id="49ba8-1028">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1028">X</span></span> | \- |
| <span data-ttu-id="49ba8-1029">NOMBRE DE USUARIO DE \_ LA OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-1029">WINHTTP\_OPTION\_USERNAME</span></span><br/><span data-ttu-id="49ba8-1030">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="49ba8-1030">**LPWSTR**</span></span> | \- | <span data-ttu-id="49ba8-1031">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1031">X</span></span> | <span data-ttu-id="49ba8-1032">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1032">X</span></span> | <span data-ttu-id="49ba8-1033">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1033">X</span></span> | \- |
| <span data-ttu-id="49ba8-1034">OPCIÓN WINHTTP \_ TIEMPO DE ESPERA DE CIERRE DE SOCKET \_ \_ \_ \_ WEB</span><span class="sxs-lookup"><span data-stu-id="49ba8-1034">WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT</span></span><br/><span data-ttu-id="49ba8-1035">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-1035">**DWORD**</span></span> | \- | \- | <span data-ttu-id="49ba8-1036">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1036">X</span></span> | <span data-ttu-id="49ba8-1037">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1037">X</span></span> | \- |
| <span data-ttu-id="49ba8-1038">OPCIÓN WINHTTP \_ \_ WEB SOCKET \_ \_ KEEPALIVE \_ INTERVAL</span><span class="sxs-lookup"><span data-stu-id="49ba8-1038">WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL</span></span><br/><span data-ttu-id="49ba8-1039">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-1039">**DWORD**</span></span> | \- | \- | <span data-ttu-id="49ba8-1040">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1040">X</span></span> | <span data-ttu-id="49ba8-1041">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1041">X</span></span> | \- |
| <span data-ttu-id="49ba8-1042">TAMAÑO DEL BÚFER \_ DE RECEPCIÓN DE LA OPCIÓN WINHTTP \_ \_ WEB SOCKET \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="49ba8-1042">WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="49ba8-1043">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-1043">**DWORD**</span></span> | <span data-ttu-id="49ba8-1044">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1044">X</span></span> | <span data-ttu-id="49ba8-1045">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1045">X</span></span> | <span data-ttu-id="49ba8-1046">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1046">X</span></span> | <span data-ttu-id="49ba8-1047">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1047">X</span></span> | <span data-ttu-id="49ba8-1048">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="49ba8-1048">Windows 8.1</span></span> |
| <span data-ttu-id="49ba8-1049">TAMAÑO DEL BÚFER DE ENVÍO DE SOCKET WEB DE LA \_ \_ \_ \_ \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-1049">WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="49ba8-1050">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-1050">**DWORD**</span></span> | <span data-ttu-id="49ba8-1051">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1051">X</span></span> | <span data-ttu-id="49ba8-1052">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1052">X</span></span> | <span data-ttu-id="49ba8-1053">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1053">X</span></span> | <span data-ttu-id="49ba8-1054">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1054">X</span></span> | <span data-ttu-id="49ba8-1055">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="49ba8-1055">Windows 8.1</span></span> |
| <span data-ttu-id="49ba8-1056">RECUENTO DE \_ SUBPROCESOS \_ DE TRABAJO DE LA \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-1056">WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT</span></span><br/><span data-ttu-id="49ba8-1057">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-1057">**DWORD**</span></span> | \- | \- | \- | <span data-ttu-id="49ba8-1058">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1058">X</span></span> | \- |
| <span data-ttu-id="49ba8-1059">TAMAÑO DEL BÚFER \_ DE ESCRITURA DE LA \_ \_ OPCIÓN \_ WINHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-1059">WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="49ba8-1060">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="49ba8-1060">**DWORD**</span></span> | \- | <span data-ttu-id="49ba8-1061">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1061">X</span></span> | <span data-ttu-id="49ba8-1062">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1062">X</span></span> | <span data-ttu-id="49ba8-1063">X</span><span class="sxs-lookup"><span data-stu-id="49ba8-1063">X</span></span> | \- |

> [!Note]
> <span data-ttu-id="49ba8-1064">Para Windows XP y Windows 2000, vea [Requisitos en tiempo de ejecución.](winhttp-start-page.md)</span><span class="sxs-lookup"><span data-stu-id="49ba8-1064">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="49ba8-1065">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49ba8-1065">Requirements</span></span>

| <span data-ttu-id="49ba8-1066">Requisito</span><span class="sxs-lookup"><span data-stu-id="49ba8-1066">Requirement</span></span> | <span data-ttu-id="49ba8-1067">Valor</span><span class="sxs-lookup"><span data-stu-id="49ba8-1067">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="49ba8-1068">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49ba8-1068">Minimum supported client</span></span> | <span data-ttu-id="49ba8-1069">Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="49ba8-1069">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>            |
| <span data-ttu-id="49ba8-1070">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49ba8-1070">Minimum supported server</span></span> | <span data-ttu-id="49ba8-1071">Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="49ba8-1071">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>         |
| <span data-ttu-id="49ba8-1072">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="49ba8-1072">Redistributable</span></span>          | <span data-ttu-id="49ba8-1073">WinHTTP 5.0 y Internet Explorer 5.01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="49ba8-1073">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span> |
| <span data-ttu-id="49ba8-1074">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49ba8-1074">Header</span></span>                   | <span data-ttu-id="49ba8-1075">Winhttp.h</span><span class="sxs-lookup"><span data-stu-id="49ba8-1075">Winhttp.h</span></span>                                                                       |

## <a name="see-also"></a><span data-ttu-id="49ba8-1076">Vea también</span><span class="sxs-lookup"><span data-stu-id="49ba8-1076">See also</span></span>

[<span data-ttu-id="49ba8-1077">Versiones winHTTP</span><span class="sxs-lookup"><span data-stu-id="49ba8-1077">WinHTTP Versions</span></span>](winhttp-versions.md)

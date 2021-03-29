---
title: Cómo un cliente autentica un servicio de Windows Sockets basado en SCP
description: En este tema se muestra el código que utiliza una aplicación cliente para crear un SPN para un servicio.
ms.assetid: b5ef79c6-e321-435c-b3de-817fdea8836a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38471f48d8c80d0795b7176b95df0029d42325ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486595"
---
# <a name="how-a-client-authenticates-an-scp-based-windows-sockets-service"></a><span data-ttu-id="859e2-103">Cómo un cliente autentica un servicio de Windows Sockets basado en SCP</span><span class="sxs-lookup"><span data-stu-id="859e2-103">How a Client Authenticates an SCP-based Windows Sockets Service</span></span>

<span data-ttu-id="859e2-104">En este tema se muestra el código que utiliza una aplicación cliente para crear un SPN para un servicio.</span><span class="sxs-lookup"><span data-stu-id="859e2-104">This topic shows the code that a client application uses to compose an SPN for a service.</span></span> <span data-ttu-id="859e2-105">El cliente enlaza con el punto de conexión de servicio (SCP) del servicio para recuperar los datos necesarios para conectarse al servicio.</span><span class="sxs-lookup"><span data-stu-id="859e2-105">The client binds to the service's service connection point (SCP) to retrieve the data required to connect to the service.</span></span> <span data-ttu-id="859e2-106">El SCP también contiene datos que el cliente puede usar para crear el SPN del servicio.</span><span class="sxs-lookup"><span data-stu-id="859e2-106">The SCP also contains data that the client can use to compose the service's SPN.</span></span> <span data-ttu-id="859e2-107">Para obtener más información y un ejemplo de código que se enlaza al SCP y recupera las propiedades necesarias, vea [cómo los clientes buscan y usan un punto de conexión de servicio](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="859e2-107">For more information and a code example that binds to the SCP and retrieves the necessary properties, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span>

<span data-ttu-id="859e2-108">En este tema también se muestra cómo un cliente utiliza un paquete de seguridad SSPI y el SPN del servicio para establecer una conexión autenticada mutuamente con el servicio de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="859e2-108">This topic also shows how a client uses an SSPI security package and the service's SPN to establish a mutually authenticated connection to the Windows Sockets service.</span></span> <span data-ttu-id="859e2-109">Tenga en cuenta que este código es casi idéntico al código requerido en Microsoft Windows NT 4,0 y versiones anteriores solo para autenticar el cliente en el servidor.</span><span class="sxs-lookup"><span data-stu-id="859e2-109">Be aware that this code is almost identical to the code required in Microsoft Windows NT 4.0 and earlier just to authenticate the client to the server.</span></span> <span data-ttu-id="859e2-110">La única diferencia es que el cliente debe proporcionar el SPN y especificar la \_ marca de autenticación de solicitud mutua de ISC \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="859e2-110">The only difference is that the client must supply the SPN and specify the ISC\_REQ\_MUTUAL\_AUTH flag.</span></span>

## <a name="client-code-to-make-an-spn-for-a-service"></a><span data-ttu-id="859e2-111">Código de cliente para crear un SPN para un servicio</span><span class="sxs-lookup"><span data-stu-id="859e2-111">Client Code to Make an SPN for a Service</span></span>


```C++
// Initialize these strings by querying the service's SCP.
TCHAR szDn[MAX_PATH],     // DN of the service's SCP.
      szServer[MAX_PATH], // DNS name of the service's server.
      szClass[MAX_PATH];  // Service class.
 
TCHAR szSpn[MAX_PATH];    // Buffer for SPN.
SOCKET sockServer;        // Socket connected to service.
DWORD dwRes, dwLen;
.
.
.
// Compose the SPN for the service using the DN, Class, and Server
// returned by ScpLocate.
dwLen = sizeof(szSpn);
dwRes = DsMakeSpn(
     szClass,    // Service class.
     szDn,       // DN of the service's SCP.
     szServer,   // DNS name of the server on which service is running.
     0,          // No port component in SPN.
     NULL,       // No referrer.
     &dwLen,     // Size of szSpn buffer.
     szSpn);     // Buffer to receive the SPN.

if (!DoAuthentication (sockServer, szSpn)) {
    closesocket (sockServer);
    return(FALSE);
}
.
.
.
```



## <a name="client-code-to-authenticate-the-service"></a><span data-ttu-id="859e2-112">Código de cliente para autenticar el servicio</span><span class="sxs-lookup"><span data-stu-id="859e2-112">Client Code to Authenticate the Service</span></span>

<span data-ttu-id="859e2-113">Este ejemplo de código consta de dos rutinas: **enauthentication** y **GenClientContext**.</span><span class="sxs-lookup"><span data-stu-id="859e2-113">This code example consists of two routines: **DoAuthentication** and **GenClientContext**.</span></span> <span data-ttu-id="859e2-114">Después de llamar a [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) para crear un SPN para el servicio, el cliente pasa el SPN a la rutina de **autenticación** , que llama a **GenClientContext** para generar el búfer inicial que se va a enviar al servicio.</span><span class="sxs-lookup"><span data-stu-id="859e2-114">After calling [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) to compose an SPN for the service, the client passes the SPN to the **DoAuthentication** routine, which calls the **GenClientContext** to generate the initial buffer to send to the service.</span></span> <span data-ttu-id="859e2-115">La **autenticación de autenticación** utiliza el identificador de socket para enviar el búfer y recibir la respuesta del servicio pasada al paquete SSPI mediante otra llamada a **GenClientContext**.</span><span class="sxs-lookup"><span data-stu-id="859e2-115">**DoAuthentication** uses the socket handle to send the buffer and receive the service's response passed to the SSPI package by another call to **GenClientContext**.</span></span> <span data-ttu-id="859e2-116">Este bucle se repite hasta que se produce un error en la autenticación o **GenClientContext** establece una marca que indica que la autenticación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="859e2-116">This loop is repeated until the authentication fails or **GenClientContext** sets a flag that indicates the authentication succeeded.</span></span>

<span data-ttu-id="859e2-117">La rutina **GenClientContext** interactúa con el paquete SSPI para generar los datos de autenticación que se van a enviar al servicio y procesar los datos recibidos del servicio.</span><span class="sxs-lookup"><span data-stu-id="859e2-117">The **GenClientContext** routine interacts with the SSPI package to generate the authentication data to send to the service and process the data received from the service.</span></span> <span data-ttu-id="859e2-118">Los componentes clave de los datos de autenticación proporcionados por el cliente incluyen:</span><span class="sxs-lookup"><span data-stu-id="859e2-118">The key components of the authentication data provided by the client include:</span></span>

-   <span data-ttu-id="859e2-119">Nombre de la entidad de seguridad de servicio que identifica las credenciales que el servicio debe autenticar.</span><span class="sxs-lookup"><span data-stu-id="859e2-119">The service principal name which identifies the credentials that the service must authenticate.</span></span>
-   <span data-ttu-id="859e2-120">Las credenciales del cliente.</span><span class="sxs-lookup"><span data-stu-id="859e2-120">The client's credentials.</span></span> <span data-ttu-id="859e2-121">La función [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) del paquete de seguridad extrae estas credenciales del contexto de seguridad del cliente que se establece en el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="859e2-121">The [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) function of the security package extracts these credentials from the client's security context established at logon.</span></span>
-   <span data-ttu-id="859e2-122">Para solicitar la autenticación mutua, el cliente debe especificar la \_ marca de autenticación mutua de REQ de ISC \_ \_ cuando llama a la función [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) durante la rutina **GenClientContext** .</span><span class="sxs-lookup"><span data-stu-id="859e2-122">To request mutual authentication, the client must specify the ISC\_REQ\_MUTUAL\_AUTH flag when it calls the [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) function during the **GenClientContext** routine.</span></span>


```C++
// Structure for storing the state of the authentication sequence.
typedef struct _AUTH_SEQ 
{
    BOOL _fNewConversation;
    CredHandle _hcred;
    BOOL _fHaveCredHandle;
    BOOL _fHaveCtxtHandle;
    struct _SecHandle  _hctxt;
} AUTH_SEQ, *PAUTH_SEQ;
 
/***************************************************************/
//   DoAuthentication routine for the client.
//
//   Manages the client's authentication conversation with the service 
//   using the supplied socket handle.
//
//   Returns TRUE if the mutual authentication is successful.
//   Otherwise, it returns FALSE.
//
/***************************************************************/
BOOL DoAuthentication (
        SOCKET s, 
        LPTSTR szSpn)
{
BOOL done = FALSE;
DWORD cbOut, cbIn;
 
// Call the security package to generate the initial buffer of 
// authentication data to send to the service.
cbOut = g_cbMaxMessage;
if (!GenClientContext (s, NULL, 0, g_pOutBuf, 
                       &cbOut, &done, szSpn))
    return(FALSE);
    
if (!SendMsg (s, g_pOutBuf, cbOut))
    return(FALSE);
 
// Pass the service's response back to the security package, and send 
// the package's output back to the service. Repeat until complete.
while (!done) 
{
    if (!ReceiveMsg (s, g_pInBuf, g_cbMaxMessage, &cbIn))
        return(FALSE);
 
    cbOut = g_cbMaxMessage;
    if (!GenClientContext (s, g_pInBuf, cbIn, g_pOutBuf, 
                           &cbOut, &done, szSpn))
        return(FALSE);
 
    if (!SendMsg (s, g_pOutBuf, cbOut))
        return(FALSE);
}
 
return(TRUE);
}
 
/***************************************************************/
//   GenClientContext routine
//
//   Handles the client's interactions with the security package.
//   Optionally takes an input buffer coming from the service 
//   and generates a buffer of data to send back to the 
//   service. Also returns an indication when the authentication
//   is complete.
//
//   Returns TRUE if the mutual authentication is successful.
//   Otherwise, it returns FALSE.
//
/***************************************************************/
BOOL GenClientContext (
            DWORD dwKey,     // Socket handle used as key.
            BYTE *pIn,
            DWORD cbIn,
            BYTE *pOut,
            DWORD *pcbOut,
            BOOL *pfDone,
            LPTSTR szSpn)
{
SECURITY_STATUS  ssStatus;
TimeStamp        Lifetime;
SecBufferDesc    OutBuffDesc;
SecBuffer        OutSecBuff;
SecBufferDesc    InBuffDesc;
SecBuffer        InSecBuff;
ULONG            ContextAttributes;
PAUTH_SEQ        pAS; // Structure to store state of authentication.
 
// Get structure that contains the state of the authentication sequence.
if (!GetEntry (dwKey, (PVOID*) &pAS))
    return(FALSE);
 
if (pAS->_fNewConversation)
{
    ssStatus = g_pFuncs->AcquireCredentialsHandle (
            NULL,    // Principal
            PACKAGE_NAME,
            SECPKG_CRED_OUTBOUND,
            NULL,    // LOGON id
            NULL,    // Authentication data
            NULL,    // Get key function.
            NULL,    // Get key argument.
            &pAS->_hcred,
            &Lifetime
            );
    if (SEC_SUCCESS (ssStatus))
        pAS->_fHaveCredHandle = TRUE;
    else 
    {
        fprintf (stderr, 
                 "AcquireCredentialsHandle failed: %u\n", ssStatus);
        return(FALSE);
    }
}
 
// Prepare output buffer.
OutBuffDesc.ulVersion = 0;
OutBuffDesc.cBuffers = 1;
OutBuffDesc.pBuffers = &OutSecBuff;
 
OutSecBuff.cbBuffer = *pcbOut;
OutSecBuff.BufferType = SECBUFFER_TOKEN;
OutSecBuff.pvBuffer = pOut;
 
// Prepare input buffer.
if (!pAS->_fNewConversation) 
{
    InBuffDesc.ulVersion = 0;
    InBuffDesc.cBuffers = 1;
    InBuffDesc.pBuffers = &InSecBuff;
 
    InSecBuff.cbBuffer = cbIn;
    InSecBuff.BufferType = SECBUFFER_TOKEN;
    InSecBuff.pvBuffer = pIn;
}
 
_tprintf(TEXT("InitializeSecurityContext: pszTarget=%s\n"),szSpn);
 
ssStatus = g_pFuncs->InitializeSecurityContext (
                     &pAS->_hcred,
                     pAS->_fNewConversation ? NULL : &pAS->_hctxt,
                     szSpn,
                     ISC_REQ_MUTUAL_AUTH,      // Context requirements
                     0,                        // Reserved1
                     SECURITY_NATIVE_DREP,
                     pAS->_fNewConversation ? NULL : &InBuffDesc,
                     0,                        // Reserved2
                     &pAS->_hctxt,
                     &OutBuffDesc,
                     &ContextAttributes,
                     &Lifetime
                     );
if (!SEC_SUCCESS (ssStatus)) 
{
    fprintf (stderr, "init context failed: %X\n", ssStatus);
    return FALSE;
}
 
pAS->_fHaveCtxtHandle = TRUE;
 
// Complete token if applicable.
if ( (SEC_I_COMPLETE_NEEDED == ssStatus) || 
     (SEC_I_COMPLETE_AND_CONTINUE == ssStatus))  
{
    if (g_pFuncs->CompleteAuthToken) 
    {
        ssStatus = g_pFuncs->CompleteAuthToken (&pAS->_hctxt, 
                                                &OutBuffDesc);
        if (!SEC_SUCCESS(ssStatus)) 
        {
            fprintf (stderr, "complete failed: %u\n", ssStatus);
            return FALSE;
        }
    } else 
    {
        fprintf (stderr, "Complete not supported.\n");
        return FALSE;
    }
}
 
*pcbOut = OutSecBuff.cbBuffer;
 
if (pAS->_fNewConversation)
    pAS->_fNewConversation = FALSE;
 
*pfDone = !((SEC_I_CONTINUE_NEEDED == ssStatus) ||
            (SEC_I_COMPLETE_AND_CONTINUE == ssStatus));
 
// Check the ISC_RET_MUTUAL_AUTH flag to verify that 
// mutual authentication was performed.
if (*pfDone && !(ContextAttributes && ISC_RET_MUTUAL_AUTH) )
    _tprintf(TEXT("Mutual Auth not set in returned context.\n"));
 
return TRUE;
}
```



 

 





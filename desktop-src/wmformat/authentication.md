---
title: Autenticación (Windows Media Format 11 SDK)
description: Autenticación
ms.assetid: 9c181615-e864-4588-846f-d04d73824f5f
keywords:
- SDK de Windows Media Format, autenticación
- SDK de Windows Media Format, autenticación de red
- Advanced Systems Format (ASF), autenticación
- ASF (formato de sistemas avanzados), autenticación
- Advanced Systems Format (ASF), autenticación de red
- ASF (formato de sistemas avanzados), autenticación de red
- autenticación
- autenticación de red, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf815881ac7beb354fffbfdb9b5475d040e9e83
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105705111"
---
# <a name="authentication-windows-media-format-11-sdk"></a><span data-ttu-id="a3874-111">Autenticación (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="a3874-111">Authentication (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="a3874-112">El objeto lector puede controlar los desafíos de autenticación de red, incluida la autenticación implícita y la autenticación NTLM.</span><span class="sxs-lookup"><span data-stu-id="a3874-112">The reader object can handle network authentication challenges, including digest authentication and NTLM authentication.</span></span> <span data-ttu-id="a3874-113">En algunos casos, la aplicación debe proporcionar las credenciales del usuario a través de una interfaz de devolución de llamada:</span><span class="sxs-lookup"><span data-stu-id="a3874-113">In some cases the application must provide the user's credentials through a callback interface:</span></span>

-   <span data-ttu-id="a3874-114">Autenticación implícita: la aplicación debe implementar la interfaz **IWMCredentialCallback** , tal y como se describe más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="a3874-114">Digest authentication: The application must implement the **IWMCredentialCallback** interface, as described later in this topic.</span></span>
-   <span data-ttu-id="a3874-115">Autenticación NTLM: el lector responde automáticamente con las credenciales de inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="a3874-115">NTLM authentication: The reader automatically responds with the user's logon credentials.</span></span> <span data-ttu-id="a3874-116">Si el usuario actual está autorizado para iniciar sesión en el servidor, la aplicación no tiene que hacer nada.</span><span class="sxs-lookup"><span data-stu-id="a3874-116">If the current user is authorized to log on to the server, the application does not have to do anything.</span></span> <span data-ttu-id="a3874-117">Si el usuario no tiene autorización, la aplicación debe implementar la interfaz **IWMCredentialCallback** .</span><span class="sxs-lookup"><span data-stu-id="a3874-117">If the user does not have authorization, the application must implement the **IWMCredentialCallback** interface.</span></span>

    > [!Note]  
    > <span data-ttu-id="a3874-118">Windows Media Services versión 4,1 no admite la autenticación NTLM a través de un servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="a3874-118">Windows Media Services version 4.1 does not support NTLM authentication through a proxy server.</span></span> <span data-ttu-id="a3874-119">La autenticación NTLM requiere varios intercambios de cliente-servidor en la misma conexión y la versión 4,1 no mantiene una conexión persistente con el proxy.</span><span class="sxs-lookup"><span data-stu-id="a3874-119">NTLM authentication requires several client-server exchanges on the same connection, and version 4.1 does not keep a persistent connection with the proxy.</span></span> <span data-ttu-id="a3874-120">Windows Media Services 9 series en Microsoft Windows Server 2003 admite la autenticación NTLM a través de un servidor proxy, siempre y cuando el proxy admita conexiones persistentes.</span><span class="sxs-lookup"><span data-stu-id="a3874-120">Windows Media Services 9 Series in Microsoft Windows Server 2003 supports NTLM authentication through a proxy server, as long as the proxy supports keep-alive connections.</span></span>

     

<span data-ttu-id="a3874-121">Como se indicó, en algunos casos, la aplicación debe proporcionar las credenciales del usuario.</span><span class="sxs-lookup"><span data-stu-id="a3874-121">As noted, in some cases the application must provide the user's credentials.</span></span> <span data-ttu-id="a3874-122">Esto sucede a través de la interfaz **IWMCredentialCallback** , que tiene un único método, **AcquireCredentials**.</span><span class="sxs-lookup"><span data-stu-id="a3874-122">This occurs through the **IWMCredentialCallback** interface, which has a single method, **AcquireCredentials**.</span></span> <span data-ttu-id="a3874-123">Para admitir la autenticación, implemente esta interfaz en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a3874-123">To support authentication, implement this interface in your application.</span></span> <span data-ttu-id="a3874-124">El objeto lector consulta esta interfaz llamando a **QueryInterface** en el puntero [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) que recibió de la aplicación en el método [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) .</span><span class="sxs-lookup"><span data-stu-id="a3874-124">The reader object queries for this interface by calling **QueryInterface** on the [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) pointer that it received from the application in the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method.</span></span> <span data-ttu-id="a3874-125">Si el objeto lector necesita obtener las credenciales del usuario, llama al método **AcquireCredentials** de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a3874-125">If the reader object needs to get the user's credentials, it calls the application's **AcquireCredentials** method.</span></span>

<span data-ttu-id="a3874-126">Si las credenciales se van a enviar a través de la red sin cifrado, el lector establece la \_ \_ marca de texto no cifrado de credenciales WMT \_ en el parámetro *pdwFlags* .</span><span class="sxs-lookup"><span data-stu-id="a3874-126">If the credentials will be sent over the network without encryption, the reader sets the WMT\_CREDENTIAL\_CLEAR\_TEXT flag in the *pdwFlags* parameter.</span></span> <span data-ttu-id="a3874-127">Esto permite a la aplicación advertir al usuario de que sus credenciales se enviarán en texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="a3874-127">This gives the application an opportunity to warn the user that his or her credentials will be sent in plain text.</span></span>

<span data-ttu-id="a3874-128">De lo contrario, el objeto lector cifra automáticamente las credenciales antes de enviarlas a través de la red.</span><span class="sxs-lookup"><span data-stu-id="a3874-128">Otherwise, the reader object automatically encrypts the credentials before sending them over the network.</span></span> <span data-ttu-id="a3874-129">La aplicación puede devolverlos al objeto lector en texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="a3874-129">The application can return them to the reader object in plain text.</span></span> <span data-ttu-id="a3874-130">Además, si el objeto de lector establece la \_ marca de cifrado de credenciales WMT \_ , significa que el lector admite la obtención de credenciales cifradas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a3874-130">In addition, if the reader object sets the WMT\_CREDENTIAL\_ENCRYPT flag, it means the reader supports getting encrypted credentials from the application.</span></span> <span data-ttu-id="a3874-131">En ese caso, la aplicación puede devolver las credenciales en texto sin formato, o bien cifrarlas mediante la función **CryptProtectData** , que se describe en la documentación del SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="a3874-131">In that case, the application can either return the credentials in plain text, or else encrypt them itself using the **CryptProtectData** function, which is described in the Platform SDK documentation.</span></span> <span data-ttu-id="a3874-132">Si la aplicación cifra las credenciales, debe establecer la \_ \_ marca de cifrado de credenciales WMT en el parámetro *pdwFlags* antes de que el método devuelva.</span><span class="sxs-lookup"><span data-stu-id="a3874-132">If the application encrypts the credentials, it must set the WMT\_CREDENTIAL\_ENCRYPT flag in the *pdwFlags* parameter before the method returns.</span></span>

<span data-ttu-id="a3874-133">Por lo general, no es necesario cifrar los datos, porque el objeto lector los cifra si es necesario.</span><span class="sxs-lookup"><span data-stu-id="a3874-133">Generally, it is not necessary to encrypt the data, because the reader object encrypts the data if necessary.</span></span> <span data-ttu-id="a3874-134">Sin embargo, el cifrado puede ser útil si la aplicación mantiene el nombre de usuario y la contraseña en la memoria, ya que impide que un atacante inspeccione un volcado de memoria del proceso.</span><span class="sxs-lookup"><span data-stu-id="a3874-134">However, encryption might be useful if the application keeps the user name and password in memory, because it prevents an attacker from inspecting a memory dump of the process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3874-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3874-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3874-136">**Interfaz IWMCredentialCallback**</span><span class="sxs-lookup"><span data-stu-id="a3874-136">**IWMCredentialCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> <dt>

[<span data-ttu-id="a3874-137">**Interfaz IWMReader**</span><span class="sxs-lookup"><span data-stu-id="a3874-137">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> </dl>

 

 





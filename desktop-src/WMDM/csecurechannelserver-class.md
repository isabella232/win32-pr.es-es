---
title: Clase CSecureChannelServer
description: Clase CSecureChannelServer
ms.assetid: e6e1463a-5a26-4b83-85e0-a639d384a199
keywords:
- Windows Media Administrador de dispositivos, clase CSecureChannelServer
- Administrador de dispositivos, clase CSecureChannelServer
- proveedores de servicios, clase CSecureChannelServer
- referencia de programación, clase CSecureChannelServer
- referencia de Windows Media Administrador de dispositivos, clase CSecureChannelServer
- Clase CSecureChannelServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99efdd4d4fa245000d27b5874439375d968591e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792058"
---
# <a name="csecurechannelserver-class"></a><span data-ttu-id="b27c6-109">Clase CSecureChannelServer</span><span class="sxs-lookup"><span data-stu-id="b27c6-109">CSecureChannelServer Class</span></span>

<span data-ttu-id="b27c6-110">La clase **CSecureChannelServer** es una clase auxiliar (no una interfaz) que permite a un proveedor de servicios o a un proveedor de contenido seguro autenticar una aplicación mediante la interfaz [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) , para cifrar y descifrar los datos, y para crear firmas Mac.</span><span class="sxs-lookup"><span data-stu-id="b27c6-110">The **CSecureChannelServer** class is a helper class (not an interface) that enables a service provider or secure content provider to authenticate an application using the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface, to encrypt and decrypt data, and to create MAC signatures.</span></span> <span data-ttu-id="b27c6-111">El proceso de autenticación requiere que la aplicación cree un objeto **CSecureChannelClient** y que el proveedor de servicios cree un objeto **CSecureChannelServer** .</span><span class="sxs-lookup"><span data-stu-id="b27c6-111">The authentication process requires that the application create a **CSecureChannelClient** object and that the service provider create a **CSecureChannelServer** object.</span></span> <span data-ttu-id="b27c6-112">Las clases **CSecureChannelClient** y **CSecureChannelServer** se declaran en la biblioteca de vínculos estáticos, Mssachlp. lib.</span><span class="sxs-lookup"><span data-stu-id="b27c6-112">The **CSecureChannelClient** and **CSecureChannelServer** classes are declared in the static link library, Mssachlp.lib.</span></span> <span data-ttu-id="b27c6-113">Todos los métodos de las interfaces de Administrador de dispositivos de Windows Media, proveedor de servicios y proveedor de contenido seguro pueden devolver WMDM \_ E \_ NOTCERTIFIED para indicar que el llamador no se ha autenticado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b27c6-113">All methods of Windows Media Device Manager, service provider, and secure content provider interfaces can return WMDM\_E\_NOTCERTIFIED to indicate that the caller has not authenticated successfully.</span></span>

<span data-ttu-id="b27c6-114">La clase **CSecureChannelServer** expone los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="b27c6-114">The **CSecureChannelServer** class exposes the following methods.</span></span>



| <span data-ttu-id="b27c6-115">Método</span><span class="sxs-lookup"><span data-stu-id="b27c6-115">Method</span></span>                                                            | <span data-ttu-id="b27c6-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b27c6-116">Description</span></span>                                                                                 |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b27c6-117">[**DecryptParam**](/previous-versions/bb231598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b27c6-117">[**DecryptParam**](/previous-versions/bb231598(v=vs.85))</span></span>         | <span data-ttu-id="b27c6-118">Descifra los datos contenidos en un parámetro.</span><span class="sxs-lookup"><span data-stu-id="b27c6-118">Decrypts the data contained in a parameter.</span></span>                                                 |
| <span data-ttu-id="b27c6-119">[**EncryptParam**](/previous-versions/ms868509(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b27c6-119">[**EncryptParam**](/previous-versions/ms868509(v=msdn.10))</span></span>         | <span data-ttu-id="b27c6-120">Cifra los datos contenidos en un parámetro.</span><span class="sxs-lookup"><span data-stu-id="b27c6-120">Encrypts the data contained in a parameter.</span></span>                                                 |
| <span data-ttu-id="b27c6-121">[**fIsAuthenticated**](/previous-versions/bb231600(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b27c6-121">[**fIsAuthenticated**](/previous-versions/bb231600(v=vs.85))</span></span> | <span data-ttu-id="b27c6-122">Comprueba que se ha establecido correctamente un canal de autenticación seguro.</span><span class="sxs-lookup"><span data-stu-id="b27c6-122">Verifies that a secure authentication channel has been successfully established.</span></span>            |
| <span data-ttu-id="b27c6-123">[**GetAppSec**](/previous-versions/bb231601(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b27c6-123">[**GetAppSec**](/previous-versions/bb231601(v=vs.85))</span></span>               | <span data-ttu-id="b27c6-124">Recupera los niveles de seguridad de la aplicación de los componentes locales y remotos.</span><span class="sxs-lookup"><span data-stu-id="b27c6-124">Retrieves the application security levels of the local and remote components.</span></span>               |
| <span data-ttu-id="b27c6-125">[**GetSessionKey**](/previous-versions/bb231602(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b27c6-125">[**GetSessionKey**](/previous-versions/bb231602(v=vs.85))</span></span>       | <span data-ttu-id="b27c6-126">Recupera la clave de sesión actual.</span><span class="sxs-lookup"><span data-stu-id="b27c6-126">Retrieves the current session key.</span></span>                                                          |
| <span data-ttu-id="b27c6-127">[**MACFinal**](/previous-versions/ms868513(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b27c6-127">[**MACFinal**](/previous-versions/ms868513(v=msdn.10))</span></span>                 | <span data-ttu-id="b27c6-128">Libera el canal de código de autenticación de mensajes (MAC) y recupera un valor de MAC final.</span><span class="sxs-lookup"><span data-stu-id="b27c6-128">Releases the message authentication code (MAC) channel and retrieves a final MAC value.</span></span>     |
| <span data-ttu-id="b27c6-129">[**MACInit**](/previous-versions/ms868514(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b27c6-129">[**MACInit**](/previous-versions/ms868514(v=msdn.10))</span></span>                   | <span data-ttu-id="b27c6-130">Adquiere un canal de código de autenticación de mensajes (MAC).</span><span class="sxs-lookup"><span data-stu-id="b27c6-130">Acquires a message authentication code (MAC) channel.</span></span>                                       |
| <span data-ttu-id="b27c6-131">[**MACUpdate**](/previous-versions/ms868515(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b27c6-131">[**MACUpdate**](/previous-versions/ms868515(v=msdn.10))</span></span>               | <span data-ttu-id="b27c6-132">Actualiza el valor de código de autenticación de mensajes (MAC) con un valor de parámetro.</span><span class="sxs-lookup"><span data-stu-id="b27c6-132">Updates the message authentication code (MAC) value with a parameter value.</span></span>                 |
| <span data-ttu-id="b27c6-133">[**SACAuth**](/previous-versions/ms868516(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b27c6-133">[**SACAuth**](/previous-versions/ms868516(v=msdn.10))</span></span>                   | <span data-ttu-id="b27c6-134">Establece un canal autenticado seguro entre los componentes.</span><span class="sxs-lookup"><span data-stu-id="b27c6-134">Establishes a secure authenticated channel between components.</span></span>                              |
| <span data-ttu-id="b27c6-135">[**SACGetProtocols**](/previous-versions/ms868517(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b27c6-135">[**SACGetProtocols**](/previous-versions/ms868517(v=msdn.10))</span></span>   | <span data-ttu-id="b27c6-136">Informa de los protocolos admitidos por un componente.</span><span class="sxs-lookup"><span data-stu-id="b27c6-136">Reports the protocols supported by a component.</span></span>                                             |
| <span data-ttu-id="b27c6-137">[**SetCertificate**](/previous-versions/ms868518(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b27c6-137">[**SetCertificate**](/previous-versions/ms868518(v=msdn.10))</span></span>     | <span data-ttu-id="b27c6-138">Especifica el certificado y la clave privada del servidor de canal autenticado seguro (SAC).</span><span class="sxs-lookup"><span data-stu-id="b27c6-138">Specifies the certificate and private key of the secure authenticated channel (SAC) server.</span></span> |
| <span data-ttu-id="b27c6-139">[**SetSessionKey**](/previous-versions/ms868519(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b27c6-139">[**SetSessionKey**](/previous-versions/ms868519(v=msdn.10))</span></span>       | <span data-ttu-id="b27c6-140">Establece la clave de sesión que se usa para comunicarse con otro componente.</span><span class="sxs-lookup"><span data-stu-id="b27c6-140">Sets the session key that is used to communicate with another component.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="b27c6-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b27c6-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b27c6-142">**Clase CSecureChannelClient**</span><span class="sxs-lookup"><span data-stu-id="b27c6-142">**CSecureChannelClient Class**</span></span>](csecurechannelclient-class.md)
</dt> <dt>

[<span data-ttu-id="b27c6-143">**Interfaz IComponentAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="b27c6-143">**IComponentAuthenticate Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[<span data-ttu-id="b27c6-144">**Interfaces para proveedores de servicios**</span><span class="sxs-lookup"><span data-stu-id="b27c6-144">**Interfaces for Service Providers**</span></span>](interfaces-for-service-providers.md)
</dt> <dt>

[<span data-ttu-id="b27c6-145">**Usar canales autenticados seguros**</span><span class="sxs-lookup"><span data-stu-id="b27c6-145">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 
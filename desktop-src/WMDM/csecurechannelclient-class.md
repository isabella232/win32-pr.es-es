---
title: Clase CSecureChannelClient
description: Clase CSecureChannelClient
ms.assetid: f02220b8-0d1c-416c-97ea-e5e7455fcbba
keywords:
- Windows Media Administrador de dispositivos, clase CSecureChannelClient
- Administrador de dispositivos, clase CSecureChannelClient
- aplicaciones de escritorio, clase CSecureChannelClient
- referencia de programación, clase CSecureChannelClient
- referencia de Windows Media Administrador de dispositivos, clase CSecureChannelClient
- Clase CSecureChannelClient
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a886ba45648b2ba0356e9d7f246c2de912cedd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695634"
---
# <a name="csecurechannelclient-class"></a><span data-ttu-id="c7be2-109">Clase CSecureChannelClient</span><span class="sxs-lookup"><span data-stu-id="c7be2-109">CSecureChannelClient Class</span></span>

<span data-ttu-id="c7be2-110">La clase **CSecureChannelClient** es una clase auxiliar (no una interfaz) que permite a las aplicaciones autenticarse, cifrar y descifrar datos, y crear equipos Mac.</span><span class="sxs-lookup"><span data-stu-id="c7be2-110">The **CSecureChannelClient** class is a helper class (not an interface) that enables applications to authenticate themselves, encrypt and decrypt data, and create MACs.</span></span>

<span data-ttu-id="c7be2-111">La clase **CSecureChannelClient** expone los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="c7be2-111">The **CSecureChannelClient** class exposes the following methods.</span></span>



| <span data-ttu-id="c7be2-112">Método</span><span class="sxs-lookup"><span data-stu-id="c7be2-112">Method</span></span>                                                            | <span data-ttu-id="c7be2-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7be2-113">Description</span></span>                                                                                                               |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7be2-114">[**Authenticate**](/previous-versions/ms983906(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c7be2-114">[**Authenticate**](/previous-versions/ms983906(v=msdn.10))</span></span>         | <span data-ttu-id="c7be2-115">Desencadena el intercambio de certificados entre componentes para establecer la confianza.</span><span class="sxs-lookup"><span data-stu-id="c7be2-115">Triggers the exchange of certificates between components to establish trust.</span></span>                                              |
| <span data-ttu-id="c7be2-116">[**DecryptParam**](/previous-versions/bb231586(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c7be2-116">[**DecryptParam**](/previous-versions/bb231586(v=vs.85))</span></span>         | <span data-ttu-id="c7be2-117">Descifra los datos recibidos a través de un parámetro.</span><span class="sxs-lookup"><span data-stu-id="c7be2-117">Decrypts data received through a parameter.</span></span>                                                                               |
| <span data-ttu-id="c7be2-118">[**EncryptParam**](/previous-versions/bb231587(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c7be2-118">[**EncryptParam**](/previous-versions/bb231587(v=vs.85))</span></span>         | <span data-ttu-id="c7be2-119">Cifra los datos que se envían a través de un parámetro.</span><span class="sxs-lookup"><span data-stu-id="c7be2-119">Encrypts data being sent out through a parameter.</span></span>                                                                         |
| <span data-ttu-id="c7be2-120">[**fIsAuthenticated**](/previous-versions/ms868497(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c7be2-120">[**fIsAuthenticated**](/previous-versions/ms868497(v=msdn.10))</span></span> | <span data-ttu-id="c7be2-121">Comprueba que se ha establecido correctamente un canal de autenticación seguro.</span><span class="sxs-lookup"><span data-stu-id="c7be2-121">Verifies that a secure authentication channel has been successfully established.</span></span> <span data-ttu-id="c7be2-122">Las aplicaciones no usan este método.</span><span class="sxs-lookup"><span data-stu-id="c7be2-122">This method is not used by applications.</span></span> |
| <span data-ttu-id="c7be2-123">[**GetAppSec**](/previous-versions/ms868498(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c7be2-123">[**GetAppSec**](/previous-versions/ms868498(v=msdn.10))</span></span>               | <span data-ttu-id="c7be2-124">Recupera los niveles de seguridad de la aplicación de los componentes locales y remotos.</span><span class="sxs-lookup"><span data-stu-id="c7be2-124">Retrieves the application security levels of the local and remote components.</span></span>                                             |
| <span data-ttu-id="c7be2-125">[**GetSessionKey**](/previous-versions/bb231590(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c7be2-125">[**GetSessionKey**](/previous-versions/bb231590(v=vs.85))</span></span>       | <span data-ttu-id="c7be2-126">Recupera la clave de sesión actual.</span><span class="sxs-lookup"><span data-stu-id="c7be2-126">Retrieves the current session key.</span></span> <span data-ttu-id="c7be2-127">Las aplicaciones no usan este método.</span><span class="sxs-lookup"><span data-stu-id="c7be2-127">This method is not used by applications.</span></span>                                               |
| <span data-ttu-id="c7be2-128">[**MACFinal**](/previous-versions/bb231591(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c7be2-128">[**MACFinal**](/previous-versions/bb231591(v=vs.85))</span></span>                 | <span data-ttu-id="c7be2-129">Libera el canal de código de autenticación de mensajes (MAC) y recupera un valor de MAC final.</span><span class="sxs-lookup"><span data-stu-id="c7be2-129">Releases the message authentication code (MAC) channel and retrieves a final MAC value.</span></span>                                   |
| <span data-ttu-id="c7be2-130">[**MACInit**](/previous-versions/bb231592(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c7be2-130">[**MACInit**](/previous-versions/bb231592(v=vs.85))</span></span>                   | <span data-ttu-id="c7be2-131">Adquiere un canal de código de autenticación de mensajes (MAC).</span><span class="sxs-lookup"><span data-stu-id="c7be2-131">Acquires a message authentication code (MAC) channel.</span></span>                                                                     |
| <span data-ttu-id="c7be2-132">[**MACUpdate**](/previous-versions/bb231593(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c7be2-132">[**MACUpdate**](/previous-versions/bb231593(v=vs.85))</span></span>               | <span data-ttu-id="c7be2-133">Agrega un valor a un código de autenticación de mensajes (MAC).</span><span class="sxs-lookup"><span data-stu-id="c7be2-133">Adds a value to a message authentication code (MAC).</span></span>                                                                      |
| <span data-ttu-id="c7be2-134">[**SetCertificate**](/previous-versions/ms868504(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c7be2-134">[**SetCertificate**](/previous-versions/ms868504(v=msdn.10))</span></span>     | <span data-ttu-id="c7be2-135">Especifica el certificado y la clave privada del cliente de canal autenticado seguro (SAC).</span><span class="sxs-lookup"><span data-stu-id="c7be2-135">Specifies the certificate and private key of the secure authenticated channel (SAC) client.</span></span>                               |
| <span data-ttu-id="c7be2-136">[**SetInterface**](/previous-versions/bb231595(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c7be2-136">[**SetInterface**](/previous-versions/bb231595(v=vs.85))</span></span>         | <span data-ttu-id="c7be2-137">Selecciona la interfaz que se usa para las comunicaciones de canal autenticado seguro (SAC).</span><span class="sxs-lookup"><span data-stu-id="c7be2-137">Selects the interface used for secure authenticated channel (SAC) communications.</span></span>                                         |
| <span data-ttu-id="c7be2-138">[**SetSessionKey**](/previous-versions/ms868506(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c7be2-138">[**SetSessionKey**](/previous-versions/ms868506(v=msdn.10))</span></span>       | <span data-ttu-id="c7be2-139">Establece la clave de sesión que se usa para comunicarse con otro componente.</span><span class="sxs-lookup"><span data-stu-id="c7be2-139">Sets the session key that is used to communicate with another component.</span></span> <span data-ttu-id="c7be2-140">Las aplicaciones no usan este método.</span><span class="sxs-lookup"><span data-stu-id="c7be2-140">This method is not used by applications.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="c7be2-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c7be2-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7be2-142">**Clase CSecureChannelServer**</span><span class="sxs-lookup"><span data-stu-id="c7be2-142">**CSecureChannelServer Class**</span></span>](csecurechannelserver-class.md)
</dt> <dt>

[<span data-ttu-id="c7be2-143">**Interfaz IComponentAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="c7be2-143">**IComponentAuthenticate Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[<span data-ttu-id="c7be2-144">**Interfaces para aplicaciones**</span><span class="sxs-lookup"><span data-stu-id="c7be2-144">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> </dl>

 

 
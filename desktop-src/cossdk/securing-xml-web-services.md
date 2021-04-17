---
description: El acceso a las aplicaciones COM+ que se exponen como servicios Web XML se controla mediante el servidor Web de IIS, que procesa las solicitudes entrantes.
ms.assetid: 440b0636-8afc-4fb3-a179-140958948b94
title: Proteger los servicios Web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94953ce0769c44ddaeda27cacdac99ab4ff252d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705369"
---
# <a name="securing-xml-web-services"></a><span data-ttu-id="9e199-103">Proteger los servicios Web XML</span><span class="sxs-lookup"><span data-stu-id="9e199-103">Securing XML Web Services</span></span>

<span data-ttu-id="9e199-104">El acceso a las aplicaciones COM+ que se exponen como servicios Web XML se controla mediante el servidor Web de IIS, que procesa las solicitudes entrantes.</span><span class="sxs-lookup"><span data-stu-id="9e199-104">Access to COM+ applications exposed as XML web services is controlled by the IIS web server, which processes the incoming requests.</span></span> <span data-ttu-id="9e199-105">También puede configurar IIS para que requiera que las comunicaciones con el autor de la llamada tengan lugar a través de un canal seguro establecido mediante el protocolo Capa de sockets seguros (SSL).</span><span class="sxs-lookup"><span data-stu-id="9e199-105">You can also configure IIS to require the communications with the caller take place over a secure channel established using the Secure Sockets Layer (SSL) protocol.</span></span>

> [!Note]  
> <span data-ttu-id="9e199-106">Un servicio Web XML protegido no admite el acceso de WKO a través de WSDL.</span><span class="sxs-lookup"><span data-stu-id="9e199-106">A secured XML web service does not support WKO access via WSDL.</span></span> <span data-ttu-id="9e199-107">En su lugar, los clientes que han instalado el .NET Framework versión 1,1 pueden llamarlo en el modo CAO.</span><span class="sxs-lookup"><span data-stu-id="9e199-107">Instead, clients that have installed the .NET Framework version 1.1 can call it in CAO mode.</span></span> <span data-ttu-id="9e199-108">Si los clientes de terceros necesitan tener acceso al servicio Web XML a través de WSDL, debe permitir el acceso anónimo.</span><span class="sxs-lookup"><span data-stu-id="9e199-108">If third-party clients need to access your XML web service via WSDL, you must allow anonymous access.</span></span>

 

> [!Note]  
> <span data-ttu-id="9e199-109">Para usar el protocolo SSL para establecer un canal de comunicación seguro, debe obtener e instalar un certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="9e199-109">To use the SSL protocol to establish a secure communication channel, you must obtain and install an SSL certificate.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="9e199-110">Herramienta administrativa Servicios de componentes</span><span class="sxs-lookup"><span data-stu-id="9e199-110">Component Services Administrative Tool</span></span>

<span data-ttu-id="9e199-111">Para seleccionar el mecanismo de autenticación para un servicio Web XML, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="9e199-111">To select the authentication mechanism for an XML web service, use the following steps:</span></span>

1.  <span data-ttu-id="9e199-112">Haga clic con el botón secundario en el icono de **mi PC** en el escritorio y haga clic en **administrar**.</span><span class="sxs-lookup"><span data-stu-id="9e199-112">Right-click the **My Computer** icon on your desktop, and click **Manage**.</span></span>

2.  <span data-ttu-id="9e199-113">En **servicios y aplicaciones** e **Internet Information** Services, busque el icono correspondiente al directorio raíz virtual del servicio Web XML.</span><span class="sxs-lookup"><span data-stu-id="9e199-113">Under **Services and Applications** and **Internet Information Service**, locate the icon corresponding to the virtual root directory for your XML web service.</span></span> <span data-ttu-id="9e199-114">Haga clic con el botón derecho en el icono del directorio y elija **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="9e199-114">Right-click the directory icon, and choose **Properties**.</span></span>

3.  <span data-ttu-id="9e199-115">En la pestaña **seguridad de directorios** del cuadro de diálogo Propiedades, busque **autenticación y control de acceso** y haga clic en el botón **Editar** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9e199-115">On the **Directory Security** tab of the properties dialog, locate **Authentication and access control** and click the corresponding **Edit** button.</span></span>

4.  <span data-ttu-id="9e199-116">En el cuadro de diálogo **métodos de autenticación** , en **acceso autenticado**, use las casillas de verificación para seleccionar los mecanismos de autenticación que desea permitir.</span><span class="sxs-lookup"><span data-stu-id="9e199-116">In the **Authentication Methods** dialog box, under **Authenticated access**, use the check boxes to select the authentication mechanisms you wish to allow.</span></span> <span data-ttu-id="9e199-117">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e199-117">Click **OK**.</span></span>

    > [!Note]  
    > <span data-ttu-id="9e199-118">Puede configurar IIS para autenticar a los autores de llamadas mediante cualquiera de las siguientes opciones en el cuadro de diálogo **métodos de autenticación** de IIS: **autenticación integrada de Windows**, **autenticación implícita para servidores de dominio de Windows**, **autenticación básica (la contraseña se envía en texto no cifrado)** o **autenticación de .NET Passport**.</span><span class="sxs-lookup"><span data-stu-id="9e199-118">You can configure IIS to authenticate callers by using any of the following options on the IIS **Authentication Methods** dialog: **Integrated Windows authentication**, **Digest authentication for Windows domain servers**, **Basic authentication (password is sent in clear text)**, or **.NET Passport authentication**.</span></span> <span data-ttu-id="9e199-119">También puede permitir el acceso anónimo.</span><span class="sxs-lookup"><span data-stu-id="9e199-119">You can also allow anonymous access.</span></span>

     

5.  <span data-ttu-id="9e199-120">En el cuadro de diálogo Propiedades, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9e199-120">In the properties dialog, click **OK**.</span></span>

<span data-ttu-id="9e199-121">Para permitir el acceso anónimo y no seguro a un servicio Web XML, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="9e199-121">To allow nonsecure, anonymous access to an XML web service, use the following steps:</span></span>

1.  <span data-ttu-id="9e199-122">Haga clic con el botón secundario en el icono de **mi PC** en el escritorio y haga clic en **administrar**.</span><span class="sxs-lookup"><span data-stu-id="9e199-122">Right-click the **My Computer** icon on your desktop, and click **Manage**.</span></span>

2.  <span data-ttu-id="9e199-123">En **servicios y aplicaciones** e **Internet Information** Services, busque el icono correspondiente al directorio raíz virtual del servicio Web XML.</span><span class="sxs-lookup"><span data-stu-id="9e199-123">Under **Services and Applications** and **Internet Information Service**, locate the icon corresponding to the virtual root directory for your XML web service.</span></span> <span data-ttu-id="9e199-124">Haga clic con el botón derecho en el icono del directorio y elija **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="9e199-124">Right-click the directory icon, and choose **Properties**.</span></span>

3.  <span data-ttu-id="9e199-125">En la pestaña **seguridad de directorios** del cuadro de diálogo Propiedades, busque **autenticación y control de acceso** y haga clic en el botón **Editar** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9e199-125">On the **Directory Security** tab of the properties dialog, locate **Authentication and access control** and click the corresponding **Edit** button.</span></span> <span data-ttu-id="9e199-126">Active la casilla **Habilitar acceso anónimo** .</span><span class="sxs-lookup"><span data-stu-id="9e199-126">Select the **Enable anonymous access** check box.</span></span> <span data-ttu-id="9e199-127">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e199-127">Click **OK**.</span></span>

4.  <span data-ttu-id="9e199-128">En la pestaña **seguridad de directorios** del cuadro de diálogo Propiedades, busque **comunicaciones seguras** y haga clic en el botón **Editar** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9e199-128">On the **Directory Security** tab of the properties dialog, locate **Secure communications** and click the corresponding **Edit** button.</span></span> <span data-ttu-id="9e199-129">Desactive la casilla **requerir canal seguro (SSL)** .</span><span class="sxs-lookup"><span data-stu-id="9e199-129">Uncheck the **Require secure channel (SSL)** check box.</span></span> <span data-ttu-id="9e199-130">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e199-130">Click **OK**.</span></span>

5.  <span data-ttu-id="9e199-131">En el cuadro de diálogo Propiedades, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9e199-131">In the properties dialog, click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="9e199-132">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9e199-132">Visual Basic</span></span>

<span data-ttu-id="9e199-133">No corresponde.</span><span class="sxs-lookup"><span data-stu-id="9e199-133">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="9e199-134">C/C++</span><span class="sxs-lookup"><span data-stu-id="9e199-134">C/C++</span></span>

<span data-ttu-id="9e199-135">No corresponde.</span><span class="sxs-lookup"><span data-stu-id="9e199-135">Does not apply.</span></span>

## <a name="additional-security-considerations"></a><span data-ttu-id="9e199-136">Consideraciones de seguridad adicionales</span><span class="sxs-lookup"><span data-stu-id="9e199-136">Additional Security Considerations</span></span>

<span data-ttu-id="9e199-137">Al exigir un canal seguro, es más fácil proteger la confidencialidad de los datos intercambiados mediante el cifrado de las comunicaciones entre el cliente y el servicio Web XML.</span><span class="sxs-lookup"><span data-stu-id="9e199-137">By requiring a secure channel, you help protect the confidentiality of the data exchanged by encrypting the communications between the client and your XML web service.</span></span> <span data-ttu-id="9e199-138">Si permite la autenticación mediante contraseñas de texto no cifrado, debe requerir un canal seguro para evitar la exposición de contraseñas en la red.</span><span class="sxs-lookup"><span data-stu-id="9e199-138">If you allow authentication using clear text passwords, you should require a secure channel in order to avoid exposing passwords on the network.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e199-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e199-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e199-140">Obtener acceso a los servicios Web XML en el modo de CAO</span><span class="sxs-lookup"><span data-stu-id="9e199-140">Accessing XML Web Services in CAO Mode</span></span>](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[<span data-ttu-id="9e199-141">Obtener acceso a los servicios Web XML en modo WKO</span><span class="sxs-lookup"><span data-stu-id="9e199-141">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="9e199-142">Consideraciones de seguridad del servicio SOAP de COM+</span><span class="sxs-lookup"><span data-stu-id="9e199-142">COM+ SOAP Service Security Considerations</span></span>](com--soap-service-security-considerations.md)
</dt> <dt>

[<span data-ttu-id="9e199-143">Crear servicios Web XML</span><span class="sxs-lookup"><span data-stu-id="9e199-143">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> </dl>

 

 




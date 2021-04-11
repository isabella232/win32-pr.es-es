---
title: Actualización de licencias para almacenes que tienen el logotipo de PlaysForSure
description: Actualización de licencias para almacenes que tienen el logotipo de PlaysForSure
ms.assetid: d08d6b6e-937e-4dec-b7ca-376cdad069f9
keywords:
- Windows Media Player tiendas en línea, actualizar licencias
- tiendas en línea, actualización de licencias
- Windows Media Player tiendas en línea, actualización de licencias
- tiendas en línea, actualizar licencias
- Windows Media Player tiendas en línea, logotipo de PlaysForSure
- tiendas en línea, logotipo de PlaysForSure
- actualizar licencias
- licencias, actualizar
- PlaysForSure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e48a3ddfd2b0670e3720f7c71587d0330a69a7
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104149098"
---
# <a name="refreshing-licenses-for-stores-that-have-the-playsforsure-logo"></a><span data-ttu-id="bb4ac-112">Actualización de licencias para almacenes que tienen el logotipo de PlaysForSure</span><span class="sxs-lookup"><span data-stu-id="bb4ac-112">Refreshing Licenses for Stores That Have the PlaysForSure Logo</span></span>

<span data-ttu-id="bb4ac-113">Algunos almacenes de música en línea tienen el logotipo de PlaysForSure, pero no se integran con Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-113">Certain online music stores have the PlaysForSure logo but are not integrated with Windows Media Player 11.</span></span> <span data-ttu-id="bb4ac-114">Esos almacenes deben proporcionar un documento ServiceInfo y un componente ligero para que Windows Media Player 11 pueda obtener y actualizar las licencias de su contenido.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-114">Those stores must provide a ServiceInfo document and a lightweight component so that Windows Media Player 11 can obtain and update licenses for their content.</span></span>

<span data-ttu-id="bb4ac-115">En el ejemplo siguiente se muestra cómo funciona el proceso de actualización de licencias.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-115">The following example illustrates how the license updating process works.</span></span>

1.  <span data-ttu-id="bb4ac-116">El usuario obtiene las pistas de música 50 de la tienda en línea de Proseware.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-116">The user obtains 50 music tracks from the Proseware online store.</span></span> <span data-ttu-id="bb4ac-117">Cada pista es un archivo con la extensión de nombre de archivo. WMA.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-117">Each track is a file with the .wma file name extension.</span></span> <span data-ttu-id="bb4ac-118">Junto con las pistas, el usuario obtiene las licencias para reproducir las pistas.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-118">Along with the tracks, the user obtains licenses to play the tracks.</span></span>
2.  <span data-ttu-id="bb4ac-119">El usuario copia las pistas 50 en un nuevo equipo que tiene instalado Windows Media Player 11 y agrega las pistas a la biblioteca de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-119">The user copies the 50 tracks to a new computer that has Windows Media Player 11 installed and adds the tracks to the Windows Media Player library.</span></span>
3.  <span data-ttu-id="bb4ac-120">En algún momento posterior, el módulo de actualización de licencias (LRM), que forma parte de Windows Media Player 11, inspecciona los metadatos de las pistas 50 y determina que Proseware es el proveedor de contenido.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-120">At some later time, the License Refresh Module (LRM), which is part of Windows Media Player 11, inspects the metadata in the fifty tracks and determines that Proseware is the content provider.</span></span>
    > [!Note]  
    > <span data-ttu-id="bb4ac-121">Windows Media Player puede identificar el proveedor de contenido inspeccionando el atributo **ContentDistributor** en un archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-121">Windows Media Player is able to identify the content provider by inspecting the **ContentDistributor** attribute in a media file.</span></span> <span data-ttu-id="bb4ac-122">Si una tienda en línea que tiene el logotipo de PlaysForSure proporciona un archivo multimedia que usa Windows Media Digital Rights Management (WMDRM), la tienda en línea debe colocar el atributo **ContentDistributor** en el archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-122">If an online store that has the PlaysForSure logo provides a media file that uses Windows Media Digital Rights Management (WMDRM), the online store must place the **ContentDistributor** attribute in the media file.</span></span> <span data-ttu-id="bb4ac-123">Para obtener más información, vea Agregar el atributo distribuidor de contenido en el SDK de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-123">For more information, see Adding the Content Distributor Attribute in the Windows Media Player SDK.</span></span>

     

4.  <span data-ttu-id="bb4ac-124">LRM busca la dirección URL del documento ServiceInfo de Proseware, descarga el documento e inspecciona el elemento **install** del documento para obtener la dirección URL de un paquete que LRM puede usar para instalar el componente de Proseware.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-124">The LRM looks up the URL of Proseware's ServiceInfo document, downloads the document, and inspects the document's **Install** element to obtain the URL of a package that the LRM can use to install Proseware's component.</span></span> <span data-ttu-id="bb4ac-125">LRM instala y carga el componente.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-125">The LRM installs and loads the component.</span></span>
5.  <span data-ttu-id="bb4ac-126">Para cada una de las pistas 50, LRM llama al método [IWMPSubscriptionService:: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) del componente Proseware.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-126">For each of the 50 tracks, the LRM calls the Proseware component's [IWMPSubscriptionService::allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) method.</span></span> <span data-ttu-id="bb4ac-127">El método **allowPlay** coloca una licencia para la pista individual en el nuevo equipo y devuelve **true** en el parámetro *pfAllowPlay* .</span><span class="sxs-lookup"><span data-stu-id="bb4ac-127">The **allowPlay** method places a license for the individual track on the new computer and returns **TRUE** in the *pfAllowPlay* parameter.</span></span>
    > [!Note]  
    > <span data-ttu-id="bb4ac-128">El componente Proseware debe proporcionar todas las licencias necesarias para reproducir la pista individual. Es decir, el componente debe proporcionar una licencia raíz y una licencia de hoja, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-128">The Proseware component must provide all licenses required to play the individual track. That is, the component must provide both a root license and a leaf license if needed.</span></span>

     

    <span data-ttu-id="bb4ac-129">Durante la primera llamada al método **allowPlay** , el componente Proseware debe mostrar un cuadro de diálogo para comprobar que el usuario actual tiene una cuenta de Proseware y tiene derecho a reproducir la pista. Durante las llamadas posteriores a **allowPlay**, el componente puede usar las credenciales que obtuvo en la primera llamada para comprobar que el usuario tiene derecho a reproducir el resto de las pistas.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-129">During the first call to the **allowPlay** method, the Proseware component must display a dialog box to verify that the current user has a Proseware account and has the right to play the track. During subsequent calls to **allowPlay**, the component can use the credentials that it obtained in the first call to verify that the user has the right to play the remaining tracks.</span></span>

<span data-ttu-id="bb4ac-130">El componente, que está escrito por la tienda en línea, debe implementar el método **allowPlay** de la interfaz **IWMPSubscriptionService** .</span><span class="sxs-lookup"><span data-stu-id="bb4ac-130">The component, which is written by the online store, must implement the **allowPlay** method of the **IWMPSubscriptionService** interface.</span></span> <span data-ttu-id="bb4ac-131">El componente debe devolver E \_ NOTIMPL de cada uno de los otros tres métodos: **allowCDBurn**, **allowPDATransfer** y **startBackgroundProcessing**.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-131">The component must return E\_NOTIMPL from each of the other three methods: **allowCDBurn**, **allowPDATransfer**, and **startBackgroundProcessing**.</span></span> <span data-ttu-id="bb4ac-132">Además, el componente debe establecer el valor de la entrada del registro **Capabilities** en 1; es decir, se \_ debe establecer la marca de capacidad de límite de suscripción \_ ALLOWPLAY y se deben borrar todas las demás marcas de funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-132">Also, the component must set the value of the **Capabilities** registry entry to 1; that is, the SUBSCRIPTION\_CAP\_ALLOWPLAY capability flag must be set, and all other capability flags must be cleared.</span></span> <span data-ttu-id="bb4ac-133">Para obtener más información acerca del registro del componente, consulte [claves del registro y entradas para una tienda en línea de tipo 2](registry-keys-and-entries-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="bb4ac-133">For more information about registering the component, see [Registry Keys and Entries for a Type 2 Online Store](registry-keys-and-entries-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="bb4ac-134">Para obtener información sobre cómo crear un componente que implemente la interfaz **IWMPSubscriptionService** , vea [crear el complemento para una tienda en línea de tipo 2](building-the-plug-in-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="bb4ac-134">For information about creating a component that implements the **IWMPSubscriptionService** interface, see [Building the Plug-in for a Type 2 Online Store](building-the-plug-in-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="bb4ac-135">Para obtener información acerca de cómo proporcionar a Microsoft un documento ServiceInfo, envíe un correo electrónico al equipo de servicios virtuales de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="bb4ac-135">For information about providing Microsoft with a ServiceInfo document, send email to the Windows Media Player Virtual Services team.</span></span> <span data-ttu-id="bb4ac-136">La dirección de correo electrónico del equipo es mpsvctm@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="bb4ac-136">The team's email address is mpsvctm@microsoft.com.</span></span>

<span data-ttu-id="bb4ac-137">Para obtener orientación técnica sobre el uso de una variedad de SDK de Windows Media para crear un servicio que ofrezca contenido multimedia digital con licencia, vaya al [Centro para desarrolladores de Microsoft Windows Media](https://msdn.microsoft.com/windowsmedia/default.aspx) y busque "crear una tienda en línea de suscripciones de Windows Media Player 10".</span><span class="sxs-lookup"><span data-stu-id="bb4ac-137">For technical guidance on using a variety of Windows Media SDKs to create a service that offers licensed digital media content, go to the [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx) and search for "Creating a Windows Media Player 10 Subscription Online Store".</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb4ac-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bb4ac-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb4ac-139">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="bb4ac-139">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="bb4ac-140">**Windows Media Player tiendas en línea**</span><span class="sxs-lookup"><span data-stu-id="bb4ac-140">**Windows Media Player Online Stores**</span></span>](windows-media-player-online-stores.md)
</dt> </dl>

 

 





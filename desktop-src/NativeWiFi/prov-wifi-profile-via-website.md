---
title: Aprovisionamiento de un perfil de Wi-Fi a través de un sitio web
description: Permita a los usuarios descargar un perfil de un sitio web y aprovisionarlo.
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: e34c83fbee100316256293e27eac96dae685c37d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995602"
---
# <a name="provision-a-wi-fi-profile-via-a-website"></a><span data-ttu-id="efa50-103">Aprovisionamiento de un perfil de Wi-Fi a través de un sitio web</span><span class="sxs-lookup"><span data-stu-id="efa50-103">Provision a Wi-Fi profile via a website</span></span>

<span data-ttu-id="efa50-104">El flujo de trabajo que se describe en este tema se presentó en la versión 2004 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="efa50-104">The workflow described in this topic was introduced in Windows 10, version 2004.</span></span> <span data-ttu-id="efa50-105">En este tema se muestra cómo configurar un sitio web para que un usuario pueda aprovisionar un perfil para una red Passpoint (o para una red normal) antes de pasar al alcance de los puntos de acceso de Wi-Fi correspondientes.</span><span class="sxs-lookup"><span data-stu-id="efa50-105">This topic shows how to configure a website so that a user can provision a profile for a Passpoint network (or for a normal network) prior to moving into range of the corresponding Wi-Fi access points.</span></span> <span data-ttu-id="efa50-106">Un escenario de ejemplo es el de un usuario que puede estar planeando visitar un aeropuerto o una conferencia por primera vez, y que quieren prepararse de antemano descargando y aprovisionando un perfil en casa.</span><span class="sxs-lookup"><span data-stu-id="efa50-106">An example scenario is that of a user who might be planning to visit an airport or a conference for the first time, and they want to prepare in advance by downloading and provisioning a profile at home.</span></span>

<span data-ttu-id="efa50-107">Como desarrollador, puede habilitar el flujo de trabajo proporcionando un perfil XML y configurando un sitio Web.</span><span class="sxs-lookup"><span data-stu-id="efa50-107">As a developer, you enable the workflow by providing an XML profile, and configuring a website.</span></span> <span data-ttu-id="efa50-108">Después, los usuarios pueden aprovisionar un perfil de Wi-Fi descargándolo desde su sitio web a través de un explorador Web.</span><span class="sxs-lookup"><span data-stu-id="efa50-108">Your users can then provision a Wi-Fi profile by downloading it from your website via a web browser.</span></span> <span data-ttu-id="efa50-109">En el dispositivo del usuario, el perfil de Wi-Fi se aprovisiona con la activación de URI y la aplicación de **configuración** de Windows.</span><span class="sxs-lookup"><span data-stu-id="efa50-109">On the user's device, the Wi-Fi profile is then provisioned by using URI activation and the Windows **Settings** app.</span></span>

<span data-ttu-id="efa50-110">Este flujo de trabajo sustituye al mecanismo de Internet Explorer para el aprovisionamiento de perfiles de Wi-Fi, que se basa en las API de JavaScript específicas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="efa50-110">This workflow supersedes the mechanism in Internet Explorer for provisioning Wi-Fi profiles, which relies on Microsoft-specific JavaScript APIs.</span></span> <span data-ttu-id="efa50-111">Se espera que este nuevo flujo de trabajo funcione con todos los exploradores principales.</span><span class="sxs-lookup"><span data-stu-id="efa50-111">This new workflow is expected to work with all major browsers.</span></span>

## <a name="the-workflow-in-more-detail"></a><span data-ttu-id="efa50-112">El flujo de trabajo con más detalle</span><span class="sxs-lookup"><span data-stu-id="efa50-112">The workflow in more detail</span></span>

<span data-ttu-id="efa50-113">Puede activar este flujo de trabajo desde un hipervínculo que incluya como argumento el URI de descarga del documento XML de aprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="efa50-113">You can activate this workflow from a hyperlink that includes as an argument the download URI of the provisioning XML document.</span></span>

```xml
ms-settings:wifi-provisioning?uri={download_uri}
```

<span data-ttu-id="efa50-114">Por ejemplo, el siguiente marcado HTML proporciona un vínculo para instalar los perfiles que se encuentran en un documento hipotético `http://contoso.com/ProvisioningDoc.xml` .</span><span class="sxs-lookup"><span data-stu-id="efa50-114">For example, the following HTML markup gives a link to install the profile(s) that are found in a hypothetical document `http://contoso.com/ProvisioningDoc.xml`.</span></span>

```html
<a href="ms-settings:wifi-provisioning?uri=http://contoso.com/ProvisioningDoc.xml">Install</a>
```

<span data-ttu-id="efa50-115">El XML debe cumplir el esquema de aprovisionamiento (consulte [aprovisionamiento de cuentas](/windows-hardware/drivers/mobilebroadband/account-provisioning)).</span><span class="sxs-lookup"><span data-stu-id="efa50-115">Your XML must adhere to the provisioning schema (see [Account provisioning](/windows-hardware/drivers/mobilebroadband/account-provisioning)).</span></span> <span data-ttu-id="efa50-116">El XML también debe incluir uno o varios elementos [WLANProfile](./wlan-profileschema-wlanprofile-element.md)   .</span><span class="sxs-lookup"><span data-stu-id="efa50-116">Your XML must also include one or more [WLANProfile](./wlan-profileschema-wlanprofile-element.md) elements.</span></span><span data-ttu-id="efa50-117">Cada perfil se mostrará en el cuadro de diálogo **Agregar** que se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="efa50-117"> Each profile will be displayed in the **Add** dialog described next.</span></span>

<span data-ttu-id="efa50-118">Cuando el usuario hace clic en el vínculo HTML, el flujo de trabajo de instalación se invoca en la aplicación de **configuración** .</span><span class="sxs-lookup"><span data-stu-id="efa50-118">When the user clicks your HTML link, the installation workflow is invoked in the **Settings** app.</span></span> <span data-ttu-id="efa50-119">El documento XML de aprovisionamiento lo descarga la aplicación de **configuración** .</span><span class="sxs-lookup"><span data-stu-id="efa50-119">Your provisioning XML document is downloaded by the **Settings** app.</span></span> <span data-ttu-id="efa50-120">Una vez descargado, se muestra información sobre los perfiles, la firma y el firmante (siempre que el documento se adhiera al esquema).</span><span class="sxs-lookup"><span data-stu-id="efa50-120">Once it's downloaded, information about the profiles, signature, and signer are displayed (provided that the document adheres to the schema).</span></span>

![La aplicación de configuración](images/install-dialog.png)

<span data-ttu-id="efa50-122">El botón **Agregar** del cuadro de diálogo de la aplicación **configuración** solo está habilitado si el archivo de aprovisionamiento está firmado y es de confianza.</span><span class="sxs-lookup"><span data-stu-id="efa50-122">The **Add** button in the dialog in the **Settings** app is enabled only if the provisioning file is signed and trusted.</span></span>

## <a name="in-your-web-page-determine-whether-this-workflow-is-supported"></a><span data-ttu-id="efa50-123">En la página web, determine si se admite este flujo de trabajo</span><span class="sxs-lookup"><span data-stu-id="efa50-123">In your web page, determine whether this workflow is supported</span></span>

<span data-ttu-id="efa50-124">No hay ninguna manera de que JavaScript determine la versión de compilación exacta de Windows.</span><span class="sxs-lookup"><span data-stu-id="efa50-124">There is no way in JavaScript to determine the exact build version of Windows.</span></span> <span data-ttu-id="efa50-125">Pero si el usuario usa el explorador Web Microsoft Edge, puede determinar la versión de Edge mediante la inspección del valor del `User-agent` encabezado HTTP.</span><span class="sxs-lookup"><span data-stu-id="efa50-125">But if your user is using the Microsoft Edge web browser, then you can determine the version of Edge by inspecting the value of the `User-agent` HTTP header.</span></span> <span data-ttu-id="efa50-126">Si la versión es mayor o igual que `18.nnnnn` , se admite el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="efa50-126">If the version is greater than or equal to `18.nnnnn`, then the workflow is supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="efa50-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="efa50-127">Related topics</span></span>

* [<span data-ttu-id="efa50-128">Aprovisionamiento de cuentas</span><span class="sxs-lookup"><span data-stu-id="efa50-128">Account provisioning</span></span>](/windows-hardware/drivers/mobilebroadband/account-provisioning)
* [<span data-ttu-id="efa50-129">Elemento WLANProfile</span><span class="sxs-lookup"><span data-stu-id="efa50-129">WLANProfile element</span></span>](./wlan-profileschema-wlanprofile-element.md)
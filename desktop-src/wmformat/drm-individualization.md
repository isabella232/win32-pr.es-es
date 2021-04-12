---
title: Individualización de DRM
description: Individualización de DRM
ms.assetid: 8f129bc1-3db9-4b41-9d60-daff037237ff
keywords:
- SDK de Windows Media Format, individualización de DRM
- Administración de derechos digitales (DRM), individualización
- DRM (administración de derechos digitales), individualización
- individualización de DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217be5cb5c1c7abef882c28961439baa93011c29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356890"
---
# <a name="drm-individualization"></a><span data-ttu-id="c44d4-107">Individualización de DRM</span><span class="sxs-lookup"><span data-stu-id="c44d4-107">DRM Individualization</span></span>

<span data-ttu-id="c44d4-108">Los propietarios de contenido protegido pueden requerir a los usuarios que actualicen algunos de los componentes de administración de derechos digitales (DRM) incluidos en el SDK de Windows Media Format antes de tener acceso a su contenido.</span><span class="sxs-lookup"><span data-stu-id="c44d4-108">Owners of protected content may require users to upgrade some of the digital rights management (DRM) components included in the Windows Media Format SDK before accessing their content.</span></span> <span data-ttu-id="c44d4-109">Si un usuario acepta la actualización, se descargará una versión individual de un archivo de seguridad (una única para su equipo) desde un sitio web de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c44d4-109">If a user accepts the upgrade, an individualized version of a security file (one unique to their computer) will be downloaded from a Microsoft Web site.</span></span> <span data-ttu-id="c44d4-110">Si el usuario rechaza la actualización, no podrá tener acceso al contenido. sin embargo, todavía podrán acceder al contenido no protegido y al contenido protegido que no requiera la actualización.</span><span class="sxs-lookup"><span data-stu-id="c44d4-110">If the user declines the upgrade, they will not be able to access the content; however, they will still be able to access unprotected content and protected content that does not require the upgrade.</span></span> <span data-ttu-id="c44d4-111">La realización de una actualización de seguridad ayuda a aumentar el nivel de protección que ofrece DRM.</span><span class="sxs-lookup"><span data-stu-id="c44d4-111">Performing a security upgrade helps increase the level of protection offered by DRM.</span></span>

<span data-ttu-id="c44d4-112">La individualización se puede realizar en el momento de la instalación o cuando una aplicación encuentra por primera vez un archivo ASF protegido que lo requiere.</span><span class="sxs-lookup"><span data-stu-id="c44d4-112">Individualization can be done either at setup time or when an application first encounters a protected ASF file that requires it.</span></span> <span data-ttu-id="c44d4-113">Dado que este proceso modifica los componentes del sistema de un usuario, la aplicación debe notificar al usuario y obtener su consentimiento informado antes de realizar la actualización.</span><span class="sxs-lookup"><span data-stu-id="c44d4-113">Because this process modifies a user's system components, the application must notify the user and obtain their informed consent before performing the upgrade.</span></span> <span data-ttu-id="c44d4-114">Microsoft Windows Media Player, por ejemplo, muestra un cuadro de diálogo con el siguiente texto:</span><span class="sxs-lookup"><span data-stu-id="c44d4-114">Microsoft Windows Media Player, for example, shows a dialog box with the following text:</span></span>

<span data-ttu-id="c44d4-115">**Actualización de seguridad necesaria**</span><span class="sxs-lookup"><span data-stu-id="c44d4-115">**Security Upgrade Required**</span></span>

<span data-ttu-id="c44d4-116">**El propietario del contenido protegido al que está intentando obtener acceso requiere que primero actualice algunos de los componentes de administración de derechos digitales (DRM) de Microsoft en el equipo.**</span><span class="sxs-lookup"><span data-stu-id="c44d4-116">**The owner of the protected content you are trying to access requires you to first upgrade some of the Microsoft digital rights management (DRM) components on your computer.**</span></span>

<span data-ttu-id="c44d4-117">**Haga clic en Aceptar para actualizar los componentes de DRM.**</span><span class="sxs-lookup"><span data-stu-id="c44d4-117">**Click OK to upgrade your DRM components.**</span></span>

<span data-ttu-id="c44d4-118">**Indicaciones**</span><span class="sxs-lookup"><span data-stu-id="c44d4-118">**Details:**</span></span>

<span data-ttu-id="c44d4-119">**Al hacer clic en aceptar, se envían un identificador único y un archivo de seguridad DRM a un servicio de Microsoft en Internet. El archivo se reemplaza por una versión personalizada que contiene el identificador único. Esto aumenta el nivel de protección proporcionado por DRM.**</span><span class="sxs-lookup"><span data-stu-id="c44d4-119">**When you click OK, a unique identifier and a DRM security file are sent to a Microsoft service on the Internet. The file is replaced with a customized version that contains your unique identifier. This increases the level of protection provided by DRM.**</span></span>

<span data-ttu-id="c44d4-120">Cualquier aplicación que admita la individualización debe utilizar el mismo texto u otro similar.</span><span class="sxs-lookup"><span data-stu-id="c44d4-120">Any application that supports individualization should use the same or similar wording.</span></span> <span data-ttu-id="c44d4-121">Para obtener más información sobre la Directiva de privacidad de Microsoft, consulte la sección [declaración de privacidad](privacy-statement.md) de esta documentación.</span><span class="sxs-lookup"><span data-stu-id="c44d4-121">For more information on Microsoft's Privacy Policy, see the [Privacy Statement](privacy-statement.md) section of this documentation.</span></span>

> [!Note]  
> <span data-ttu-id="c44d4-122">DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="c44d4-122">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c44d4-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c44d4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c44d4-124">**Características de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="c44d4-124">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="c44d4-125">**Individualización de aplicaciones DRM**</span><span class="sxs-lookup"><span data-stu-id="c44d4-125">**Individualizing DRM Applications**</span></span>](individualizing-drm-applications.md)
</dt> </dl>

 

 





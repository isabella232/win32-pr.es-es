---
title: Image Mastering API
description: Image Mastering API
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fabf41d1c82420709b39bb5db03c2ac3e851d2
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119689"
---
# <a name="image-mastering-api"></a><span data-ttu-id="fd3a9-103">Image Mastering API</span><span class="sxs-lookup"><span data-stu-id="fd3a9-103">Image Mastering API</span></span>

## <a name="purpose"></a><span data-ttu-id="fd3a9-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="fd3a9-104">Purpose</span></span>

<span data-ttu-id="fd3a9-105">La API de mastering de imágenes de Microsoft Windows permite a las aplicaciones almacenar y grabar imágenes en medios de almacenamiento óptico de CD, DVD y Dv-ray.</span><span class="sxs-lookup"><span data-stu-id="fd3a9-105">The Microsoft Windows image mastering API enables applications to stage and burn images to CD, DVD, and Blu-ray optical storage media.</span></span> <span data-ttu-id="fd3a9-106">Otros medios parecidos a discos que menten imágenes de la misma manera también pueden usar esta API.</span><span class="sxs-lookup"><span data-stu-id="fd3a9-106">Other disc-like media that lay images in the same manner can also use this API.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="fd3a9-107">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="fd3a9-107">Developer audience</span></span>

<span data-ttu-id="fd3a9-108">IMAPI está diseñado para C/C++ y Visual Basic desarrolladores y aquellos que escriben scripts mediante VBScript.</span><span class="sxs-lookup"><span data-stu-id="fd3a9-108">IMAPI is designed for C/C++ and Visual Basic developers and those writing scripts using VBScript.</span></span>

<span data-ttu-id="fd3a9-109">Se recomienda conocer las tecnologías de CD, DVD y Dv-ray y los sistemas de archivos.</span><span class="sxs-lookup"><span data-stu-id="fd3a9-109">Knowledge of CD, DVD, and Blu-ray technologies and file systems is recommended.</span></span> <span data-ttu-id="fd3a9-110">Los desarrolladores pueden beneficiarse de la familiaridad con la revisión más reciente de Comando multimedia (MMC) [en ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="fd3a9-110">Developers may benefit from a familiarity with the latest revision of Multimedia Command (MMC) at [ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="fd3a9-111">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="fd3a9-111">Run-time requirements</span></span>

<span data-ttu-id="fd3a9-112">IMAPI 2.0 se admite de forma nativa a partir de Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="fd3a9-112">IMAPI 2.0 is supported natively starting with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="fd3a9-113">La habilitación de la funcionalidad IMAPI 2.0 para Windows XP y Windows Server 2003 requiere la instalación del paquete de actualización [KB932716.](https://support.microsoft.com/kb/932716)</span><span class="sxs-lookup"><span data-stu-id="fd3a9-113">Enabling IMAPI 2.0 functionality for Windows XP and Windows Server 2003 requires the installation of the [KB932716](https://support.microsoft.com/kb/932716) update package.</span></span> <span data-ttu-id="fd3a9-114">Si este paquete no está instalado, Windows XP sigue siendo compatible de forma nativa con [IMAPI 1.0.](imapiv1.md)</span><span class="sxs-lookup"><span data-stu-id="fd3a9-114">If this package is not installed, Windows XP still natively supports [IMAPI 1.0](imapiv1.md).</span></span>

> [!Note]  
> <span data-ttu-id="fd3a9-115">Windows Feature Pack para Storage está disponible para el público a través del Centro [de descarga de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05).</span><span class="sxs-lookup"><span data-stu-id="fd3a9-115">The Windows Feature Pack for Storage is available to the public via the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05).</span></span> <span data-ttu-id="fd3a9-116">Puede encontrar información adicional sobre los cambios específicos de la API en la sección [Novedades.](what-s-new.md)</span><span class="sxs-lookup"><span data-stu-id="fd3a9-116">Additional information regarding specific API changes can be found in the [What's New](what-s-new.md) section.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="fd3a9-117">En esta sección</span><span class="sxs-lookup"><span data-stu-id="fd3a9-117">In this section</span></span>



| <span data-ttu-id="fd3a9-118">Tema</span><span class="sxs-lookup"><span data-stu-id="fd3a9-118">Topic</span></span>                                             | <span data-ttu-id="fd3a9-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd3a9-119">Description</span></span>                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd3a9-120">Novedades</span><span class="sxs-lookup"><span data-stu-id="fd3a9-120">What's New</span></span>](what-s-new.md)<br/>           | <span data-ttu-id="fd3a9-121">Información que detalla cada versión significativa de Image Mastering API.</span><span class="sxs-lookup"><span data-stu-id="fd3a9-121">Information detailing each significant release of the Image Mastering API.</span></span><br/> |
| [<span data-ttu-id="fd3a9-122">Acerca de IMAPI</span><span class="sxs-lookup"><span data-stu-id="fd3a9-122">About IMAPI</span></span>](about-imapi.md)<br/>         | <span data-ttu-id="fd3a9-123">Información general sobre Image Mastering API.</span><span class="sxs-lookup"><span data-stu-id="fd3a9-123">General information about the Image Mastering API.</span></span><br/>                         |
| [<span data-ttu-id="fd3a9-124">Uso de IMAPI</span><span class="sxs-lookup"><span data-stu-id="fd3a9-124">Using IMAPI</span></span>](using-imapi.md)<br/>         | <span data-ttu-id="fd3a9-125">Temas relacionados con tareas que muestran cómo usar Image Mastering API.</span><span class="sxs-lookup"><span data-stu-id="fd3a9-125">Task-related topics that demonstrate how to use the Image Mastering API.</span></span><br/>   |
| [<span data-ttu-id="fd3a9-126">Referencia de IMAPI</span><span class="sxs-lookup"><span data-stu-id="fd3a9-126">IMAPI Reference</span></span>](imapi-reference.md)<br/> | <span data-ttu-id="fd3a9-127">Descripciones detalladas de interfaces IMAPI y otros elementos de programación.</span><span class="sxs-lookup"><span data-stu-id="fd3a9-127">Detailed descriptions of IMAPI interfaces and other programming elements.</span></span><br/>  |



 

## <a name="additional-resources"></a><span data-ttu-id="fd3a9-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="fd3a9-128">Additional resources</span></span>

<span data-ttu-id="fd3a9-129">Puede encontrar más información sobre IMAPI y otros temas relacionados en las siguientes ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="fd3a9-129">Further information regarding IMAPI and other related subjects can be found at the following locations:</span></span>



| <span data-ttu-id="fd3a9-130">Tema</span><span class="sxs-lookup"><span data-stu-id="fd3a9-130">Topic</span></span>                                                                                                 | <span data-ttu-id="fd3a9-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd3a9-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd3a9-132">Microsoft Optical Storage Blog</span><span class="sxs-lookup"><span data-stu-id="fd3a9-132">Microsoft Optical Storage Blog</span></span>](/archive/blogs/opticalstorage/)                | <span data-ttu-id="fd3a9-133">Resalta los temas que se centran en la implementación de Image Mastering API en escenarios de desarrollo del mundo real.</span><span class="sxs-lookup"><span data-stu-id="fd3a9-133">Highlights topics that focus on the implementation of the Image Mastering API in real world development scenarios.</span></span>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="fd3a9-134">Foro de discusión de plataformas ópticas</span><span class="sxs-lookup"><span data-stu-id="fd3a9-134">Optical Platform Discussion Forum</span></span>](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | <span data-ttu-id="fd3a9-135">Analice CDROM.SYS, IMAPIv2 y Live File System.</span><span class="sxs-lookup"><span data-stu-id="fd3a9-135">Discuss CDROM.SYS, IMAPIv2 and Live File System issues.</span></span> <span data-ttu-id="fd3a9-136">Este foro se centra en temas de nivel de sistema y está pensado para desarrolladores de aplicaciones en lugar de usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="fd3a9-136">This forum focuses on system-level topics and is intended for application developers rather than endusers.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="fd3a9-137">T10 Technical Committee</span><span class="sxs-lookup"><span data-stu-id="fd3a9-137">T10 Technical Committee</span></span>](https://www.t10.org/)                       | <span data-ttu-id="fd3a9-138">Un comité técnico del Comité Inter internationalista de estándares de tecnologías de la información (INCITS) pronunciaba "conclusiones".</span><span class="sxs-lookup"><span data-stu-id="fd3a9-138">A Technical Committee of the InterNational Committee on Information Technology Standards (INCITS, pronounced "insights").</span></span> <span data-ttu-id="fd3a9-139">INCITS está reconocido por y funciona según las reglas aprobadas por, el American National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="fd3a9-139">INCITS is accredited by, and operates under rules that are approved by, the American National Standards Institute (ANSI).</span></span> <span data-ttu-id="fd3a9-140">Estas reglas están diseñadas para garantizar que los estándares voluntarias se desarrollan mediante el consenso de los grupos del sector.</span><span class="sxs-lookup"><span data-stu-id="fd3a9-140">These rules are designed to ensure that voluntary standards are developed by the consensus of industry groups.</span></span> |
| [<span data-ttu-id="fd3a9-141">Asociación de tecnología de almacenamiento óptico ( TECHNOLOGY)</span><span class="sxs-lookup"><span data-stu-id="fd3a9-141">Optical Storage Technology Association (OSTA)</span></span>](http://www.osta.org/) | <span data-ttu-id="fd3a9-142">Trabaja para dar forma al futuro del sector a través de reuniones periódicas de aplicaciones comerciales de almacenamiento óptico (COSA), compatibilidad de DVD, marketing, MPV (MusicPhotoVideo), comités de UDF y un nuevo comité de blue.</span><span class="sxs-lookup"><span data-stu-id="fd3a9-142">Works to shape the future of the industry through regular meetings of Commercial Optical Storage Applications (COSA), DVD Compatibility, Marketing, MPV (MusicPhotoVideo), UDF committees, and a new adhoc Blue Laser committee.</span></span> <span data-ttu-id="fd3a9-143">Se invita a empresas interesadas de todo el mundo a unirse a la organización y participar en sus comités y programas.</span><span class="sxs-lookup"><span data-stu-id="fd3a9-143">Interested companies worldwide are invited to join the organization and participate in its committees and programs.</span></span>               |



 

 


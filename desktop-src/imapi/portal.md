---
title: API de procesamiento de imágenes
description: .
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc23c972cf111dee5edf3cb014a52351eda3605e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "103995708"
---
# <a name="image-mastering-api"></a><span data-ttu-id="f2143-103">API de procesamiento de imágenes</span><span class="sxs-lookup"><span data-stu-id="f2143-103">Image Mastering API</span></span>

## <a name="purpose"></a><span data-ttu-id="f2143-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="f2143-104">Purpose</span></span>

<span data-ttu-id="f2143-105">La API de Microsoft Windows Image Mastering permite a las aplicaciones almacenar en fases y grabar imágenes en medios de almacenamiento ópticos de CD, DVD y Blu-Ray.</span><span class="sxs-lookup"><span data-stu-id="f2143-105">The Microsoft Windows image mastering API enables applications to stage and burn images to CD, DVD, and Blu-ray optical storage media.</span></span> <span data-ttu-id="f2143-106">Otros medios similares a los discos que establecen imágenes de la misma manera también pueden usar esta API.</span><span class="sxs-lookup"><span data-stu-id="f2143-106">Other disc-like media that lay images in the same manner can also use this API.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="f2143-107">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="f2143-107">Developer audience</span></span>

<span data-ttu-id="f2143-108">IMAPi está diseñado para desarrolladores de C/C++ y Visual Basic y para los que escriben scripts con VBScript.</span><span class="sxs-lookup"><span data-stu-id="f2143-108">IMAPI is designed for C/C++ and Visual Basic developers and those writing scripts using VBScript.</span></span>

<span data-ttu-id="f2143-109">Se recomienda el conocimiento de las tecnologías y los sistemas de archivos de CD, DVD y Blu-Ray.</span><span class="sxs-lookup"><span data-stu-id="f2143-109">Knowledge of CD, DVD, and Blu-ray technologies and file systems is recommended.</span></span> <span data-ttu-id="f2143-110">Los desarrolladores pueden beneficiarse de una familiaridad con la última revisión del comando multimedia (MMC) en [FTP://ftp.T10.org/T10/drafts/MMC6](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="f2143-110">Developers may benefit from a familiarity with the latest revision of Multimedia Command (MMC) at [ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="f2143-111">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="f2143-111">Run-time requirements</span></span>

<span data-ttu-id="f2143-112">IMAPi 2,0 se admite de forma nativa a partir de Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f2143-112">IMAPI 2.0 is supported natively starting with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="f2143-113">La habilitación de la funcionalidad de IMAPi 2,0 para Windows XP y Windows Server 2003 requiere la instalación del paquete de actualización de [KB932716](https://support.microsoft.com/kb/932716) .</span><span class="sxs-lookup"><span data-stu-id="f2143-113">Enabling IMAPI 2.0 functionality for Windows XP and Windows Server 2003 requires the installation of the [KB932716](https://support.microsoft.com/kb/932716) update package.</span></span> <span data-ttu-id="f2143-114">Si este paquete no está instalado, Windows XP sigue siendo compatible de forma nativa con [imapi 1,0](imapiv1.md).</span><span class="sxs-lookup"><span data-stu-id="f2143-114">If this package is not installed, Windows XP still natively supports [IMAPI 1.0](imapiv1.md).</span></span>

> [!Note]  
> <span data-ttu-id="f2143-115">Windows Feature Pack para el almacenamiento está disponible para el público a través del [centro de descarga de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05).</span><span class="sxs-lookup"><span data-stu-id="f2143-115">The Windows Feature Pack for Storage is available to the public via the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05).</span></span> <span data-ttu-id="f2143-116">Puede encontrar información adicional relacionada con los cambios específicos de la API en la sección [novedades](what-s-new.md) .</span><span class="sxs-lookup"><span data-stu-id="f2143-116">Additional information regarding specific API changes can be found in the [What's New](what-s-new.md) section.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="f2143-117">En esta sección</span><span class="sxs-lookup"><span data-stu-id="f2143-117">In this section</span></span>



| <span data-ttu-id="f2143-118">Tema</span><span class="sxs-lookup"><span data-stu-id="f2143-118">Topic</span></span>                                             | <span data-ttu-id="f2143-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2143-119">Description</span></span>                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2143-120">Novedades</span><span class="sxs-lookup"><span data-stu-id="f2143-120">What's New</span></span>](what-s-new.md)<br/>           | <span data-ttu-id="f2143-121">Información que detalla cada versión significativa de la API de masterización de imágenes.</span><span class="sxs-lookup"><span data-stu-id="f2143-121">Information detailing each significant release of the Image Mastering API.</span></span><br/> |
| [<span data-ttu-id="f2143-122">Acerca de IMAPi</span><span class="sxs-lookup"><span data-stu-id="f2143-122">About IMAPI</span></span>](about-imapi.md)<br/>         | <span data-ttu-id="f2143-123">Información general sobre la API de maestro de imágenes.</span><span class="sxs-lookup"><span data-stu-id="f2143-123">General information about the Image Mastering API.</span></span><br/>                         |
| [<span data-ttu-id="f2143-124">Usar IMAPi</span><span class="sxs-lookup"><span data-stu-id="f2143-124">Using IMAPI</span></span>](using-imapi.md)<br/>         | <span data-ttu-id="f2143-125">Temas relacionados con tareas que muestran cómo usar la API de maestro de imágenes.</span><span class="sxs-lookup"><span data-stu-id="f2143-125">Task-related topics that demonstrate how to use the Image Mastering API.</span></span><br/>   |
| [<span data-ttu-id="f2143-126">Referencia de IMAPi</span><span class="sxs-lookup"><span data-stu-id="f2143-126">IMAPI Reference</span></span>](imapi-reference.md)<br/> | <span data-ttu-id="f2143-127">Descripciones detalladas de las interfaces de IMAPi y otros elementos de programación.</span><span class="sxs-lookup"><span data-stu-id="f2143-127">Detailed descriptions of IMAPI interfaces and other programming elements.</span></span><br/>  |



 

## <a name="additional-resources"></a><span data-ttu-id="f2143-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f2143-128">Additional resources</span></span>

<span data-ttu-id="f2143-129">Puede encontrar más información sobre IMAPi y otros temas relacionados en las siguientes ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="f2143-129">Further information regarding IMAPI and other related subjects can be found at the following locations:</span></span>



|                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2143-130">Blog de Microsoft Optical Storage</span><span class="sxs-lookup"><span data-stu-id="f2143-130">Microsoft Optical Storage Blog</span></span>](/archive/blogs/opticalstorage/)                | <span data-ttu-id="f2143-131">Destaca los temas que se centran en la implementación de la API de creación de imágenes maestras en escenarios de desarrollo reales.</span><span class="sxs-lookup"><span data-stu-id="f2143-131">Highlights topics that focus on the implementation of the Image Mastering API in real world development scenarios.</span></span>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="f2143-132">Foro de discusión de plataforma óptica</span><span class="sxs-lookup"><span data-stu-id="f2143-132">Optical Platform Discussion Forum</span></span>](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | <span data-ttu-id="f2143-133">Comente los problemas de CDROM.SYS, IMAPIv2 y del sistema de archivos LFS.</span><span class="sxs-lookup"><span data-stu-id="f2143-133">Discuss CDROM.SYS, IMAPIv2 and Live File System issues.</span></span> <span data-ttu-id="f2143-134">Este foro se centra en los temas de nivel de sistema y está destinado a los desarrolladores de aplicaciones en lugar de a endusers.</span><span class="sxs-lookup"><span data-stu-id="f2143-134">This forum focuses on system-level topics and is intended for application developers rather than endusers.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="f2143-135">Comité técnico de T10</span><span class="sxs-lookup"><span data-stu-id="f2143-135">T10 Technical Committee</span></span>](https://www.t10.org/)                       | <span data-ttu-id="f2143-136">Un Comité técnico del Comité Internacional sobre estándares de tecnología de la información (INCITS, pronunciado "información").</span><span class="sxs-lookup"><span data-stu-id="f2143-136">A Technical Committee of the InterNational Committee on Information Technology Standards (INCITS, pronounced "insights").</span></span> <span data-ttu-id="f2143-137">INCITS es acreditado por y funciona en reglas aprobadas por el American National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f2143-137">INCITS is accredited by, and operates under rules that are approved by, the American National Standards Institute (ANSI).</span></span> <span data-ttu-id="f2143-138">Estas reglas están diseñadas para garantizar que los estándares voluntarios se desarrollan por el consenso de los grupos del sector.</span><span class="sxs-lookup"><span data-stu-id="f2143-138">These rules are designed to ensure that voluntary standards are developed by the consensus of industry groups.</span></span> |
| [<span data-ttu-id="f2143-139">Asociación de tecnología de almacenamiento óptico (OSTA)</span><span class="sxs-lookup"><span data-stu-id="f2143-139">Optical Storage Technology Association (OSTA)</span></span>](http://www.osta.org/) | <span data-ttu-id="f2143-140">Trabaja para dar forma al futuro del sector a través de reuniones periódicas de aplicaciones de almacenamiento óptico comercial (COSA), compatibilidad con DVD, marketing, MPV (MusicPhotoVideo), comités de UDF y un nuevo Comité de láser Blue ad hoc.</span><span class="sxs-lookup"><span data-stu-id="f2143-140">Works to shape the future of the industry through regular meetings of Commercial Optical Storage Applications (COSA), DVD Compatibility, Marketing, MPV (MusicPhotoVideo), UDF committees, and a new adhoc Blue Laser committee.</span></span> <span data-ttu-id="f2143-141">Las compañías interesadas en todo el mundo están invitadas a unirse a la organización y participar en sus comités y programas.</span><span class="sxs-lookup"><span data-stu-id="f2143-141">Interested companies worldwide are invited to join the organization and participate in its committees and programs.</span></span>               |



 

 


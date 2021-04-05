---
title: WM/MediaClassSecondaryID
description: El atributo WM/MediaClassSecondaryID contiene el GUID de la clase multimedia secundaria.
ms.assetid: 3d1429bc-f168-4b25-9d26-c1c28b852160
keywords:
- Formato de Windows Media WM/MediaClassSecondaryID
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5923ff0ff0545f1feb769973f2528bd82e351e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419663"
---
# <a name="wmmediaclasssecondaryid"></a><span data-ttu-id="69b01-104">WM/MediaClassSecondaryID</span><span class="sxs-lookup"><span data-stu-id="69b01-104">WM/MediaClassSecondaryID</span></span>

<span data-ttu-id="69b01-105">El atributo **WM/MediaClassSecondaryID** contiene el GUID de la clase multimedia secundaria.</span><span class="sxs-lookup"><span data-stu-id="69b01-105">The **WM/MediaClassSecondaryID** attribute contains the GUID of the secondary media class.</span></span>

## <a name="global-constant"></a><span data-ttu-id="69b01-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="69b01-106">Global Constant</span></span>

<span data-ttu-id="69b01-107">g \_ wszWMMediaClassSecondaryID</span><span class="sxs-lookup"><span data-stu-id="69b01-107">g\_wszWMMediaClassSecondaryID</span></span>

## <a name="data-type"></a><span data-ttu-id="69b01-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="69b01-108">Data Type</span></span>

<span data-ttu-id="69b01-109">**\_GUID de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="69b01-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="69b01-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69b01-110">Remarks</span></span>

<span data-ttu-id="69b01-111">Este atributo debe establecerse en uno de los valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="69b01-111">This attribute should be set to one of the values in the following table.</span></span>



| <span data-ttu-id="69b01-112">GUID de clase secundaria</span><span class="sxs-lookup"><span data-stu-id="69b01-112">Secondary class GUID</span></span>                   | <span data-ttu-id="69b01-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="69b01-113">Description</span></span>                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69b01-114">"E0236BEB-C281-4EDE-A36D-7AF76A3D45B5"</span><span class="sxs-lookup"><span data-stu-id="69b01-114">"E0236BEB-C281-4EDE-A36D-7AF76A3D45B5"</span></span> | <span data-ttu-id="69b01-115">Se usa para los archivos de libro de audio.</span><span class="sxs-lookup"><span data-stu-id="69b01-115">Use for audio book files.</span></span>                                                                                                                                                               |
| <span data-ttu-id="69b01-116">"3A172A13-2BD9-4831-835B-114F6A95943F"</span><span class="sxs-lookup"><span data-stu-id="69b01-116">"3A172A13-2BD9-4831-835B-114F6A95943F"</span></span> | <span data-ttu-id="69b01-117">Se usa para los archivos de audio que contienen la palabra oral, pero no los libros de audio.</span><span class="sxs-lookup"><span data-stu-id="69b01-117">Use for audio files that contain spoken word, but are not audio books.</span></span> <span data-ttu-id="69b01-118">Por ejemplo, las rutinas de comedia de los servidores.</span><span class="sxs-lookup"><span data-stu-id="69b01-118">For example, stand-up comedy routines.</span></span>                                                                           |
| <span data-ttu-id="69b01-119">"6677DB9B-E5A0-4063-A1AD-ACEB52840CF1"</span><span class="sxs-lookup"><span data-stu-id="69b01-119">"6677DB9B-E5A0-4063-A1AD-ACEB52840CF1"</span></span> | <span data-ttu-id="69b01-120">Se usa para los archivos de audio relacionados con las noticias.</span><span class="sxs-lookup"><span data-stu-id="69b01-120">Use for audio files related to news.</span></span>                                                                                                                                                    |
| <span data-ttu-id="69b01-121">"1B824A67-3F80-4E3E-9CDE-F7361B0F5F1B"</span><span class="sxs-lookup"><span data-stu-id="69b01-121">"1B824A67-3F80-4E3E-9CDE-F7361B0F5F1B"</span></span> | <span data-ttu-id="69b01-122">Se usa para los archivos de audio con la conversación Mostrar contenido.</span><span class="sxs-lookup"><span data-stu-id="69b01-122">Use for audio files with talk show content.</span></span>                                                                                                                                             |
| <span data-ttu-id="69b01-123">"1FE2E091-4E1E-40CE-B22D-348C732E0B10"</span><span class="sxs-lookup"><span data-stu-id="69b01-123">"1FE2E091-4E1E-40CE-B22D-348C732E0B10"</span></span> | <span data-ttu-id="69b01-124">Se usa para archivos de vídeo relacionados con las noticias.</span><span class="sxs-lookup"><span data-stu-id="69b01-124">Use for video files related to news.</span></span>                                                                                                                                                    |
| <span data-ttu-id="69b01-125">"D6DE1D88-C77C-4593-BFBC-9C61E8C373E3"</span><span class="sxs-lookup"><span data-stu-id="69b01-125">"D6DE1D88-C77C-4593-BFBC-9C61E8C373E3"</span></span> | <span data-ttu-id="69b01-126">Se usa para archivos de vídeo que contienen presentaciones basadas en Web, películas cortas, finalizadores de películas, etc.</span><span class="sxs-lookup"><span data-stu-id="69b01-126">Use for video files containing Web-based shows, short films, movie trailers, and so on.</span></span> <span data-ttu-id="69b01-127">Este es el identificador general para el entretenimiento de vídeo que no encaja en otra categoría.</span><span class="sxs-lookup"><span data-stu-id="69b01-127">This is the general identifier for video entertainment that does not fit into another category.</span></span> |
| <span data-ttu-id="69b01-128">"00033368-5009-4AC3-A820-5D2D09A4E7C1"</span><span class="sxs-lookup"><span data-stu-id="69b01-128">"00033368-5009-4AC3-A820-5D2D09A4E7C1"</span></span> | <span data-ttu-id="69b01-129">Se usa para archivos de audio que contienen clips de sonido de juegos.</span><span class="sxs-lookup"><span data-stu-id="69b01-129">Use for audio files containing sound clips from games.</span></span>                                                                                                                                  |
| <span data-ttu-id="69b01-130">"F24FF731-96FC-4D0F-A2F5-5A3483682B1A"</span><span class="sxs-lookup"><span data-stu-id="69b01-130">"F24FF731-96FC-4D0F-A2F5-5A3483682B1A"</span></span> | <span data-ttu-id="69b01-131">Se usa para archivos de audio que contienen canciones completas de pistas de sonido de juegos.</span><span class="sxs-lookup"><span data-stu-id="69b01-131">Use for audio files containing complete songs from game sound tracks.</span></span> <span data-ttu-id="69b01-132">Si solo parte de una canción está codificada en el archivo, use en su lugar el identificador de los clips de sonido del juego.</span><span class="sxs-lookup"><span data-stu-id="69b01-132">If only part of a song is encoded in the file, use the identifier for game sound clips instead.</span></span>                   |
| <span data-ttu-id="69b01-133">"E3E689E2-BA8C-4330-96DF-A0EEEFFA6876"</span><span class="sxs-lookup"><span data-stu-id="69b01-133">"E3E689E2-BA8C-4330-96DF-A0EEEFFA6876"</span></span> | <span data-ttu-id="69b01-134">Se usa para archivos de vídeo que contienen vídeos musicales.</span><span class="sxs-lookup"><span data-stu-id="69b01-134">Use for video files containing music videos.</span></span>                                                                                                                                            |
| <span data-ttu-id="69b01-135">"B76628F4-300D-443D-9CB5-01C285109DAF"</span><span class="sxs-lookup"><span data-stu-id="69b01-135">"B76628F4-300D-443D-9CB5-01C285109DAF"</span></span> | <span data-ttu-id="69b01-136">Se usa para archivos de vídeo que contienen vídeos de inicio generales.</span><span class="sxs-lookup"><span data-stu-id="69b01-136">Use for video files containing general home video.</span></span>                                                                                                                                      |
| <span data-ttu-id="69b01-137">"A9B87FC9-BD47-4BF0-AC4F-655B89F7D868"</span><span class="sxs-lookup"><span data-stu-id="69b01-137">"A9B87FC9-BD47-4BF0-AC4F-655B89F7D868"</span></span> | <span data-ttu-id="69b01-138">Se usa para archivos de vídeo que contienen películas de características.</span><span class="sxs-lookup"><span data-stu-id="69b01-138">Use for video files containing feature films.</span></span>                                                                                                                                           |
| <span data-ttu-id="69b01-139">"BA7F258A-62F7-47A9-B21F-4651C42A000E"</span><span class="sxs-lookup"><span data-stu-id="69b01-139">"BA7F258A-62F7-47A9-B21F-4651C42A000E"</span></span> | <span data-ttu-id="69b01-140">Se usa para archivos de vídeo que contienen programas de televisión.</span><span class="sxs-lookup"><span data-stu-id="69b01-140">Use for video files containing television shows.</span></span> <span data-ttu-id="69b01-141">En el caso de las presentaciones basadas en Web, use el identificador más genérico.</span><span class="sxs-lookup"><span data-stu-id="69b01-141">For Web-based shows, use the more generic identifier.</span></span>                                                                                  |
| <span data-ttu-id="69b01-142">"44051B5B-B103-4B5C-92AB-93060A9463F0"</span><span class="sxs-lookup"><span data-stu-id="69b01-142">"44051B5B-B103-4B5C-92AB-93060A9463F0"</span></span> | <span data-ttu-id="69b01-143">Se usa para los archivos de vídeo que contienen vídeos corporativos.</span><span class="sxs-lookup"><span data-stu-id="69b01-143">Use for video files containing corporate video.</span></span> <span data-ttu-id="69b01-144">Por ejemplo, reuniones grabadas o vídeos de aprendizaje.</span><span class="sxs-lookup"><span data-stu-id="69b01-144">For example, recorded meetings or training videos.</span></span>                                                                                      |
| <span data-ttu-id="69b01-145">"0B710218-8C0C-475E-AF73-4C41C0C8F8CE"</span><span class="sxs-lookup"><span data-stu-id="69b01-145">"0B710218-8C0C-475E-AF73-4C41C0C8F8CE"</span></span> | <span data-ttu-id="69b01-146">Use para archivos de vídeo que contengan vídeo en casa procedente de fotografías.</span><span class="sxs-lookup"><span data-stu-id="69b01-146">Use for video files containing home video made from photographs.</span></span>                                                                                                                        |



 

<span data-ttu-id="69b01-147">Al especificar un identificador de clase secundaria, el archivo también debe contener un atributo de identificador de clase principal.</span><span class="sxs-lookup"><span data-stu-id="69b01-147">When specifying a secondary class identifier, the file should also contain a primary class identifier attribute.</span></span>

## <a name="see-also"></a><span data-ttu-id="69b01-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="69b01-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b01-149">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="69b01-149">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="69b01-150">**WM/MediaClassPrimaryID**</span><span class="sxs-lookup"><span data-stu-id="69b01-150">**WM/MediaClassPrimaryID**</span></span>](wm-mediaprimaryid.md)
</dt> </dl>

 

 





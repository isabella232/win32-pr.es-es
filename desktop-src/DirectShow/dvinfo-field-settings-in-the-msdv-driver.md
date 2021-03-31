---
description: Configuración del campo DVINFO en el controlador MSDV
ms.assetid: f0723da5-4f53-4f83-a657-ae42815a784e
title: Configuración del campo DVINFO en el controlador MSDV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4205a680833b0e2f8c6be2dc4cb65faa60515867
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806151"
---
# <a name="dvinfo-field-settings-in-the-msdv-driver"></a><span data-ttu-id="3c2aa-103">Configuración del campo DVINFO en el controlador MSDV</span><span class="sxs-lookup"><span data-stu-id="3c2aa-103">DVINFO Field Settings in the MSDV Driver</span></span>

<span data-ttu-id="3c2aa-104">En esta sección se describe cómo el controlador MSDV rellena la estructura [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) .</span><span class="sxs-lookup"><span data-stu-id="3c2aa-104">This section describes how the MSDV driver fills in the [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) structure.</span></span>

<span data-ttu-id="3c2aa-105">La `DVINFO` estructura define el bloque de formato para las conexiones de PIN entre MSDV y otros filtros.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-105">The `DVINFO` structure defines the format block for pin connections between MSDV and other filters.</span></span> <span data-ttu-id="3c2aa-106">De forma predeterminada, se usa el filtro de divisor DV al capturar desde un dispositivo DV y se usa el filtro DV MUX al transmitir al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-106">By default, the DV Splitter filter is used when capturing from a DV device, and the DV Mux filter is used when transmitting to the device.</span></span> <span data-ttu-id="3c2aa-107">Sin embargo, las aplicaciones pueden proporcionar sus propios filtros personalizados, por lo que resulta útil entender cómo MSDV rellena el `DVINFO` bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-107">However, applications may provide their own custom filters, so it is useful to understand how MSDV populates the `DVINFO` format block.</span></span>

<span data-ttu-id="3c2aa-108">La `DVINFO` estructura contiene la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="3c2aa-108">The `DVINFO` structure contains the following information:</span></span>

-   <span data-ttu-id="3c2aa-109">Dos paquetes de origen auxiliares de audio (AAUX), para el primer y el segundo bloque de audio.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-109">Two audio auxiliary (AAUX) source packs, for the first and second audio blocks.</span></span>
-   <span data-ttu-id="3c2aa-110">Dos paquetes de control de código fuente de AAUX, para el primer y el segundo bloque de audio.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-110">Two AAUX source control packs, for the first and second audio blocks.</span></span>
-   <span data-ttu-id="3c2aa-111">Un paquete de origen de vídeo auxiliar (VAUX).</span><span class="sxs-lookup"><span data-stu-id="3c2aa-111">A video auxiliary (VAUX) source pack.</span></span>
-   <span data-ttu-id="3c2aa-112">Un módulo de control de código fuente de VAUX.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-112">A VAUX source control pack.</span></span>

<span data-ttu-id="3c2aa-113">Cada fotograma de una secuencia DV contiene paquetes de AAUX y VAUX.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-113">Every frame in a DV stream contains AAUX and VAUX packs.</span></span> <span data-ttu-id="3c2aa-114">Sin embargo, el `DVINFO` bloque de formato es estático y solo se usa para establecer la conexión del PIN.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-114">However, the `DVINFO` format block is static, and is only used to establish the pin connection.</span></span> <span data-ttu-id="3c2aa-115">Cuando se conecta el controlador MSDV, no examina ninguno de los paquetes AAUX o VAUX de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-115">When the MSDV driver connects, it does not examine any of the AAUX or VAUX packs in the stream.</span></span> <span data-ttu-id="3c2aa-116">En su lugar, utiliza un conjunto de valores predeterminados, en función de las siguientes características del dispositivo DV:</span><span class="sxs-lookup"><span data-stu-id="3c2aa-116">Instead, it uses a set of default values, based on the following characteristics of the DV device:</span></span>

-   <span data-ttu-id="3c2aa-117">Si el dispositivo admite un formato de consumidor (DVCR) o formato profesional (DVCPRO)</span><span class="sxs-lookup"><span data-stu-id="3c2aa-117">Whether the device supports a consumer format (DVCR) or professional format (DVCPRO)</span></span>
-   <span data-ttu-id="3c2aa-118">El tipo de señal</span><span class="sxs-lookup"><span data-stu-id="3c2aa-118">The signal type</span></span>
-   <span data-ttu-id="3c2aa-119">Si el formato es NTSC o PAL.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-119">Whether the format is NTSC or PAL.</span></span> <span data-ttu-id="3c2aa-120">(Si el dispositivo no informa de esta información, MSDV tiene como valor predeterminado la configuración de NTSC)</span><span class="sxs-lookup"><span data-stu-id="3c2aa-120">(If the device does not report this information, MSDV defaults to the NTSC settings)</span></span>

<span data-ttu-id="3c2aa-121">Una vez que se inicia el streaming, es responsabilidad de los filtros de modo de usuario, como el divisor de DV, examinar el contenido real de cada fotograma DV.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-121">Once streaming begins, it is the responsibility of the user-mode filters, such as the DV Splitter, to examine the actual contents of each DV frame.</span></span> <span data-ttu-id="3c2aa-122">Dado que la información puede cambiar de un marco a otro, es posible que el filtro tenga que realizar un cambio de formato dinámico.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-122">Because the information can change from frame to frame, the filter may need to perform a dynamic format change.</span></span> <span data-ttu-id="3c2aa-123">Por ejemplo, si la velocidad de audio cambia, es posible que el filtro tenga que volver a negociar el tipo de audio.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-123">For example, if the audio rate changes, the filter might need to renegotiate the audio type.</span></span>

<span data-ttu-id="3c2aa-124">Si captura un archivo DV de tipo 1, la `DVINFO` estructura se escribe en el archivo como el fragmento de formato de secuencia (' strf ').</span><span class="sxs-lookup"><span data-stu-id="3c2aa-124">If you capture a type-1 DV file, the `DVINFO` structure is written into the file as the stream format ('strf') chunk.</span></span> <span data-ttu-id="3c2aa-125">Estos datos se toman directamente del bloque Format proporcionado por MSDV.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-125">This data is taken directly from the format block provided by MSDV.</span></span> <span data-ttu-id="3c2aa-126">Como se indicó, el contenido real de la secuencia puede ser diferente.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-126">As noted, the actual content of the stream might be different.</span></span> <span data-ttu-id="3c2aa-127">Es responsabilidad de la aplicación examinar los paquetes AAUX y VAUX en cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-127">It is the application's responsibility to examine the AAUX and VAUX packs in each frame.</span></span>

<span data-ttu-id="3c2aa-128">En los temas siguientes, puede encontrar tablas que enumeran todos los campos usados por MSDV.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-128">In the following topics, you can find tables listing all of the fields used by MSDV.</span></span>

-   [<span data-ttu-id="3c2aa-129">Paquete de origen (AS) de AAUX</span><span class="sxs-lookup"><span data-stu-id="3c2aa-129">AAUX Source (AS) Pack</span></span>](aaux-source--as--pack.md)
-   [<span data-ttu-id="3c2aa-130">Paquete de control de código fuente de AAUX (ASC)</span><span class="sxs-lookup"><span data-stu-id="3c2aa-130">AAUX Source Control (ASC) Pack</span></span>](aaux-source-control--asc--pack.md)
-   [<span data-ttu-id="3c2aa-131">Paquete de origen de VAUX (VS)</span><span class="sxs-lookup"><span data-stu-id="3c2aa-131">VAUX Source (VS) Pack</span></span>](vaux-source--vs--pack.md)
-   [<span data-ttu-id="3c2aa-132">Paquete de control de código fuente de VAUX (VSC)</span><span class="sxs-lookup"><span data-stu-id="3c2aa-132">VAUX Source Control (VSC) Pack</span></span>](vaux-source-control--vsc--pack.md)

<span data-ttu-id="3c2aa-133">Al leer estas tablas, consulte las siguientes especificaciones:</span><span class="sxs-lookup"><span data-stu-id="3c2aa-133">When reading these tables, please consult the following specifications:</span></span>

-   <span data-ttu-id="3c2aa-134">IEC 61834</span><span class="sxs-lookup"><span data-stu-id="3c2aa-134">IEC 61834</span></span>
-   <span data-ttu-id="3c2aa-135">314M SMPTE</span><span class="sxs-lookup"><span data-stu-id="3c2aa-135">SMPTE 314M</span></span>
-   <span data-ttu-id="3c2aa-136">SMPTE 370</span><span class="sxs-lookup"><span data-stu-id="3c2aa-136">SMPTE 370</span></span>

<span data-ttu-id="3c2aa-137">En cada tabla, la primera columna proporciona el código de campo, seguido del número de bits (entre paréntesis).</span><span class="sxs-lookup"><span data-stu-id="3c2aa-137">In each table, the first column gives the field code, followed by the number of bits (in parentheses).</span></span> <span data-ttu-id="3c2aa-138">Las columnas restantes proporcionan los valores de campo.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-138">The remaining columns give the field values.</span></span> <span data-ttu-id="3c2aa-139">Muchos de los campos AAUX y VAUX no son relevantes para la conexión de PIN, en cuyo caso MSDV establece un valor ficticio.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-139">Many of the AAUX and VAUX fields are not relevant for the pin connection, in which case MSDV sets a dummy value.</span></span> <span data-ttu-id="3c2aa-140">El valor numérico de todo el paquete se muestra en la parte inferior de cada tabla.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-140">The numeric value of the entire pack is listed at the bottom of each table.</span></span>

<span data-ttu-id="3c2aa-141">Las notas después de cada tabla proporcionan más información acerca de los campos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-141">The notes after each table give more information about selected fields.</span></span> <span data-ttu-id="3c2aa-142">Para obtener descripciones completas, consulte las especificaciones.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-142">For complete descriptions, refer to the specifications.</span></span> <span data-ttu-id="3c2aa-143">Además, algunos campos no tienen el mismo significado en SMPTE 314M/SMPTE 370 como en IEC 61834.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-143">Also, some fields do not have the same meaning in SMPTE 314M/SMPTE 370 as they do in IEC 61834.</span></span>

> [!Note]  
> <span data-ttu-id="3c2aa-144">Actualmente, DirectShow no admite formatos DVCPRO.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-144">Currently, DirectShow does not support DVCPRO formats.</span></span> <span data-ttu-id="3c2aa-145">Los valores enumerados para los formatos DVCPRO se definen para su uso futuro.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-145">The values listed for the DVCPRO formats are defined for future use.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3c2aa-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c2aa-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c2aa-147">Vídeo digital en DirectShow</span><span class="sxs-lookup"><span data-stu-id="3c2aa-147">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="3c2aa-148">Datos de DV en el formato de archivo AVI</span><span class="sxs-lookup"><span data-stu-id="3c2aa-148">DV Data in the AVI File Format</span></span>](dv-data-in-the-avi-file-format.md)
</dt> <dt>

[<span data-ttu-id="3c2aa-149">Controlador MSDV</span><span class="sxs-lookup"><span data-stu-id="3c2aa-149">MSDV Driver</span></span>](msdv-driver.md)
</dt> </dl>

 

 




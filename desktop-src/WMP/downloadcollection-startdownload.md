---
title: DownloadCollection. startDownload, método
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método startDownload pone en cola una descarga.
ms.assetid: 54cf91fe-cef9-4424-9f99-629e773eade1
keywords:
- método startDownload de Windows Media Player
- método startDownload de Windows Media Player, clase DownloadCollection
- Clase DownloadCollection Windows Media Player, método startDownload
topic_type:
- apiref
api_name:
- DownloadCollection.startDownload
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3187ce00dda45f7e4660b4961c78af6db2af50e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700085"
---
# <a name="downloadcollectionstartdownload-method"></a><span data-ttu-id="39478-108">DownloadCollection. startDownload, método</span><span class="sxs-lookup"><span data-stu-id="39478-108">DownloadCollection.startDownload method</span></span>

> [!Note]  
> <span data-ttu-id="39478-109">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="39478-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="39478-110">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="39478-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="39478-111">El método **startDownload** pone en cola una descarga.</span><span class="sxs-lookup"><span data-stu-id="39478-111">The **startDownload** method queues a download.</span></span>

## <a name="syntax"></a><span data-ttu-id="39478-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39478-112">Syntax</span></span>


```JScript
retVal = DownloadCollection.startDownload(
  sourceURL,
  type
)
```



## <a name="parameters"></a><span data-ttu-id="39478-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39478-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39478-114">*sourceURL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="39478-114">*sourceURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39478-115">**Cadena** que especifica la dirección URL de la descarga.</span><span class="sxs-lookup"><span data-stu-id="39478-115">**String** specifying the URL of the download.</span></span>

</dd> <dt>

<span data-ttu-id="39478-116">*tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="39478-116">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39478-117">**Cadena** que especifica el tipo de descarga.</span><span class="sxs-lookup"><span data-stu-id="39478-117">**String** specifying the type of download.</span></span> <span data-ttu-id="39478-118">Contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="39478-118">Contains one of the following values.</span></span>



| <span data-ttu-id="39478-119">Value</span><span class="sxs-lookup"><span data-stu-id="39478-119">Value</span></span>      | <span data-ttu-id="39478-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="39478-120">Description</span></span>                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39478-121">background</span><span class="sxs-lookup"><span data-stu-id="39478-121">background</span></span> | <span data-ttu-id="39478-122">(Windows XP y versiones posteriores). La descarga se produce como un proceso en segundo plano a medida que el tiempo de procesador está disponible.</span><span class="sxs-lookup"><span data-stu-id="39478-122">(Windows XP and later.) The download occurs as a background process as processor time becomes available.</span></span> <span data-ttu-id="39478-123">Los Estados de descarga se conservan incluso cuando se apaga Windows Media Player o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="39478-123">Download states persist even when Windows Media Player or Windows XP is shut down.</span></span> |
| <span data-ttu-id="39478-124">en tiempo real</span><span class="sxs-lookup"><span data-stu-id="39478-124">real time</span></span>  | <span data-ttu-id="39478-125">(Todos los sistemas operativos compatibles). La descarga se produce a la vez.</span><span class="sxs-lookup"><span data-stu-id="39478-125">(All supported operating systems.) The download occurs all at once.</span></span> <span data-ttu-id="39478-126">No se conservan los Estados de descarga entre sesiones.</span><span class="sxs-lookup"><span data-stu-id="39478-126">No download states persist between sessions.</span></span>                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39478-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39478-127">Return value</span></span>

<span data-ttu-id="39478-128">Este método devuelve un objeto **DownloadItem** .</span><span class="sxs-lookup"><span data-stu-id="39478-128">This method returns a **DownloadItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="39478-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39478-129">Remarks</span></span>

<span data-ttu-id="39478-130">Cuando se inicia una nueva descarga, Download Manager la agrega como un elemento a la colección de descarga que inició la descarga.</span><span class="sxs-lookup"><span data-stu-id="39478-130">When a new download is started, Download Manager adds it as an item to the download collection that initiated the download.</span></span>

<span data-ttu-id="39478-131">Solo se pueden descargar los siguientes formatos de medios digitales:</span><span class="sxs-lookup"><span data-stu-id="39478-131">Only the following digital media formats can be downloaded:</span></span>

-   <span data-ttu-id="39478-132">Formato ASF</span><span class="sxs-lookup"><span data-stu-id="39478-132">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="39478-133">MP3</span><span class="sxs-lookup"><span data-stu-id="39478-133">MP3</span></span>
-   <span data-ttu-id="39478-134">Audio de Windows Media (WMA)</span><span class="sxs-lookup"><span data-stu-id="39478-134">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="39478-135">Vídeo de Windows Media (WMV)</span><span class="sxs-lookup"><span data-stu-id="39478-135">Windows Media Video (WMV)</span></span>

<span data-ttu-id="39478-136">El parámetro *sourceURL* no admite cadenas con codificación Unicode.</span><span class="sxs-lookup"><span data-stu-id="39478-136">The *sourceURL* parameter does not support Unicode-encoded strings.</span></span> <span data-ttu-id="39478-137">Debe apuntar a contenido válido.</span><span class="sxs-lookup"><span data-stu-id="39478-137">It must point to valid content.</span></span> <span data-ttu-id="39478-138">No se admiten las redirecciones.</span><span class="sxs-lookup"><span data-stu-id="39478-138">Redirects are not supported.</span></span>

<span data-ttu-id="39478-139">Cuando se usa Windows XP, los archivos de audio se colocan automáticamente en sus subcarpetas de **música** apropiadas según los valores de metadatos de nivel de archivo.</span><span class="sxs-lookup"><span data-stu-id="39478-139">When using Windows XP, audio files are automatically placed into appropriate **My Music** subfolders based upon file-level metadata values.</span></span> <span data-ttu-id="39478-140">Los archivos de vídeo se colocan en \\ el \\ \\  \\ *tipo* de número aleatorio de descarga de música, donde el *número aleatorio* es un valor aleatorio generado por Windows Media Player para cada usuario, y el *tipo* es "en tiempo real" o "en segundo plano", en función del tipo de descarga.</span><span class="sxs-lookup"><span data-stu-id="39478-140">Video files are placed into \\My Music\\download\\*random number*\\*type*, where *random number* is a random value generated by Windows Media Player for each user, and *type* is either "real time" or "background", depending upon the download type.</span></span>

<span data-ttu-id="39478-141">Cuando se usa Windows Media Player 9 series con Windows 98 y Windows Millennium Edition (me), los archivos de audio y vídeo se colocan en el \\ \\ \\  \\ *tipo* de número aleatorio de descarga de música, donde el *número aleatorio* es un valor aleatorio generado por el reproductor para cada usuario y el *tipo* es "tiempo real" o "fondo", dependiendo del tipo de descarga.</span><span class="sxs-lookup"><span data-stu-id="39478-141">When using Windows Media Player 9 Series with Windows 98 and Windows Millennium Edition (ME), audio and video files are placed into \\My Music\\download\\*random number*\\*type*, where *random number* is a random value generated by the Player for each user, and *type* is either "real time" or "background", depending upon the download type.</span></span>

<span data-ttu-id="39478-142">Tenga en cuenta que se puede cambiar el nombre de los archivos en función de los atributos de metadatos contenidos en el archivo y las reglas especificadas por el usuario en el cuadro de diálogo **Opciones** .</span><span class="sxs-lookup"><span data-stu-id="39478-142">Note that files may be renamed based upon metadata attributes contained in the file and rules specified by the user in the **Options** dialog box.</span></span> <span data-ttu-id="39478-143">Los archivos que no contienen metadatos, como **álbum** o **intérprete**, pueden moverse a carpetas etiquetadas como intérprete desconocido o álbum desconocido.</span><span class="sxs-lookup"><span data-stu-id="39478-143">Files that don't contain metadata, such as **Album** or **Artist**, may be moved to folders labeled Unknown Artist or Unknown Album.</span></span>

## <a name="requirements"></a><span data-ttu-id="39478-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39478-144">Requirements</span></span>



| <span data-ttu-id="39478-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="39478-145">Requirement</span></span> | <span data-ttu-id="39478-146">Value</span><span class="sxs-lookup"><span data-stu-id="39478-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39478-147">Versión</span><span class="sxs-lookup"><span data-stu-id="39478-147">Version</span></span><br/> | <span data-ttu-id="39478-148">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="39478-148">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="39478-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="39478-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="39478-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39478-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39478-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="39478-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39478-152">**Objeto DownloadCollection**</span><span class="sxs-lookup"><span data-stu-id="39478-152">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> <dt>

[<span data-ttu-id="39478-153">**Objeto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="39478-153">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 






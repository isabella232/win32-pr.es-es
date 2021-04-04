---
title: Acerca del proceso de conversión
description: Acerca del proceso de conversión
ms.assetid: 147b82fd-9e82-4acf-8f8a-43eb02e99024
keywords:
- Windows Media Player, proceso de conversión
- Complementos de Windows Media Player, conversión
- complementos, conversión
- Complementos de conversión, proceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6fe2f2bbedf03b78c0d19abaf3793e8e92c788
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077333"
---
# <a name="about-the-conversion-process"></a><span data-ttu-id="7c75d-107">Acerca del proceso de conversión</span><span class="sxs-lookup"><span data-stu-id="7c75d-107">About the Conversion Process</span></span>

<span data-ttu-id="7c75d-108">Una vez que Windows Media Player crea una instancia del complemento de conversión, el proceso continúa como sigue:</span><span class="sxs-lookup"><span data-stu-id="7c75d-108">After Windows Media Player instantiates the conversion plug-in, the process proceeds as follows:</span></span>

1.  <span data-ttu-id="7c75d-109">El reproductor llama a [IWMPConvert:: ConvertFile](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile).</span><span class="sxs-lookup"><span data-stu-id="7c75d-109">The Player calls [IWMPConvert::ConvertFile](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile).</span></span>
2.  <span data-ttu-id="7c75d-110">El complemento convierte el archivo proporcionado en el parámetro *bstrInputFile* en un formato ASF.</span><span class="sxs-lookup"><span data-stu-id="7c75d-110">The plug-in converts the file provided in the *bstrInputFile* parameter into an ASF format.</span></span>
3.  <span data-ttu-id="7c75d-111">Si por algún motivo se produce un error en la conversión, el complemento devuelve un código de error adecuado y el proceso se detiene.</span><span class="sxs-lookup"><span data-stu-id="7c75d-111">If the conversion fails for some reason, the plug-in returns an appropriate failure code and the process stops.</span></span>
4.  <span data-ttu-id="7c75d-112">Si la conversión se realiza correctamente, el complemento coloca el archivo convertido en la carpeta proporcionada en el parámetro *bstrDestinationFolder* y devuelve la ruta de acceso completa al archivo convertido mediante el parámetro *pbstrOutputFile* .</span><span class="sxs-lookup"><span data-stu-id="7c75d-112">If the conversion succeeds, the plug-in places the converted file into the folder provided in the *bstrDestinationFolder* parameter and returns the fully qualified path to the converted file through the *pbstrOutputFile* parameter.</span></span>
5.  <span data-ttu-id="7c75d-113">El complemento devuelve un código de éxito de **ConvertFile**.</span><span class="sxs-lookup"><span data-stu-id="7c75d-113">The plug-in returns a success code from **ConvertFile**.</span></span>
6.  <span data-ttu-id="7c75d-114">El reproductor copia el archivo convertido en una carpeta de la jerarquía de carpetas de música del usuario.</span><span class="sxs-lookup"><span data-stu-id="7c75d-114">The Player copies the converted file to a folder in the user's music folder hierarchy.</span></span> <span data-ttu-id="7c75d-115">Exactamente donde el reproductor copia el archivo en depende del contenido.</span><span class="sxs-lookup"><span data-stu-id="7c75d-115">Exactly where the Player copies the file to depends on content.</span></span> <span data-ttu-id="7c75d-116">Como parte de este proceso, el reproductor podría cambiar el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="7c75d-116">As part of this process, the Player might rename the file.</span></span>
7.  <span data-ttu-id="7c75d-117">El reproductor copia el archivo original (desconvertido) en una carpeta de la jerarquía de carpetas de música del usuario.</span><span class="sxs-lookup"><span data-stu-id="7c75d-117">The Player copies the original (unconverted) file to a folder in the user's music folder hierarchy.</span></span> <span data-ttu-id="7c75d-118">Como parte de este proceso, el reproductor podría cambiar el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="7c75d-118">As part of this process, the Player might rename the file.</span></span> <span data-ttu-id="7c75d-119">Esta es la copia del archivo que usa el reproductor cuando el usuario sincroniza el contenido del equipo con un dispositivo que requiere el formato de archivo original.</span><span class="sxs-lookup"><span data-stu-id="7c75d-119">This is the copy of the file that the Player uses when the user syncs the content from the computer to a device that requires the original file format.</span></span> <span data-ttu-id="7c75d-120">Este archivo se denomina *archivo de instantáneas*.</span><span class="sxs-lookup"><span data-stu-id="7c75d-120">This file is called a *shadow file*.</span></span>
8.  <span data-ttu-id="7c75d-121">El reproductor agrega información sobre el archivo convertido a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="7c75d-121">The Player adds information about the converted file to the library.</span></span> <span data-ttu-id="7c75d-122">Esto incluye establecer el valor del atributo **ShadowFilePath** en la nueva ubicación donde se guarda el archivo de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="7c75d-122">This includes setting the value for the **ShadowFilePath** attribute to the new location where the shadow file is saved.</span></span>

<span data-ttu-id="7c75d-123">Si necesita trabajar con el archivo convertido, puede consultar la biblioteca para recuperar el contenido mediante los atributos **ContentDistributor** y **WM/UniqueFileIdentifier** .</span><span class="sxs-lookup"><span data-stu-id="7c75d-123">If you need to work with the converted file, you can query the library to retrieve the content by using the **ContentDistributor** and **WM/UniqueFileIdentifier** attributes.</span></span> <span data-ttu-id="7c75d-124">Si necesita trabajar con el archivo de instantáneas, debe recuperar el objeto **multimedia** del archivo convertido y, a continuación, consultar el atributo **ShadowFilePath** .</span><span class="sxs-lookup"><span data-stu-id="7c75d-124">If you need to work with the shadow file, you must still retrieve the **Media** object for the converted file and then query for the **ShadowFilePath** attribute.</span></span> <span data-ttu-id="7c75d-125">Vea [Agregar metadatos a archivos convertidos](adding-metadata-to-converted-files.md).</span><span class="sxs-lookup"><span data-stu-id="7c75d-125">See [Adding Metadata to Converted Files](adding-metadata-to-converted-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c75d-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7c75d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c75d-127">**Acerca de los complementos de conversión**</span><span class="sxs-lookup"><span data-stu-id="7c75d-127">**About Conversion Plug-ins**</span></span>](about-conversion-plug-ins.md)
</dt> <dt>

[<span data-ttu-id="7c75d-128">**Agregar metadatos a archivos convertidos**</span><span class="sxs-lookup"><span data-stu-id="7c75d-128">**Adding Metadata to Converted Files**</span></span>](adding-metadata-to-converted-files.md)
</dt> <dt>

[<span data-ttu-id="7c75d-129">**Leer valores de atributo**</span><span class="sxs-lookup"><span data-stu-id="7c75d-129">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="7c75d-130">**Atributo ShadowFilePath**</span><span class="sxs-lookup"><span data-stu-id="7c75d-130">**ShadowFilePath Attribute**</span></span>](shadowfilepath-attribute.md)
</dt> <dt>

[<span data-ttu-id="7c75d-131">**Atributo WM/ContentDistributor**</span><span class="sxs-lookup"><span data-stu-id="7c75d-131">**WM/ContentDistributor Attribute**</span></span>](wm-contentdistributor-attribute.md)
</dt> <dt>

[<span data-ttu-id="7c75d-132">**Atributo WM/UniqueFileIdentifier**</span><span class="sxs-lookup"><span data-stu-id="7c75d-132">**WM/UniqueFileIdentifier Attribute**</span></span>](wm-uniquefileidentifier-attribute.md)
</dt> </dl>

 

 





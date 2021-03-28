---
description: Muestra cómo personalizar el archivo en el cuadro de diálogo usar para mostrar información adicional y opciones para los archivos que están abiertos actualmente en la aplicación.
title: Ejemplo de File Is In Use
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 22EFE7CC-D223-46b3-BD6B-293E3FA0BA01
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 223e0addf201f3526654a17346963b4639e0d215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360784"
---
# <a name="file-is-in-use-sample"></a><span data-ttu-id="a709a-103">Ejemplo de File Is In Use</span><span class="sxs-lookup"><span data-stu-id="a709a-103">File Is In Use Sample</span></span>

<span data-ttu-id="a709a-104">Muestra cómo personalizar el **archivo en** el cuadro de diálogo usar para mostrar información adicional y opciones para los archivos que están abiertos actualmente en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a709a-104">Demonstrates how to customize the **File In Use** dialog to display additional information and options for files that are currently opened in the application.</span></span>

<span data-ttu-id="a709a-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="a709a-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a709a-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a709a-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="a709a-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="a709a-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="a709a-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="a709a-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="a709a-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="a709a-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="a709a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a709a-110">Requirements</span></span>



| <span data-ttu-id="a709a-111">Producto</span><span class="sxs-lookup"><span data-stu-id="a709a-111">Product</span></span>                                | <span data-ttu-id="a709a-112">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="a709a-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="a709a-113">Windows</span><span class="sxs-lookup"><span data-stu-id="a709a-113">Windows</span></span>                                | <span data-ttu-id="a709a-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a709a-114">Windows Vista</span></span>           |
| <span data-ttu-id="a709a-115">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="a709a-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="a709a-116">6.1</span><span class="sxs-lookup"><span data-stu-id="a709a-116">6.1</span></span>                     |



 

<span data-ttu-id="a709a-117">Para obtener más requisitos, vea el archivo desample.docx IFileIsInUse que se \_ incluye con el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a709a-117">For additional requirements, see the IFileIsInUse\_sample.docx file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="a709a-118">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="a709a-118">Downloading the Sample</span></span>

| <span data-ttu-id="a709a-119">Ubicación</span><span class="sxs-lookup"><span data-stu-id="a709a-119">Location</span></span>      | <span data-ttu-id="a709a-120">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="a709a-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a709a-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="a709a-121">GitHub</span></span>  | [<span data-ttu-id="a709a-122">Ejemplo de FileIsInUse</span><span class="sxs-lookup"><span data-stu-id="a709a-122">FileIsInUse sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse) |

## <a name="building-the-sample"></a><span data-ttu-id="a709a-123">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="a709a-123">Building the Sample</span></span>

<span data-ttu-id="a709a-124">Para compilar el ejemplo desde la ventana del símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="a709a-124">To build the sample from the Command Prompt window:</span></span>

1.  <span data-ttu-id="a709a-125">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **FileIsInUse** .</span><span class="sxs-lookup"><span data-stu-id="a709a-125">Open the Command Prompt window and navigate to the **FileIsInUse** project directory.</span></span>
2.  <span data-ttu-id="a709a-126">Escriba `msbuild FileIsInUse.sln`.</span><span class="sxs-lookup"><span data-stu-id="a709a-126">Enter `msbuild FileIsInUse.sln`.</span></span>

<span data-ttu-id="a709a-127">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="a709a-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="a709a-128">Abra el explorador de Windows y navegue hasta el directorio del proyecto **FilesInUse** .</span><span class="sxs-lookup"><span data-stu-id="a709a-128">Open Windows Explorer and navigate to the **FilesInUse** project directory.</span></span> <span data-ttu-id="a709a-129">Por ejemplo, la ruta de instalación predeterminada completa es `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileIsInUse` .</span><span class="sxs-lookup"><span data-stu-id="a709a-129">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileIsInUse`.</span></span>
2.  <span data-ttu-id="a709a-130">Haga doble clic en el icono del archivo FileIsInUseSample. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a709a-130">Double-click the icon for the FileIsInUseSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="a709a-131">La extensión de nombre de archivo. sln no se muestra en configuración de carpeta predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a709a-131">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="a709a-132">En esa situación, puede identificarse por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".</span><span class="sxs-lookup"><span data-stu-id="a709a-132">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="a709a-133">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="a709a-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="a709a-134">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="a709a-134">Running the Sample</span></span>

1.  <span data-ttu-id="a709a-135">Desplácese hasta el directorio que contiene el nuevo ejecutable, mediante la ventana del símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="a709a-135">Navigate to the directory that contains the new executable, using the command prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="a709a-136">En el símbolo del sistema, escriba `FileIsInUseSample.exe` o, en el explorador de Windows, haga doble clic en el icono de FileIsInUseSample.exe.</span><span class="sxs-lookup"><span data-stu-id="a709a-136">At the command prompt, enter `FileIsInUseSample.exe`, or from Windows Explorer, double-click the icon for FileIsInUseSample.exe.</span></span>

<span data-ttu-id="a709a-137">Para obtener información detallada sobre este ejemplo de código, vea el archivo desample.docx IFileIsInUse que se \_ incluye con el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a709a-137">For detailed information about this code sample, see the IFileIsInUse\_sample.docx file included with the sample.</span></span>

 

 




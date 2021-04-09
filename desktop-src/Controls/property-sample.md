---
title: Ejemplo de propiedad
ms.assetid: 44642d32-2cbc-4dd9-bccc-15924f310539
description: 'Más información acerca de: ejemplo de propiedad'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c11fda9b133ca6fa3b2f9942d8d48bec3a9e47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152821"
---
# <a name="property-sample"></a><span data-ttu-id="ae5e5-103">Ejemplo de propiedad</span><span class="sxs-lookup"><span data-stu-id="ae5e5-103">Property Sample</span></span>

<span data-ttu-id="ae5e5-104">En este tema se describe el ejemplo de código de ejemplo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ae5e5-104">This topic describes the Property Sample code sample.</span></span> <span data-ttu-id="ae5e5-105">Contiene las secciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="ae5e5-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="ae5e5-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae5e5-106">Description</span></span>](#description)
-   [<span data-ttu-id="ae5e5-107">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="ae5e5-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="ae5e5-108">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="ae5e5-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="ae5e5-109">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="ae5e5-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="ae5e5-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ae5e5-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="ae5e5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae5e5-111">Description</span></span>

<span data-ttu-id="ae5e5-112">En el ejemplo de propiedad se muestra cómo implementar tres estilos diferentes de hojas de propiedades: modal, no modal y asistente.</span><span class="sxs-lookup"><span data-stu-id="ae5e5-112">The Property Sample shows how to implement three different styles of property sheets: modal, modeless, and wizard.</span></span> <span data-ttu-id="ae5e5-113">También se muestra cómo usar la función [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback) para modificar el cuadro de diálogo de la hoja de propiedades antes o después de crearlo.</span><span class="sxs-lookup"><span data-stu-id="ae5e5-113">It also shows how to use the [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback) function to modify the property sheet dialog before or after it is created.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="ae5e5-114">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="ae5e5-114">Minimum Requirements</span></span>



| <span data-ttu-id="ae5e5-115">Producto</span><span class="sxs-lookup"><span data-stu-id="ae5e5-115">Product</span></span>          | <span data-ttu-id="ae5e5-116">Versión</span><span class="sxs-lookup"><span data-stu-id="ae5e5-116">Version</span></span>                              |
|------------------|--------------------------------------|
| <span data-ttu-id="ae5e5-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ae5e5-117">DLL</span></span>              | <span data-ttu-id="ae5e5-118">comctl32.dll versión 4,0</span><span class="sxs-lookup"><span data-stu-id="ae5e5-118">comctl32.dll version 4.0</span></span>             |
| <span data-ttu-id="ae5e5-119">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="ae5e5-119">Operating System</span></span> | <span data-ttu-id="ae5e5-120">Windows 95, Microsoft Windows NT 3,1</span><span class="sxs-lookup"><span data-stu-id="ae5e5-120">Windows 95, Microsoft Windows NT 3.1</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="ae5e5-121">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="ae5e5-121">Downloading the Sample</span></span>

<span data-ttu-id="ae5e5-122">El ejemplo de propiedad se instala como parte del [Kit de desarrollo de software (SDK) de Windows](https://msdn.microsoft.com/windows/bb980924.aspx) y está disponible en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="ae5e5-122">The Property Sample is installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="ae5e5-123">Location</span><span class="sxs-lookup"><span data-stu-id="ae5e5-123">Location</span></span>    | <span data-ttu-id="ae5e5-124">Ruta de acceso/URL</span><span class="sxs-lookup"><span data-stu-id="ae5e5-124">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae5e5-125">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="ae5e5-125">Windows SDK</span></span> | <span data-ttu-id="ae5e5-126">% Archivos de programa% \\ Microsoft SDK \\ Windows número de versión ejemplos de la \\ \[ \] \\ \\ \\ \\ \\ propiedad común de los controles WinUI</span><span class="sxs-lookup"><span data-stu-id="ae5e5-126">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\controls\\common\\property</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="ae5e5-127">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="ae5e5-127">Building the Sample</span></span>

<span data-ttu-id="ae5e5-128">Para compilar el ejemplo mediante el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="ae5e5-128">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="ae5e5-129">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto.</span><span class="sxs-lookup"><span data-stu-id="ae5e5-129">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="ae5e5-130">Escriba `msbuild [project file]`.</span><span class="sxs-lookup"><span data-stu-id="ae5e5-130">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="ae5e5-131">Para compilar el ejemplo con Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="ae5e5-131">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="ae5e5-132">Abra el explorador de Windows y navegue hasta el directorio del proyecto.</span><span class="sxs-lookup"><span data-stu-id="ae5e5-132">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="ae5e5-133">Haga doble clic en el icono del archivo. vcproj para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ae5e5-133">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="ae5e5-134">En el menú **compilar** , seleccione **compilar solución** para compilar la solución.</span><span class="sxs-lookup"><span data-stu-id="ae5e5-134">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae5e5-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ae5e5-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae5e5-136">Acerca de las hojas de propiedades</span><span class="sxs-lookup"><span data-stu-id="ae5e5-136">About Property Sheets</span></span>](property-sheets.md)
</dt> </dl>

 

 





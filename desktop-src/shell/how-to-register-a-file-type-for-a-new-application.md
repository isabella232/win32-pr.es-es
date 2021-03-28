---
description: Si tiene previsto asociar uno o varios tipos de archivo a una nueva aplicación, debe definir un ProgID para cada tipo de archivo que desee asociar a la aplicación.
ms.assetid: 997600C9-5264-44EC-BAEC-CB5CEEA0BD14
title: Cómo registrar un tipo de archivo para una nueva aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728cc48075ab1c2631f0a950059da65ae326ae79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985423"
---
# <a name="how-to-register-a-file-type-for-a-new-application"></a><span data-ttu-id="97e78-103">Cómo registrar un tipo de archivo para una nueva aplicación</span><span class="sxs-lookup"><span data-stu-id="97e78-103">How to Register a File Type for a New Application</span></span>

<span data-ttu-id="97e78-104">Si tiene previsto asociar uno o varios tipos de archivo a una nueva aplicación, debe definir un ProgID para cada tipo de archivo que desee asociar a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="97e78-104">If you plan to associate one or more file types with a new application, you must define a ProgID for each file type that you want to associate with the application.</span></span>

<span data-ttu-id="97e78-105">Para crear un ProgID para cada tipo de archivo único que controla la aplicación, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="97e78-105">To create a ProgID for each unique file type that your application handles, use these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="97e78-106">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="97e78-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="97e78-107">Paso 1:</span><span class="sxs-lookup"><span data-stu-id="97e78-107">Step 1:</span></span>

<span data-ttu-id="97e78-108">Tenga en cuenta que algunos tipos de archivo tienen varias extensiones que señalan al mismo ProgID; por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="97e78-108">Note that some file types have multiple extensions that point to the same ProgID; for example:</span></span>

-   <span data-ttu-id="97e78-109">**HKEY \_ Clases \_ raíz** \\ **app. JPEG** (su ProgID)</span><span class="sxs-lookup"><span data-stu-id="97e78-109">**HKEY\_CLASSES\_ROOT**\\**App.jpeg** (your ProgID)</span></span>
-   <span data-ttu-id="97e78-110">**HKEY \_ Clases \_ root** \\ **. jpg** = app. JPEG (asignaciones de tipo de archivo)</span><span class="sxs-lookup"><span data-stu-id="97e78-110">**HKEY\_CLASSES\_ROOT**\\ **.jpg** = App.jpeg (the file type mappings)</span></span>
-   <span data-ttu-id="97e78-111">**HKEY \_ Clases \_ root** \\ **. JPEG** = app. JPEG</span><span class="sxs-lookup"><span data-stu-id="97e78-111">**HKEY\_CLASSES\_ROOT**\\ **.jpeg** = App.jpeg</span></span>

### <a name="step-2"></a><span data-ttu-id="97e78-112">Paso 2:</span><span class="sxs-lookup"><span data-stu-id="97e78-112">Step 2:</span></span>

<span data-ttu-id="97e78-113">Quite los valores de ProgID al instalar y desinstalar el programa.</span><span class="sxs-lookup"><span data-stu-id="97e78-113">Remove the ProgID values when you install and uninstall your program.</span></span>

### <a name="step-3"></a><span data-ttu-id="97e78-114">Paso 3:</span><span class="sxs-lookup"><span data-stu-id="97e78-114">Step 3:</span></span>

<span data-ttu-id="97e78-115">Dejar las asignaciones de tipos de archivo sin modificar en el momento de la desinstalación.</span><span class="sxs-lookup"><span data-stu-id="97e78-115">Leave the file type mappings unchanged at uninstall time.</span></span> <span data-ttu-id="97e78-116">Esto funciona porque las asignaciones de tipo de archivo se almacenan por usuario en \_ las clases HKEY \_ root \\ . ext y el sistema identifica el caso en el que falta el valor ProgID y lo omite.</span><span class="sxs-lookup"><span data-stu-id="97e78-116">Doing so works because file type mappings are stored per user in HKEY\_CLASSES\_ROOT\\.ext, and the system identifies the case where the ProgID value is missing and ignores it.</span></span> <span data-ttu-id="97e78-117">Dejar las asignaciones de tipos de archivo sin cambios evita la necesidad de tener código condicional que solo Quite la asignación de tipo de archivo si el valor sigue señalando al ProgID.</span><span class="sxs-lookup"><span data-stu-id="97e78-117">Leaving file type mappings unchanged avoids the need to have conditional code that only removes the file type mapping if the value still points to your ProgID.</span></span> <span data-ttu-id="97e78-118">Es importante evitar hacerlo en los casos en los que otra aplicación podría haber cambiado y, por tanto, no se puede quitar fácilmente el valor.</span><span class="sxs-lookup"><span data-stu-id="97e78-118">It is important to avoid doing so in cases where it might have been changed by another application and you thus cannot easily remove the value.</span></span>

### <a name="step-4"></a><span data-ttu-id="97e78-119">Paso 4:</span><span class="sxs-lookup"><span data-stu-id="97e78-119">Step 4:</span></span>

<span data-ttu-id="97e78-120">Especifique un valor único para la descripción del tipo de archivo de cada ProgID del tipo de archivo mediante una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="97e78-120">Specify a unique value for the file type description of each file type ProgID by doing one of the following:</span></span>

-   <span data-ttu-id="97e78-121">Deje el valor predeterminado de ProgID vacío, en cuyo caso el sistema utiliza el archivo. ext.</span><span class="sxs-lookup"><span data-stu-id="97e78-121">Leave the default value of the ProgID empty, in which case the system uses the .ext file.</span></span>
-   <span data-ttu-id="97e78-122">Proporcione un valor localizado a través de FriendlyTypeName y, para la compatibilidad con las aplicaciones antiguas que leen el registro directamente, asegúrese de proporcionar el valor predeterminado del ProgID como la descripción del tipo de archivo (es decir, use el mismo valor al que hace referencia el FriendlyTypeName en el recurso en inglés).</span><span class="sxs-lookup"><span data-stu-id="97e78-122">Provide a localized value via FriendlyTypeName and, for compatibility with old applications that read the registry directly, be sure to provide the default value of the ProgID as the file type description (that is, use the same value that is referred to by the FriendlyTypeName in the English resource).</span></span>

## <a name="remarks"></a><span data-ttu-id="97e78-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97e78-123">Remarks</span></span>

<span data-ttu-id="97e78-124">Si tiene previsto asociar el archivo a una aplicación existente, busque un ProgID de aplicación en el registro.</span><span class="sxs-lookup"><span data-stu-id="97e78-124">If you plan to associate the file with an existing application, locate an application ProgID in the registry.</span></span> <span data-ttu-id="97e78-125">Para obtener más información, vea [tipos de archivo](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="97e78-125">For more information, see [File Types](fa-file-types.md).</span></span>

 

 




---
description: Representa información sobre un experimento (captura).
MS-HAID: vspixengine.Experiment
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura del experimento
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 632F1F92-3E32-4B0A-8E38-2613694C267F
api_name:
- Experiment
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e932d2f2b60a72ca167f3f6edd7f4ddae9b68710
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805983"
---
# <a name="span-idvspixengineexperimentspanexperiment-structure"></a><span data-ttu-id="a5bd0-103"><span id="vspixengine.experiment"></span>Estructura del experimento</span><span class="sxs-lookup"><span data-stu-id="a5bd0-103"><span id="vspixengine.experiment"></span>Experiment structure</span></span>

<span data-ttu-id="a5bd0-104">Representa información sobre un experimento (captura).</span><span class="sxs-lookup"><span data-stu-id="a5bd0-104">Represents information about an experiment (capture).</span></span>

## <a name="syntax"></a><span data-ttu-id="a5bd0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5bd0-105">Syntax</span></span>


```C++
} Experiment;
```

## <a name="members"></a><span data-ttu-id="a5bd0-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="a5bd0-106">Members</span></span>

<span data-ttu-id="a5bd0-107">**processId**</span><span class="sxs-lookup"><span data-stu-id="a5bd0-107">**processId**</span></span>  
<span data-ttu-id="a5bd0-108">IDENTIFICADOR del proceso asociado.</span><span class="sxs-lookup"><span data-stu-id="a5bd0-108">The associated process ID.</span></span>

<span data-ttu-id="a5bd0-109">**applicationName**</span><span class="sxs-lookup"><span data-stu-id="a5bd0-109">**applicationName**</span></span>  
<span data-ttu-id="a5bd0-110">Cadena COM que contiene el nombre de la aplicación en la que se va a ejecutar el experimento.</span><span class="sxs-lookup"><span data-stu-id="a5bd0-110">A COM string containing the name of the application to run the experiment on.</span></span>

<span data-ttu-id="a5bd0-111">**commandLineArguments**</span><span class="sxs-lookup"><span data-stu-id="a5bd0-111">**commandLineArguments**</span></span>  
<span data-ttu-id="a5bd0-112">Cadena COM que contiene los argumentos de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="a5bd0-112">A COM string containing the command line arguments.</span></span>

<span data-ttu-id="a5bd0-113">**workingDirectory**</span><span class="sxs-lookup"><span data-stu-id="a5bd0-113">**workingDirectory**</span></span>  
<span data-ttu-id="a5bd0-114">Cadena COM que contiene la ruta de acceso del directorio de trabajo.</span><span class="sxs-lookup"><span data-stu-id="a5bd0-114">A COM string containing the path of the working directory.</span></span>

<span data-ttu-id="a5bd0-115">**tempPixRunFile**</span><span class="sxs-lookup"><span data-stu-id="a5bd0-115">**tempPixRunFile**</span></span>  
<span data-ttu-id="a5bd0-116">Cadena COM que contiene la ruta de acceso del archivo temporal que se usa para realizar el experimento.</span><span class="sxs-lookup"><span data-stu-id="a5bd0-116">A COM string containing the filepath of the temporary file used to perform the experiment.</span></span>

<span data-ttu-id="a5bd0-117">**startOption**</span><span class="sxs-lookup"><span data-stu-id="a5bd0-117">**startOption**</span></span>  
<span data-ttu-id="a5bd0-118">Opción de inicio asociada al experimento.</span><span class="sxs-lookup"><span data-stu-id="a5bd0-118">The start option associated with the experiment.</span></span>

<span data-ttu-id="a5bd0-119">**experimentType**</span><span class="sxs-lookup"><span data-stu-id="a5bd0-119">**experimentType**</span></span>  
<span data-ttu-id="a5bd0-120">El tipo de experimento (captura).</span><span class="sxs-lookup"><span data-stu-id="a5bd0-120">The kind of experiment (capture).</span></span>

<span data-ttu-id="a5bd0-121">**uiLocale**</span><span class="sxs-lookup"><span data-stu-id="a5bd0-121">**uiLocale**</span></span>  
<span data-ttu-id="a5bd0-122">IDENTIFICADOR de la configuración regional utilizada para los elementos de superposición de la interfaz de usuario durante la Experiement (captura).</span><span class="sxs-lookup"><span data-stu-id="a5bd0-122">The ID of the locale used for UI overlay elements during the experiement (capture).</span></span> <span data-ttu-id="a5bd0-123">Esto se pasa desde el host (como Visual Studio Diagnóstico de gráficos) al motor de captura.</span><span class="sxs-lookup"><span data-stu-id="a5bd0-123">This is passed from the host (such as Visual Studio Graphics Diagnostics) to the capture engine.</span></span>

<span data-ttu-id="a5bd0-124">**registryRoot**</span><span class="sxs-lookup"><span data-stu-id="a5bd0-124">**registryRoot**</span></span>  
<span data-ttu-id="a5bd0-125">Cadena COM que contiene la raíz del registro.</span><span class="sxs-lookup"><span data-stu-id="a5bd0-125">A COM string containing the registry root.</span></span> <span data-ttu-id="a5bd0-126">Esto se pasa desde el host (como Visual Studio Diagnóstico de gráficos) al motor de captura.</span><span class="sxs-lookup"><span data-stu-id="a5bd0-126">This is passed from the host (such as Visual Studio Graphics Diagnostics) to the capture engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5bd0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5bd0-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a5bd0-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5bd0-128">Header</span></span></p></td><td><span data-ttu-id="a5bd0-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a5bd0-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 




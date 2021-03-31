---
description: Errores de registro
ms.assetid: 690ea91b-5bc0-45f0-8354-ec625709f7bd
title: Errores de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76cded9d4cfaedd93e846fec52b07bf5d4eef9a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805629"
---
# <a name="logging-errors"></a><span data-ttu-id="91f2d-103">Errores de registro</span><span class="sxs-lookup"><span data-stu-id="91f2d-103">Logging Errors</span></span>

<span data-ttu-id="91f2d-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="91f2d-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="91f2d-105">Los [servicios de edición de DirectShow](directshow-editing-services.md) (des) proporcionan un mecanismo integrado para registrar los errores que se producen al cargar, construir o representar un proyecto des.</span><span class="sxs-lookup"><span data-stu-id="91f2d-105">[DirectShow Editing Services](directshow-editing-services.md) (DES) provides a built-in mechanism for logging errors that occur when loading, constructing, or rendering a DES project.</span></span> <span data-ttu-id="91f2d-106">En este artículo se presenta una aplicación de consola de ejemplo que carga un archivo de proyecto XML e intenta representarlo.</span><span class="sxs-lookup"><span data-stu-id="91f2d-106">This article presents a sample console application that loads an XML project file and attempts to render it.</span></span> <span data-ttu-id="91f2d-107">Si se produce un error, la aplicación imprime un mensaje de error en la ventana de la consola.</span><span class="sxs-lookup"><span data-stu-id="91f2d-107">If an error occurs, the application prints an error message in the console window.</span></span> <span data-ttu-id="91f2d-108">El código de ejemplo que se presenta en este artículo se basa en el ejemplo que se proporciona en [cargar y obtener una vista previa de un proyecto](loading-and-previewing-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="91f2d-108">The sample code presented in this article builds on the example given in [Loading and Previewing a Project](loading-and-previewing-a-project.md).</span></span>

> [!Note]  
> <span data-ttu-id="91f2d-109">No es necesario que la aplicación implemente el registro de errores.</span><span class="sxs-lookup"><span data-stu-id="91f2d-109">Your application is not required to implement error logging.</span></span> <span data-ttu-id="91f2d-110">DES no registra los errores a menos que lo solicite explícitamente.</span><span class="sxs-lookup"><span data-stu-id="91f2d-110">DES does not log errors unless you explicitly request it.</span></span>

 

<span data-ttu-id="91f2d-111">En este artículo se supone que entiende la programación del cliente COM y el modelo de la escala de tiempo DES.</span><span class="sxs-lookup"><span data-stu-id="91f2d-111">This article assumes that you understand COM client programming and the DES timeline model.</span></span> <span data-ttu-id="91f2d-112">Además, debe comprender los aspectos básicos de la programación de objetos COM.</span><span class="sxs-lookup"><span data-stu-id="91f2d-112">In addition, you need to understand the basics of COM object programming.</span></span> <span data-ttu-id="91f2d-113">Para obtener información acerca de las escalas de tiempo en DES, vea [el modelo Timeline](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="91f2d-113">For information about timelines in DES, see [The Timeline Model](the-timeline-model.md).</span></span>

<span data-ttu-id="91f2d-114">Este artículo contiene las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="91f2d-114">This article contains the following sections.</span></span>

-   [<span data-ttu-id="91f2d-115">Información general sobre el registro de errores</span><span class="sxs-lookup"><span data-stu-id="91f2d-115">Overview of Error Logging</span></span>](overview-of-error-logging.md)
-   [<span data-ttu-id="91f2d-116">Crear una clase de registro de errores</span><span class="sxs-lookup"><span data-stu-id="91f2d-116">Creating an Error Logging Class</span></span>](creating-an-error-logging-class.md)
-   [<span data-ttu-id="91f2d-117">Implementación de IAMErrorLog</span><span class="sxs-lookup"><span data-stu-id="91f2d-117">Implementing IAMErrorLog</span></span>](implementing-iamerrorlog.md)
-   [<span data-ttu-id="91f2d-118">Configuración del registro de errores</span><span class="sxs-lookup"><span data-stu-id="91f2d-118">Setting the Error Log</span></span>](setting-the-error-log.md)
-   [<span data-ttu-id="91f2d-119">Registro de errores DES: código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="91f2d-119">DES Error Logging: Example Code</span></span>](des-error-logging--example-code.md)

## <a name="related-topics"></a><span data-ttu-id="91f2d-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="91f2d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91f2d-121">Usar servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="91f2d-121">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 




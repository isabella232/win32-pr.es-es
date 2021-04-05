---
description: Una biblioteca de vínculos dinámicos (DLL) es un módulo que contiene funciones y datos que puede usar otro módulo (aplicación o DLL).
ms.assetid: 09e35b46-86a1-44ed-ab6d-207857b2605c
title: Bibliotecas de Dynamic-Link (bibliotecas de vínculos dinámicos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8068cd0b8f1d5431c5638a10350d9a1ae7060aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811486"
---
# <a name="dynamic-link-libraries-dynamic-link-libraries"></a><span data-ttu-id="0c27c-103">Bibliotecas de Dynamic-Link (bibliotecas de vínculos dinámicos)</span><span class="sxs-lookup"><span data-stu-id="0c27c-103">Dynamic-Link Libraries (Dynamic-Link Libraries)</span></span>

<span data-ttu-id="0c27c-104">Una *biblioteca de vínculos dinámicos* (dll) es un módulo que contiene funciones y datos que puede usar otro módulo (aplicación o dll).</span><span class="sxs-lookup"><span data-stu-id="0c27c-104">A *dynamic-link library* (DLL) is a module that contains functions and data that can be used by another module (application or DLL).</span></span>

<span data-ttu-id="0c27c-105">Un archivo DLL puede definir dos tipos de funciones: exportada e interna.</span><span class="sxs-lookup"><span data-stu-id="0c27c-105">A DLL can define two kinds of functions: exported and internal.</span></span> <span data-ttu-id="0c27c-106">Las funciones exportadas están diseñadas para ser llamadas por otros módulos, así como desde el archivo DLL en el que se definen.</span><span class="sxs-lookup"><span data-stu-id="0c27c-106">The exported functions are intended to be called by other modules, as well as from within the DLL where they are defined.</span></span> <span data-ttu-id="0c27c-107">Normalmente, las funciones internas están pensadas para ser llamadas solo desde dentro del archivo DLL donde están definidas.</span><span class="sxs-lookup"><span data-stu-id="0c27c-107">Internal functions are typically intended to be called only from within the DLL where they are defined.</span></span> <span data-ttu-id="0c27c-108">Aunque un archivo DLL puede exportar datos, sus datos normalmente solo se usan en sus funciones.</span><span class="sxs-lookup"><span data-stu-id="0c27c-108">Although a DLL can export data, its data is generally used only by its functions.</span></span> <span data-ttu-id="0c27c-109">Sin embargo, no hay nada que impida que otro módulo lea o escriba esa dirección.</span><span class="sxs-lookup"><span data-stu-id="0c27c-109">However, there is nothing to prevent another module from reading or writing that address.</span></span>

<span data-ttu-id="0c27c-110">Los archivos dll proporcionan una manera de modularr las aplicaciones para que su funcionalidad se pueda actualizar y reutilizar más fácilmente.</span><span class="sxs-lookup"><span data-stu-id="0c27c-110">DLLs provide a way to modularize applications so that their functionality can be updated and reused more easily.</span></span> <span data-ttu-id="0c27c-111">Los archivos dll también ayudan a reducir la sobrecarga de memoria cuando varias aplicaciones usan la misma funcionalidad al mismo tiempo, porque aunque cada aplicación recibe su propia copia de los datos de la DLL, las aplicaciones comparten el código DLL.</span><span class="sxs-lookup"><span data-stu-id="0c27c-111">DLLs also help reduce memory overhead when several applications use the same functionality at the same time, because although each application receives its own copy of the DLL data, the applications share the DLL code.</span></span>

<span data-ttu-id="0c27c-112">La interfaz de programación de aplicaciones (API) de Windows se implementa como un conjunto de archivos dll, por lo que cualquier proceso que use la API de Windows usa la vinculación dinámica.</span><span class="sxs-lookup"><span data-stu-id="0c27c-112">The Windows application programming interface (API) is implemented as a set of DLLs, so any process that uses the Windows API uses dynamic linking.</span></span>

-   [<span data-ttu-id="0c27c-113">Acerca de las bibliotecas de Dynamic-Link</span><span class="sxs-lookup"><span data-stu-id="0c27c-113">About Dynamic-Link Libraries</span></span>](about-dynamic-link-libraries.md)
-   [<span data-ttu-id="0c27c-114">Usar bibliotecas de Dynamic-Link</span><span class="sxs-lookup"><span data-stu-id="0c27c-114">Using Dynamic-Link Libraries</span></span>](using-dynamic-link-libraries.md)
-   [<span data-ttu-id="0c27c-115">Referencia de biblioteca de vínculos dinámicos</span><span class="sxs-lookup"><span data-stu-id="0c27c-115">Dynamic-Link Library Reference</span></span>](dynamic-link-library-reference.md)

> [!Note]  
> <span data-ttu-id="0c27c-116">Si es un usuario que está experimentando dificultades con un archivo DLL en el equipo, debe ponerse en contacto con el servicio de soporte al cliente para el proveedor de software que publica el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="0c27c-116">If you are a user experiencing difficulty with a DLL on your computer, you should contact customer support for the software vendor that publishes the DLL.</span></span> <span data-ttu-id="0c27c-117">Si cree que necesita soporte técnico para un producto de Microsoft (incluido Windows), visite el sitio de soporte técnico en [support.Microsoft.com](https://support.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="0c27c-117">If you feel you are in need of support for a Microsoft product (including Windows), please go to our technical support site at [support.microsoft.com](https://support.microsoft.com).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0c27c-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0c27c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c27c-119">DLL (Visual C++)</span><span class="sxs-lookup"><span data-stu-id="0c27c-119">DLLs (Visual C++)</span></span>](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 

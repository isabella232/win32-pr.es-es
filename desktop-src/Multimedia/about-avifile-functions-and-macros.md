---
title: Acerca de las funciones y macros de AVIFile
description: Acerca de las funciones y macros de AVIFile
ms.assetid: 877f6759-8271-47eb-8a7f-540393e5ae89
keywords:
- AVIFileInit función)
- AVIFileExit función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f66bbac900b69841fd7cba814aad339731b75727
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076334"
---
# <a name="about-avifile-functions-and-macros"></a><span data-ttu-id="c4d1b-105">Acerca de las funciones y macros de AVIFile</span><span class="sxs-lookup"><span data-stu-id="c4d1b-105">About AVIFile Functions and Macros</span></span>

<span data-ttu-id="c4d1b-106">Las funciones y macros de AVIFile controlan la información de los archivos basados en tiempo como uno o varios *flujos de datos* en lugar de los bloques etiquetados de los datos denominados fragmentos.</span><span class="sxs-lookup"><span data-stu-id="c4d1b-106">The AVIFile functions and macros handle the information in time-based files as one or more *data streams* instead of tagged blocks of data called chunks.</span></span> <span data-ttu-id="c4d1b-107">Los flujos de datos hacen referencia a los componentes de un archivo basado en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="c4d1b-107">Data streams refer to the components of a time-based file.</span></span> <span data-ttu-id="c4d1b-108">Un archivo AVI puede contener varios tipos diferentes de datos, como una secuencia de vídeo, una banda sonora en inglés y una banda sonora en francés.</span><span class="sxs-lookup"><span data-stu-id="c4d1b-108">An AVI file can contain several different types of data, such as a video sequence, an English soundtrack, and a French soundtrack.</span></span> <span data-ttu-id="c4d1b-109">Con AVIFile, una aplicación puede tener acceso a cada uno de estos componentes por separado.</span><span class="sxs-lookup"><span data-stu-id="c4d1b-109">Using AVIFile, an application can access each of these components separately.</span></span>

> [!Note]  
> <span data-ttu-id="c4d1b-110">Aunque las funciones y macros de AVIFile funcionan con cualquier archivo RIFF, en esta información general solo se muestra su uso con archivos AVI.</span><span class="sxs-lookup"><span data-stu-id="c4d1b-110">Although the AVIFile functions and macros work with any RIFF file, this overview demonstrates their use with AVI files only.</span></span> <span data-ttu-id="c4d1b-111">Los archivos AVI suelen ser los archivos basados en el tiempo que se usan con las macros y funciones de AVIFile.</span><span class="sxs-lookup"><span data-stu-id="c4d1b-111">AVI files are typically the time-based files used with the AVIFile macros and functions.</span></span>

 

<span data-ttu-id="c4d1b-112">Las funciones y macros de AVIFile se encuentran en una biblioteca de vínculos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="c4d1b-112">AVIFile functions and macros are contained in a dynamic-link library.</span></span> <span data-ttu-id="c4d1b-113">Para inicializar la biblioteca, utilice la función [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) .</span><span class="sxs-lookup"><span data-stu-id="c4d1b-113">To initialize the library, use the [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) function.</span></span> <span data-ttu-id="c4d1b-114">Después de inicializar la biblioteca, puede utilizar cualquiera de las funciones o macros de AVIFile.</span><span class="sxs-lookup"><span data-stu-id="c4d1b-114">After you initialize the library, you can use any of the AVIFile functions or macros.</span></span> <span data-ttu-id="c4d1b-115">Para liberar la biblioteca, utilice la función [**AVIFileExit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit) .</span><span class="sxs-lookup"><span data-stu-id="c4d1b-115">To release the library, use the [**AVIFileExit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit) function.</span></span> <span data-ttu-id="c4d1b-116">AVIFile mantiene un recuento de referencias de las aplicaciones que usan la biblioteca, pero no las que la han liberado.</span><span class="sxs-lookup"><span data-stu-id="c4d1b-116">AVIFile maintains a reference count of the applications that are using the library, but not those that have released it.</span></span> <span data-ttu-id="c4d1b-117">Las aplicaciones deben equilibrar cada uso de **AVIFileInit** con una llamada a **AVIFileExit** para liberar por completo la biblioteca después de que cada aplicación termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="c4d1b-117">Your applications should balance each use of **AVIFileInit** with a call to **AVIFileExit** to completely release the library after each application finishes using it.</span></span>

 

 





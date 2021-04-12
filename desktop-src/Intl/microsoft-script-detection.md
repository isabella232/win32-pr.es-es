---
description: El servicio de detección de scripts de ELS se denomina detección de scripts de Microsoft.
ms.assetid: daf9f549-1eff-4666-b777-227ec31fba30
title: Detección de scripts de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd38b36cb409c1f03d84b9fc21f2fe4439b8152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155157"
---
# <a name="microsoft-script-detection"></a><span data-ttu-id="46437-103">Detección de scripts de Microsoft</span><span class="sxs-lookup"><span data-stu-id="46437-103">Microsoft Script Detection</span></span>

<span data-ttu-id="46437-104">El servicio de detección de scripts de ELS se denomina detección de scripts de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="46437-104">The ELS script detection service is called Microsoft Script Detection.</span></span> <span data-ttu-id="46437-105">Este servicio permite que las aplicaciones detecten los scripts en los que se escribe el texto.</span><span class="sxs-lookup"><span data-stu-id="46437-105">This service allows applications to detect the scripts in which text is written.</span></span> <span data-ttu-id="46437-106">El homólogo National Language support (NLS) de un servicio de detección de scripts es la función [GetStringScripts](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) .</span><span class="sxs-lookup"><span data-stu-id="46437-106">The National Language Support (NLS) counterpart of a script detection service is the [GetStringScripts](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) function.</span></span> <span data-ttu-id="46437-107">Sin embargo, el servicio ELS también recupera los intervalos de texto que pertenecen a cada sistema de escritura.</span><span class="sxs-lookup"><span data-stu-id="46437-107">However, the ELS service additionally retrieves the text ranges that belong to each writing system.</span></span>

## <a name="input-to-microsoft-script-detection"></a><span data-ttu-id="46437-108">Entrada para la detección de scripts de Microsoft</span><span class="sxs-lookup"><span data-stu-id="46437-108">Input to Microsoft Script Detection</span></span>

<span data-ttu-id="46437-109">La entrada del servicio de detección de scripts de Microsoft es texto UTF-16 para el que el servicio determina los intervalos de scripts.</span><span class="sxs-lookup"><span data-stu-id="46437-109">The input to the Microsoft Script Detection service is UTF-16 text for which the service determines script ranges.</span></span>

## <a name="output-of-microsoft-script-detection"></a><span data-ttu-id="46437-110">Salida de la detección de scripts de Microsoft</span><span class="sxs-lookup"><span data-stu-id="46437-110">Output of Microsoft Script Detection</span></span>

<span data-ttu-id="46437-111">La salida del servicio de detección de scripts de Microsoft es una matriz de intervalos, cada uno de los cuales contiene una cadena UTF-16 terminada en NULL con el nombre especificado por Unicode del sistema de escritura asociado.</span><span class="sxs-lookup"><span data-stu-id="46437-111">The output of the Microsoft Script Detection service is an array of ranges, each containing a null-terminated UTF-16 string with the Unicode-specified name of the associated writing system.</span></span> <span data-ttu-id="46437-112">El servicio informa de los caracteres comunes normales (Zyyy) y heredados (Qaai) como pertenecientes al intervalo de scripts anterior.</span><span class="sxs-lookup"><span data-stu-id="46437-112">The service reports regular common (Zyyy) and inherited (Qaai) characters as belonging to the previous script range.</span></span> <span data-ttu-id="46437-113">Los caracteres comunes y heredados iniciales se indican como pertenecientes al siguiente intervalo de script.</span><span class="sxs-lookup"><span data-stu-id="46437-113">Beginning common and inherited characters are reported as belonging to the next script range.</span></span> <span data-ttu-id="46437-114">Si todos los caracteres del texto de entrada son comunes o se heredan, la salida del servicio es un intervalo único con la cadena vacía como datos.</span><span class="sxs-lookup"><span data-stu-id="46437-114">If all the characters in the input text are common or inherited, the output of the service is a single range with the empty string as its data.</span></span>

## <a name="microsoft-script-detection-operation"></a><span data-ttu-id="46437-115">Operación de detección de scripts de Microsoft</span><span class="sxs-lookup"><span data-stu-id="46437-115">Microsoft Script Detection Operation</span></span>

<span data-ttu-id="46437-116">El servicio de detección de scripts de Microsoft asigna los puntos de código que pertenecen al intervalo común al sistema de escritura anterior.</span><span class="sxs-lookup"><span data-stu-id="46437-116">The Microsoft Script Detection service maps the code points belonging to the common range to the preceding writing system.</span></span> <span data-ttu-id="46437-117">Como alternativa, el servicio puede asignar los puntos de código al siguiente sistema de escritura si los puntos de código están al principio de la cadena de entrada.</span><span class="sxs-lookup"><span data-stu-id="46437-117">Alternatively, the service can map the code points to the next writing system if the code points are at the beginning of the input string.</span></span> <span data-ttu-id="46437-118">La aplicación no tiene que tratar con el intervalo común.</span><span class="sxs-lookup"><span data-stu-id="46437-118">The application does not have to deal with the common range at all.</span></span>

## <a name="microsoft-script-detection-guid"></a><span data-ttu-id="46437-119">GUID de detección de scripts de Microsoft</span><span class="sxs-lookup"><span data-stu-id="46437-119">Microsoft Script Detection GUID</span></span>

<span data-ttu-id="46437-120">El GUID del servicio Microsoft Detección de idioma se declara en Elssrvc. h, tal como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="46437-120">The GUID for the Microsoft Language Detection service is declared in Elssrvc.h, as shown in the following code.</span></span>


```C++
// {2D64B439-6CAF-4f6b-B688-E5D0F4FAA7D7}
static const GUID ELS_GUID_SCRIPT_DETECTION =
    { 0x2D64B439, 0x6CAF, 0x4F6B, { 0xB6, 0x88, 0xE5, 0xD0, 0xF4, 0xFA, 0xA7, 0xD7 } };
```



## <a name="related-topics"></a><span data-ttu-id="46437-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="46437-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46437-122">Acerca de los servicios lingüísticos extendidos</span><span class="sxs-lookup"><span data-stu-id="46437-122">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 




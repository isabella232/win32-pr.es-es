---
description: Usar las clases base de DirectShow
ms.assetid: 7eab0e55-1566-4b4c-b37c-32c5a1f37363
title: Usar las clases base de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 870c910505d6df42d0b9a6094470bf803b83d6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277589"
---
# <a name="using-the-directshow-base-classes"></a><span data-ttu-id="dd2eb-103">Usar las clases base de DirectShow</span><span class="sxs-lookup"><span data-stu-id="dd2eb-103">Using the DirectShow Base Classes</span></span>

<span data-ttu-id="dd2eb-104">Para usar las clases base en DirectShow, debe compilar y vincular la biblioteca de clases base.</span><span class="sxs-lookup"><span data-stu-id="dd2eb-104">To use the base classes in DirectShow, you must build and link the base class library.</span></span>

<span data-ttu-id="dd2eb-105">La biblioteca de clases base se proporciona como un ejemplo de SDK en el kit de desarrollo de software (SDK) de Microsoft Windows ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ).</span><span class="sxs-lookup"><span data-stu-id="dd2eb-105">The base class library is provided as a SDK sample in the Microsoft Windows Software Development Kit (SDK) (<https://go.microsoft.com/fwlink/p/?linkid=62332>).</span></span> <span data-ttu-id="dd2eb-106">La ubicación exacta depende de la versión del SDK que haya instalado, pero la ruta de acceso relativa es:</span><span class="sxs-lookup"><span data-stu-id="dd2eb-106">The exact location depends on the version of the SDK that you have installed, but the relative path is:</span></span>

<span data-ttu-id="dd2eb-107">*(Ejemplos del SDK raíz)* \\ BaseClasses de DirectShow \\</span><span class="sxs-lookup"><span data-stu-id="dd2eb-107">*(SDK samples root)*\\DirectShow\\BaseClasses</span></span>

<span data-ttu-id="dd2eb-108">Encabezado: streams. h</span><span class="sxs-lookup"><span data-stu-id="dd2eb-108">Header: Streams.h</span></span>

<span data-ttu-id="dd2eb-109">Biblioteca: el ejemplo genera versiones comercial y de depuración de la biblioteca:</span><span class="sxs-lookup"><span data-stu-id="dd2eb-109">Library: The sample builds retail and debug versions of the library:</span></span>

-   <span data-ttu-id="dd2eb-110">Versión comercial: Strmbase. lib</span><span class="sxs-lookup"><span data-stu-id="dd2eb-110">Retail version: Strmbase.lib</span></span>
-   <span data-ttu-id="dd2eb-111">Versión de depuración: Strmbasd. lib.</span><span class="sxs-lookup"><span data-stu-id="dd2eb-111">Debug version: Strmbasd.lib.</span></span>

<span data-ttu-id="dd2eb-112">Para obtener más información sobre cómo configurar el entorno de compilación, vea [configurar el entorno de compilación](setting-up-the-build-environment.md).</span><span class="sxs-lookup"><span data-stu-id="dd2eb-112">For more information on setting up your build environment, see [Setting Up the Build Environment](setting-up-the-build-environment.md).</span></span>

## <a name="preprocessor-symbols"></a><span data-ttu-id="dd2eb-113">Símbolos de preprocesador</span><span class="sxs-lookup"><span data-stu-id="dd2eb-113">Preprocessor Symbols</span></span>

<span data-ttu-id="dd2eb-114">Cuando se incluye el archivo de encabezado streams. h, los siguientes símbolos de preprocesador tienen un significado especial:</span><span class="sxs-lookup"><span data-stu-id="dd2eb-114">When you include the header file Streams.h, the following preprocessor symbols have special meaning:</span></span>

-   <span data-ttu-id="dd2eb-115">RENDIMIENTO: reservado.</span><span class="sxs-lookup"><span data-stu-id="dd2eb-115">PERF: Reserved.</span></span> <span data-ttu-id="dd2eb-116">No utilice este símbolo de preprocesador.</span><span class="sxs-lookup"><span data-stu-id="dd2eb-116">Do not use this preprocessor symbol.</span></span>
-   <span data-ttu-id="dd2eb-117">VFWROBUST: habilita la validación de puntero en la versión comercial.</span><span class="sxs-lookup"><span data-stu-id="dd2eb-117">VFWROBUST: Enables pointer validation in retail.</span></span> <span data-ttu-id="dd2eb-118">Para obtener más información, vea [macros de validación de punteros](pointer-validation-macros.md).</span><span class="sxs-lookup"><span data-stu-id="dd2eb-118">For more information, see [Pointer Validation Macros](pointer-validation-macros.md).</span></span> <span data-ttu-id="dd2eb-119">En las compilaciones de depuración, no es necesario definir VFWROBUST.</span><span class="sxs-lookup"><span data-stu-id="dd2eb-119">In debug builds, it is not necessary to define VFWROBUST.</span></span>

> [!Note]  
> <span data-ttu-id="dd2eb-120">En Windows Vista y versiones posteriores, las macros de validación de puntero están vacías.</span><span class="sxs-lookup"><span data-stu-id="dd2eb-120">In Windows Vista and later, the pointer validation macros are empty.</span></span>

 

 

 




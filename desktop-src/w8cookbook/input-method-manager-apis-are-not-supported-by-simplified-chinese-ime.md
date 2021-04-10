---
title: El IME de chino simplificado no admite las API del administrador de métodos de entrada
description: El IME de chino simplificado no admite las API del administrador de métodos de entrada
ms.assetid: 829E1920-8A5C-4DBB-A844-72DA75D58B92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d01d79d569ee7c72508bc217b68bcdf784f0d61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149404"
---
# <a name="input-method-manager-apis-are-not-supported-by-simplified-chinese-ime"></a><span data-ttu-id="c2908-103">El IME de chino simplificado no admite las API del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="c2908-103">Input Method manager APIs are not supported by Simplified Chinese IME</span></span>

## <a name="platforms"></a><span data-ttu-id="c2908-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="c2908-104">Platforms</span></span>

<dl> <span data-ttu-id="c2908-105">Clientes-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c2908-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="c2908-106">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c2908-106">Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="c2908-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2908-107">Description</span></span>

<span data-ttu-id="c2908-108">Las siguientes API del administrador de métodos de entrada no son compatibles con los IME de chino simplificado en Windows 8.1:</span><span class="sxs-lookup"><span data-stu-id="c2908-108">The following input method manager APIs are not supported by Simplified Chinese IMEs in Windows 8.1:</span></span>

-   <span data-ttu-id="c2908-109">Interfaz IFECommon</span><span class="sxs-lookup"><span data-stu-id="c2908-109">IFECommon interface</span></span>
-   <span data-ttu-id="c2908-110">Interfaz IFEDictionary</span><span class="sxs-lookup"><span data-stu-id="c2908-110">IFEDictionary interface</span></span>
-   <span data-ttu-id="c2908-111">Interfaz IFELanguage</span><span class="sxs-lookup"><span data-stu-id="c2908-111">IFELanguage interface</span></span>
-   <span data-ttu-id="c2908-112">Interfaz IImePad</span><span class="sxs-lookup"><span data-stu-id="c2908-112">IImePad interface</span></span>
-   <span data-ttu-id="c2908-113">Interfaz IImePadApplet</span><span class="sxs-lookup"><span data-stu-id="c2908-113">IImePadApplet interface</span></span>
-   <span data-ttu-id="c2908-114">Interfaz IImeSpecifyApplets</span><span class="sxs-lookup"><span data-stu-id="c2908-114">IImeSpecifyApplets interface</span></span>

## <a name="manifestations"></a><span data-ttu-id="c2908-115">Manifestaciones</span><span class="sxs-lookup"><span data-stu-id="c2908-115">Manifestations</span></span>

<span data-ttu-id="c2908-116">Las funciones que usan esas API no funcionan con el IME de chino simplificado.</span><span class="sxs-lookup"><span data-stu-id="c2908-116">The functions that use those APIs don’t work with Simplified Chinese IME.</span></span>

## <a name="solution"></a><span data-ttu-id="c2908-117">Solución</span><span class="sxs-lookup"><span data-stu-id="c2908-117">Solution</span></span>

<span data-ttu-id="c2908-118">Las aplicaciones deben diseñarse para que los usuarios puedan completar la tarea deseada sin usar la API especificada.</span><span class="sxs-lookup"><span data-stu-id="c2908-118">Applications must be designed so that users can complete the desired task without using the specified API.</span></span>

## <a name="resources"></a><span data-ttu-id="c2908-119">Recursos</span><span class="sxs-lookup"><span data-stu-id="c2908-119">Resources</span></span>

-   [<span data-ttu-id="c2908-120">Interfaces del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="c2908-120">Input Method Manager Interfaces</span></span>](../intl/input-method-manager-interfaces.md)
-   [<span data-ttu-id="c2908-121">IFECommon</span><span class="sxs-lookup"><span data-stu-id="c2908-121">IFECommon</span></span>](/windows/win32/api/msime/nn-msime-ifecommon)
-   [<span data-ttu-id="c2908-122">Interfaz IFECommon</span><span class="sxs-lookup"><span data-stu-id="c2908-122">IFECommon interface</span></span>](/windows/win32/api/msime/nn-msime-ifecommon)
-   [<span data-ttu-id="c2908-123">Interfaz IFEDictionary</span><span class="sxs-lookup"><span data-stu-id="c2908-123">IFEDictionary interface</span></span>](/windows/win32/api/msime/nn-msime-ifedictionary)
-   [<span data-ttu-id="c2908-124">IFELanguage</span><span class="sxs-lookup"><span data-stu-id="c2908-124">IFELanguage</span></span>](/windows/win32/api/msime/nn-msime-ifelanguage)
-   [<span data-ttu-id="c2908-125">IImePad</span><span class="sxs-lookup"><span data-stu-id="c2908-125">IImePad</span></span>](/windows/win32/api/imepad/nn-imepad-iimepad)
-   [<span data-ttu-id="c2908-126">IImePadApplet</span><span class="sxs-lookup"><span data-stu-id="c2908-126">IImePadApplet</span></span>](/windows/win32/api/imepad/nn-imepad-iimepadapplet)
-   [<span data-ttu-id="c2908-127">IimePlugInDictDictionaryList</span><span class="sxs-lookup"><span data-stu-id="c2908-127">IimePlugInDictDictionaryList</span></span>](/windows/win32/api/msimeapi/nn-msimeapi-iimeplugindictdictionarylist)
-   [<span data-ttu-id="c2908-128">IImeSpecifyApplets</span><span class="sxs-lookup"><span data-stu-id="c2908-128">IImeSpecifyApplets</span></span>](/windows/win32/api/imepad/nn-imepad-iimespecifyapplets)

 

 
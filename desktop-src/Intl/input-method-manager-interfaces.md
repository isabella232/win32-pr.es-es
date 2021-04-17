---
description: En esta sección se describen las interfaces de IMM.
ms.assetid: 25092F1D-0B54-4E5E-AC9E-F8F3A0181482
title: Interfaces del administrador de métodos de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bd04c02425aef19ed329867a5b228bd4838af8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687614"
---
# <a name="input-method-manager-interfaces"></a><span data-ttu-id="0e18f-103">Interfaces del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="0e18f-103">Input Method Manager Interfaces</span></span>

<span data-ttu-id="0e18f-104">En esta sección se describen las interfaces de IMM.</span><span class="sxs-lookup"><span data-stu-id="0e18f-104">This section describes the IMM interfaces.</span></span>



| <span data-ttu-id="0e18f-105">Interfaz</span><span class="sxs-lookup"><span data-stu-id="0e18f-105">Interface</span></span>                                                            | <span data-ttu-id="0e18f-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e18f-106">Description</span></span>                                                                                                                                    |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e18f-107">**IFECommon**</span><span class="sxs-lookup"><span data-stu-id="0e18f-107">**IFECommon**</span></span>](/windows/desktop/api/Msime/nn-msime-ifecommon)                                       | <span data-ttu-id="0e18f-108">Proporciona servicios relacionados con el IME que son comunes para distintos idiomas.</span><span class="sxs-lookup"><span data-stu-id="0e18f-108">Provides IME-related services that are common for different languages.</span></span>                                                                         |
| [<span data-ttu-id="0e18f-109">**IFEDictionary**</span><span class="sxs-lookup"><span data-stu-id="0e18f-109">**IFEDictionary**</span></span>](/windows/desktop/api/Msime/nn-msime-ifedictionary)                               | <span data-ttu-id="0e18f-110">Permite a los clientes tener acceso a un diccionario de usuario IME de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0e18f-110">Allows clients to access a Microsoft IME user dictionary.</span></span>                                                                                      |
| [<span data-ttu-id="0e18f-111">**IFELanguage**</span><span class="sxs-lookup"><span data-stu-id="0e18f-111">**IFELanguage**</span></span>](/windows/desktop/api/Msime/nn-msime-ifelanguage)                                   | <span data-ttu-id="0e18f-112">Proporciona servicios de procesamiento de lenguajes mediante Microsoft IME.</span><span class="sxs-lookup"><span data-stu-id="0e18f-112">Provides language processing services using the Microsoft IME.</span></span>                                                                                 |
| [<span data-ttu-id="0e18f-113">**IImePad**</span><span class="sxs-lookup"><span data-stu-id="0e18f-113">**IImePad**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimepad)                                           | <span data-ttu-id="0e18f-114">Inserta texto en las aplicaciones de IMEPadApplets que implementan la interfaz [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) .</span><span class="sxs-lookup"><span data-stu-id="0e18f-114">Inserts text into apps from IMEPadApplets that implement the [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) interface.</span></span>                                 |
| [<span data-ttu-id="0e18f-115">**IImePadApplet**</span><span class="sxs-lookup"><span data-stu-id="0e18f-115">**IImePadApplet**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet)                               | <span data-ttu-id="0e18f-116">Introduce cadenas en aplicaciones a través de la interfaz [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) .</span><span class="sxs-lookup"><span data-stu-id="0e18f-116">Inputs strings into apps through the [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) interface.</span></span>                                                                     |
| [<span data-ttu-id="0e18f-117">**IImePlugInDictDictionaryList**</span><span class="sxs-lookup"><span data-stu-id="0e18f-117">**IImePlugInDictDictionaryList**</span></span>](/windows/desktop/api/Msimeapi/nn-msimeapi-iimeplugindictdictionarylist) | <span data-ttu-id="0e18f-118">Proporciona acceso a la lista de diccionarios de complemento IME.</span><span class="sxs-lookup"><span data-stu-id="0e18f-118">Provides access to the list of IME plug-in dictionaries.</span></span>                                                                                       |
| [<span data-ttu-id="0e18f-119">**IImeSpecifyApplets**</span><span class="sxs-lookup"><span data-stu-id="0e18f-119">**IImeSpecifyApplets**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimespecifyapplets)                     | <span data-ttu-id="0e18f-120">Especifica los métodos llamados desde el objeto de interfaz [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) para emular la interfaz [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) .</span><span class="sxs-lookup"><span data-stu-id="0e18f-120">Specifies methods called from the [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) interface object to emulate the [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) interface.</span></span> |



 

 

 




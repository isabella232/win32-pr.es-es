---
description: Puede escribir módulos de directivas en el lenguaje de programación C, C++ o Visual Basic.
ms.assetid: 37a93c67-02f2-4c4e-a000-2bb98e0ca948
title: Escribir módulos personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92247cd6b975bac520032dcc3aada1328f7b6c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002079"
---
# <a name="writing-custom-modules"></a><span data-ttu-id="60fe5-103">Escribir módulos personalizados</span><span class="sxs-lookup"><span data-stu-id="60fe5-103">Writing Custom Modules</span></span>

<span data-ttu-id="60fe5-104">Puede escribir módulos de directivas en el lenguaje de programación C, C++ o Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="60fe5-104">You can write policy modules in the C, C++, or Visual Basic programming language.</span></span> <span data-ttu-id="60fe5-105">El compilador de Microsoft necesario está disponible en Visual C++ versión 5,0 o posterior, o en Visual Basic versión 5,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="60fe5-105">The required Microsoft compiler is available in Visual C++ version 5.0 or later or in Visual Basic version 5.0 or later.</span></span> <span data-ttu-id="60fe5-106">Una [*entidad de certificación*](../secgloss/c-gly.md) (CA) empresarial solo debe usar el módulo de directivas empresariales proporcionado por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="60fe5-106">An enterprise [*certification authority*](../secgloss/c-gly.md) (CA) should use only the Microsoft-provided enterprise policy module.</span></span>

<span data-ttu-id="60fe5-107">Debe implementar [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) al escribir un módulo de directivas personalizado.</span><span class="sxs-lookup"><span data-stu-id="60fe5-107">You must implement [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) when writing a custom policy module.</span></span> <span data-ttu-id="60fe5-108">Además, debe implementar [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) al escribir un módulo de directivas personalizado.</span><span class="sxs-lookup"><span data-stu-id="60fe5-108">Additionally, you must implement [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) when writing a custom policy module.</span></span>

<span data-ttu-id="60fe5-109">Los módulos de directivas pueden llamar a métodos desde [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) para ayudar en el procesamiento de una [*solicitud de certificado*](../secgloss/c-gly.md). **ICertServerPolicy** permite establecer y recuperar propiedades y extensiones de certificado.</span><span class="sxs-lookup"><span data-stu-id="60fe5-109">Policy modules can call methods from [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) to assist in the processing of a [*certificate request*](../secgloss/c-gly.md); **ICertServerPolicy** allows properties and certificate extensions to be set and retrieved.</span></span>

<span data-ttu-id="60fe5-110">Para obtener más información, vea los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="60fe5-110">For more information, see the following topics.</span></span>



| <span data-ttu-id="60fe5-111">Tema</span><span class="sxs-lookup"><span data-stu-id="60fe5-111">Topic</span></span>                                                                      | <span data-ttu-id="60fe5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="60fe5-112">Description</span></span>                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="60fe5-113">Establecer propiedades de certificado</span><span class="sxs-lookup"><span data-stu-id="60fe5-113">Setting Certificate Properties</span></span>](setting-certificate-properties.md)       | <span data-ttu-id="60fe5-114">Establecer las propiedades de un certificado</span><span class="sxs-lookup"><span data-stu-id="60fe5-114">Setting the properties of a certificate</span></span> |
| [<span data-ttu-id="60fe5-115">Escribir módulos de salida personalizados</span><span class="sxs-lookup"><span data-stu-id="60fe5-115">Writing Custom Exit Modules</span></span>](writing-custom-exit-modules.md)             | <span data-ttu-id="60fe5-116">Escribir módulos de salida personalizados</span><span class="sxs-lookup"><span data-stu-id="60fe5-116">Writing custom exit modules</span></span>             |
| [<span data-ttu-id="60fe5-117">Escribir controladores de extensión personalizados</span><span class="sxs-lookup"><span data-stu-id="60fe5-117">Writing Custom Extension Handlers</span></span>](writing-custom-extension-handlers.md) | <span data-ttu-id="60fe5-118">Escribir controladores de extensión personalizados</span><span class="sxs-lookup"><span data-stu-id="60fe5-118">Writing custom extension handlers</span></span>       |



 

 

 

---
description: En este tema se proporciona información sobre las consideraciones de seguridad relacionadas con GDI. En este tema no se proporciona todo lo que necesita saber acerca de los problemas de seguridad. En su lugar, úselo como punto de partida y referencia para esta área tecnológica.
ms.assetid: 374e3ac7-f635-47f1-a72a-14e1be85c795
title: 'Consideraciones de seguridad: GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71644da7d313e2efe0f287002c3e41a3a813a733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002409"
---
# <a name="security-considerations-gdi"></a><span data-ttu-id="1478a-105">Consideraciones de seguridad: GDI</span><span class="sxs-lookup"><span data-stu-id="1478a-105">Security Considerations: GDI</span></span>

<span data-ttu-id="1478a-106">En este tema se proporciona información sobre las consideraciones de seguridad relacionadas con GDI.</span><span class="sxs-lookup"><span data-stu-id="1478a-106">This topic provides information about security considerations related to GDI.</span></span> <span data-ttu-id="1478a-107">En este tema no se proporciona todo lo que necesita saber acerca de los problemas de seguridad.</span><span class="sxs-lookup"><span data-stu-id="1478a-107">This topic does not provide all you need to know about security issues.</span></span> <span data-ttu-id="1478a-108">En su lugar, úselo como punto de partida y referencia para esta área tecnológica.</span><span class="sxs-lookup"><span data-stu-id="1478a-108">Instead, use it as a starting point and reference for this technology area.</span></span>

<span data-ttu-id="1478a-109">GDI generalmente tiene pocos problemas de seguridad, ya que se ocupa de mostrar en lugar de la entrada.</span><span class="sxs-lookup"><span data-stu-id="1478a-109">GDI generally has few security concerns because it deals with display rather than input.</span></span> <span data-ttu-id="1478a-110">Sin embargo, estos son algunos de los problemas que debe tener en cuenta.</span><span class="sxs-lookup"><span data-stu-id="1478a-110">However, here are a few issues that you should consider.</span></span>

<span data-ttu-id="1478a-111">Los mapas de bits, los metaarchivos y las fuentes son estructuras complejas que podrían resultar dañados.</span><span class="sxs-lookup"><span data-stu-id="1478a-111">Bitmaps, metafiles, and fonts are complex structures that could become corrupted.</span></span> <span data-ttu-id="1478a-112">Es recomendable intentar asegurarse de que estos elementos no estén dañados y de un origen de confianza.</span><span class="sxs-lookup"><span data-stu-id="1478a-112">It is good practice to try to ensure that these items are uncorrupted and from a trustworthy source.</span></span>

<span data-ttu-id="1478a-113">Una aplicación puede especificar el descriptor de seguridad para algunas de las API de impresión y puesta en cola.</span><span class="sxs-lookup"><span data-stu-id="1478a-113">An application can specify the security descriptor for some of the printing and spooling APIs.</span></span> <span data-ttu-id="1478a-114">Debe tener cuidado al establecer el descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="1478a-114">You should take care when setting the security descriptor.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1478a-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1478a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1478a-116">Centro de seguridad de Microsoft</span><span class="sxs-lookup"><span data-stu-id="1478a-116">Microsoft Security Central</span></span>](https://www.microsoft.com/security/)
</dt> <dt>

[<span data-ttu-id="1478a-117">Centro para desarrolladores de seguridad</span><span class="sxs-lookup"><span data-stu-id="1478a-117">Security Developer Center</span></span>](https://technet.microsoft.com/security/)
</dt> <dt>

[<span data-ttu-id="1478a-118">TechCenter de seguridad</span><span class="sxs-lookup"><span data-stu-id="1478a-118">Security TechCenter</span></span>](https://technet.microsoft.com/security/default.aspx)
</dt> </dl>

 

 




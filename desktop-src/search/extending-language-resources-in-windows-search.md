---
description: Windows Search usa recursos de idioma como los separadores de palabras y lematizadores para dividir el texto en su configuración regional nativa durante la creación de índices y el procesamiento de consultas.
ms.assetid: 6e8ab091-c22c-4425-b8b9-211d53816304
title: Extensión de recursos de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727f5812d0aee370c96d98f1c57dfffcbea5bc8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714998"
---
# <a name="extending-language-resources"></a><span data-ttu-id="f01e6-103">Extensión de recursos de idioma</span><span class="sxs-lookup"><span data-stu-id="f01e6-103">Extending Language Resources</span></span>

<span data-ttu-id="f01e6-104">Windows Search usa recursos de idioma como los separadores de palabras y lematizadores para dividir el texto en su configuración regional nativa durante la creación de índices y el procesamiento de consultas.</span><span class="sxs-lookup"><span data-stu-id="f01e6-104">Windows Search uses language resources such as word breakers and stemmers to break text in its native locale during index creation and query processing.</span></span> <span data-ttu-id="f01e6-105">Microsoft proporciona separadores de palabras y lematizadores para varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="f01e6-105">Microsoft provides word breakers and stemmers for several languages.</span></span> <span data-ttu-id="f01e6-106">En esta sección se describe cómo implementar y usar separadores de palabras y lematizadores personalizados para idiomas y configuraciones regionales más allá de los proporcionados por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f01e6-106">This section describes how to implement and use custom word breakers and stemmers for languages and locales beyond those provided by Microsoft.</span></span>

-   [<span data-ttu-id="f01e6-107">Descripción de los componentes de recursos de lenguaje</span><span class="sxs-lookup"><span data-stu-id="f01e6-107">Understanding Language Resource Components</span></span>](understanding-language-resource-components.md)
-   [<span data-ttu-id="f01e6-108">Implementar un separador de palabras y un analizador lingüístico</span><span class="sxs-lookup"><span data-stu-id="f01e6-108">Implementing a Word Breaker and Stemmer</span></span>](implementing-a-word-breaker-and-stemmer.md)
-   [<span data-ttu-id="f01e6-109">Consideraciones lingüísticas y Unicode</span><span class="sxs-lookup"><span data-stu-id="f01e6-109">Linguistic and Unicode Considerations</span></span>](linguistic-and-unicode-considerations.md)
-   [<span data-ttu-id="f01e6-110">Solución de problemas de recursos de lenguaje y procedimientos recomendados</span><span class="sxs-lookup"><span data-stu-id="f01e6-110">Troubleshooting Language Resources and Best Practices</span></span>](troubleshooting-language-resources.md)

## <a name="additional-resources"></a><span data-ttu-id="f01e6-111">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f01e6-111">Additional Resources</span></span>

-   <span data-ttu-id="f01e6-112">Para obtener una lista de lanuages compatibles con los separadores de palabras, consulte [idiomas compatibles con Windows Search](-search-3x-wds-language-support.md).</span><span class="sxs-lookup"><span data-stu-id="f01e6-112">For a list of lanuages supported by word breakers, see [Languages Supported by Windows Search](-search-3x-wds-language-support.md).</span></span>
-   <span data-ttu-id="f01e6-113">Si necesita identificar el idioma de un fragmento de texto, puede usar la detección automática de idioma (LAD), que está disponible en Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f01e6-113">If you need to identify the language of a piece of text, you can use Language Auto-Detection (LAD), which is available in Windows 7 and later.</span></span> <span data-ttu-id="f01e6-114">Para obtener más información, vea [servicios lingüísticos extendidos](../intl/extended-linguistic-services.md) (Els).</span><span class="sxs-lookup"><span data-stu-id="f01e6-114">For more information, see [Extended Linguistic Services](../intl/extended-linguistic-services.md) (ELS).</span></span>
-   <span data-ttu-id="f01e6-115">Para obtener documentación de referencia aplicable, vea [interfaces de complementos de datos](-search-data-addins-interfaces-entry-page.md).</span><span class="sxs-lookup"><span data-stu-id="f01e6-115">For applicable reference documentation, see [Data Add-in Interfaces](-search-data-addins-interfaces-entry-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f01e6-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f01e6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f01e6-117">Administración del índice</span><span class="sxs-lookup"><span data-stu-id="f01e6-117">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[<span data-ttu-id="f01e6-118">Consulta del índice mediante programación</span><span class="sxs-lookup"><span data-stu-id="f01e6-118">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="f01e6-119">Extender el índice</span><span class="sxs-lookup"><span data-stu-id="f01e6-119">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 

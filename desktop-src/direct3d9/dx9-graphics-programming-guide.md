---
description: Esta guía contiene una descripción de la canalización de gráficos implementada por Microsoft Direct3D.
ms.assetid: 54c5f8de-a976-4a82-9a23-a7f6cffef5e1
title: Guía de programación para Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be451422cca297b08f22f1a0eee19e4a1934187
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495305"
---
# <a name="programming-guide-for-direct3d-9"></a><span data-ttu-id="3cf6c-103">Guía de programación para Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="3cf6c-103">Programming Guide for Direct3D 9</span></span>

<span data-ttu-id="3cf6c-104">Esta guía contiene una descripción de la canalización de gráficos implementada por Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3cf6c-104">This guide contains a description of the graphics pipeline implemented by Microsoft Direct3D.</span></span> <span data-ttu-id="3cf6c-105">Es una guía para los desarrolladores que implementan la funcionalidad de gráficos de Direct3D en sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="3cf6c-105">It is a guide for developers who implement Direct3D graphics functionality into their applications.</span></span> <span data-ttu-id="3cf6c-106">La guía contiene descripciones de arquitectura, diagramas de bloques funcionales y descripciones de los bloques de creación de la canalización, así como fragmentos de código y aplicaciones de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3cf6c-106">The guide contains architecture descriptions, functional block diagrams, and descriptions of the building blocks in the pipeline, as well as code snippets and sample applications.</span></span> <span data-ttu-id="3cf6c-107">La información se divide en las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="3cf6c-107">The information is divided into the following sections:</span></span>

-   <span data-ttu-id="3cf6c-108">[Introducción](getting-started.md) : esta sección contiene información general de la canalización y los tutoriales que pueden ayudarle a obtener una aplicación gráfica sencilla que se ejecuta en unos minutos.</span><span class="sxs-lookup"><span data-stu-id="3cf6c-108">[Getting Started](getting-started.md) - This section contains both an overview of the pipeline and tutorials that can help you get a simple graphics application running in a few minutes.</span></span>
-   <span data-ttu-id="3cf6c-109">[Efectos](effects.md) : en esta sección se tratan los efectos y los archivos de efecto para compilar aplicaciones que se pueden ejecutar en una variedad de plataformas de hardware.</span><span class="sxs-lookup"><span data-stu-id="3cf6c-109">[Effects](effects.md) - This section covers effects and effect files for building applications that can run on a variety of hardware platforms.</span></span>
-   <span data-ttu-id="3cf6c-110">[Temas avanzados](advanced-topics.md) : esta sección contiene ejemplos de diferentes tipos de efectos especiales que se pueden implementar.</span><span class="sxs-lookup"><span data-stu-id="3cf6c-110">[Advanced Topics](advanced-topics.md) - This section contains examples of different types of special effects you can implement.</span></span> <span data-ttu-id="3cf6c-111">Los temas como el entorno y la asignación de rugosidad, el suavizado de contorno, la fusión de vértices, la intercalación, la iluminación de alto rango dinámico (HDR) y la transferencia de Radiance precalculada (PRT) muestran cómo aplicar efectos especiales de vanguardia a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3cf6c-111">Topics such as environment and bump mapping, antialiasing, vertex blending, tweening, high dynamic range (HDR) lighting, and precomputed radiance transfer (PRT) show how to apply leading-edge special effects to your application.</span></span>
-   <span data-ttu-id="3cf6c-112">[Sugerencias de programación](programming-tips.md) : esta sección contiene información para ayudarle a desarrollar aplicaciones de gráficos Direct3D de forma eficaz.</span><span class="sxs-lookup"><span data-stu-id="3cf6c-112">[Programming Tips](programming-tips.md) - This section contains information to help you develop Direct3D graphics applications efficiently.</span></span>

<span data-ttu-id="3cf6c-113">Para obtener más información sobre los métodos de API específicos, vea las páginas de [referencia](dx9-graphics-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="3cf6c-113">For more information about specific API methods, see the [Reference](dx9-graphics-reference.md) pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3cf6c-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3cf6c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cf6c-115">Gráficos de Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="3cf6c-115">Direct3D 9 Graphics</span></span>](dx9-graphics.md)
</dt> </dl>

 

 




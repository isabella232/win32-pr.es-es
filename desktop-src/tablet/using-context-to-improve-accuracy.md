---
description: Un motor de reconocimiento de escritura A mano, o reconocedor, es un software que procesa la entrada manuscrita y convierte la entrada manuscrita en texto.
ms.assetid: b64f6856-453c-4080-84e0-0a9e69e79de7
title: Usar el contexto para mejorar la precisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd5c807804c1855e0be56b09f08448e3dc2967d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666481"
---
# <a name="using-context-to-improve-accuracy"></a><span data-ttu-id="45178-103">Usar el contexto para mejorar la precisión</span><span class="sxs-lookup"><span data-stu-id="45178-103">Using Context to Improve Accuracy</span></span>

<span data-ttu-id="45178-104">Un motor de reconocimiento de escritura A mano, o reconocedor, es un software que procesa la entrada manuscrita y convierte la entrada manuscrita en texto.</span><span class="sxs-lookup"><span data-stu-id="45178-104">A handwriting recognition engine, or recognizer, is software that processes ink and converts that ink into text.</span></span> <span data-ttu-id="45178-105">Un contexto es relevante, información específica de la aplicación que se proporciona a un reconocedor para mejorar la precisión del reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="45178-105">A context is relevant, application-specific information that you provide to a recognizer to improve recognition accuracy.</span></span> <span data-ttu-id="45178-106">En otras palabras, el contexto es cualquier parte de la información sobre la entrada que ayuda al reconocedor en el procesamiento preciso de la tinta en un campo.</span><span class="sxs-lookup"><span data-stu-id="45178-106">In other words, context is any piece of information about input that aids the recognizer in accurately processing the ink in a field.</span></span>

<span data-ttu-id="45178-107">En esta sección se describen las distintas formas en las que puede aprovechar el contexto de la aplicación de Tablet PC y hacer hincapié en la técnica de programación preferida para las aplicaciones que no están habilitadas para tinta.</span><span class="sxs-lookup"><span data-stu-id="45178-107">This section describes the different ways you can take advantage of context in your Tablet PC application, placing emphasis on the preferred programmatic technique for applications that are not ink enabled.</span></span>

> [!Note]  
> <span data-ttu-id="45178-108">Hay lugares en las secciones de tecnología de Tablet PC del kit de desarrollo de software (SDK) de Windows Vista, donde se usa el término "contexto" en relación con el objeto [**RecognizerContext**](inkrecognizercontext-class.md) y sus propiedades [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) y [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) .</span><span class="sxs-lookup"><span data-stu-id="45178-108">There are places in the Tablet PC Technology sections of the Windows Vista Software Development Kit (SDK) where the term "context" is used in regard to the [**RecognizerContext**](inkrecognizercontext-class.md) object and its [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) and [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) properties.</span></span> <span data-ttu-id="45178-109">No confunda estos otros usos de "contexto" con la definición de esta sección.</span><span class="sxs-lookup"><span data-stu-id="45178-109">Do not confuse these other usages of "context" with the definition in this section.</span></span>

 

 

 




---
title: Barra de idioma (aplicaciones TSF)
description: Una aplicación no puede agregar elementos a la barra de idioma. solo un servicio de texto puede agregar elementos a la barra de idioma.
ms.assetid: facb0da1-3f80-4745-b021-c026e7e5356c
keywords:
- Marco de trabajo de servicios de texto (TSF), barra de idioma
- TSF (marco de trabajo de servicios de texto), barra de idioma
- Aplicaciones habilitadas para TSF, barra de idioma
- barra de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef227b29c8b481bfaefc4a218305ba8974fe54e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103904968"
---
# <a name="language-bar-tsf-applications"></a><span data-ttu-id="1bdd0-107">Barra de idioma (aplicaciones TSF)</span><span class="sxs-lookup"><span data-stu-id="1bdd0-107">Language Bar (TSF Applications)</span></span>

<span data-ttu-id="1bdd0-108">Una aplicación no puede agregar elementos a la barra de idioma. solo un servicio de texto puede agregar elementos a la barra de idioma.</span><span class="sxs-lookup"><span data-stu-id="1bdd0-108">An application cannot add items to the language bar; only a text service can add items to the language bar.</span></span> <span data-ttu-id="1bdd0-109">Una aplicación puede afectar al modo en que se muestran determinados elementos de la barra de idioma.</span><span class="sxs-lookup"><span data-stu-id="1bdd0-109">An application can affect how certain items on the language bar appear.</span></span>

<span data-ttu-id="1bdd0-110">El compartimiento de [ \_ \_ \_ DICTATIONSTAT del compartimiento de GUID](predefined-compartments.md) se usa para indicar el tipo de entrada de voz que la aplicación puede aceptar: entrada de texto directo (dictado) o comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="1bdd0-110">The [GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT](predefined-compartments.md) compartment is used to indicate the type of speech input that the application can accept: direct text input (dictation) and/or voice commands.</span></span> <span data-ttu-id="1bdd0-111">De forma predeterminada, el dictado está habilitado y el comando de voz está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="1bdd0-111">By default, dictation is enabled and voice command is disabled.</span></span> <span data-ttu-id="1bdd0-112">Si la aplicación puede aceptar comandos de voz, debe establecer el valor de [comandos de TF \_ \_ habilitado](speech-recognition-constants.md) en el compartimiento del compartimiento de GUID \_ \_ \_ DICTATIONSTAT.</span><span class="sxs-lookup"><span data-stu-id="1bdd0-112">If the application can accept voice commands, it should set the [TF\_COMMANDING\_ENABLED](speech-recognition-constants.md) value in the GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT compartment.</span></span> <span data-ttu-id="1bdd0-113">Si la aplicación puede aceptar el dictado, debe establecer el \_ \_ valor de TF dict Enabled en el compartimiento del compartimiento de GUID \_ \_ \_ DICTATIONSTAT.</span><span class="sxs-lookup"><span data-stu-id="1bdd0-113">If the application can accept dictation, it should set the TF\_DICTATION\_ENABLED value in the GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT compartment.</span></span> <span data-ttu-id="1bdd0-114">Los \_ comandos TF Dictation \_ on o TF \_ en el \_ valor de este compartimiento determinan qué modo (dictación o comando) de entrada de voz está actualmente en.</span><span class="sxs-lookup"><span data-stu-id="1bdd0-114">The TF\_DICTATION\_ON or TF\_COMMANDING\_ON value of this compartment determines which mode (dictation or command) speech input is currently in.</span></span>

<span data-ttu-id="1bdd0-115">Si la aplicación admite el almacenamiento persistente de datos de propiedades, debe establecer el compartimiento del [compartimiento de GUID \_ \_ PERSISTMENUENABLED](predefined-compartments.md) en un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="1bdd0-115">If the application supports persistent storage of property data, it should set the [GUID\_COMPARTMENT\_PERSISTMENUENABLED](predefined-compartments.md) compartment to a nonzero value.</span></span> <span data-ttu-id="1bdd0-116">Esto hace que el servicio de texto de voz habilite el elemento de menú **guardar datos de voz** .</span><span class="sxs-lookup"><span data-stu-id="1bdd0-116">This causes the speech text service to enable the **Save Speech Data** menu item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bdd0-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1bdd0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bdd0-118">Cómo configurar el marco de trabajo de servicios de texto</span><span class="sxs-lookup"><span data-stu-id="1bdd0-118">How To Set Up Text Services Framework</span></span>](how-to-set-up-tsf.md)
</dt> <dt>

[<span data-ttu-id="1bdd0-119">Barra de idioma (servicios de texto)</span><span class="sxs-lookup"><span data-stu-id="1bdd0-119">Language Bar (Text Services)</span></span>](language-bar.md)
</dt> </dl>

 

 





---
title: Diseño de animación
description: Diseño de animación
ms.assetid: 8812e4cc-9062-4c65-81ef-229bd29534cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7d6cf86cfe115ec209fb305f0ae017951bd7f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994109"
---
# <a name="animation-design"></a><span data-ttu-id="ed379-103">Diseño de animación</span><span class="sxs-lookup"><span data-stu-id="ed379-103">Animation Design</span></span>

<span data-ttu-id="ed379-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ed379-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

### <a name="image-design"></a><span data-ttu-id="ed379-105">Diseño de imagen</span><span class="sxs-lookup"><span data-stu-id="ed379-105">Image Design</span></span>

<span data-ttu-id="ed379-106">Use la paleta Microsoft Office al diseñar los caracteres para minimizar los posibles problemas de realización de la paleta.</span><span class="sxs-lookup"><span data-stu-id="ed379-106">Use the Microsoft Office Palette when designing your characters to minimize any potential palette realization issues.</span></span> <span data-ttu-id="ed379-107">Evite seleccionar un color de transparencia similar a los colores que usa en el documento.</span><span class="sxs-lookup"><span data-stu-id="ed379-107">Avoid selecting a transparency color that is similar to the colors that you use in your document.</span></span>

### <a name="sounds"></a><span data-ttu-id="ed379-108">Sonidos</span><span class="sxs-lookup"><span data-stu-id="ed379-108">Sounds</span></span>

<span data-ttu-id="ed379-109">El agente de Microsoft le permite reproducir sonidos en las animaciones.</span><span class="sxs-lookup"><span data-stu-id="ed379-109">Microsoft Agent enables you to play sounds in your animations.</span></span> <span data-ttu-id="ed379-110">Se recomienda no incluir sonidos para las animaciones **inactivas** .</span><span class="sxs-lookup"><span data-stu-id="ed379-110">We recommend you do not include sounds for your **Idle** animations.</span></span> <span data-ttu-id="ed379-111">Esto se debe a que no habrá un retraso en el medio de la animación, si el agente tiene que cargar el archivo DLL de multimedia del sistema.</span><span class="sxs-lookup"><span data-stu-id="ed379-111">This is so there won't be a delay in the middle of the animation, if Agent has to load the system multimedia DLL.</span></span>

### <a name="frame-size"></a><span data-ttu-id="ed379-112">Tamaño de marco</span><span class="sxs-lookup"><span data-stu-id="ed379-112">Frame Size</span></span>

<span data-ttu-id="ed379-113">Los asistentes de Office típicos son 123 x 93 píxeles.</span><span class="sxs-lookup"><span data-stu-id="ed379-113">Typical Office Assistants are 123 x 93 pixels.</span></span> <span data-ttu-id="ed379-114">Aunque puede crear caracteres de otros tamaños, se escalarán a 123 x 93 en la galería de asistentes.</span><span class="sxs-lookup"><span data-stu-id="ed379-114">While you can create characters of other sizes, they will be scaled to 123 x 93 in the Assistant Gallery.</span></span>

### <a name="frame-transition"></a><span data-ttu-id="ed379-115">Transición de fotogramas</span><span class="sxs-lookup"><span data-stu-id="ed379-115">Frame Transition</span></span>

<span data-ttu-id="ed379-116">Todas las animaciones, excepto **adiós**, **saludo**, **Mostrar** y **ocultar** , deben comenzar y finalizar con la animación RestPose.</span><span class="sxs-lookup"><span data-stu-id="ed379-116">All animations except for **Goodbye**, **Greeting**, **Show** and **Hide** should begin and end with the RestPose animation.</span></span> <span data-ttu-id="ed379-117">Microsoft Office no reproduce animaciones de **devolución** explícitas, por lo que no debe definirlas.</span><span class="sxs-lookup"><span data-stu-id="ed379-117">Microsoft Office does not play explicit **Return** animations, so you should not define them.</span></span> <span data-ttu-id="ed379-118">Todas las animaciones también deben tener una bifurcación de salida.</span><span class="sxs-lookup"><span data-stu-id="ed379-118">All animations should also have Exit Branching.</span></span> <span data-ttu-id="ed379-119">Exit Branching nos permite "acelerar y finalizar" la animación actual antes de llamar a la siguiente animación.</span><span class="sxs-lookup"><span data-stu-id="ed379-119">Exit branching enables us to 'hurry up and finish' the current animation before we call the next animation.</span></span> <span data-ttu-id="ed379-120">Si no proporciona una bifurcación de salida, la transición entre animaciones puede ser irregular.</span><span class="sxs-lookup"><span data-stu-id="ed379-120">If you don't supply Exit Branching, the transition between animations may be jerky.</span></span>

### <a name="character-properties"></a><span data-ttu-id="ed379-121">Propiedades de caracteres</span><span class="sxs-lookup"><span data-stu-id="ed379-121">Character Properties</span></span>

<span data-ttu-id="ed379-122">Microsoft Agent le permite establecer las propiedades [**Name**](name-property.md), [**Description**](description-property.md) y [**ExtraData**](extradata-property.md) del carácter.</span><span class="sxs-lookup"><span data-stu-id="ed379-122">Microsoft Agent enables you to set the character's [**Name**](name-property.md), [**Description**](description-property.md) and [**ExtraData**](extradata-property.md) properties.</span></span> <span data-ttu-id="ed379-123">Microsoft Office usa el campo **ExtraData** para contener una o varias frases de introducción y frases de recordatorio.</span><span class="sxs-lookup"><span data-stu-id="ed379-123">Microsoft Office uses the **ExtraData** field to hold to one or more Introduction Phrases and Reminder Phrases.</span></span> <span data-ttu-id="ed379-124">Microsoft Office elige de las otras frases de introducción para colocar en el globo de voz en la galería de asistentes.</span><span class="sxs-lookup"><span data-stu-id="ed379-124">Microsoft Office picks from the other Introduction Phrases to put in the speech balloon in the Assistant Gallery.</span></span> <span data-ttu-id="ed379-125">Usamos las frases de recordatorio cuando recibe un recordatorio de Outlook.</span><span class="sxs-lookup"><span data-stu-id="ed379-125">We use the Reminder Phrases when you receive a reminder from Outlook.</span></span>

<span data-ttu-id="ed379-126">El campo [**ExtraData**](extradata-property.md) tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="ed379-126">The [**ExtraData**](extradata-property.md) field is formatted as follows:</span></span>

<span data-ttu-id="ed379-127">IntroPhrase1~~IntroPhrase2~~IntroPhrase3 ^ ^ ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3</span><span class="sxs-lookup"><span data-stu-id="ed379-127">IntroPhrase1~~IntroPhrase2~~IntroPhrase3^^ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3</span></span>

<span data-ttu-id="ed379-128">Las frases de introducción están separadas por un par de caracteres de tilde (~), seguidos de frases de recordatorio.</span><span class="sxs-lookup"><span data-stu-id="ed379-128">Intro Phrases are separated by a pair of tilde characters (~), followed by Reminder Phrases.</span></span> <span data-ttu-id="ed379-129">Estas frases de recordatorio también se separan mediante un par de caracteres de tilde.</span><span class="sxs-lookup"><span data-stu-id="ed379-129">These Reminder Phrases are also separated by a pair of tilde characters.</span></span> <span data-ttu-id="ed379-130">Los dos conjuntos de frases se separan con dos caracteres de intercalación (^^).</span><span class="sxs-lookup"><span data-stu-id="ed379-130">The two sets of phrases are separated by two caret characters (^^).</span></span> <span data-ttu-id="ed379-131">No hay ningún límite en cuanto al número de cada tipo de frase, salvo que debe haber al menos una de cada.</span><span class="sxs-lookup"><span data-stu-id="ed379-131">There is no limit to the number of each kind of phrase, except that there must be at least one of each.</span></span>

 

 





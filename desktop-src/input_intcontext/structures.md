---
title: Estructuras de contexto de interacción
description: En los temas de esta sección se proporcionan las especificaciones de referencia para las estructuras de contexto de interacción.
ms.assetid: 38C5CE85-405B-455F-809D-19C77B8A217B
keywords:
- interacción con el usuario
- input
- puntero
- Función táctil
- mouse
- Lápiz
- lápiz
ms.topic: article
ms.date: 02/06/2020
ms.openlocfilehash: 975b1342c681d4d154ba31d31348e13063c9fc88
ms.sourcegitcommit: 6b8d5058d02daacad4d2ed7830da63b63a509586
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/07/2020
ms.locfileid: "104420163"
---
# <a name="interaction-context-structures"></a><span data-ttu-id="04798-110">Estructuras de contexto de interacción</span><span class="sxs-lookup"><span data-stu-id="04798-110">Interaction Context Structures</span></span>

<span data-ttu-id="04798-111">En los temas de esta sección se proporcionan las especificaciones de referencia para las estructuras de [contexto de interacción](interaction-context-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="04798-111">The topics in this section provide the reference specifications for [Interaction Context](interaction-context-portal.md) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="04798-112">En esta sección</span><span class="sxs-lookup"><span data-stu-id="04798-112">In this section</span></span>

| <span data-ttu-id="04798-113">Tema</span><span class="sxs-lookup"><span data-stu-id="04798-113">Topic</span></span> | <span data-ttu-id="04798-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="04798-114">Description</span></span> |
|---|---|
| [<span data-ttu-id="04798-115">**\_parámetro de deslizamiento cruzado \_**</span><span class="sxs-lookup"><span data-stu-id="04798-115">**CROSS\_SLIDE\_PARAMETER**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-cross_slide_parameter)<br/>                           | <span data-ttu-id="04798-116">Define el umbral de deslizamiento transversal y su umbral de distancia.</span><span class="sxs-lookup"><span data-stu-id="04798-116">Defines the cross-slide threshold and its distance threshold.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="04798-117">**\_ \_ diapositiva cruzado de argumentos de interacción \_**</span><span class="sxs-lookup"><span data-stu-id="04798-117">**INTERACTION\_ARGUMENTS\_CROSS\_SLIDE**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-interaction_arguments_cross_slide)<br/>  | <span data-ttu-id="04798-118">Define el estado de la interacción entre diapositivas.</span><span class="sxs-lookup"><span data-stu-id="04798-118">Defines the state of the cross-slide interaction.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="04798-119">**\_manipulación de argumentos de interacción \_**</span><span class="sxs-lookup"><span data-stu-id="04798-119">**INTERACTION\_ARGUMENTS\_MANIPULATION**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-interaction_arguments_manipulation)<br/> | <span data-ttu-id="04798-120">Define el estado de una manipulación.</span><span class="sxs-lookup"><span data-stu-id="04798-120">Defines the state of a manipulation.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="04798-121">**\_puntear argumentos de interacción \_**</span><span class="sxs-lookup"><span data-stu-id="04798-121">**INTERACTION\_ARGUMENTS\_TAP**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-interaction_arguments_tap)<br/>                   | <span data-ttu-id="04798-122">Define el estado de la interacción de TAP.</span><span class="sxs-lookup"><span data-stu-id="04798-122">Defines the state of the tap interaction.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="04798-123">**\_configuración de contexto de interacción \_**</span><span class="sxs-lookup"><span data-stu-id="04798-123">**INTERACTION\_CONTEXT\_CONFIGURATION**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-interaction_context_configuration)<br/>   | <span data-ttu-id="04798-124">Define la configuración de un objeto de [contexto de interacción](interaction-context-portal.md) que habilita, deshabilita o modifica el comportamiento de una interacción.</span><span class="sxs-lookup"><span data-stu-id="04798-124">Defines the configuration of an [Interaction Context](interaction-context-portal.md) object that enables, disables, or modifies the behavior of an interaction.</span></span><br/> |
| [<span data-ttu-id="04798-125">**\_resultado del contexto de interacción \_**</span><span class="sxs-lookup"><span data-stu-id="04798-125">**INTERACTION\_CONTEXT\_OUTPUT**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-interaction_context_output)<br/>                 | <span data-ttu-id="04798-126">Define la salida del objeto de [contexto de interacción](interaction-context-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="04798-126">Defines the output of the [Interaction Context](interaction-context-portal.md) object.</span></span><br/>                                                                          |
| [<span data-ttu-id="04798-127">**transformación de manipulación \_**</span><span class="sxs-lookup"><span data-stu-id="04798-127">**MANIPULATION\_TRANSFORM**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-manipulation_transform)<br/>                          | <span data-ttu-id="04798-128">Define los datos de transformación para una manipulación.</span><span class="sxs-lookup"><span data-stu-id="04798-128">Defines the transformation data for a manipulation.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="04798-129">**velocidad de manipulación \_**</span><span class="sxs-lookup"><span data-stu-id="04798-129">**MANIPULATION\_VELOCITY**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-manipulation_velocity)<br/>                            | <span data-ttu-id="04798-130">Define los datos de velocidad de una manipulación.</span><span class="sxs-lookup"><span data-stu-id="04798-130">Defines the velocity data of a manipulation.</span></span><br/>                                                                                                                     |
## <a name="related-topics"></a><span data-ttu-id="04798-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04798-131">Related topics</span></span>

[<span data-ttu-id="04798-132">Interacción del usuario</span><span class="sxs-lookup"><span data-stu-id="04798-132">User Interaction</span></span>](../user-interaction.md)

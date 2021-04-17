---
title: Mensajes (aspectos básicos del diseño)
description: Los mensajes son cualquier tipo de mensaje que los usuarios necesitan o desean ver cuando usan su aplicación. Obtenga información sobre cómo presentar errores, advertencias, confirmaciones y notificaciones en la aplicación.
ms.assetid: 700F1F1F-B41D-4C0A-B2EC-91C84E46E526
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dba3296c9824b2153184c45b6a021ea823b4d151
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105697906"
---
# <a name="messages-design-basics"></a><span data-ttu-id="fb616-104">Mensajes (aspectos básicos del diseño)</span><span class="sxs-lookup"><span data-stu-id="fb616-104">Messages (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="fb616-105">Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows.</span><span class="sxs-lookup"><span data-stu-id="fb616-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="fb616-106">Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="fb616-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="fb616-107">Los mensajes son cualquier tipo de mensaje que los usuarios necesitan o desean ver cuando usan su aplicación.</span><span class="sxs-lookup"><span data-stu-id="fb616-107">Messages are any kind of message users need or want to see as they use your app.</span></span> <span data-ttu-id="fb616-108">Obtenga información sobre cómo presentar errores, advertencias, confirmaciones y notificaciones en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fb616-108">Learn how to present errors, warning, confirmations, and notifications in your app.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fb616-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="fb616-109">In this section</span></span>



| <span data-ttu-id="fb616-110">Tema</span><span class="sxs-lookup"><span data-stu-id="fb616-110">Topic</span></span>                                        | <span data-ttu-id="fb616-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb616-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb616-112">Mensajes de error</span><span class="sxs-lookup"><span data-stu-id="fb616-112">Error Messages</span></span>](mess-error.md)<br/>  | <span data-ttu-id="fb616-113">Un mensaje de error alerta a los usuarios de un problema que ya se ha producido.</span><span class="sxs-lookup"><span data-stu-id="fb616-113">An error message alerts users of a problem that has already occurred.</span></span> <span data-ttu-id="fb616-114">Por el contrario, un mensaje de advertencia alerta a los usuarios de una condición que puede provocar un problema en el futuro.</span><span class="sxs-lookup"><span data-stu-id="fb616-114">By contrast, a warning message alerts users of a condition that might cause a problem in the future.</span></span> <span data-ttu-id="fb616-115">Los mensajes de error se pueden presentar mediante cuadros de diálogo modales, mensajes en contexto, notificaciones o globos.</span><span class="sxs-lookup"><span data-stu-id="fb616-115">Error messages can be presented using modal dialog boxes, in-place messages, notifications, or balloons.</span></span><br/>                                                  |
| [<span data-ttu-id="fb616-116">Mensajes de advertencia</span><span class="sxs-lookup"><span data-stu-id="fb616-116">Warning Messages</span></span>](mess-warn.md)<br/> | <span data-ttu-id="fb616-117">Un mensaje de advertencia es un cuadro de diálogo modal, un mensaje en contexto, una notificación o un globo que alerta al usuario de una condición que puede provocar un problema en el futuro.</span><span class="sxs-lookup"><span data-stu-id="fb616-117">A warning message is a modal dialog box, in-place message, notification, or balloon that alerts the user of a condition that might cause a problem in the future.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="fb616-118">Confirmaciones</span><span class="sxs-lookup"><span data-stu-id="fb616-118">Confirmations</span></span>](mess-confirm.md)<br/> | <span data-ttu-id="fb616-119">Una confirmación es un cuadro de diálogo modal que pregunta si el usuario desea continuar con una acción.</span><span class="sxs-lookup"><span data-stu-id="fb616-119">A confirmation is a modal dialog box that asks if the user wants to proceed with an action.</span></span><br/>                                                                                                                                                                                                                                          |
| [<span data-ttu-id="fb616-120">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="fb616-120">Notifications</span></span>](mess-notif.md)<br/>   | <span data-ttu-id="fb616-121">Una notificación informa a los usuarios de eventos que no están relacionados con la actividad del usuario actual, mostrando brevemente un globo de un icono en el área de notificación.</span><span class="sxs-lookup"><span data-stu-id="fb616-121">A notification informs users of events that are unrelated to the current user activity, by briefly displaying a balloon from an icon in the notification area.</span></span> <span data-ttu-id="fb616-122">La notificación podría deberse a una acción del usuario o a un evento del sistema importante, o podría ofrecer información potencialmente útil de Microsoft Windows o una aplicación.</span><span class="sxs-lookup"><span data-stu-id="fb616-122">The notification could result from a user action or significant system event, or could offer potentially useful information from Microsoft Windows or an application.</span></span><br/> |



 

 


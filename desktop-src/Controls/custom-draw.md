---
title: Dibujo personalizado
description: El dibujo personalizado no es un control común; es un servicio que proporcionan muchos controles comunes.
ms.assetid: vs|controls|~\controls\custdraw\custdraw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5184d06dbb8e04185bf12a43c6c71dd96b933a6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994029"
---
# <a name="custom-draw"></a><span data-ttu-id="dde76-103">Dibujo personalizado</span><span class="sxs-lookup"><span data-stu-id="dde76-103">Custom Draw</span></span>

<span data-ttu-id="dde76-104">El dibujo personalizado no es un control común; es un servicio que proporcionan muchos controles comunes.</span><span class="sxs-lookup"><span data-stu-id="dde76-104">Custom draw is not a common control; it is a service that many common controls provide.</span></span> <span data-ttu-id="dde76-105">El servicio de dibujo personalizado permite que una aplicación tenga mayor flexibilidad en la personalización de la apariencia de un control.</span><span class="sxs-lookup"><span data-stu-id="dde76-105">The custom draw service allows an application greater flexibility in customizing a control's appearance.</span></span> <span data-ttu-id="dde76-106">La aplicación puede aprovechar las notificaciones de dibujo personalizadas para cambiar fácilmente la fuente usada para mostrar elementos o dibujar manualmente un elemento sin tener que realizar un dibujo de propietario completo.</span><span class="sxs-lookup"><span data-stu-id="dde76-106">Your application can harness custom draw notifications to easily change the font used to display items or manually draw an item without having to do a full owner draw.</span></span>

<span data-ttu-id="dde76-107">Esta sección contiene información sobre los elementos de programación utilizados con Draw personalizado.</span><span class="sxs-lookup"><span data-stu-id="dde76-107">This section contains information about the programming elements used with custom draw.</span></span>

## <a name="overviews"></a><span data-ttu-id="dde76-108">Temas de introducción</span><span class="sxs-lookup"><span data-stu-id="dde76-108">Overviews</span></span>



| <span data-ttu-id="dde76-109">Tema</span><span class="sxs-lookup"><span data-stu-id="dde76-109">Topic</span></span>                                      | <span data-ttu-id="dde76-110">Contenido</span><span class="sxs-lookup"><span data-stu-id="dde76-110">Contents</span></span>                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dde76-111">Acerca de Draw personalizado</span><span class="sxs-lookup"><span data-stu-id="dde76-111">About Custom Draw</span></span>](about-custom-draw.md) | <span data-ttu-id="dde76-112">Esta sección contiene información general sobre la funcionalidad de dibujo personalizado y proporciona información conceptual sobre cómo una aplicación puede admitir el dibujo personalizado.</span><span class="sxs-lookup"><span data-stu-id="dde76-112">This section contains general information about custom draw functionality and provides a conceptual overview of how an application can support custom draw.</span></span><br/> |
| [<span data-ttu-id="dde76-113">Usar Draw personalizado</span><span class="sxs-lookup"><span data-stu-id="dde76-113">Using Custom Draw</span></span>](using-custom-draw.md) | <span data-ttu-id="dde76-114">Esta sección contiene ejemplos que muestran cómo implementar Draw personalizado.</span><span class="sxs-lookup"><span data-stu-id="dde76-114">This section contains examples that demonstrate how to implement custom draw.</span></span> <br/>                                                                              |



 

## <a name="notifications"></a><span data-ttu-id="dde76-115">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="dde76-115">Notifications</span></span>



| <span data-ttu-id="dde76-116">Tema</span><span class="sxs-lookup"><span data-stu-id="dde76-116">Topic</span></span>                               | <span data-ttu-id="dde76-117">Contenido</span><span class="sxs-lookup"><span data-stu-id="dde76-117">Contents</span></span>                                                                                                                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dde76-118">NM \_ CUSTOMDRAW</span><span class="sxs-lookup"><span data-stu-id="dde76-118">NM\_CUSTOMDRAW</span></span>](nm-customdraw.md) | <span data-ttu-id="dde76-119">Notifica a la ventana primaria de un control sobre las operaciones de dibujo personalizadas.</span><span class="sxs-lookup"><span data-stu-id="dde76-119">Notifies a control's parent window about custom drawing operations.</span></span> <span data-ttu-id="dde76-120">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="dde76-120">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

## <a name="structures"></a><span data-ttu-id="dde76-121">Estructuras</span><span class="sxs-lookup"><span data-stu-id="dde76-121">Structures</span></span>



| <span data-ttu-id="dde76-122">Tema</span><span class="sxs-lookup"><span data-stu-id="dde76-122">Topic</span></span>                                | <span data-ttu-id="dde76-123">Contenido</span><span class="sxs-lookup"><span data-stu-id="dde76-123">Contents</span></span>                                                                                              |
|--------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dde76-124">**NMCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="dde76-124">**NMCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) | <span data-ttu-id="dde76-125">Contiene información específica de un código de notificación de [nm \_ CUSTOMDRAW](nm-customdraw.md) .</span><span class="sxs-lookup"><span data-stu-id="dde76-125">Contains information specific to an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code.</span></span><br/> |



 

 

 






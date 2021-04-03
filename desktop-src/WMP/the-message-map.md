---
title: El mapa de mensajes
description: El mapa de mensajes
ms.assetid: 4640b0f5-625e-4a9e-86f5-3e75d0afb40d
keywords:
- Complementos de Media Player de Windows, mapa de mensajes
- complementos, mapa de mensajes
- Complementos de la interfaz de usuario, mapa de mensajes
- Complementos de la interfaz de usuario, mapa de mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea7fc04caf752383368ab6e51ae19c82e8c3515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075832"
---
# <a name="the-message-map"></a><span data-ttu-id="b317f-107">El mapa de mensajes</span><span class="sxs-lookup"><span data-stu-id="b317f-107">The Message Map</span></span>

<span data-ttu-id="b317f-108">La ventana del complemento responde a varios eventos llamando a métodos que se asignan a los mensajes de eventos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="b317f-108">The plug-in window responds to various events by calling methods that are mapped to corresponding event messages.</span></span> <span data-ttu-id="b317f-109">El asistente proporciona una asignación para que se llame a OnPaint y OnEraseBackground en el momento adecuado.</span><span class="sxs-lookup"><span data-stu-id="b317f-109">The wizard provides a mapping so that OnPaint and OnEraseBackground will be called at the appropriate times.</span></span> <span data-ttu-id="b317f-110">Para crear el botón **Buscar** y responder a los clics de este, la sección mapa de mensajes se modifica de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b317f-110">To create the **Search** button and to respond to clicks from it, the message map section is modified as follows:</span></span>


```C++
BEGIN_MSG_MAP(CPluginWindow)
    MESSAGE_HANDLER(WM_PAINT, OnPaint)
    MESSAGE_HANDLER(WM_ERASEBKGND, OnEraseBackground)
    MESSAGE_HANDLER(WM_CREATE, OnCreate)
    COMMAND_ID_HANDLER(IDC_SEARCH, OnSearch)
END_MSG_MAP()

```



## <a name="related-topics"></a><span data-ttu-id="b317f-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b317f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b317f-112">**Implementación de CPluginWindow**</span><span class="sxs-lookup"><span data-stu-id="b317f-112">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 





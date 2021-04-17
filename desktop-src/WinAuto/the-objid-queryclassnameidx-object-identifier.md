---
title: Identificador del objeto OBJID_QUERYCLASSNAMEIDX
description: Microsoft Active Accessibility usa el identificador de objeto de OBJID \_ QUERYCLASSNAMEIDX con el \_ mensaje de WM GETOBJECT para determinar la clase a la que pertenece un control común o un control de Windows estándar.
ms.assetid: 2167df6d-5df3-40b7-bebe-142f4bd98cd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d73a152380411ef0b230de8f0e3372a6718b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704577"
---
# <a name="the-objid_queryclassnameidx-object-identifier"></a><span data-ttu-id="d57c9-103">Identificador de \_ objeto de QUERYCLASSNAMEIDX OBJID</span><span class="sxs-lookup"><span data-stu-id="d57c9-103">The OBJID\_QUERYCLASSNAMEIDX Object Identifier</span></span>

<span data-ttu-id="d57c9-104">Microsoft Active Accessibility usa el identificador de objeto de [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) con el mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) para determinar la clase a la que pertenece un control común o un control de Windows estándar.</span><span class="sxs-lookup"><span data-stu-id="d57c9-104">Microsoft Active Accessibility uses the [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md) object identifier with the [**WM\_GETOBJECT**](wm-getobject.md) message to determine the class to which a standard Windows control or common control belongs.</span></span> <span data-ttu-id="d57c9-105">Un control responde a este mensaje devolviendo un valor que Microsoft Active Accessibility asigna al nombre de clase del control.</span><span class="sxs-lookup"><span data-stu-id="d57c9-105">A control responds to this message by returning a value that Microsoft Active Accessibility maps to the class name of the control.</span></span> <span data-ttu-id="d57c9-106">Microsoft Active Accessibility usa esta información para proporcionar compatibilidad de accesibilidad para los controles estándar de Windows y los controles comunes.</span><span class="sxs-lookup"><span data-stu-id="d57c9-106">Microsoft Active Accessibility uses this information to provide accessibility support for standard Windows controls and common controls.</span></span>

<span data-ttu-id="d57c9-107">Por lo general, solo los controles estándar de Windows y los controles comunes responden al identificador de objeto de [**\_ QUERYCLASSNAMEIDX OBJID**](object-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="d57c9-107">Generally, only the standard Windows controls and the common controls respond to the [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md) object identifier.</span></span> <span data-ttu-id="d57c9-108">Sin embargo, un control personalizado también puede responder si incluye la misma funcionalidad que un control estándar o común de Windows existente.</span><span class="sxs-lookup"><span data-stu-id="d57c9-108">However, a custom control can also respond if it includes all of the same functionality as an existing standard Windows control or common control.</span></span> <span data-ttu-id="d57c9-109">Esto permite que el control personalizado sea compatible con uno de los objetos proxy estándar proporcionados por Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="d57c9-109">This enables the custom control to be supported by one of the standard proxy objects provided by Microsoft Active Accessibility.</span></span>

<span data-ttu-id="d57c9-110">Para obtener más información, vea el [Apéndice F: valores de identificador de objeto para OBJID \_ QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).</span><span class="sxs-lookup"><span data-stu-id="d57c9-110">For more information, see [Appendix F: Object Identifier Values for OBJID\_QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).</span></span>

 

 





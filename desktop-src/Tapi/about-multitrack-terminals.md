---
description: Un terminal multipista se puede considerar como un terminal que es una colección de otros terminales. Cada terminal secundario (un &\# 0034; track&\# 0034;) puede ser un terminal Multipista o un terminal de una sola pista.
ms.assetid: bf23bc26-5763-45a3-a63d-e43ce2480956
title: Acerca de los terminales multipista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58042236c737f6ab0b933699d75e19358f6e6b81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677816"
---
# <a name="about-multitrack-terminals"></a><span data-ttu-id="9c8cb-104">Acerca de los terminales multipista</span><span class="sxs-lookup"><span data-stu-id="9c8cb-104">About Multitrack Terminals</span></span>

<span data-ttu-id="9c8cb-105">Un terminal multipista se puede considerar como un terminal que es una colección de otros terminales.</span><span class="sxs-lookup"><span data-stu-id="9c8cb-105">A multitrack terminal can be thought of as a terminal that is a collection of other terminals.</span></span> <span data-ttu-id="9c8cb-106">Cada terminal secundario (una "pista") puede ser un terminal Multipista o un terminal de una sola pista.</span><span class="sxs-lookup"><span data-stu-id="9c8cb-106">Each child terminal (a "track") can be a multitrack terminal or a single-track terminal.</span></span>

<span data-ttu-id="9c8cb-107">Todos los terminales multipista exponen la interfaz [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) , que incluye métodos genéricos para enumerar, crear y quitar terminales de seguimiento de un terminal multipista.</span><span class="sxs-lookup"><span data-stu-id="9c8cb-107">All multitrack terminals expose the [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) interface, which includes generic methods for enumerating, creating, and removing track terminals from a multitrack terminal.</span></span> <span data-ttu-id="9c8cb-108">Todos los terminales, una sola pista y una Multipista, exponen la interfaz [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .</span><span class="sxs-lookup"><span data-stu-id="9c8cb-108">All terminals, single-track and multitrack, expose the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface.</span></span>

<span data-ttu-id="9c8cb-109">Un cliente que tiene un puntero a una interfaz [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) puede detectar si el terminal es Multipista o de una sola pista; para ello, consulta el terminal de la interfaz [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) , que solo se expone en terminales multipista.</span><span class="sxs-lookup"><span data-stu-id="9c8cb-109">A client that has a pointer to an [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface can discover whether the terminal is multitrack or single-track by querying the terminal for the [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) interface, which is exposed only on multitrack terminals.</span></span>

<span data-ttu-id="9c8cb-110">El terminal principal puede usar la interfaz [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) de sus terminales de seguimiento o puede requerir que los terminales de seguimiento expongan interfaces privadas.</span><span class="sxs-lookup"><span data-stu-id="9c8cb-110">The parent terminal may use the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface of its track terminals, or it may require track terminals to expose private interfaces.</span></span>

<span data-ttu-id="9c8cb-111">Para obtener más información, consulte [seguimiento de terminales](track-terminals.md).</span><span class="sxs-lookup"><span data-stu-id="9c8cb-111">For more information, see [Track Terminals](track-terminals.md).</span></span>

 

 

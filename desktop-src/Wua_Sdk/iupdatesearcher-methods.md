---
description: La interfaz IUpdateSearcher define los siguientes métodos.
ms.assetid: 82735555-b23a-43b0-bf5b-a8cf72dc40d4
title: Métodos IUpdateSearcher
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 462cbd371546743bab836ed1cdc2479e30f13612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666512"
---
# <a name="iupdatesearcher-methods"></a><span data-ttu-id="cf152-103">Métodos IUpdateSearcher</span><span class="sxs-lookup"><span data-stu-id="cf152-103">IUpdateSearcher Methods</span></span>

<span data-ttu-id="cf152-104">La interfaz [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) define los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="cf152-104">The [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) interface defines the following methods.</span></span>



| <span data-ttu-id="cf152-105">Método</span><span class="sxs-lookup"><span data-stu-id="cf152-105">Method</span></span>                                                              | <span data-ttu-id="cf152-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf152-106">Description</span></span>                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf152-107">**BeginSearch**</span><span class="sxs-lookup"><span data-stu-id="cf152-107">**BeginSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)                   | <span data-ttu-id="cf152-108">Comienza la ejecución de una búsqueda asincrónica de las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="cf152-108">Begins execution of an asynchronous search for updates.</span></span> <span data-ttu-id="cf152-109">La búsqueda usa las opciones de búsqueda que están configuradas actualmente.</span><span class="sxs-lookup"><span data-stu-id="cf152-109">The search uses the search options that are currently configured.</span></span> |
| [<span data-ttu-id="cf152-110">**EndSearch**</span><span class="sxs-lookup"><span data-stu-id="cf152-110">**EndSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)                       | <span data-ttu-id="cf152-111">Completa una búsqueda asincrónica de las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="cf152-111">Completes an asynchronous search for updates.</span></span>                                                                             |
| [<span data-ttu-id="cf152-112">**EscapeString**</span><span class="sxs-lookup"><span data-stu-id="cf152-112">**EscapeString**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-escapestring)                 | <span data-ttu-id="cf152-113">Convierte una cadena en una cadena que se puede utilizar como un valor literal en una cadena de criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cf152-113">Converts a string into a string that can be used as a literal value in a search criteria string.</span></span>                          |
| [<span data-ttu-id="cf152-114">**GetTotalHistoryCount**</span><span class="sxs-lookup"><span data-stu-id="cf152-114">**GetTotalHistoryCount**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-gettotalhistorycount) | <span data-ttu-id="cf152-115">Devuelve el número de eventos de actualización del equipo.</span><span class="sxs-lookup"><span data-stu-id="cf152-115">Returns the number of update events on the computer.</span></span>                                                                      |
| [<span data-ttu-id="cf152-116">**QueryHistory**</span><span class="sxs-lookup"><span data-stu-id="cf152-116">**QueryHistory**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-queryhistory)                | <span data-ttu-id="cf152-117">Consulta sincrónicamente el equipo en busca del historial de eventos de actualización.</span><span class="sxs-lookup"><span data-stu-id="cf152-117">Synchronously queries the computer for the history of update events.</span></span>                                                      |
| [<span data-ttu-id="cf152-118">**Search**</span><span class="sxs-lookup"><span data-stu-id="cf152-118">**Search**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search)                             | <span data-ttu-id="cf152-119">Realiza una búsqueda sincrónica de las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="cf152-119">Performs a synchronous search for updates.</span></span> <span data-ttu-id="cf152-120">La búsqueda usa las opciones de búsqueda que están configuradas actualmente.</span><span class="sxs-lookup"><span data-stu-id="cf152-120">The search uses the search options that are currently configured.</span></span>              |



 

 

 




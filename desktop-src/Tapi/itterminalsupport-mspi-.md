---
description: La interfaz ITTerminalSupport se expone en un objeto Address si existe un MSP. Los métodos de esta interfaz permiten a una aplicación detectar terminales disponibles o crear uno, y obtener punteros a objetos de terminal necesarios.
ms.assetid: 39cb9734-3e70-4e37-9358-c638c6618c11
title: ITTerminalSupport (MSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63822f55742d5a4c7a0114abeb625f2393a51ae7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688590"
---
# <a name="itterminalsupport-mspi"></a><span data-ttu-id="664bc-104">ITTerminalSupport (MSPI)</span><span class="sxs-lookup"><span data-stu-id="664bc-104">ITTerminalSupport (MSPI)</span></span>

<span data-ttu-id="664bc-105">La interfaz [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) se expone en un [objeto Address](address-object.md) si existe un MSP.</span><span class="sxs-lookup"><span data-stu-id="664bc-105">The [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) interface is exposed on an [Address object](address-object.md) if an MSP exists.</span></span> <span data-ttu-id="664bc-106">Los métodos de esta interfaz permiten a una aplicación detectar terminales disponibles o crear uno, y obtener punteros a [objetos de terminal](terminal-object.md)necesarios.</span><span class="sxs-lookup"><span data-stu-id="664bc-106">The methods of this interface allow an application to discover available terminals and/or create one, and get pointers to required [Terminal objects](terminal-object.md).</span></span>

<span data-ttu-id="664bc-107">La interfaz [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) se implementa mediante un MSP y no está disponible si no hay ningún proveedor de servicios multimedia asociado a la dirección.</span><span class="sxs-lookup"><span data-stu-id="664bc-107">The [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) interface is implemented by an MSP and is not available if there is no media service provider associated with the address.</span></span> <span data-ttu-id="664bc-108">Consulte **ITTerminalSupport** en la sección interfaz MSP para obtener más información sobre esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="664bc-108">Please see **ITTerminalSupport** in the MSP Interface section for details on this interface.</span></span>

 

 

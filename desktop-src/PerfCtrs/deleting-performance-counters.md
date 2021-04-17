---
description: Para quitar los contadores de rendimiento de las aplicaciones del sistema, realice los pasos siguientes.
ms.assetid: 40fc9831-1025-4052-a941-70767ee4e10f
title: Eliminar contadores de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba257a1a44b5272543b7e61dcdc4b4e96225c160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667336"
---
# <a name="deleting-performance-counters"></a><span data-ttu-id="f2060-103">Eliminar contadores de rendimiento</span><span class="sxs-lookup"><span data-stu-id="f2060-103">Deleting Performance Counters</span></span>

<span data-ttu-id="f2060-104">Para quitar los contadores de rendimiento de la aplicación del sistema, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="f2060-104">To remove your application's performance counters from the system, perform the following steps.</span></span>

1.  <span data-ttu-id="f2060-105">Utilice la herramienta **Unlodctr** incluida con el equipo para quitar del registro los datos relacionados con los contadores.</span><span class="sxs-lookup"><span data-stu-id="f2060-105">Use the **unlodctr** tool included with the computer to remove the counter related data from the registry.</span></span> <span data-ttu-id="f2060-106">Tenga en cuenta que la clave de **rendimiento** de la aplicación debe existir para que la herramienta **Unlodctr** se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="f2060-106">Note that the application's **Performance** key must exist for the **unlodctr** tool to succeed.</span></span> <span data-ttu-id="f2060-107">Para obtener más información, vea [quitar los nombres y descripciones de los contadores del registro](removing-counter-names-and-descriptions-from-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="f2060-107">For details, see [Removing Counter Names and Descriptions from the Registry](removing-counter-names-and-descriptions-from-the-registry.md).</span></span>
2.  <span data-ttu-id="f2060-108">Elimine las claves de **rendimiento** y **vinculación** en la clave de **servicios** de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f2060-108">Delete the **Performance** and **Linkage** keys under the application's **Services** key.</span></span> <span data-ttu-id="f2060-109">Para eliminar estas claves, use la utilidad Regedt32.exe o llame a [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).</span><span class="sxs-lookup"><span data-stu-id="f2060-109">To delete these keys, use either the Regedt32.exe utility or call [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).</span></span>

 

 

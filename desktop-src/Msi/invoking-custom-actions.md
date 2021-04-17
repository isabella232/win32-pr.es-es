---
description: Las acciones personalizadas se invocan de la misma manera que las acciones estándar, ya sea mediante invocación explícita o durante la ejecución de una tabla de secuencia.
ms.assetid: 05f15bae-983a-4763-840d-f2590f4e2a7a
title: Invocar acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f1e9a575d32cbb8fe22323d4a741eb7936ef9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688542"
---
# <a name="invoking-custom-actions"></a><span data-ttu-id="d19ca-103">Invocar acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="d19ca-103">Invoking Custom Actions</span></span>

<span data-ttu-id="d19ca-104">Las acciones personalizadas se invocan de la misma manera que las acciones estándar, ya sea mediante invocación explícita o durante la ejecución de una tabla de secuencia.</span><span class="sxs-lookup"><span data-stu-id="d19ca-104">Custom actions are invoked in the same manner as standard actions, either by explicit invocation or during the execution of a sequence table.</span></span> <span data-ttu-id="d19ca-105">Hay dos métodos para llamar a las acciones:</span><span class="sxs-lookup"><span data-stu-id="d19ca-105">There are two methods for calling actions:</span></span>

-   <span data-ttu-id="d19ca-106">Llame a la acción especificada directamente con la función [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) .</span><span class="sxs-lookup"><span data-stu-id="d19ca-106">You call the specified action directly with the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function.</span></span>
-   <span data-ttu-id="d19ca-107">Una acción de nivel superior llama a la tabla de secuencias que contiene la acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="d19ca-107">A top-level action calls the sequence table containing the custom action.</span></span> <span data-ttu-id="d19ca-108">Para obtener más información sobre la programación de una acción personalizada en una tabla de secuencia, consulte [secuenciación de acciones personalizadas](sequencing-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="d19ca-108">For more information about scheduling a custom action in a sequence table, see [Sequencing Custom Actions](sequencing-custom-actions.md).</span></span>

<span data-ttu-id="d19ca-109">Cuando el instalador obtiene un nombre de acción de la función [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) , o de una tabla de secuencia, busca primero una acción estándar de ese nombre.</span><span class="sxs-lookup"><span data-stu-id="d19ca-109">When the installer obtains an action name from the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function, or from a sequence table, it first searches for a standard action of that name.</span></span> <span data-ttu-id="d19ca-110">Si no encuentra la acción estándar, el instalador consulta la [tabla CustomAction](customaction-table.md) para comprobar si la acción especificada es una acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="d19ca-110">If it cannot find the standard action, then the installer queries the [CustomAction table](customaction-table.md) to check if the specified action is a custom action.</span></span> <span data-ttu-id="d19ca-111">Si la acción especificada no es una acción personalizada, el instalador consulta la [tabla de diálogo](dialog-table.md) de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d19ca-111">If the specified action is not a custom action, then the installer queries the [Dialog table](dialog-table.md) for a dialog box.</span></span>

 

 




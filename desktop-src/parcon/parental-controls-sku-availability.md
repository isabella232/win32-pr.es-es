---
description: Disponibilidad de SKU de controles parentales
ms.assetid: 5fbf6c4a-3897-4a12-bef6-19478fdb48aa
title: Disponibilidad de SKU de controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b858bc62e8f10a3b06313befd99d67e497b8d442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697140"
---
# <a name="parental-controls-sku-availability"></a><span data-ttu-id="7df51-103">Disponibilidad de SKU de controles parentales</span><span class="sxs-lookup"><span data-stu-id="7df51-103">Parental Controls SKU Availability</span></span>

<span data-ttu-id="7df51-104">En la actualidad, las interfaces de usuario, las características y las API de control parental que se describen en esta sección están previstas para que solo estén disponibles en SKU centradas en el consumidor, como:</span><span class="sxs-lookup"><span data-stu-id="7df51-104">The Parental Controls user interfaces, features, and APIs described in this section are currently planned to be available only on consumer-focused SKUs such as:</span></span>

-   <span data-ttu-id="7df51-105">Windows Vista Starter</span><span class="sxs-lookup"><span data-stu-id="7df51-105">Windows Vista Starter</span></span>
-   <span data-ttu-id="7df51-106">Windows Vista Home Basic</span><span class="sxs-lookup"><span data-stu-id="7df51-106">Windows Vista Home Basic</span></span>
-   <span data-ttu-id="7df51-107">Windows Vista Home Premium</span><span class="sxs-lookup"><span data-stu-id="7df51-107">Windows Vista Home Premium</span></span>
-   <span data-ttu-id="7df51-108">Windows Vista Ultimate</span><span class="sxs-lookup"><span data-stu-id="7df51-108">Windows Vista Ultimate</span></span>

<span data-ttu-id="7df51-109">El control parental solo se instala en estas SKU.</span><span class="sxs-lookup"><span data-stu-id="7df51-109">Parental Controls only installs on these SKUs.</span></span> <span data-ttu-id="7df51-110">Las soluciones que tienen un requisito para implementar en las SKU de negocio deberán:</span><span class="sxs-lookup"><span data-stu-id="7df51-110">Solutions having a requirement to deploy onto business SKUs will need to either:</span></span>

-   <span data-ttu-id="7df51-111">Detectar y no proporcionar la funcionalidad de controles parentales en las SKU de negocio.</span><span class="sxs-lookup"><span data-stu-id="7df51-111">Detect and not provide parental controls functionality on business SKUs.</span></span>
-   <span data-ttu-id="7df51-112">Detecte y proporcione un medio alternativo de configuración, registro y restricciones.</span><span class="sxs-lookup"><span data-stu-id="7df51-112">Detect and provide an alternative means of configuration, logging, and restrictions.</span></span>

<span data-ttu-id="7df51-113">Se recomienda que las soluciones detecten la disponibilidad de la infraestructura de controles parentales comprobando si COM CoCreateInstance se ha ejecutado correctamente en la API de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="7df51-113">It is recommended that solutions detect availability of the Parental Controls Infrastructure by checking for success of COM CoCreateInstance on the Compliance API.</span></span>

<span data-ttu-id="7df51-114">Las aplicaciones basadas en controles parentales que dependen de la infraestructura de Windows Vista también pueden querer suprimir sus propias opciones de configuración de la interfaz de usuario u otra funcionalidad cuando se suprime la interfaz de usuario de controles parentales en una SKU compatible.</span><span class="sxs-lookup"><span data-stu-id="7df51-114">Parental Controls-aware applications depending on the Windows Vista infrastructure may also want to suppress any of their own UI exposing settings or other functionality when Parental Controls UI is suppressed on a supported SKU.</span></span> <span data-ttu-id="7df51-115">Se proporciona una función para la determinación de la visibilidad que abarca casos como la supresión unida a un dominio.</span><span class="sxs-lookup"><span data-stu-id="7df51-115">A function is provided for visibility determination that covers cases such as domain-joined suppression.</span></span>

 

 




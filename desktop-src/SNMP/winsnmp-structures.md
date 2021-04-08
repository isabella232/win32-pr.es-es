---
title: Estructuras WinSNMP
description: Las funciones de API WinSNMP usan las siguientes estructuras.
ms.assetid: ec74217e-8d02-4bda-b365-7b8f6c14cffb
keywords:
- Estructuras WinSNMP de SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b263f6078171c096eb7208ae4c7ef29847aead9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904702"
---
# <a name="winsnmp-structures"></a><span data-ttu-id="d37dd-104">Estructuras WinSNMP</span><span class="sxs-lookup"><span data-stu-id="d37dd-104">WinSNMP Structures</span></span>

<span data-ttu-id="d37dd-105">\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="d37dd-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d37dd-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="d37dd-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="d37dd-107">En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]</span><span class="sxs-lookup"><span data-stu-id="d37dd-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="d37dd-108">Las funciones de API WinSNMP usan las siguientes estructuras.</span><span class="sxs-lookup"><span data-stu-id="d37dd-108">The WinSNMP API functions use the following structures.</span></span>



| <span data-ttu-id="d37dd-109">Estructura</span><span class="sxs-lookup"><span data-stu-id="d37dd-109">Structure</span></span>                                  | <span data-ttu-id="d37dd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d37dd-110">Description</span></span>                                                                                                            |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d37dd-111">**smiCNTR64**</span><span class="sxs-lookup"><span data-stu-id="d37dd-111">**smiCNTR64**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smicntr64)         | <span data-ttu-id="d37dd-112">Contiene un valor entero de 64 bits sin signo que representa un contador.</span><span class="sxs-lookup"><span data-stu-id="d37dd-112">Contains a 64-bit unsigned integer value that represents a counter.</span></span>                                                    |
| [<span data-ttu-id="d37dd-113">**smiOCTETS**</span><span class="sxs-lookup"><span data-stu-id="d37dd-113">**smiOCTETS**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)         | <span data-ttu-id="d37dd-114">Contiene un puntero a una cadena de octeto SNMP de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="d37dd-114">Contains a pointer to an SNMP octet string of variable length.</span></span>                                                         |
| [<span data-ttu-id="d37dd-115">**smiOID**</span><span class="sxs-lookup"><span data-stu-id="d37dd-115">**smiOID**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)               | <span data-ttu-id="d37dd-116">Contiene un puntero a una matriz de longitud variable de los subidentificadores que están asociados a un objeto con nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="d37dd-116">Contains a pointer to a variable length array of the subidentifiers that are associated with a specified named object.</span></span> |
| [<span data-ttu-id="d37dd-117">**smiVALUE**</span><span class="sxs-lookup"><span data-stu-id="d37dd-117">**smiVALUE**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)           | <span data-ttu-id="d37dd-118">Representa el valor que está asociado a un nombre de variable en una entrada de enlace de variable.</span><span class="sxs-lookup"><span data-stu-id="d37dd-118">Represents the value that is associated with a variable name in a variable binding entry.</span></span>                              |
| [<span data-ttu-id="d37dd-119">**smiVENDORINFO**</span><span class="sxs-lookup"><span data-stu-id="d37dd-119">**smiVENDORINFO**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smivendorinfo) | <span data-ttu-id="d37dd-120">Contiene información sobre la implementación de Microsoft de WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="d37dd-120">Contains information about the Microsoft implementation of WinSNMP.</span></span>                                                    |



 

 

 
---
title: Códigos de error WinSNMP
description: Códigos de error WinSNMP
ms.assetid: 03b13b82-a31c-47e2-8b4d-17dcc4d19e56
keywords:
- Códigos de error WinSNMP SNMP
- Códigos de error SNMP, WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d3cff7bd1e534f5f9c1fb0ae2ea2687d2ba99a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488146"
---
# <a name="winsnmp-error-codes"></a><span data-ttu-id="6e3fd-105">Códigos de error WinSNMP</span><span class="sxs-lookup"><span data-stu-id="6e3fd-105">WinSNMP Error Codes</span></span>

<span data-ttu-id="6e3fd-106">\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-106">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6e3fd-107">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-107">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6e3fd-108">En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]</span><span class="sxs-lookup"><span data-stu-id="6e3fd-108">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

> [!Note]  
> <span data-ttu-id="6e3fd-109">Los errores descritos en este tema son distintos de los códigos de error SNMP definidos por las RFC pertinentes.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-109">The errors described in this topic are distinct from the SNMP error codes defined by the relevant RFCs.</span></span>

 

<span data-ttu-id="6e3fd-110">Todas las funciones WinSNMP devuelven el valor **snmpapi \_ error** si se produce un error en la función.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-110">All WinSNMP functions return the value **SNMPAPI\_FAILURE** if the function fails.</span></span> <span data-ttu-id="6e3fd-111">La aplicación WinSNMP debe llamar inmediatamente a la función [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) para recuperar la información de error extendida cuando se produce un error en una función WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-111">The WinSNMP application must immediately call the [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) function to retrieve extended error information when a WinSNMP function fails.</span></span> <span data-ttu-id="6e3fd-112">En la tabla siguiente se enumeran los temas que describen los códigos de error extendidos devueltos por las funciones WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-112">The following table lists topics that discuss extended error codes returned by WinSNMP functions.</span></span>



| <span data-ttu-id="6e3fd-113">Tema</span><span class="sxs-lookup"><span data-stu-id="6e3fd-113">Topic</span></span>                                                        | <span data-ttu-id="6e3fd-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e3fd-114">Description</span></span>                                             |
|--------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="6e3fd-115">Códigos de error comunes de WinSNMP</span><span class="sxs-lookup"><span data-stu-id="6e3fd-115">WinSNMP Common Error Codes</span></span>](winsnmp-common-error-codes.md) | <span data-ttu-id="6e3fd-116">Describe los códigos de error comunes de la API WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-116">Describes common error codes for the WinSNMP API.</span></span>       |
| [<span data-ttu-id="6e3fd-117">Errores de transporte de red</span><span class="sxs-lookup"><span data-stu-id="6e3fd-117">Network Transport Errors</span></span>](network-transport-errors.md)     | <span data-ttu-id="6e3fd-118">Describe los errores de transporte de red para la API WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-118">Describes network transport errors for the WinSNMP API.</span></span> |



 

<span data-ttu-id="6e3fd-119">Los errores WinSNMP que transmiten información específica del contexto se incluyen en la página de referencia de la función.</span><span class="sxs-lookup"><span data-stu-id="6e3fd-119">The WinSNMP errors that convey context-specific information are included in the function reference page.</span></span>

 

 
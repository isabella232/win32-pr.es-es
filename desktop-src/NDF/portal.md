---
title: Marco de diagnóstico de red
description: El marco de diagnóstico de redes (NDF) proporciona a los desarrolladores de aplicaciones y componentes una manera de simplificar la solución de problemas de red para los usuarios.
ms.assetid: 61dfb66b-4bc6-43a9-ad61-698f5cd67f4a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0342ee4cb285f0a0f1c76c74b3bdc5b412b07e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075429"
---
# <a name="network-diagnostics-framework"></a><span data-ttu-id="fa751-103">Marco de diagnóstico de red</span><span class="sxs-lookup"><span data-stu-id="fa751-103">Network Diagnostics Framework</span></span>

## <a name="purpose"></a><span data-ttu-id="fa751-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="fa751-104">Purpose</span></span>

<span data-ttu-id="fa751-105">El marco de diagnóstico de redes (NDF) proporciona a los desarrolladores de aplicaciones y componentes una manera de simplificar la solución de problemas de red para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="fa751-105">The Network Diagnostics Framework (NDF) provides a way for component and application developers to simplify network troubleshooting for users.</span></span> <span data-ttu-id="fa751-106">Los usuarios pueden intentar diagnosticar y reparar un problema de red mediante una sola herramienta de solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="fa751-106">Users can attempt to diagnose and repair a network problem using a single troubleshooting tool.</span></span>

<span data-ttu-id="fa751-107">Microsoft proporciona clases auxiliares de NDF, algunas de las cuales son extensibles para que los desarrolladores puedan crear unidades de solución de problemas llamadas extensiones de clase auxiliar para proporcionar diagnósticos más detallados específicos de determinados componentes de software o hardware.</span><span class="sxs-lookup"><span data-stu-id="fa751-107">Microsoft provides NDF helper classes, some of which are extensible so that developers can create troubleshooting units called helper class extensions to provide more detailed diagnoses specific to particular software or hardware components.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="fa751-108">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="fa751-108">Where applicable</span></span>

<span data-ttu-id="fa751-109">El software de un proveedor que se basa en la conectividad de red puede usar NDF.</span><span class="sxs-lookup"><span data-stu-id="fa751-109">NDF can be used by any vendor's software which relies on network connectivity.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="fa751-110">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="fa751-110">Developer audience</span></span>

<span data-ttu-id="fa751-111">La API NDF está diseñada para desarrolladores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="fa751-111">The NDF API is designed for C/C++ developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="fa751-112">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="fa751-112">Run-time requirements</span></span>

<span data-ttu-id="fa751-113">NDF está disponible para equipos que ejecutan Windows Vista, Windows Server 2008 o posterior.</span><span class="sxs-lookup"><span data-stu-id="fa751-113">NDF is available for computers running Windows Vista, Windows Server 2008, or later.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fa751-114">En esta sección</span><span class="sxs-lookup"><span data-stu-id="fa751-114">In this section</span></span>



| <span data-ttu-id="fa751-115">Tema</span><span class="sxs-lookup"><span data-stu-id="fa751-115">Topic</span></span>                                                                       | <span data-ttu-id="fa751-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa751-116">Description</span></span>                                                                                                                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa751-117">Acerca de NDF</span><span class="sxs-lookup"><span data-stu-id="fa751-117">About NDF</span></span>](about-ndf.md)<br/>                                       | <span data-ttu-id="fa751-118">Proporciona un resumen general de la tecnología NDF.</span><span class="sxs-lookup"><span data-stu-id="fa751-118">Provides a general summary of the NDF technology.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="fa751-119">Uso de NDF</span><span class="sxs-lookup"><span data-stu-id="fa751-119">Using NDF</span></span>](using-ndf.md)<br/>                                       | <span data-ttu-id="fa751-120">Proporciona información y ejemplos sobre el uso de la funcionalidad NDF, así como la forma de ampliar esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="fa751-120">Provides information and examples on using NDF functionality, as well as how to extend this functionality.</span></span><br/>                                                                                    |
| [<span data-ttu-id="fa751-121">Referencia NDF</span><span class="sxs-lookup"><span data-stu-id="fa751-121">NDF Reference</span></span>](ndf-reference.md)<br/>                               | <span data-ttu-id="fa751-122">Proporciona información sobre enumeraciones, funciones, interfaces y estructuras que admiten el uso de NDF, así como información sobre las clases auxiliares extensibles proporcionadas por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fa751-122">Provides information about enumerations, functions, interfaces, and structures that support the use of NDF, as well as information about the extensible helper classes provided by Microsoft.</span></span><br/> |
| [<span data-ttu-id="fa751-123">Seguimiento de red en Windows 7</span><span class="sxs-lookup"><span data-stu-id="fa751-123">Network Tracing in Windows 7</span></span>](network-tracing-in-windows-7.md)<br/> | <span data-ttu-id="fa751-124">Describe las herramientas y el seguimiento de la red que se van a usar para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="fa751-124">Discusses network tracing and tools to use for troubleshooting.</span></span><br/>                                                                                                                               |



 

 

 






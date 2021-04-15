---
description: Un proveedor de servicios multimedia debe implementar un subconjunto mínimo de interfaces MSPI ITMSPAddress ITTerminalSupport ITStreamControl y ITStream.
ms.assetid: 59560bdf-953e-48e8-b565-46c3e0123c7e
title: Escritura de un proveedor de servicios multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782dddb9a87725bde7c104d459b71204a04de018
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361832"
---
# <a name="writing-a-media-service-provider"></a><span data-ttu-id="d448b-103">Escritura de un proveedor de servicios multimedia</span><span class="sxs-lookup"><span data-stu-id="d448b-103">Writing a Media Service Provider</span></span>

<span data-ttu-id="d448b-104">Un proveedor de servicios multimedia debe implementar un subconjunto mínimo de interfaces MSPI: [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)y [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span><span class="sxs-lookup"><span data-stu-id="d448b-104">A media service provider must implement a minimum subset of MSPI interfaces: [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol), and [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span></span> <span data-ttu-id="d448b-105">La compatibilidad con subsecuencias es opcional.</span><span class="sxs-lookup"><span data-stu-id="d448b-105">SubStream support is optional.</span></span> <span data-ttu-id="d448b-106">Además, un MSP determinado puede implementar métodos adicionales, como los controles necesarios para el hardware especializado.</span><span class="sxs-lookup"><span data-stu-id="d448b-106">In addition, a given MSP may implement additional methods, such as controls required for specialized hardware.</span></span>

<span data-ttu-id="d448b-107">Los siguientes documentos materiales:</span><span class="sxs-lookup"><span data-stu-id="d448b-107">The following material documents:</span></span>

-   <span data-ttu-id="d448b-108">Las [clases base de TAPI 3 MSP](tapi-3-msp-base-classes.md), que son un conjunto de clases de C++ diseñado para simplificar la tarea de crear un MSP basado en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d448b-108">The [TAPI 3 MSP Base Classes](tapi-3-msp-base-classes.md), which are a set of C++ classes designed to simplify the task of building a DirectShow-based MSP.</span></span> <span data-ttu-id="d448b-109">Las clases base implementan todas las interfaces de MSPI de forma genérica.</span><span class="sxs-lookup"><span data-stu-id="d448b-109">The base classes implement all the MSPI interfaces in a generic manner.</span></span> <span data-ttu-id="d448b-110">Distintos MSP pueden invalidar funciones específicas de MSP y proporcionar sus propias implementaciones.</span><span class="sxs-lookup"><span data-stu-id="d448b-110">Different MSPs can override MSP-specific functions and provide their own implementations.</span></span>
-   <span data-ttu-id="d448b-111">El [Administrador de terminales TAPI 3](tapi-3-terminal-manager.md), que proporciona interfaces y métodos usados por un MSP para controlar los terminales.</span><span class="sxs-lookup"><span data-stu-id="d448b-111">The [TAPI 3 Terminal Manager](tapi-3-terminal-manager.md), which provides interfaces and methods used by an MSP to control terminals.</span></span>
-   <span data-ttu-id="d448b-112">[Terminales conectables](writing-a-pluggable-terminal.md), que permiten a una aplicación en lugar de a un MSP crear terminales.</span><span class="sxs-lookup"><span data-stu-id="d448b-112">[Pluggable Terminals](writing-a-pluggable-terminal.md), which allow an application instead of an MSP to create terminals.</span></span> <span data-ttu-id="d448b-113">Los desarrolladores que ya tienen experiencia en escribir proveedores de servicios serán los creadores principales de terminales conectables.</span><span class="sxs-lookup"><span data-stu-id="d448b-113">Developers who are already experienced at writing service providers will be the primary creators of pluggable terminals.</span></span> <span data-ttu-id="d448b-114">La versión inicial implementada para esta versión está destinada a las aplicaciones de servidor de conferencias que necesitan agregar clientes que no son de Windows 2000 o que no son de multidifusión a conferencias de multidifusión SDP/IP de varios usuarios de varias partes.</span><span class="sxs-lookup"><span data-stu-id="d448b-114">The initial version implemented for this release is aimed at conferencing server applications that need to add non-Windows 2000 or non-multicast clients to TAPI 3 multi-party SDP/IP multicast conferences.</span></span>

 

 

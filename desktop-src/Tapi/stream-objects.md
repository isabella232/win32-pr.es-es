---
description: Los objetos de secuencia son una abstracción de la secuencia de medios o las secuencias asociadas a una sesión de llamada.
ms.assetid: 4bd7a305-69ff-4892-bf03-df9c6479adab
title: Objetos de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb89dbacf73baaffbca9aa3791aa73937a69e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687803"
---
# <a name="stream-objects"></a><span data-ttu-id="f7e31-103">Objetos de secuencia</span><span class="sxs-lookup"><span data-stu-id="f7e31-103">Stream Objects</span></span>

<span data-ttu-id="f7e31-104">Los objetos de secuencia son una abstracción de la secuencia de medios o las secuencias asociadas a una sesión de llamada.</span><span class="sxs-lookup"><span data-stu-id="f7e31-104">Stream objects are an abstraction of the media stream or streams associated with a call session.</span></span> <span data-ttu-id="f7e31-105">Las interfaces y los métodos expuestos en los objetos Stream y substream permiten a una aplicación ejercitar controles muy detallados, como pausar una secuencia, agregar nuevos tipos de medios a una sesión de comunicaciones o ajustar el volumen de audio de un participante de conferencia determinado.</span><span class="sxs-lookup"><span data-stu-id="f7e31-105">The interfaces and methods exposed on stream and substream objects allow an application to exercise very detailed controls such as pausing a stream, adding new media types to a communications session, or adjusting the audio volume of a particular conference participant.</span></span>

<span data-ttu-id="f7e31-106">Los dos tipos principales de Stream son la secuencia y la subsecuencia.</span><span class="sxs-lookup"><span data-stu-id="f7e31-106">The two main types of stream are the stream and the substream.</span></span> <span data-ttu-id="f7e31-107">Las interfaces y los métodos de una implementación estándar son similares para ambos, pero el subflujo permite un nivel de control inferior.</span><span class="sxs-lookup"><span data-stu-id="f7e31-107">The interfaces and methods of a standard implementation are similar for both, but substreaming allowing a lower level of control.</span></span> <span data-ttu-id="f7e31-108">Todos los proveedores de servicios multimedia (MSP) deben implementar las interfaces básicas de control de secuencias, pero la compatibilidad con subsecuencias es opcional.</span><span class="sxs-lookup"><span data-stu-id="f7e31-108">All media service providers (MSPs) must implement the basic stream control interfaces, but support for substreams is optional.</span></span>

<span data-ttu-id="f7e31-109">Además, algunos proveedores de servicios implementan [interfaces específicas del proveedor](provider-specific-interfaces.md) para las secuencias.</span><span class="sxs-lookup"><span data-stu-id="f7e31-109">In addition, some service providers implement [provider-specific interfaces](provider-specific-interfaces.md) for streams.</span></span> <span data-ttu-id="f7e31-110">Por ejemplo, IPConf MSP proporciona controles de nivel de participante.</span><span class="sxs-lookup"><span data-stu-id="f7e31-110">For example, the IPConf MSP provides participant level controls.</span></span> <span data-ttu-id="f7e31-111">Consulte [IPCONF MSP interfaces](ipconf-msp-interfaces.md) para obtener un resumen.</span><span class="sxs-lookup"><span data-stu-id="f7e31-111">See [IPConf MSP Interfaces](ipconf-msp-interfaces.md) for a summary.</span></span> <span data-ttu-id="f7e31-112">Para otras interfaces que podrían implementarse, vea la documentación del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="f7e31-112">For other interfaces that might be implemented, see the service provider's documentation.</span></span>

<span data-ttu-id="f7e31-113">MSP y TAPI crean objetos de secuencia para una llamada durante la configuración inicial de una sesión de entrada o de salida.</span><span class="sxs-lookup"><span data-stu-id="f7e31-113">The MSP and TAPI create stream objects for a call during initial setup of an outgoing or incoming session.</span></span> <span data-ttu-id="f7e31-114">La aplicación es responsable de identificar los terminales adecuados para estos flujos y seleccionar los terminales en los flujos.</span><span class="sxs-lookup"><span data-stu-id="f7e31-114">The application is responsible for identifying appropriate terminals for these streams, and selecting the terminals onto the streams.</span></span>

<span data-ttu-id="f7e31-115">Tenga en cuenta que, en algunos casos, un MSP puede requerir que la aplicación detenga o PAUSE las secuencias antes de ciertas operaciones de la sesión de llamada.</span><span class="sxs-lookup"><span data-stu-id="f7e31-115">Note that in some cases an MSP may require that the application stop or pause streams prior to certain call session operations.</span></span>

<span data-ttu-id="f7e31-116">Las interfaces de secuencia se documentan en la referencia de la [interfaz del proveedor de servicios multimedia (MSPI)](media-service-provider-interface-mspi-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f7e31-116">The stream interfaces are documented in the [Media Service Provider Interface (MSPI) Reference](media-service-provider-interface-mspi-reference.md).</span></span>

<span data-ttu-id="f7e31-117">En el ejemplo de [selección de un](select-a-terminal.md) código de terminal se muestra un ejemplo de cómo enumerar secuencias y seleccionar terminales en ellas.</span><span class="sxs-lookup"><span data-stu-id="f7e31-117">The [Select a Terminal](select-a-terminal.md) code example shows an example of enumerating streams and selecting terminals onto them.</span></span>

 

 




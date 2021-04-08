---
description: Las clases de dispositivos simplifican el desarrollo al permitir que los programadores traten los dispositivos que tienen propiedades similares de manera similar.
ms.assetid: 061f3037-1c71-4da1-88d7-29906c136d7b
title: Dispositivo (clase) (TAPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560f95b40ffa34f5e02ee7857928b75425fc7ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001933"
---
# <a name="device-class"></a><span data-ttu-id="3d4f2-103">Clase de dispositivo</span><span class="sxs-lookup"><span data-stu-id="3d4f2-103">Device Class</span></span>

<span data-ttu-id="3d4f2-104">Las clases de dispositivos simplifican el desarrollo al permitir que los programadores traten los dispositivos que tienen propiedades similares de manera similar.</span><span class="sxs-lookup"><span data-stu-id="3d4f2-104">Device classes simplify development by letting programmers treat devices that have similar properties in a similar manner.</span></span> <span data-ttu-id="3d4f2-105">Por ejemplo, un teléfono digital de una oficina normalmente tiene más capacidades que un auricular estándar en casa, pero ambos responden de forma muy similar a un conjunto básico de funciones y ambos pertenecen a una clase de dispositivo de teléfono.</span><span class="sxs-lookup"><span data-stu-id="3d4f2-105">For example, a digital phone in an office typically has more capabilities than a standard handset in a home, but both respond in much the same way to a basic set of functions, and both belong to a phone device class.</span></span> <span data-ttu-id="3d4f2-106">Las clases de dispositivos ayudan a que TAPI sea extensible al proporcionar un marco desde el que clasificar y admitir nuevos equipos.</span><span class="sxs-lookup"><span data-stu-id="3d4f2-106">Device classes help make TAPI extensible by providing a framework from which to classify and support new equipment.</span></span>

<span data-ttu-id="3d4f2-107">Vea [clases de dispositivos TAPI](./tapi-device-classes.md) para las clases que TAPI ha predefinido.</span><span class="sxs-lookup"><span data-stu-id="3d4f2-107">See [TAPI Device Classes](./tapi-device-classes.md) for classes that TAPI has predefined.</span></span> <span data-ttu-id="3d4f2-108">Un proveedor de servicios puede implementar y definir clases de dispositivo adicionales para el equipo que admite.</span><span class="sxs-lookup"><span data-stu-id="3d4f2-108">A service provider may implement and define additional device classes for the equipment it supports.</span></span> <span data-ttu-id="3d4f2-109">Una aplicación nunca necesita saber qué proveedor de servicios controla qué dispositivo, pero puede requerir información sobre el control de las nuevas clases de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="3d4f2-109">An application never needs to know which service provider controls which device, but may require information on the control of new device classes.</span></span>

<span data-ttu-id="3d4f2-110">Un proveedor de servicios implementa una clase de dispositivo mediante la asignación de solicitudes a comandos de dispositivo reales.</span><span class="sxs-lookup"><span data-stu-id="3d4f2-110">A service provider implements a device class by mapping requests into actual device commands.</span></span> <span data-ttu-id="3d4f2-111">Por ejemplo, cuando el proveedor de servicios para un módem compatible con Hayes recibe un comando que se pasa a través de TAPISVR para realizar una llamada, envía los comandos clásicos AT al módem.</span><span class="sxs-lookup"><span data-stu-id="3d4f2-111">For example, when the service provider for a Hayes-compatible modem receives a command passed through TAPISVR to make a call, it sends classic AT commands to the modem.</span></span>

<span data-ttu-id="3d4f2-112">La interfaz del proveedor de servicios se puede asignar a una amplia gama de entornos, incluidos los que tradicionalmente no se han considerado como pertenecientes a la telefonía.</span><span class="sxs-lookup"><span data-stu-id="3d4f2-112">The service provider interface can be mapped to a wide range of environments, including those not traditionally thought of as belonging to telephony.</span></span> <span data-ttu-id="3d4f2-113">Un ejemplo es la conferencia multimedia a través de una red basada en IP, como Internet.</span><span class="sxs-lookup"><span data-stu-id="3d4f2-113">An example is multimedia conferencing over an IP-based network such as the Internet.</span></span>

<span data-ttu-id="3d4f2-114">Los desarrolladores de aplicaciones deben tener en cuenta la existencia de otras aplicaciones que pueden compartir servicios de telefonía.</span><span class="sxs-lookup"><span data-stu-id="3d4f2-114">Application developers should keep in mind the existence of other applications that may share telephony services.</span></span>

 

 

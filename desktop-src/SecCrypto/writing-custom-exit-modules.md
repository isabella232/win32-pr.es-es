---
description: Los módulos de salida personalizados deben implementar la interfaz ICertExit, a la que llama el motor del servidor.
ms.assetid: 509e7945-b656-4c4c-b5eb-45fbe80377c7
title: Escribir módulos de salida personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81798996059e878ef11dbcdf290298094d0849cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668322"
---
# <a name="writing-custom-exit-modules"></a><span data-ttu-id="a51d7-103">Escribir módulos de salida personalizados</span><span class="sxs-lookup"><span data-stu-id="a51d7-103">Writing Custom Exit Modules</span></span>

<span data-ttu-id="a51d7-104">Los módulos de salida personalizados deben implementar la interfaz [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) , a la que llama el motor del servidor.</span><span class="sxs-lookup"><span data-stu-id="a51d7-104">Custom exit modules must implement the [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) interface, which is called by the server engine.</span></span> <span data-ttu-id="a51d7-105">El motor de servidor llama al método [**ICertExit:: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) cuando se carga el módulo de salida.</span><span class="sxs-lookup"><span data-stu-id="a51d7-105">The [**ICertExit::Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) method is called by the server engine when the exit module is loaded.</span></span> <span data-ttu-id="a51d7-106">Permite que el módulo de salida realice la inicialización y devuelve un valor que informa al motor de servidor de los tipos de eventos para los que desea recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="a51d7-106">It allows the exit module to perform initialization and returns a value that informs the server engine of the kinds of events for which it wants notification.</span></span> <span data-ttu-id="a51d7-107">El método [**ICertExit:: getDescription**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) debe devolver una cadena de Descripción cuando el motor del servidor lo solicite.</span><span class="sxs-lookup"><span data-stu-id="a51d7-107">The [**ICertExit::GetDescription**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) method must return a description string when the server engine requests it.</span></span> <span data-ttu-id="a51d7-108">El motor del servidor llama al método [**ICertExit:: Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) para notificar al módulo de salida que se ha producido un evento.</span><span class="sxs-lookup"><span data-stu-id="a51d7-108">The [**ICertExit::Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) method is called by the server engine to notify the exit module that an event has occurred.</span></span>

<span data-ttu-id="a51d7-109">Los módulos de salida pueden llamar a la interfaz [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) , que admite muchos de los mismos métodos que la interfaz [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) , con la excepción de los métodos [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) y [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) .</span><span class="sxs-lookup"><span data-stu-id="a51d7-109">Exit modules can call the [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) interface, which supports many of the same methods as the [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) interface, with the exception of the [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) and [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) methods.</span></span>

<span data-ttu-id="a51d7-110">Para obtener información sobre cómo quitar el módulo de salida existente e instalar uno nuevo, vea el tema de personalización del módulo de salida en la ayuda de.</span><span class="sxs-lookup"><span data-stu-id="a51d7-110">For information about removing the existing exit module and installing a new one, see the Exit Module Customization topic in Help.</span></span>

 

 




---
description: Desarrollar componentes en cola
ms.assetid: 867b7512-82ad-4877-8675-aa2d7e62ff8a
title: Desarrollar componentes en cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8808ef3e6cba8ff561dd94473fca8f00631081f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807183"
---
# <a name="developing-queued-components"></a><span data-ttu-id="90c18-103">Desarrollar componentes en cola</span><span class="sxs-lookup"><span data-stu-id="90c18-103">Developing Queued Components</span></span>

<span data-ttu-id="90c18-104">El servicio de componentes en cola de COM+ requiere que todos los métodos de aplicación solo contengan \[ \] parámetros in, sin valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="90c18-104">The COM+ queued components service requires all application methods to contain only \[in\] parameters, with no return values.</span></span> <span data-ttu-id="90c18-105">Dado que el objeto de servidor no está necesariamente disponible cuando el cliente realiza la llamada, se pueden devolver resultados del servidor mediante el envío de un mensaje que cree otro objeto.</span><span class="sxs-lookup"><span data-stu-id="90c18-105">Because the server object is not necessarily available when the client makes the call, server results can be returned by sending a message that creates another object.</span></span> <span data-ttu-id="90c18-106">De esta manera, la comunicación bidireccional no se produce en todos los casos, sino solo cuando es necesario, mediante una serie de mensajes unidireccionales entre los objetos.</span><span class="sxs-lookup"><span data-stu-id="90c18-106">In this way, two-way communication occurs not in every case but only when it is required, by a series of one-way messages between objects.</span></span>

<span data-ttu-id="90c18-107">Para usar el servicio de componentes en cola de COM+, debe tener el servicio de [Message Queue Server](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) ya instalado.</span><span class="sxs-lookup"><span data-stu-id="90c18-107">To use the COM+ queued components service, you must have the [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) service already installed.</span></span> <span data-ttu-id="90c18-108">Message Queue Server no se instala automáticamente.</span><span class="sxs-lookup"><span data-stu-id="90c18-108">Message Queuing is not installed automatically.</span></span> <span data-ttu-id="90c18-109">Message Queue Server debe estar seleccionado durante la instalación del sistema operativo o mediante **Agregar o quitar programas**.</span><span class="sxs-lookup"><span data-stu-id="90c18-109">Message Queuing must be selected during the operating system setup or by using **Add/Remove programs**.</span></span> <span data-ttu-id="90c18-110">Se crea automáticamente un certificado interno de Message Queue Server al iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="90c18-110">An internal Message Queuing certificate is created automatically at logon.</span></span>

<span data-ttu-id="90c18-111">Los temas que se describen en la tabla siguiente proporcionan consideraciones adicionales para las situaciones más especializadas.</span><span class="sxs-lookup"><span data-stu-id="90c18-111">The topics described in the following table provide additional considerations for more specialized situations.</span></span>



| <span data-ttu-id="90c18-112">Tema</span><span class="sxs-lookup"><span data-stu-id="90c18-112">Topic</span></span>                                                                                           | <span data-ttu-id="90c18-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="90c18-113">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90c18-114">[Pasar objetos como parámetros](passing-objects-as-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="90c18-114">[Passing Objects as Parameter](passing-objects-as-parameters.md)s</span></span><br/>                   | <span data-ttu-id="90c18-115">Describe cómo pasar objetos como \[ parámetros in \] a los componentes en cola.</span><span class="sxs-lookup"><span data-stu-id="90c18-115">Describes how to pass objects as \[in\] parameters to queued components.</span></span><br/>                    |
| [<span data-ttu-id="90c18-116">Limitaciones de seguridad en el modo de grupo de trabajo</span><span class="sxs-lookup"><span data-stu-id="90c18-116">Security Limitations in Workgroup Mode</span></span>](security-limitations-in-workgroup-mode.md)<br/> | <span data-ttu-id="90c18-117">Describe las limitaciones en el uso de la autenticación de Message Queue Server en el modo de grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="90c18-117">Describes limitations on the use of Message Queuing authentication in workgroup mode.</span></span><br/>       |
| [<span data-ttu-id="90c18-118">Consideraciones sobre los subprocesos</span><span class="sxs-lookup"><span data-stu-id="90c18-118">Threading Considerations</span></span>](threading-considerations.md)<br/>                             | <span data-ttu-id="90c18-119">Describe problemas específicos relacionados con el paso de punteros de interfaz de la grabadora entre subprocesos.</span><span class="sxs-lookup"><span data-stu-id="90c18-119">Describes specific concerns related to passing recorder interface pointers between threads.</span></span><br/> |
| [<span data-ttu-id="90c18-120">Recibir una respuesta</span><span class="sxs-lookup"><span data-stu-id="90c18-120">Receiving a Response</span></span>](receiving-a-response.md)<br/>                                     | <span data-ttu-id="90c18-121">Describe cómo construir una respuesta a una llamada de componente en cola.</span><span class="sxs-lookup"><span data-stu-id="90c18-121">Describes how to construct a response to a queued component call.</span></span><br/>                           |



 

 

 





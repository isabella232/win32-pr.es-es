---
description: Información general sobre el control de errores al usar las interfaces de programación de aplicaciones (API) de StylusInput.
ms.assetid: 7d7ff5b2-3eda-4570-96fe-b3b8f41ff69b
title: Consideraciones sobre el control de errores de la API de StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fa582a8dbf531588f6d3d0c142c4ec7b40a058
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001194"
---
# <a name="error-handling-considerations-for-the-stylusinput-api"></a><span data-ttu-id="d55be-103">Consideraciones sobre el control de errores de la API de StylusInput</span><span class="sxs-lookup"><span data-stu-id="d55be-103">Error Handling Considerations for the StylusInput API</span></span>

<span data-ttu-id="d55be-104">El objeto [**RealTimeStylus**](realtimestylus-class.md) detecta las excepciones no controladas producidas por un complemento.</span><span class="sxs-lookup"><span data-stu-id="d55be-104">Unhandled exceptions thrown by a plug-in are caught by the [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="d55be-105">Cuando un complemento inicia una excepción, se interrumpe el flujo de datos normal.</span><span class="sxs-lookup"><span data-stu-id="d55be-105">When a plug-in throws an exception, the normal flow of data is interrupted.</span></span> <span data-ttu-id="d55be-106">El objeto **RealTimeStylus** :</span><span class="sxs-lookup"><span data-stu-id="d55be-106">The **RealTimeStylus** object:</span></span>

1.  <span data-ttu-id="d55be-107">Crea un objeto [datoserror](/previous-versions/ms575221(v=vs.100)) (en código administrado).</span><span class="sxs-lookup"><span data-stu-id="d55be-107">Creates an [ErrorData](/previous-versions/ms575221(v=vs.100)) object (in managed code).</span></span>
2.  <span data-ttu-id="d55be-108">Llama al método [**error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) (en el código administrado, el método [Microsoft. StylusInput. IStylusSyncPlugin. error](/previous-versions/ms824754(v=msdn.10)) o [Microsoft. StylusInput. IStylusAsyncPlugin. error](/previous-versions/ms824771(v=msdn.10)) ) del complemento que produjo la excepción.</span><span class="sxs-lookup"><span data-stu-id="d55be-108">Calls the [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) method (in managed code, either the [Microsoft.StylusInput.IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) or [Microsoft.StylusInput.IStylusAsyncPlugin.Error](/previous-versions/ms824771(v=msdn.10)) method) of the plug-in that threw the exception.</span></span>
3.  <span data-ttu-id="d55be-109">Llama al método [**error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) del resto de complementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="d55be-109">Calls the [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) method of the remaining plug-ins in that collection.</span></span>
4.  <span data-ttu-id="d55be-110">Si el complemento que inició la excepción es un complemento sincrónico, el objeto [datoserror](/previous-versions/ms575221(v=vs.100)) (en código administrado) se agrega a la cola de salida.</span><span class="sxs-lookup"><span data-stu-id="d55be-110">If the plug-in that threw the exception is a synchronous plug-in, the [ErrorData](/previous-versions/ms575221(v=vs.100)) object (in managed code) is added to the output queue.</span></span>
5.  <span data-ttu-id="d55be-111">El objeto [**RealTimeStylus**](realtimestylus-class.md) reanuda el procesamiento normal de los datos originales.</span><span class="sxs-lookup"><span data-stu-id="d55be-111">The [**RealTimeStylus**](realtimestylus-class.md) object resumes normal processing of the original data.</span></span>

<span data-ttu-id="d55be-112">Si un complemento produce una excepción de su método de [**error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) , el objeto [**RealTimeStylus**](realtimestylus-class.md) detecta la excepción pero no genera un nuevo objeto [datoserror](/previous-versions/ms575221(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="d55be-112">If a plug-in throws an exception from its [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) method, the [**RealTimeStylus**](realtimestylus-class.md) object catches the exception but does not generate a new [ErrorData](/previous-versions/ms575221(v=vs.100)) object.</span></span> <span data-ttu-id="d55be-113">Para obtener más información sobre cómo se agrega Datoserror a la cola, vea [los datos de complemento y la clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).</span><span class="sxs-lookup"><span data-stu-id="d55be-113">For more information about how ErrorData is added to the queue, see [Plug-in Data and the RealTimeStylus Class](plug-in-data-and-the-realtimestylus-class.md).</span></span>

<span data-ttu-id="d55be-114">El objeto [**RealTimeStylus**](realtimestylus-class.md) no detiene el procesamiento de los datos del flujo de datos del lápiz de Tablet PC cuando uno de sus complementos produce una excepción.</span><span class="sxs-lookup"><span data-stu-id="d55be-114">The [**RealTimeStylus**](realtimestylus-class.md) object does not stop processing data from the tablet pen's data stream when one of its plug-ins throws an exception.</span></span> <span data-ttu-id="d55be-115">Dependiendo del diseño, algunos de los complementos pueden necesitar suscribirse a la notificación [datoserror](/previous-versions/ms575221(v=vs.100)) y modificar su comportamiento cuando se produce una excepción.</span><span class="sxs-lookup"><span data-stu-id="d55be-115">Depending on your design, some of your plug-ins may need to subscribe to the [ErrorData](/previous-versions/ms575221(v=vs.100)) notification and modify their behavior when an exception occurs.</span></span>

 

 

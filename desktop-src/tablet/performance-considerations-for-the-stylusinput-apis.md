---
description: Descripción de las formas de mejorar el rendimiento al usar las interfaces de programación de aplicaciones (API) de StylusInput.
ms.assetid: 2a541715-2d9e-4eb2-ab60-ec95368fca5a
title: Consideraciones de rendimiento para la API de StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 721474f1e1097729246e5d497d20dcab868190a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818099"
---
# <a name="performance-considerations-for-the-stylusinput-api"></a><span data-ttu-id="9995f-103">Consideraciones de rendimiento para la API de StylusInput</span><span class="sxs-lookup"><span data-stu-id="9995f-103">Performance Considerations for the StylusInput API</span></span>

<span data-ttu-id="9995f-104">En la lista siguiente se describen algunas formas de mejorar el rendimiento de las aplicaciones que usan las API de StylusInput.</span><span class="sxs-lookup"><span data-stu-id="9995f-104">The following list describes some ways in which to improve the performance of applications that use the StylusInput APIs.</span></span>

-   <span data-ttu-id="9995f-105">Use la propiedad [Microsoft. StylusInput. IStylusSyncPlugin. Interest](/previous-versions/ms824752(v=msdn.10)) o [Microsoft. StylusInput. IStylusAsyncPlugin. Interest](/previous-versions/ms824769(v=msdn.10)) para suscribirse solo a los datos relevantes para el complemento.</span><span class="sxs-lookup"><span data-stu-id="9995f-105">Use the [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) or [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) property to subscribe only to the data that is relevant to your plug-in.</span></span> <span data-ttu-id="9995f-106">Esto reduce el número total de llamadas al método que realiza el objeto [**RealTimeStylus**](realtimestylus-class.md) y también reduce la complejidad del complemento.</span><span class="sxs-lookup"><span data-stu-id="9995f-106">This reduces the overall number of method calls the [**RealTimeStylus**](realtimestylus-class.md) object makes and also reduces the complexity of your plug-in.</span></span> <span data-ttu-id="9995f-107">El objeto **RealTimeStylus** solo comprueba la propiedad de interés cuando se adjunta el complemento.</span><span class="sxs-lookup"><span data-stu-id="9995f-107">The **RealTimeStylus** object only checks the DataInterest property when the plug-in is attached.</span></span>
-   <span data-ttu-id="9995f-108">Minimizar la complejidad de los complementos sincrónicos. Los complementos sincrónicos generalmente son llamados por el subproceso del objeto [**RealTimeStylus**](realtimestylus-class.md) y pueden contribuir a retrasos en la recopilación de entradas manuscritas.</span><span class="sxs-lookup"><span data-stu-id="9995f-108">Minimize the complexity of synchronous plug-ins. Synchronous plug-ins generally called by the [**RealTimeStylus**](realtimestylus-class.md) object's thread and may contribute to delays in ink collection.</span></span>
-   <span data-ttu-id="9995f-109">Considere la posibilidad de convertir el complemento en asincrónico.</span><span class="sxs-lookup"><span data-stu-id="9995f-109">Consider making your plug-in asynchronous.</span></span> <span data-ttu-id="9995f-110">Si el complemento es complejo y necesita agregar datos personalizados a la cola del objeto [**RealTimeStylus**](realtimestylus-class.md) , considere la posibilidad de usar un modelo **RealTimeStylus** en cascada y agregar el complemento a la colección de complementos sincrónicos del objeto **RealTimeStylus** secundario.</span><span class="sxs-lookup"><span data-stu-id="9995f-110">If your plug-in is complex and needs to add custom data to the [**RealTimeStylus**](realtimestylus-class.md) object's queue, consider using a cascaded **RealTimeStylus** model and adding the plug-in to the secondary **RealTimeStylus** object's synchronous plug-in collection.</span></span> <span data-ttu-id="9995f-111">Para obtener más información sobre el modelo **RealTimeStylus** en cascada, vea [el modelo RealTimeStylus en cascada](the-cascaded-realtimestylus-model.md).</span><span class="sxs-lookup"><span data-stu-id="9995f-111">For more information about the cascaded **RealTimeStylus** model, see [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).</span></span>

 

 

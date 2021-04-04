---
title: Marcas de prioridad
description: La marca de prioridad abre un objeto de almacenamiento en modo de prioridad.
ms.assetid: 85f2df6f-9219-4752-8c17-f219c37a4037
keywords:
- Marcas de prioridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f4af04174ddb6c0ac459a6f7e6841e061b03c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076405"
---
# <a name="priority-flags"></a><span data-ttu-id="a38f3-104">Marcas de prioridad</span><span class="sxs-lookup"><span data-stu-id="a38f3-104">Priority Flags</span></span>

<span data-ttu-id="a38f3-105">La marca de prioridad abre un objeto de almacenamiento en modo de prioridad.</span><span class="sxs-lookup"><span data-stu-id="a38f3-105">The priority flag opens a storage object in priority mode.</span></span> <span data-ttu-id="a38f3-106">Cuando abre un objeto, una aplicación suele trabajar desde una copia de la instantánea, ya que otras aplicaciones también pueden utilizar el objeto al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="a38f3-106">When it opens an object, an application usually works from a snapshot copy because other applications may also be using the object at the same time.</span></span> <span data-ttu-id="a38f3-107">Sin embargo, al abrir un objeto de almacenamiento en modo de prioridad, la aplicación tiene derechos exclusivos para confirmar cambios en el objeto.</span><span class="sxs-lookup"><span data-stu-id="a38f3-107">When opening a storage object in priority mode, however, the application has exclusive rights to commit changes to the object.</span></span>

<span data-ttu-id="a38f3-108">El modo de prioridad permite que una aplicación Lea algunas secuencias del almacenamiento antes de abrir el objeto en un modo que requeriría que el sistema realizara una copia de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="a38f3-108">Priority mode enables an application to read some streams from storage before opening the object in a mode that would require the system to make a snapshot copy.</span></span> <span data-ttu-id="a38f3-109">Dado que la aplicación tiene acceso exclusivo, no tiene que realizar una copia de instantánea del objeto.</span><span class="sxs-lookup"><span data-stu-id="a38f3-109">Because the application has exclusive access, it does not have to make a snapshot copy of the object.</span></span> <span data-ttu-id="a38f3-110">Cuando la aplicación abre posteriormente el objeto en un modo en el que se requiere una copia de instantánea, la aplicación puede excluir los flujos que ya ha leído de la instantánea, lo que reduce la sobrecarga de abrir el objeto.</span><span class="sxs-lookup"><span data-stu-id="a38f3-110">When the application subsequently opens the object in a mode where a snapshot copy is required, the application can exclude the streams it has already read from the snapshot, thereby reducing the overhead of opening the object.</span></span>

<span data-ttu-id="a38f3-111">Dado que otras aplicaciones no pueden confirmar los cambios en un objeto mientras está abierto en modo de prioridad, las aplicaciones deben mantener el objeto en ese modo lo más corto posible.</span><span class="sxs-lookup"><span data-stu-id="a38f3-111">Because other applications cannot commit changes to an object while it is open in priority mode, applications should keep the object in that mode for as short a time as possible.</span></span>

 

 





---
title: Entrando en el estado cargado
description: Entrando en el estado cargado
ms.assetid: 841b6f1a-cf9d-4a7e-9732-0701777a9617
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add74927d107d7f6b9fe2d76856adec6697a00c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774977"
---
# <a name="entering-the-loaded-state"></a><span data-ttu-id="c21d9-103">Entrando en el estado cargado</span><span class="sxs-lookup"><span data-stu-id="c21d9-103">Entering the Loaded State</span></span>

<span data-ttu-id="c21d9-104">Cuando un objeto entra en el estado de carga, se crean las estructuras en memoria que representan el objeto para que se puedan invocar las operaciones en él.</span><span class="sxs-lookup"><span data-stu-id="c21d9-104">When an object enters the loaded state, the in-memory structures representing the object are created so that operations can be invoked on it.</span></span> <span data-ttu-id="c21d9-105">Se carga el controlador del objeto o el servidor en proceso.</span><span class="sxs-lookup"><span data-stu-id="c21d9-105">The object's handler or in-process server is loaded.</span></span> <span data-ttu-id="c21d9-106">Este proceso, al que se hace referencia como *creación de instancias*, se produce cuando se carga un objeto desde el almacenamiento persistente (una transición del estado pasivo al estado cargado) o cuando se crea un objeto por primera vez.</span><span class="sxs-lookup"><span data-stu-id="c21d9-106">This process, referred to as *instantiation*, occurs when an object is loaded from persistent storage (a transition from the passive to the loaded state) or when an object is being created for the first time.</span></span>

<span data-ttu-id="c21d9-107">Internamente, la creación de instancias es un proceso de dos fases.</span><span class="sxs-lookup"><span data-stu-id="c21d9-107">Internally, instantiation is a two-phase process.</span></span> <span data-ttu-id="c21d9-108">Se crea un objeto de la clase adecuada, después del cual se llama a un método en ese objeto para realizar la inicialización y dar acceso a los datos del objeto.</span><span class="sxs-lookup"><span data-stu-id="c21d9-108">An object of the appropriate class is created, after which a method on that object is called to perform initialization and give access to the object's data.</span></span> <span data-ttu-id="c21d9-109">El método de inicialización se define en una de las interfaces admitidas del objeto.</span><span class="sxs-lookup"><span data-stu-id="c21d9-109">The initialization method is defined in one of the object's supported interfaces.</span></span> <span data-ttu-id="c21d9-110">El método de inicialización determinado llamado depende del contexto en el que se crea una instancia del objeto y de la ubicación de los datos de inicialización.</span><span class="sxs-lookup"><span data-stu-id="c21d9-110">The particular initialization method called depends on the context in which the object is being instantiated and the location of the initialization data.</span></span>

 

 





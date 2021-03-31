---
description: Algunos objetos solo admiten un identificador a la vez.
ms.assetid: 3eafd0e0-3923-4489-8a0a-63007dd3183a
title: Solucionar limitaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99caa991b1ffa0a4e0c02ff32225c3260eb4a016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278789"
---
# <a name="handle-limitations"></a><span data-ttu-id="47643-103">Solucionar limitaciones</span><span class="sxs-lookup"><span data-stu-id="47643-103">Handle Limitations</span></span>

<span data-ttu-id="47643-104">Algunos objetos solo admiten un identificador a la vez.</span><span class="sxs-lookup"><span data-stu-id="47643-104">Some objects support only one handle at a time.</span></span> <span data-ttu-id="47643-105">El sistema proporciona el identificador cuando una aplicación crea el objeto e invalida el identificador cuando la aplicación destruye el objeto.</span><span class="sxs-lookup"><span data-stu-id="47643-105">The system provides the handle when an application creates the object and invalidates the handle when the application destroys the object.</span></span> <span data-ttu-id="47643-106">Otros objetos admiten varios identificadores para un único objeto.</span><span class="sxs-lookup"><span data-stu-id="47643-106">Other objects support multiple handles to a single object.</span></span> <span data-ttu-id="47643-107">El sistema operativo quita automáticamente el objeto de la memoria después de cerrarse el último identificador del objeto.</span><span class="sxs-lookup"><span data-stu-id="47643-107">The operating system automatically removes the object from memory after the last handle to the object is closed.</span></span>

<span data-ttu-id="47643-108">El número total de identificadores abiertos en el sistema solo está limitado por la cantidad de memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="47643-108">The total number of open handles in the system is limited only by the amount of memory available.</span></span> <span data-ttu-id="47643-109">Algunos tipos de objetos admiten un número limitado de identificadores por sesión o por proceso.</span><span class="sxs-lookup"><span data-stu-id="47643-109">Some object types support a limited number of handles per session or per process.</span></span>

 

 




---
description: La función SetupSetSourceList abrirá o creará una lista de origen en el sistema de usuarios.
ms.assetid: cda632cf-6c92-48fb-aef1-25b320affd3e
title: Usar la lista de origen de MRU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbecb9e32a554d1818661b1fd7f6e782744c16e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001638"
---
# <a name="using-the-mru-source-list"></a><span data-ttu-id="8ca84-103">Usar la lista de origen de MRU</span><span class="sxs-lookup"><span data-stu-id="8ca84-103">Using the MRU Source List</span></span>

<span data-ttu-id="8ca84-104">La función [**SetupSetSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) abrirá o creará una lista de origen en el sistema del usuario.</span><span class="sxs-lookup"><span data-stu-id="8ca84-104">The [**SetupSetSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) function will open or create a source list on the user's system.</span></span> <span data-ttu-id="8ca84-105">Puede especificar para establecer la lista de usuarios, la lista de sistemas, una combinación de las listas de usuarios y del sistema, o una lista temporal como la lista de origen de MRU.</span><span class="sxs-lookup"><span data-stu-id="8ca84-105">You can specify to set the user list, the system list, a combination of the user and system lists, or a temporary list as the MRU source list.</span></span> <span data-ttu-id="8ca84-106">Si se usa una lista temporal, será la única lista disponible para la aplicación de instalación hasta que se llame a [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) o se llame a **SetupSetSourceList** por segunda vez.</span><span class="sxs-lookup"><span data-stu-id="8ca84-106">If a temporary list is used, it will be the only list available to the setup application until [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) is called, or **SetupSetSourceList** is called a second time.</span></span>

<span data-ttu-id="8ca84-107">Una vez establecida una lista, puede consultar la lista de origen mediante [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) para obtener una matriz de las rutas de acceso de origen.</span><span class="sxs-lookup"><span data-stu-id="8ca84-107">After a list is set, you can query the source list by using [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) to obtain an array of the source paths.</span></span> <span data-ttu-id="8ca84-108">Cuando la matriz de la lista de origen ya no sea necesaria, debe llamar a la función [**SetupFreeSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) para liberar los recursos asignados por [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista).</span><span class="sxs-lookup"><span data-stu-id="8ca84-108">When the source list array is no longer needed, you must call the [**SetupFreeSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) function to free the resources allocated by [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista).</span></span>

<span data-ttu-id="8ca84-109">Para agregar una ruta de acceso a una lista de origen, ya sea una que sea residente en el sistema del usuario o una lista temporal, llame a [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista).</span><span class="sxs-lookup"><span data-stu-id="8ca84-109">To add a path to a source list, either one that is resident on the user's system, or a temporary list, call [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista).</span></span> <span data-ttu-id="8ca84-110">Si la lista de origen especificada no es temporal, el origen permanecerá en el sistema del usuario y será accesible para las instalaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="8ca84-110">If the source list specified is not temporary, that source will remain on the user's system and is accessible to subsequent installations.</span></span>

<span data-ttu-id="8ca84-111">Para quitar una ruta de acceso de la ruta de origen, llame a la función [**SetupRemoveFromSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) .</span><span class="sxs-lookup"><span data-stu-id="8ca84-111">To remove a path from the source path, call the [**SetupRemoveFromSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) function.</span></span>

 

 




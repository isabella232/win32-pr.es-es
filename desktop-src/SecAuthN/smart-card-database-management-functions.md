---
description: Administrar la base de datos de tarjeta inteligente, actualizando la base de datos mediante un contexto de administrador de recursos especificado.
ms.assetid: a2f457e1-c042-42e7-9071-cf0edd68e27a
title: Funciones de administración de bases de datos de tarjeta inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c424494a30c71e15647da773027311ed53a2599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361060"
---
# <a name="smart-card-database-management-functions"></a><span data-ttu-id="ee58c-103">Funciones de administración de bases de datos de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="ee58c-103">Smart Card Database Management Functions</span></span>

<span data-ttu-id="ee58c-104">Las siguientes funciones administran la [*base de datos de tarjeta inteligente*](../secgloss/s-gly.md), actualizando la base de datos mediante un [*contexto de administrador de recursos*](../secgloss/r-gly.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="ee58c-104">The following functions manage the [*smart card database*](../secgloss/s-gly.md), updating the database by using a specified [*resource manager context*](../secgloss/r-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="ee58c-105">La seguridad de la base de datos se mantiene colocando restricciones de acceso en la base de datos, en lugar de agregar mecanismos de seguridad al [*subsistema de tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ee58c-105">Database security is maintained by placing access restrictions on the database, rather than by adding security mechanisms to the [*smart card subsystem*](../secgloss/s-gly.md).</span></span>

 



| <span data-ttu-id="ee58c-106">Tema</span><span class="sxs-lookup"><span data-stu-id="ee58c-106">Topic</span></span>                                                            | <span data-ttu-id="ee58c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee58c-107">Description</span></span>                                                                                                                                                             |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee58c-108">**SCardAddReaderToGroup**</span><span class="sxs-lookup"><span data-stu-id="ee58c-108">**SCardAddReaderToGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardaddreadertogroupa)           | <span data-ttu-id="ee58c-109">Agregue un [*lector*](../secgloss/r-gly.md) a un [*grupo de lectores*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ee58c-109">Add a [*reader*](../secgloss/r-gly.md) to a [*reader group*](../secgloss/r-gly.md).</span></span> |
| [<span data-ttu-id="ee58c-110">**SCardForgetCardType**</span><span class="sxs-lookup"><span data-stu-id="ee58c-110">**SCardForgetCardType**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea)               | <span data-ttu-id="ee58c-111">Quitar una tarjeta inteligente del sistema.</span><span class="sxs-lookup"><span data-stu-id="ee58c-111">Remove a smart card from the system.</span></span>                                                                                                                                    |
| [<span data-ttu-id="ee58c-112">**SCardForgetReader**</span><span class="sxs-lookup"><span data-stu-id="ee58c-112">**SCardForgetReader**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadera)                   | <span data-ttu-id="ee58c-113">Quitar un lector del sistema.</span><span class="sxs-lookup"><span data-stu-id="ee58c-113">Remove a reader from the system.</span></span>                                                                                                                                        |
| [<span data-ttu-id="ee58c-114">**SCardForgetReaderGroup**</span><span class="sxs-lookup"><span data-stu-id="ee58c-114">**SCardForgetReaderGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadergroupa)         | <span data-ttu-id="ee58c-115">Quitar un grupo de lectores del sistema.</span><span class="sxs-lookup"><span data-stu-id="ee58c-115">Remove a reader group from the system.</span></span>                                                                                                                                  |
| [<span data-ttu-id="ee58c-116">**SCardIntroduceCardType**</span><span class="sxs-lookup"><span data-stu-id="ee58c-116">**SCardIntroduceCardType**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea)         | <span data-ttu-id="ee58c-117">Introduzca una nueva tarjeta en el sistema.</span><span class="sxs-lookup"><span data-stu-id="ee58c-117">Introduce a new card to the system.</span></span>                                                                                                                                     |
| [<span data-ttu-id="ee58c-118">**SCardIntroduceReader**</span><span class="sxs-lookup"><span data-stu-id="ee58c-118">**SCardIntroduceReader**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadera)             | <span data-ttu-id="ee58c-119">Introduzca un nuevo lector en el sistema.</span><span class="sxs-lookup"><span data-stu-id="ee58c-119">Introduce a new reader to the system.</span></span>                                                                                                                                   |
| [<span data-ttu-id="ee58c-120">**SCardIntroduceReaderGroup**</span><span class="sxs-lookup"><span data-stu-id="ee58c-120">**SCardIntroduceReaderGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadergroupa)   | <span data-ttu-id="ee58c-121">Introduzca un nuevo grupo de lectores en el sistema.</span><span class="sxs-lookup"><span data-stu-id="ee58c-121">Introduce a new reader group to the system.</span></span>                                                                                                                             |
| [<span data-ttu-id="ee58c-122">**SCardRemoveReaderFromGroup**</span><span class="sxs-lookup"><span data-stu-id="ee58c-122">**SCardRemoveReaderFromGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardremovereaderfromgroupa) | <span data-ttu-id="ee58c-123">Quitar un lector de un grupo de lectores.</span><span class="sxs-lookup"><span data-stu-id="ee58c-123">Remove a reader from a reader group.</span></span>                                                                                                                                    |



 

 

 

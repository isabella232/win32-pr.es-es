---
description: Consultar la base de datos de tarjeta inteligente. Pueden proporcionar una lista de tarjetas inteligentes suministradas por un usuario específico, las interfaces y el proveedor de servicios principal de una tarjeta específica, los grupos de lectores definidos para el sistema y los lectores dentro de un conjunto de grupos de lectores.
ms.assetid: a30cbb99-522c-4752-bfcd-75be608785f1
title: Funciones de consulta de bases de datos de tarjeta inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd74c15eb475d5de9ccce84ba5936b724c0d8d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278264"
---
# <a name="smart-card-database-query-functions"></a><span data-ttu-id="f2fe3-104">Funciones de consulta de bases de datos de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="f2fe3-104">Smart Card Database Query Functions</span></span>

<span data-ttu-id="f2fe3-105">Las siguientes funciones consultan la [*base de datos de tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f2fe3-105">The following functions query the [*smart card database*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="f2fe3-106">Pueden proporcionar una lista de tarjetas inteligentes suministradas por un usuario específico, las interfaces y el [*proveedor de servicios principal*](../secgloss/p-gly.md) de una tarjeta específica, los [*grupos de lectores*](../secgloss/r-gly.md) definidos para el sistema y los [*lectores*](../secgloss/r-gly.md) dentro de un conjunto de grupos de lectores.</span><span class="sxs-lookup"><span data-stu-id="f2fe3-106">They can provide a list of smart cards supplied by a specific user, the interfaces and [*primary service provider*](../secgloss/p-gly.md) of a specific card, the [*reader groups*](../secgloss/r-gly.md) defined for the system, and the [*readers*](../secgloss/r-gly.md) within a set of reader groups.</span></span>

<span data-ttu-id="f2fe3-107">Cuando se usan estas funciones, se puede consultar la base de datos completa de la tarjeta inteligente, o bien se puede restringir la búsqueda estableciendo el [*contexto del administrador de recursos*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f2fe3-107">When you use these functions, you can query the complete smart card database, or you can narrow the search by setting the [*resource manager context*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="f2fe3-108">El contexto del administrador de recursos se establece mediante una llamada a [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) antes de llamar a una función de consulta.</span><span class="sxs-lookup"><span data-stu-id="f2fe3-108">The resource manager context is set by calling [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) before calling a query function.</span></span>

> [!Note]  
> <span data-ttu-id="f2fe3-109">Sin un contexto especificado, es posible que no se pueda tener acceso a cierta información debido a restricciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f2fe3-109">Without a specified context, some information may still be inaccessible due to security restrictions.</span></span>

 



| <span data-ttu-id="f2fe3-110">Tema</span><span class="sxs-lookup"><span data-stu-id="f2fe3-110">Topic</span></span>                                                  | <span data-ttu-id="f2fe3-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2fe3-111">Description</span></span>                                                                                                                                                                          |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2fe3-112">**SCardGetProviderId**</span><span class="sxs-lookup"><span data-stu-id="f2fe3-112">**SCardGetProviderId**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetproviderida)       | <span data-ttu-id="f2fe3-113">Recupera el identificador (GUID) del proveedor de [*servicios principal*](../secgloss/p-gly.md) de la tarjeta especificada.</span><span class="sxs-lookup"><span data-stu-id="f2fe3-113">Retrieve the identifier (GUID) of the [*primary service provider*](../secgloss/p-gly.md) for the given card.</span></span> |
| [<span data-ttu-id="f2fe3-114">**SCardListCards**</span><span class="sxs-lookup"><span data-stu-id="f2fe3-114">**SCardListCards**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistcardsa)               | <span data-ttu-id="f2fe3-115">Recupera una lista de tarjetas introducidas previamente en el sistema por un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="f2fe3-115">Retrieve a list of cards previously introduced to the system by a specific user.</span></span>                                                                                                     |
| [<span data-ttu-id="f2fe3-116">**SCardListInterfaces**</span><span class="sxs-lookup"><span data-stu-id="f2fe3-116">**SCardListInterfaces**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistinterfacesa)     | <span data-ttu-id="f2fe3-117">Recupera los identificadores (GUID) de las interfaces proporcionadas por una tarjeta determinada.</span><span class="sxs-lookup"><span data-stu-id="f2fe3-117">Retrieve the identifiers (GUIDs) of the interfaces supplied by a given card.</span></span>                                                                                                         |
| [<span data-ttu-id="f2fe3-118">**SCardListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="f2fe3-118">**SCardListReaderGroups**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistreadergroupsa) | <span data-ttu-id="f2fe3-119">Recupera una lista de grupos de lector que se han introducido previamente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="f2fe3-119">Retrieve a list of reader groups that have previously been introduced to the system.</span></span>                                                                                                 |
| [<span data-ttu-id="f2fe3-120">**SCardListReaders**</span><span class="sxs-lookup"><span data-stu-id="f2fe3-120">**SCardListReaders**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistreadersa)           | <span data-ttu-id="f2fe3-121">Recupera la lista de lectores dentro de un conjunto de grupos de lectores con nombre.</span><span class="sxs-lookup"><span data-stu-id="f2fe3-121">Retrieve the list of readers within a set of named reader groups.</span></span>                                                                                                                    |



 

 

 

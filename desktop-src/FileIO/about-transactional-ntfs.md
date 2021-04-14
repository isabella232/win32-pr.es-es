---
description: NTFS transaccional (TxF) integra las transacciones en el sistema de archivos NTFS, lo que facilita que los desarrolladores y administradores de aplicaciones controlen correctamente los errores y conserven la integridad de los datos.
ms.assetid: 52341315-0412-4a87-aca0-9adea7aae62f
title: Acerca de NTFS transaccional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcf8cd99dfb1ff18ef7da88d3b3c7b0a647417e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360327"
---
# <a name="about-transactional-ntfs"></a><span data-ttu-id="f6746-103">Acerca de NTFS transaccional</span><span class="sxs-lookup"><span data-stu-id="f6746-103">About Transactional NTFS</span></span>

<span data-ttu-id="f6746-104">\[Microsoft recomienda encarecidamente que los desarrolladores usen medios alternativos para lograr las necesidades de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f6746-104">\[Microsoft strongly recommends developers utilize alternative means to achieve your application s needs.</span></span> <span data-ttu-id="f6746-105">Muchos escenarios para los que se desarrolló TxF se pueden lograr mediante técnicas más sencillas y más fáciles de usar.</span><span class="sxs-lookup"><span data-stu-id="f6746-105">Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques.</span></span> <span data-ttu-id="f6746-106">Además, es posible que TxF no esté disponible en versiones futuras de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f6746-106">Furthermore, TxF may not be available in future versions of Microsoft Windows.</span></span> <span data-ttu-id="f6746-107">Para obtener más información y alternativas a TxF, vea [alternativas al uso de NTFS transaccional](deprecation-of-txf.md).\]</span><span class="sxs-lookup"><span data-stu-id="f6746-107">For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](deprecation-of-txf.md).\]</span></span>

<span data-ttu-id="f6746-108">NTFS transaccional (TxF) integra las transacciones en el sistema de archivos NTFS, lo que facilita que los desarrolladores y administradores de aplicaciones controlen correctamente los errores y conserven la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="f6746-108">Transactional NTFS (TxF) integrates transactions into the NTFS file system, which makes it easier for application developers and administrators to gracefully handle errors and preserve data integrity.</span></span>

<span data-ttu-id="f6746-109">TxF puede participar en transacciones distribuidas que las coordenadas [Coordinador de transacciones distribuidas (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)) , lo que le permite usar TxF para lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f6746-109">TxF can participate in distributed transactions that the [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)) coordinates, which allows you to use TxF for the following:</span></span>

-   <span data-ttu-id="f6746-110">Transacciones que abarcan varios almacenes de datos, por ejemplo, una única transacción para operaciones de archivo y SQL</span><span class="sxs-lookup"><span data-stu-id="f6746-110">Transactions that span multiple data stores, for example, a single transaction for file and SQL operations</span></span>
-   <span data-ttu-id="f6746-111">Transacciones que abarcan varios equipos, por ejemplo, una única transacción para las actualizaciones de archivos en varios equipos</span><span class="sxs-lookup"><span data-stu-id="f6746-111">Transactions that span multiple computers, for example, a single transaction for file updates on multiple computers</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f6746-112">En esta sección</span><span class="sxs-lookup"><span data-stu-id="f6746-112">In this section</span></span>



| <span data-ttu-id="f6746-113">Tema</span><span class="sxs-lookup"><span data-stu-id="f6746-113">Topic</span></span>                                                                                                                 | <span data-ttu-id="f6746-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6746-114">Description</span></span>                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6746-115">Cuándo usar NTFS transaccional</span><span class="sxs-lookup"><span data-stu-id="f6746-115">When to Use Transactional NTFS</span></span>](when-to-use-transactional-ntfs.md)<br/>                                       | <span data-ttu-id="f6746-116">Utilice NTFS transaccional para mantener la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="f6746-116">Use Transactional NTFS to maintain data integrity.</span></span><br/>                                                                        |
| [<span data-ttu-id="f6746-117">Implementar NTFS transaccional</span><span class="sxs-lookup"><span data-stu-id="f6746-117">Deploying Transactional NTFS</span></span>](deploying-transactional-ntfs.md)<br/>                                           | <span data-ttu-id="f6746-118">Control de almacenamiento en caché en NTFS transaccional.</span><span class="sxs-lookup"><span data-stu-id="f6746-118">Caching control in Transactional NTFS.</span></span><br/>                                                                                    |
| [<span data-ttu-id="f6746-119">Cómo usar NTFS transaccional</span><span class="sxs-lookup"><span data-stu-id="f6746-119">How to Use Transactional NTFS</span></span>](how-to-use-transactional-ntfs.md)<br/>                                         | <span data-ttu-id="f6746-120">Administrar identificadores de archivos de transacciones en NTFS transaccional.</span><span class="sxs-lookup"><span data-stu-id="f6746-120">Managing transacted file handles in Transactional NTFS.</span></span><br/>                                                                   |
| [<span data-ttu-id="f6746-121">Conceptos básicos de TxF</span><span class="sxs-lookup"><span data-stu-id="f6746-121">Basic TxF Concepts</span></span>](txf-basic-concepts.md)<br/>                                                               | <span data-ttu-id="f6746-122">Describe la coherencia de lectura confirmada, el aislamiento de lectura confirmada y los conceptos de bloqueo transaccional en NTFS transaccional.</span><span class="sxs-lookup"><span data-stu-id="f6746-122">Describes read-committed consistency, read-committed isolation, and transactional locking concepts in Transactional NTFS.</span></span><br/> |
| [<span data-ttu-id="f6746-123">Consideraciones de programación para NTFS transaccional</span><span class="sxs-lookup"><span data-stu-id="f6746-123">Programming Considerations for Transactional NTFS</span></span>](programming-considerations-for-transacted-fileio-.md)<br/> | <span data-ttu-id="f6746-124">Describe diversas consideraciones de programación para NTFS transaccional.</span><span class="sxs-lookup"><span data-stu-id="f6746-124">Describes various programming considerations for Transactional NTFS.</span></span><br/>                                                      |
| [<span data-ttu-id="f6746-125">Consideraciones de rendimiento para NTFS transaccional</span><span class="sxs-lookup"><span data-stu-id="f6746-125">Performance Considerations for Transactional NTFS</span></span>](performance-considerations-for-transactional-ntfs.md)<br/> | <span data-ttu-id="f6746-126">Recomendaciones para las transacciones de sistema de archivos óptimas.</span><span class="sxs-lookup"><span data-stu-id="f6746-126">Recommendations for optimal file system transactions.</span></span><br/>                                                                     |



 

 


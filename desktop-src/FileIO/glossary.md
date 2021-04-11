---
description: Terminología usada para describir NTFS transaccional (TxF).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44cb060c-e6a6-48d6-bbcf-d8dc1ae8ceb2
title: Glosario de TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee17e9c53b804995e7ef3491b68e963e9311a37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278818"
---
# <a name="txf-glossary"></a><span data-ttu-id="9a0ab-103">Glosario de TxF</span><span class="sxs-lookup"><span data-stu-id="9a0ab-103">TxF Glossary</span></span>

<dl> <dt>

<span data-ttu-id="9a0ab-104"><span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="9a0ab-104"><span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**availability**</span></span>
</dt> <dd>

<span data-ttu-id="9a0ab-105">La disponibilidad significa que un administrador de recursos anulará las transacciones aunque esto interrumpa la coherencia para que el sistema pueda continuar realizando el nuevo trabajo.</span><span class="sxs-lookup"><span data-stu-id="9a0ab-105">Availability means that a resource manager will abort transactions even if that would break consistency so that the system can continue to do new work.</span></span> <span data-ttu-id="9a0ab-106">El administrador de recursos predeterminado fuerza la disponibilidad en el volumen del sistema.</span><span class="sxs-lookup"><span data-stu-id="9a0ab-106">The default resource manager forces availability on the system volume.</span></span> <span data-ttu-id="9a0ab-107">Por ejemplo, si el registro de transacciones está lleno, no se puede Agregar un nuevo espacio de registro de transacciones y una transacción más antigua que se anularía requiere la entrega de un resultado desde un administrador de recursos superior para que se complete una transacción distribuida, el administrador de recursos no esperará el administrador de transacciones superior y anulará la transacción aunque pueda interrumpir la coherencia.</span><span class="sxs-lookup"><span data-stu-id="9a0ab-107">For example, if the transaction log is full, new transaction log space cannot be added, and an older transaction that would be aborted requires an outcome to be delivered from a superior resource manager in order for a distributed transaction to complete, the resource manager will not wait for the superior transaction manager and abort that transaction even though that potentially breaks consistency.</span></span>

</dd> <dt>

<span data-ttu-id="9a0ab-108"><span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**réplica**</span><span class="sxs-lookup"><span data-stu-id="9a0ab-108"><span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**consistency**</span></span>
</dt> <dd>

<span data-ttu-id="9a0ab-109">La coherencia significa que un administrador de recursos producirá un error en las transacciones nuevas si no puede progresar.</span><span class="sxs-lookup"><span data-stu-id="9a0ab-109">Consistency means that a resource manager will fail new transactions if it cannot make forward progress.</span></span> <span data-ttu-id="9a0ab-110">Por ejemplo, si el registro de transacciones está lleno, no se puede Agregar un nuevo espacio de registro de transacciones y una transacción anterior que se anularía requiere que se entregue un resultado desde un administrador de recursos superior para que se complete una transacción distribuida, el administrador de recursos esperará ese resultado.</span><span class="sxs-lookup"><span data-stu-id="9a0ab-110">For example, if the transaction log is full, new transaction log space cannot be added, and an older transaction that would be aborted requires an outcome to be delivered from a superior resource manager in order for a distributed transaction to complete, the resource manager will wait for that outcome.</span></span>

</dd> <dt>

<span data-ttu-id="9a0ab-111"><span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**miniversión**</span><span class="sxs-lookup"><span data-stu-id="9a0ab-111"><span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**miniversion**</span></span>
</dt> <dd>

<span data-ttu-id="9a0ab-112">Una miniversión es una versión de un archivo que un escritor de transacciones crea durante una transacción.</span><span class="sxs-lookup"><span data-stu-id="9a0ab-112">A miniversion is a version of a file that a transacted writer creates during a transaction.</span></span> <span data-ttu-id="9a0ab-113">La miniversión se puede abrir más adelante en la transacción con acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9a0ab-113">The miniversion can be opened later in the transaction with read-only access.</span></span>

</dd> <dt>

<span data-ttu-id="9a0ab-114"><span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**lector de transacciones**</span><span class="sxs-lookup"><span data-stu-id="9a0ab-114"><span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**transacted reader**</span></span>
</dt> <dd>

<span data-ttu-id="9a0ab-115">Un lector de transacciones es un identificador de archivo de transacción abierto con cualquier permiso que forma parte del acceso de lectura genérico, pero no forma parte del acceso de escritura genérico.</span><span class="sxs-lookup"><span data-stu-id="9a0ab-115">A transacted reader is a transacted file handle opened with any permission that is a part of generic read access, but is not part of generic write access.</span></span>

</dd> <dt>

<span data-ttu-id="9a0ab-116"><span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**escritor de transacciones**</span><span class="sxs-lookup"><span data-stu-id="9a0ab-116"><span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**transacted writer**</span></span>
</dt> <dd>

<span data-ttu-id="9a0ab-117">Un escritor de transacciones es un identificador de archivo de transacciones abierto con cualquier permiso que no forma parte del acceso de lectura genérico, pero que forma parte del acceso de escritura genérico.</span><span class="sxs-lookup"><span data-stu-id="9a0ab-117">A transacted writer is a transacted file handle opened with any permission that is not part of generic read access, but is part of generic write access.</span></span>

</dd> </dl>

 

 




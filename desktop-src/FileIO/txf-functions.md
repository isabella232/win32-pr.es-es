---
description: Funciones NTFS (TxF) transaccionales.
ms.assetid: fb6be33c-9d6c-48b2-a4da-31c60af8d972
title: Funciones TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59fa3c9a1323ce77c97ee36390190ea6301d71d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816798"
---
# <a name="txf-functions"></a><span data-ttu-id="448f6-103">Funciones TxF</span><span class="sxs-lookup"><span data-stu-id="448f6-103">TxF Functions</span></span>

<span data-ttu-id="448f6-104">NTFS transaccional (TxF) proporciona las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="448f6-104">Transactional NTFS (TxF) provides the following functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="448f6-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="448f6-105">In this section</span></span>



| <span data-ttu-id="448f6-106">Función</span><span class="sxs-lookup"><span data-stu-id="448f6-106">Function</span></span>                                                                      | <span data-ttu-id="448f6-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="448f6-107">Description</span></span>                                                                                                                  |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="448f6-108">**TxfLogCreateFileReadContext**</span><span class="sxs-lookup"><span data-stu-id="448f6-108">**TxfLogCreateFileReadContext**</span></span>](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext)<br/> | <span data-ttu-id="448f6-109">Crea un contexto que se va a utilizar para leer los registros de replicación.</span><span class="sxs-lookup"><span data-stu-id="448f6-109">Creates a context to be used to read replication records.</span></span><br/>                                                         |
| [<span data-ttu-id="448f6-110">**TxfLogDestroyReadContext**</span><span class="sxs-lookup"><span data-stu-id="448f6-110">**TxfLogDestroyReadContext**</span></span>](/windows/desktop/api/TxfW32/nf-txfw32-txflogdestroyreadcontext)<br/>       | <span data-ttu-id="448f6-111">Cierra un contexto de lectura creado por la función [**TxfLogCreateFileReadContext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext) .</span><span class="sxs-lookup"><span data-stu-id="448f6-111">Closes a read context created by the [**TxfLogCreateFileReadContext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext) function.</span></span><br/> |
| [<span data-ttu-id="448f6-112">**TxfLogReadRecords**</span><span class="sxs-lookup"><span data-stu-id="448f6-112">**TxfLogReadRecords**</span></span>](/windows/desktop/api/TxfW32/nf-txfw32-txflogreadrecords)<br/>                     | <span data-ttu-id="448f6-113">Lee los registros de rehacer del registro.</span><span class="sxs-lookup"><span data-stu-id="448f6-113">Reads the redo records from the log.</span></span><br/>                                                                              |



 

 

 





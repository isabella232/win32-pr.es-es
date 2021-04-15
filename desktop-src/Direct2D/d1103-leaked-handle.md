---
title: Identificador de D1103 filtrado
ms.assetid: 9bb08cd6-104a-4168-b14e-3caec1679388
description: Se creó una interfaz pero no se liberó.
keywords:
- Identificador de D1103 con fugas Direct2D
topic_type:
- apiref
api_name:
- D1103 Leaked Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: cc4b4e43f94bd4ceb5d7a2518879c69bd3ecf8f3
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/27/2021
ms.locfileid: "105661451"
---
# <a name="d1103-leaked-handle"></a><span data-ttu-id="4d156-104">D1103: identificador perdido</span><span class="sxs-lookup"><span data-stu-id="4d156-104">D1103: Leaked Handle</span></span>

<span data-ttu-id="4d156-105">\[Se ha creado una *interfaz* de interfaz \] pero no se ha liberado.</span><span class="sxs-lookup"><span data-stu-id="4d156-105">An interface \[*interface*\] was created but not released.</span></span>

## <a name="placeholders"></a><span data-ttu-id="4d156-106">Marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="4d156-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="4d156-107"><span id="interface"></span><span id="INTERFACE"></span>*interfaz*</span><span class="sxs-lookup"><span data-stu-id="4d156-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="4d156-108">Dirección de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="4d156-108">The address of the interface.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="4d156-109">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="4d156-109">Possible Causes</span></span>

<span data-ttu-id="4d156-110">Uso de recursos no válido.</span><span class="sxs-lookup"><span data-stu-id="4d156-110">Invalid resource usage.</span></span> <span data-ttu-id="4d156-111">Una aplicación no puede liberar una interfaz cuando ya no está en uso.</span><span class="sxs-lookup"><span data-stu-id="4d156-111">An application fails to release an interface when it is no longer in use.</span></span>

 

 





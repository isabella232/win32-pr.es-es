---
description: Las \_ constantes LINETSPIOPTION describe los proveedores de servicios de pedidos a los que se debe llamar.
ms.assetid: af91f466-d87e-4767-a2c6-d882b9108f21
title: Constantes de LINETSPIOPTION_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e8fa13047dcbad60472fac371b255f7533809c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691046"
---
# <a name="linetspioption_-constants"></a><span data-ttu-id="2fffd-103">Constantes de LINETSPIOPTION \_</span><span class="sxs-lookup"><span data-stu-id="2fffd-103">LINETSPIOPTION\_ Constants</span></span>

<span data-ttu-id="2fffd-104">Las **\_ constantes LINETSPIOPTION** describe los proveedores de servicios de pedidos a los que se debe llamar.</span><span class="sxs-lookup"><span data-stu-id="2fffd-104">The **LINETSPIOPTION\_ constants** describes the order service providers should be called.</span></span>

<dl> <dt>

<span data-ttu-id="2fffd-105"><span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**LINETSPIOPTION \_ NONREENTRANT**</span><span class="sxs-lookup"><span data-stu-id="2fffd-105"><span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**LINETSPIOPTION\_NONREENTRANT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2fffd-106">TAPI debe llamar a las funciones de este proveedor de servicios de una en una; debe esperar de cada función para que devuelva (pero no para que se completen las funciones asincrónicas) antes de llamar a la misma función u otra, ya sea en el mismo subproceso o en otro diferente, en el mismo procesador o en otro diferente.</span><span class="sxs-lookup"><span data-stu-id="2fffd-106">TAPI should call functions in this service provider one at a time; it should wait from each function to return (but not for asynchronous functions to complete) before calling the same or another function, either on the same or a different thread, on the same or a different processor.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2fffd-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fffd-107">Requirements</span></span>



| <span data-ttu-id="2fffd-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fffd-108">Requirement</span></span> | <span data-ttu-id="2fffd-109">Value</span><span class="sxs-lookup"><span data-stu-id="2fffd-109">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2fffd-110">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="2fffd-110">TAPI version</span></span><br/> | <span data-ttu-id="2fffd-111">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="2fffd-111">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="2fffd-112">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2fffd-112">Header</span></span><br/>       | <dl> <span data-ttu-id="2fffd-113"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fffd-113"><dt>Tspi.h</dt></span></span> </dl> |



 

 





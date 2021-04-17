---
description: Las \_ constantes de marcador de bits LINETERMSHARING describen diferentes formas en que un terminal puede compartirse entre dispositivos de línea, direcciones o llamadas.
ms.assetid: 50a52a50-4d94-4068-9ea4-bea862400036
title: Constantes de LINETERMSHARING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2587621b6362195a610339ba5620b32f1d4f761
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690258"
---
# <a name="linetermsharing_-constants"></a><span data-ttu-id="8e41a-103">Constantes de LINETERMSHARING \_</span><span class="sxs-lookup"><span data-stu-id="8e41a-103">LINETERMSHARING\_ Constants</span></span>

<span data-ttu-id="8e41a-104">Las constantes de marcador de bits **LINETERMSHARING \_** describen diferentes formas en que un terminal puede compartirse entre dispositivos de línea, direcciones o llamadas.</span><span class="sxs-lookup"><span data-stu-id="8e41a-104">The **LINETERMSHARING\_** bit-flag constants describe different ways in which a terminal can be shared between line devices, addresses, or calls.</span></span>

<dl> <dt>

<span data-ttu-id="8e41a-105"><span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**LINETERMSHARING \_ privado**</span><span class="sxs-lookup"><span data-stu-id="8e41a-105"><span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**LINETERMSHARING\_PRIVATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8e41a-106">El dispositivo terminal es privado para un dispositivo de una sola línea.</span><span class="sxs-lookup"><span data-stu-id="8e41a-106">The terminal device is private to a single line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8e41a-107"><span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**LINETERMSHARING \_ SHAREDCONF**</span><span class="sxs-lookup"><span data-stu-id="8e41a-107"><span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**LINETERMSHARING\_SHAREDCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8e41a-108">El dispositivo terminal se puede usar en varias líneas.</span><span class="sxs-lookup"><span data-stu-id="8e41a-108">The terminal device can be used by multiple lines.</span></span> <span data-ttu-id="8e41a-109">Las solicitudes de [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) de los distintos terminales finalizan su combinación o conferencia en el terminal.</span><span class="sxs-lookup"><span data-stu-id="8e41a-109">The [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) requests of the various terminals end up being merged or conferenced at the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8e41a-110"><span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**LINETERMSHARING \_ SHAREDEXCL**</span><span class="sxs-lookup"><span data-stu-id="8e41a-110"><span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**LINETERMSHARING\_SHAREDEXCL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8e41a-111">El dispositivo terminal se puede usar en varias líneas.</span><span class="sxs-lookup"><span data-stu-id="8e41a-111">The terminal device can be used by multiple lines.</span></span> <span data-ttu-id="8e41a-112">El dispositivo de última línea para realizar una [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) o [**TSPI \_ lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) en el terminal para un modo de terminal determinado tendrá una conexión exclusiva con el terminal para ese modo.</span><span class="sxs-lookup"><span data-stu-id="8e41a-112">The last line device to do a [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) or [**TSPI\_lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) to the terminal for a given terminal mode will have exclusive connection to the terminal for that mode.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e41a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e41a-113">Remarks</span></span>

<span data-ttu-id="8e41a-114">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="8e41a-114">No extensibility.</span></span> <span data-ttu-id="8e41a-115">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="8e41a-115">All 32 bits are reserved.</span></span>

<span data-ttu-id="8e41a-116">Estas constantes describen las clases de secuencias de control e información que se pueden enrutar directamente entre un dispositivo de línea y un dispositivo de terminal (como un conjunto de teléfonos).</span><span class="sxs-lookup"><span data-stu-id="8e41a-116">These constants describe the classes of control and information streams that can be routed directly between a line device and a terminal device (such as a phone set).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e41a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e41a-117">Requirements</span></span>



| <span data-ttu-id="8e41a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e41a-118">Requirement</span></span> | <span data-ttu-id="8e41a-119">Value</span><span class="sxs-lookup"><span data-stu-id="8e41a-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8e41a-120">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="8e41a-120">TAPI version</span></span><br/> | <span data-ttu-id="8e41a-121">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8e41a-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8e41a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e41a-122">Header</span></span><br/>       | <dl> <span data-ttu-id="8e41a-123"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e41a-123"><dt>Tapi.h</dt></span></span> </dl> |



 


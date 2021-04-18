---
description: Las \_ constantes de marcador de bits PHONEPRIVILEGE describen las distintas formas en que se puede abrir un dispositivo de teléfono.
ms.assetid: 1dc2fab9-b044-4ae3-8c16-fa450f9ef714
title: Constantes de PHONEPRIVILEGE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6d04c074e03d6f0b7f7a6c58e4268e0bd5057a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691108"
---
# <a name="phoneprivilege_-constants"></a><span data-ttu-id="e8dba-103">Constantes de PHONEPRIVILEGE \_</span><span class="sxs-lookup"><span data-stu-id="e8dba-103">PHONEPRIVILEGE\_ Constants</span></span>

<span data-ttu-id="e8dba-104">Las constantes de marcador de bits **PHONEPRIVILEGE \_** describen las distintas formas en que se puede abrir un dispositivo de teléfono.</span><span class="sxs-lookup"><span data-stu-id="e8dba-104">The **PHONEPRIVILEGE\_** bit-flag constants describe the various ways in which a phone device can be opened.</span></span>

<dl> <dt>

<span data-ttu-id="e8dba-105"><span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**MONITOR de PHONEPRIVILEGE \_**</span><span class="sxs-lookup"><span data-stu-id="e8dba-105"><span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**PHONEPRIVILEGE\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e8dba-106">Una aplicación que abre un dispositivo telefónico con el privilegio monitor está informado sobre los eventos y los cambios de estado que se producen en el teléfono.</span><span class="sxs-lookup"><span data-stu-id="e8dba-106">An application that opens a phone device with the monitor privilege is informed about events and state changes occurring on the phone.</span></span> <span data-ttu-id="e8dba-107">La aplicación no puede invocar ninguna operación en el dispositivo telefónico que cambiaría su estado, por lo que solo se pueden invocar las operaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="e8dba-107">The application cannot invoke any operations on the phone device that would change its state, so only status operations can be invoked.</span></span> <span data-ttu-id="e8dba-108">Varias aplicaciones pueden supervisar un dispositivo telefónico en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="e8dba-108">Multiple applications can monitor a phone device at any given time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8dba-109"><span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**propietario de PHONEPRIVILEGE \_**</span><span class="sxs-lookup"><span data-stu-id="e8dba-109"><span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**PHONEPRIVILEGE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e8dba-110">Una aplicación que abre un dispositivo telefónico con el privilegio Owner tiene permiso para cambiar el estado de las lámparas, el timbre, la pantalla, el conmutador y los bloques de datos del teléfono.</span><span class="sxs-lookup"><span data-stu-id="e8dba-110">An application that opens a phone device with the owner privilege is allowed to change the state of the lamps, ringer, display, hookswitch, and data blocks of the phone.</span></span> <span data-ttu-id="e8dba-111">La apertura de un dispositivo telefónico en modo propietario también proporciona la supervisión del dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="e8dba-111">Opening a phone device in owner mode also provides monitoring of the phone device.</span></span> <span data-ttu-id="e8dba-112">Solo una aplicación puede ser el propietario de un dispositivo telefónico en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="e8dba-112">Only one application is allowed to be the owner of a phone device at any given time.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8dba-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8dba-113">Remarks</span></span>

<span data-ttu-id="e8dba-114">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="e8dba-114">No extensibility.</span></span> <span data-ttu-id="e8dba-115">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="e8dba-115">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8dba-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8dba-116">Requirements</span></span>



| <span data-ttu-id="e8dba-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8dba-117">Requirement</span></span> | <span data-ttu-id="e8dba-118">Value</span><span class="sxs-lookup"><span data-stu-id="e8dba-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e8dba-119">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="e8dba-119">TAPI version</span></span><br/> | <span data-ttu-id="e8dba-120">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="e8dba-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e8dba-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8dba-121">Header</span></span><br/>       | <dl> <span data-ttu-id="e8dba-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8dba-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 





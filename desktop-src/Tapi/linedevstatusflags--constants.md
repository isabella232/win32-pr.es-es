---
description: Las \_ constantes de marcador de bits LINEDEVSTATUSFLAGS describen una colección de elementos de estado de dispositivo de línea booleanos.
ms.assetid: 5fa754d3-07b2-4b75-91ef-1bf961d9fef4
title: Constantes de LINEDEVSTATUSFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70745b1a84119af2305cadabd0a39ab5954e5b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679020"
---
# <a name="linedevstatusflags_-constants"></a><span data-ttu-id="ebb8a-103">Constantes de LINEDEVSTATUSFLAGS \_</span><span class="sxs-lookup"><span data-stu-id="ebb8a-103">LINEDEVSTATUSFLAGS\_ Constants</span></span>

<span data-ttu-id="ebb8a-104">Las constantes de marcador de bits **LINEDEVSTATUSFLAGS \_** describen una colección de elementos de estado de dispositivo de línea booleanos.</span><span class="sxs-lookup"><span data-stu-id="ebb8a-104">The **LINEDEVSTATUSFLAGS\_** bit-flag constants describe a collection of Boolean line device status items.</span></span>

<dl> <dt>

<span data-ttu-id="ebb8a-105"><span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**LINEDEVSTATUSFLAGS \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="ebb8a-105"><span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**LINEDEVSTATUSFLAGS\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebb8a-106">Especifica si la línea está conectada a TAPI.</span><span class="sxs-lookup"><span data-stu-id="ebb8a-106">Specifies whether the line is connected to TAPI.</span></span> <span data-ttu-id="ebb8a-107">Si es **true**, la línea está conectada y TAPI puede operar en el dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="ebb8a-107">If **TRUE**, the line is connected and TAPI is able to operate on the line device.</span></span> <span data-ttu-id="ebb8a-108">Si es **false**, la línea está desconectada y la aplicación no puede controlar el dispositivo de línea a través de TAPI.</span><span class="sxs-lookup"><span data-stu-id="ebb8a-108">If **FALSE**, the line is disconnected and the application is unable to control the line device through TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebb8a-109"><span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**SERVICIO de LINEDEVSTATUSFLAGS \_**</span><span class="sxs-lookup"><span data-stu-id="ebb8a-109"><span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**LINEDEVSTATUSFLAGS\_INSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebb8a-110">Indica si la línea está en el servicio.</span><span class="sxs-lookup"><span data-stu-id="ebb8a-110">Indicates whether the line is in service.</span></span> <span data-ttu-id="ebb8a-111">Si es **true**, la línea está en servicio; Si es **false**, la línea está fuera de servicio.</span><span class="sxs-lookup"><span data-stu-id="ebb8a-111">If **TRUE**, the line is in service; if **FALSE**, the line is out of service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebb8a-112"><span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**LINEDEVSTATUSFLAGS \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="ebb8a-112"><span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**LINEDEVSTATUSFLAGS\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebb8a-113">Indica si la línea está bloqueada o desbloqueada.</span><span class="sxs-lookup"><span data-stu-id="ebb8a-113">Indicates whether the line is locked or unlocked.</span></span> <span data-ttu-id="ebb8a-114">Este bit se usa con más frecuencia con dispositivos de línea asociados a teléfonos móviles.</span><span class="sxs-lookup"><span data-stu-id="ebb8a-114">This bit is most often used with line devices associated with cellular phones.</span></span> <span data-ttu-id="ebb8a-115">Muchos teléfonos móviles tienen un mecanismo de seguridad que requiere la entrada de una contraseña para permitir que el teléfono realice llamadas.</span><span class="sxs-lookup"><span data-stu-id="ebb8a-115">Many cellular phones have a security mechanism that requires the entry of a password to enable the phone to place calls.</span></span> <span data-ttu-id="ebb8a-116">Este bit se puede usar para indicar a las aplicaciones que el teléfono está bloqueado y no puede realizar llamadas hasta que la contraseña se escriba en la interfaz de usuario del teléfono para que la aplicación pueda presentar una alerta adecuada al usuario.</span><span class="sxs-lookup"><span data-stu-id="ebb8a-116">This bit can be used to indicate to applications that the phone is locked and cannot place calls until the password is entered on the user interface of the phone so that the application can present an appropriate alert to the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebb8a-117"><span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**LINEDEVSTATUSFLAGS \_ MSGWAIT**</span><span class="sxs-lookup"><span data-stu-id="ebb8a-117"><span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**LINEDEVSTATUSFLAGS\_MSGWAIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebb8a-118">Indica si la línea tiene un mensaje en espera.</span><span class="sxs-lookup"><span data-stu-id="ebb8a-118">Indicates whether the line has a message waiting.</span></span> <span data-ttu-id="ebb8a-119">Si es **true**, un mensaje está esperando; Si es **false**, no hay ningún mensaje en espera.</span><span class="sxs-lookup"><span data-stu-id="ebb8a-119">If **TRUE**, a message is waiting; if **FALSE**, no message is waiting.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ebb8a-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ebb8a-120">Remarks</span></span>

<span data-ttu-id="ebb8a-121">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="ebb8a-121">No extensibility.</span></span> <span data-ttu-id="ebb8a-122">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="ebb8a-122">All 32 bits are reserved.</span></span>

<span data-ttu-id="ebb8a-123">\_Las constantes LINEDEVSTATUSFLAGS se usan en el miembro **dwDevStatusFlags** de la estructura de datos [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) .</span><span class="sxs-lookup"><span data-stu-id="ebb8a-123">LINEDEVSTATUSFLAGS\_ constants are used within the **dwDevStatusFlags** member of the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebb8a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebb8a-124">Requirements</span></span>



| <span data-ttu-id="ebb8a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebb8a-125">Requirement</span></span> | <span data-ttu-id="ebb8a-126">Value</span><span class="sxs-lookup"><span data-stu-id="ebb8a-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ebb8a-127">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="ebb8a-127">TAPI version</span></span><br/> | <span data-ttu-id="ebb8a-128">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="ebb8a-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ebb8a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ebb8a-129">Header</span></span><br/>       | <dl> <span data-ttu-id="ebb8a-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebb8a-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 





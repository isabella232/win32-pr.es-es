---
description: Indica que ha empezado un comando de navegador de DVD.
ms.assetid: 230116b4-23f1-4c37-a781-da2c5aa20a1f
title: EC_DVD_CMD_START (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0fb723b220bf8aa12baa7133c9985225d6051921
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653376"
---
# <a name="ec_dvd_cmd_start"></a><span data-ttu-id="79ffb-103">\_Inicio de \_ cmd de DVD de EC \_</span><span class="sxs-lookup"><span data-stu-id="79ffb-103">EC\_DVD\_CMD\_START</span></span>

<span data-ttu-id="79ffb-104">Indica que ha empezado un comando de [navegador de DVD](dvd-navigator-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="79ffb-104">Signals that a [DVD Navigator](dvd-navigator-filter.md) command has begun.</span></span>

## <a name="parameters"></a><span data-ttu-id="79ffb-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79ffb-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79ffb-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="79ffb-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="79ffb-107">Identificador del comando.</span><span class="sxs-lookup"><span data-stu-id="79ffb-107">Command identifier.</span></span> <span data-ttu-id="79ffb-108">Pase este parámetro al método [**IDvdInfo2:: GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) para recuperar un puntero de interfaz [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) .</span><span class="sxs-lookup"><span data-stu-id="79ffb-108">Pass this parameter to the [**IDvdInfo2::GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) method to retrieve an [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) interface pointer.</span></span>

</dd> <dt>

<span data-ttu-id="79ffb-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="79ffb-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="79ffb-110">Valor **HRESULT** que indica el estado del comando.</span><span class="sxs-lookup"><span data-stu-id="79ffb-110">**HRESULT** value indicating the status of the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79ffb-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79ffb-111">Remarks</span></span>

<span data-ttu-id="79ffb-112">Este evento solo se desencadena si la aplicación establece la marca SendEvents de la **\_ marca de CMD \_ \_ de DVD** en un método [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) que toma una marca de [**marcas de \_ cmd \_ de DVD**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) .</span><span class="sxs-lookup"><span data-stu-id="79ffb-112">This event is only fired if your application sets the **DVD\_CMD\_FLAG\_SendEvents** flag in an [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) method that takes a [**DVD\_CMD\_FLAGS**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) flag.</span></span>

<span data-ttu-id="79ffb-113">Este evento se desencadena en el dominio de título.</span><span class="sxs-lookup"><span data-stu-id="79ffb-113">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="79ffb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79ffb-114">Requirements</span></span>



| <span data-ttu-id="79ffb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="79ffb-115">Requirement</span></span> | <span data-ttu-id="79ffb-116">Value</span><span class="sxs-lookup"><span data-stu-id="79ffb-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79ffb-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79ffb-117">Header</span></span><br/> | <dl> <span data-ttu-id="79ffb-118"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79ffb-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79ffb-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="79ffb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79ffb-120">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="79ffb-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="79ffb-121">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="79ffb-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="79ffb-122">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="79ffb-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="79ffb-123">Sincronizar comandos de DVD</span><span class="sxs-lookup"><span data-stu-id="79ffb-123">Synchronizing DVD Commands</span></span>](synchronizing-dvd-commands.md)
</dt> </dl>

 

 





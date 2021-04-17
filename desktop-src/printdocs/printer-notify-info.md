---
description: La estructura de información de notificación de impresora \_ \_ contiene información de la impresora devuelta por la función FindNextPrinterChangeNotification. La función devuelve esta información después de que se haya satisfecho una operación de espera en un objeto de notificación de cambio de impresora.
ms.assetid: c104fabe-edf5-426e-859b-694811975623
title: Estructura de PRINTER_NOTIFY_INFO (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 631169cfcdabd6a87459ebb777adb6842d09089b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687742"
---
# <a name="printer_notify_info-structure"></a><span data-ttu-id="0628d-104">Estructura de información de \_ notificación de impresora \_</span><span class="sxs-lookup"><span data-stu-id="0628d-104">PRINTER\_NOTIFY\_INFO structure</span></span>

<span data-ttu-id="0628d-105">La estructura de **\_ \_ información de notificación de impresora** contiene información de la impresora devuelta por la función [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="0628d-105">The **PRINTER\_NOTIFY\_INFO** structure contains printer information returned by the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span> <span data-ttu-id="0628d-106">La función devuelve esta información después de que se haya satisfecho una operación de espera en un objeto de notificación de cambio de impresora.</span><span class="sxs-lookup"><span data-stu-id="0628d-106">The function returns this information after a wait operation on a printer change notification object has been satisfied.</span></span>

## <a name="syntax"></a><span data-ttu-id="0628d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0628d-107">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_INFO {
  DWORD                    Version;
  DWORD                    Flags;
  DWORD                    Count;
  PRINTER_NOTIFY_INFO_DATA aData[1];
} PRINTER_NOTIFY_INFO, *PPRINTER_NOTIFY_INFO;
```



## <a name="members"></a><span data-ttu-id="0628d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0628d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0628d-109">**Versión**</span><span class="sxs-lookup"><span data-stu-id="0628d-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="0628d-110">Versión de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="0628d-110">The version of this structure.</span></span> <span data-ttu-id="0628d-111">Establezca este miembro en 2.</span><span class="sxs-lookup"><span data-stu-id="0628d-111">Set this member to 2.</span></span>

</dd> <dt>

<span data-ttu-id="0628d-112">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="0628d-112">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="0628d-113">Marca de bits que indica el estado de la estructura de notificación.</span><span class="sxs-lookup"><span data-stu-id="0628d-113">A bit flag that indicates the state of the notification structure.</span></span> <span data-ttu-id="0628d-114">Si \_ \_ se establece el bit descartado de la información de notificación de impresora \_ , indica que se tuvieron que descartar algunas notificaciones.</span><span class="sxs-lookup"><span data-stu-id="0628d-114">If the PRINTER\_NOTIFY\_INFO\_DISCARDED bit is set, it indicates that some notifications had to be discarded.</span></span>

</dd> <dt>

<span data-ttu-id="0628d-115">**Recuento**</span><span class="sxs-lookup"><span data-stu-id="0628d-115">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="0628d-116">El número de elementos de datos de la información de  notificación de [**impresora \_ \_ \_**](printer-notify-info-data.md) en la matriz de Adatum.</span><span class="sxs-lookup"><span data-stu-id="0628d-116">The number of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) elements in the **aData** array.</span></span>

</dd> <dt>

<span data-ttu-id="0628d-117">**Adatum**</span><span class="sxs-lookup"><span data-stu-id="0628d-117">**aData**</span></span>
</dt> <dd>

<span data-ttu-id="0628d-118">Una matriz de estructuras de [**\_ \_ \_ datos de notificación**](printer-notify-info-data.md) de la impresora.</span><span class="sxs-lookup"><span data-stu-id="0628d-118">An array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures.</span></span> <span data-ttu-id="0628d-119">Cada elemento de la matriz identifica un solo campo de información de trabajo o de impresora y proporciona los datos actuales para ese campo.</span><span class="sxs-lookup"><span data-stu-id="0628d-119">Each element of the array identifies a single job or printer information field, and provides the current data for that field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0628d-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0628d-120">Remarks</span></span>

<span data-ttu-id="0628d-121">Si el miembro **Flags** tiene el \_ \_ conjunto de bits descartado de información de notificación de impresora \_ , esto indica que se ha producido un desbordamiento o un error, y que es posible que se hayan perdido las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="0628d-121">If the **Flags** member has the PRINTER\_NOTIFY\_INFO\_DISCARDED bit set, this indicates that an overflow or error occurred, and notifications may have been lost.</span></span> <span data-ttu-id="0628d-122">En este caso, debe llamar a [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) y especificar la \_ marca de actualización de opciones de notificación de impresora \_ \_ para recuperar toda la información actual.</span><span class="sxs-lookup"><span data-stu-id="0628d-122">In this case, you must call [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) and specify the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag to retrieve all current information.</span></span> <span data-ttu-id="0628d-123">Hasta que solicite esta operación de actualización, el sistema no enviará notificaciones adicionales para este objeto de notificación de cambios.</span><span class="sxs-lookup"><span data-stu-id="0628d-123">Until you request this refresh operation, the system will not send additional notifications for this change notification object.</span></span>

## <a name="requirements"></a><span data-ttu-id="0628d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0628d-124">Requirements</span></span>



| <span data-ttu-id="0628d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0628d-125">Requirement</span></span> | <span data-ttu-id="0628d-126">Value</span><span class="sxs-lookup"><span data-stu-id="0628d-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0628d-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0628d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0628d-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0628d-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0628d-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0628d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0628d-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0628d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0628d-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0628d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0628d-132"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0628d-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0628d-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="0628d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0628d-134">Impresión</span><span class="sxs-lookup"><span data-stu-id="0628d-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0628d-135">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="0628d-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="0628d-136">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="0628d-136">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="0628d-137">**\_datos de \_ información de notificación de impresora \_**</span><span class="sxs-lookup"><span data-stu-id="0628d-137">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> </dl>

 

 





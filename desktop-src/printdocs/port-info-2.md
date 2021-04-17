---
description: La estructura de la información de puerto \_ \_ 2 identifica un puerto de impresora compatible.
ms.assetid: 93675294-61d4-40e4-b84c-f252978e0285
title: Estructura de PORT_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_2
- _PORT_INFO_2A
- _PORT_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1d2186193318387bb6e37a228bd4d2fd64eca6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706640"
---
# <a name="port_info_2-structure"></a><span data-ttu-id="f655b-103">Estructura de la información de puerto \_ \_ 2</span><span class="sxs-lookup"><span data-stu-id="f655b-103">PORT\_INFO\_2 structure</span></span>

<span data-ttu-id="f655b-104">La estructura de la **información de puerto \_ \_ 2** identifica un puerto de impresora compatible.</span><span class="sxs-lookup"><span data-stu-id="f655b-104">The **PORT\_INFO\_2** structure identifies a supported printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="f655b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f655b-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_2 {
  LPTSTR pPortName;
  LPTSTR pMonitorName;
  LPTSTR pDescription;
  DWORD  fPortType;
  DWORD  Reserved;
} PORT_INFO_2, *PPORT_INFO_2;
```



## <a name="members"></a><span data-ttu-id="f655b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="f655b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f655b-107">**pPortName**</span><span class="sxs-lookup"><span data-stu-id="f655b-107">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="f655b-108">Puntero a una cadena terminada en null que identifica un puerto de impresora compatible (por ejemplo, "LPT1:").</span><span class="sxs-lookup"><span data-stu-id="f655b-108">Pointer to a null-terminated string that identifies a supported printer port (for example, "LPT1:").</span></span>

</dd> <dt>

<span data-ttu-id="f655b-109">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="f655b-109">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="f655b-110">Puntero a una cadena terminada en null que identifica un monitor instalado (por ejemplo, "monitor PJL").</span><span class="sxs-lookup"><span data-stu-id="f655b-110">Pointer to a null-terminated string that identifies an installed monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="f655b-111">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="f655b-111">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f655b-112">**pDescription**</span><span class="sxs-lookup"><span data-stu-id="f655b-112">**pDescription**</span></span>
</dt> <dd>

<span data-ttu-id="f655b-113">Puntero a una cadena terminada en null que describe el puerto con más detalle (por ejemplo, si **pPortName** es "LPT1:", **pDescription** es "Puerto de impresora").</span><span class="sxs-lookup"><span data-stu-id="f655b-113">Pointer to a null-terminated string that describes the port in more detail (for example, if **pPortName** is "LPT1:", **pDescription** is "printer port").</span></span> <span data-ttu-id="f655b-114">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="f655b-114">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f655b-115">**fPortType**</span><span class="sxs-lookup"><span data-stu-id="f655b-115">**fPortType**</span></span>
</dt> <dd>

<span data-ttu-id="f655b-116">Máscara de máscara que describe el tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="f655b-116">Bitmask describing the type of port.</span></span> <span data-ttu-id="f655b-117">Este miembro puede ser una combinación de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="f655b-117">This member can be a combination of the following values:</span></span>

<dl><span id="PORT_TYPE_WRITE"></span><span id="port_type_write"></span><dt>

<span data-ttu-id="f655b-118">**tipo de puerto \_ \_ Write**</span><span class="sxs-lookup"><span data-stu-id="f655b-118">**PORT\_TYPE\_WRITE**</span></span>
</dt><span id="PORT_TYPE_READ"></span><span id="port_type_read"></span><dt>

<span data-ttu-id="f655b-119">**tipo de puerto \_ \_ leído**</span><span class="sxs-lookup"><span data-stu-id="f655b-119">**PORT\_TYPE\_READ**</span></span>
</dt><span id="PORT_TYPE_REDIRECTED"></span><span id="port_type_redirected"></span><dt>

<span data-ttu-id="f655b-120">**tipo de puerto \_ \_ Redirigido**</span><span class="sxs-lookup"><span data-stu-id="f655b-120">**PORT\_TYPE\_REDIRECTED**</span></span>
</dt><span id="PORT_TYPE_NET_ATTACHED"></span><span id="port_type_net_attached"></span><dt>

<span data-ttu-id="f655b-121">**tipo de puerto \_ \_ conectado a red \_**</span><span class="sxs-lookup"><span data-stu-id="f655b-121">**PORT\_TYPE\_NET\_ATTACHED**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="f655b-122">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="f655b-122">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="f655b-123">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f655b-123">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f655b-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f655b-124">Remarks</span></span>

<span data-ttu-id="f655b-125">Use la estructura de la **información de puerto \_ \_ 2** al llamar a [**EnumPorts**](enumports.md) si hay varios monitores instalados que admitan los mismos puertos.</span><span class="sxs-lookup"><span data-stu-id="f655b-125">Use the **PORT\_INFO\_2** structure when calling [**EnumPorts**](enumports.md) if there are multiple monitors installed that support the same ports.</span></span>

<span data-ttu-id="f655b-126">El miembro **fPortType** se puede consultar para determinar la información sobre el puerto.</span><span class="sxs-lookup"><span data-stu-id="f655b-126">The **fPortType** member can be queried to determine information about the port.</span></span> <span data-ttu-id="f655b-127">Tenga en cuenta que la configuración del puerto no afecta a los atributos de la impresora (devueltos por el miembro **attributes** de la información de la [**impresora \_ \_ 2**](printer-info-2.md)).</span><span class="sxs-lookup"><span data-stu-id="f655b-127">Note that port settings do not influence printer attributes (as returned by the **Attributes** member of [**PRINTER\_INFO\_2**](printer-info-2.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="f655b-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f655b-128">Requirements</span></span>



| <span data-ttu-id="f655b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f655b-129">Requirement</span></span> | <span data-ttu-id="f655b-130">Value</span><span class="sxs-lookup"><span data-stu-id="f655b-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f655b-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f655b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f655b-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f655b-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f655b-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f655b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f655b-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f655b-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f655b-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f655b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f655b-136"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f655b-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f655b-137">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="f655b-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f655b-138">**\_ Port \_ info \_ 2W** (Unicode) y la **\_ información de puerto \_ \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f655b-138">**\_PORT\_INFO\_2W** (Unicode) and **\_PORT\_INFO\_2A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="f655b-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="f655b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f655b-140">Impresión</span><span class="sxs-lookup"><span data-stu-id="f655b-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f655b-141">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="f655b-141">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="f655b-142">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="f655b-142">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 





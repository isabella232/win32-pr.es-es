---
description: La estructura de la información de la impresora \_ \_ 4 especifica información general de la impresora. La estructura se puede usar para recuperar la información mínima de la impresora en una llamada a EnumPrinters.
ms.assetid: 81bd0eab-dc1e-4cf1-8f63-3686f1711c1f
title: Estructura de PRINTER_INFO_4 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_4
- _PRINTER_INFO_4A
- _PRINTER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9a1501008f0235ea303dd1457fc8756c28abc21c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278196"
---
# <a name="printer_info_4-structure"></a><span data-ttu-id="54638-103">Estructura de la información de la impresora \_ \_ 4</span><span class="sxs-lookup"><span data-stu-id="54638-103">PRINTER\_INFO\_4 structure</span></span>

<span data-ttu-id="54638-104">La estructura de la información de la **impresora \_ \_ 4** especifica información general de la impresora.</span><span class="sxs-lookup"><span data-stu-id="54638-104">The **PRINTER\_INFO\_4** structure specifies general printer information.</span></span>

<span data-ttu-id="54638-105">La estructura se puede usar para recuperar la información mínima de la impresora en una llamada a [**EnumPrinters**](enumprinters.md).</span><span class="sxs-lookup"><span data-stu-id="54638-105">The structure can be used to retrieve minimal printer information on a call to [**EnumPrinters**](enumprinters.md).</span></span> <span data-ttu-id="54638-106">Esta llamada es una manera rápida y sencilla de recuperar los nombres y atributos de todas las impresoras instaladas localmente en un sistema y todas las conexiones de impresora remotas que ha establecido un usuario.</span><span class="sxs-lookup"><span data-stu-id="54638-106">Such a call is a fast and easy way to retrieve the names and attributes of all locally installed printers on a system and all remote printer connections that a user has established.</span></span>

## <a name="syntax"></a><span data-ttu-id="54638-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54638-107">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_4 {
  LPTSTR pPrinterName;
  LPTSTR pServerName;
  DWORD  Attributes;
} PRINTER_INFO_4, *PPRINTER_INFO_4;
```



## <a name="members"></a><span data-ttu-id="54638-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="54638-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="54638-109">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="54638-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="54638-110">Puntero a una cadena terminada en null que especifica el nombre de la impresora (local o remota).</span><span class="sxs-lookup"><span data-stu-id="54638-110">Pointer to a null-terminated string that specifies the name of the printer (local or remote).</span></span>

</dd> <dt>

<span data-ttu-id="54638-111">**pServerName**</span><span class="sxs-lookup"><span data-stu-id="54638-111">**pServerName**</span></span>
</dt> <dd>

<span data-ttu-id="54638-112">Puntero a una cadena terminada en null que es el nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="54638-112">Pointer to a null-terminated string that is the name of the server.</span></span>

</dd> <dt>

<span data-ttu-id="54638-113">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="54638-113">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="54638-114">Especifica información sobre los datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="54638-114">Specifies information about the returned data.</span></span>



| <span data-ttu-id="54638-115">Value</span><span class="sxs-lookup"><span data-stu-id="54638-115">Value</span></span>                       | <span data-ttu-id="54638-116">Significado</span><span class="sxs-lookup"><span data-stu-id="54638-116">Meaning</span></span>                          |
|-----------------------------|----------------------------------|
| <span data-ttu-id="54638-117">atributo de impresora \_ \_ local</span><span class="sxs-lookup"><span data-stu-id="54638-117">PRINTER\_ATTRIBUTE\_LOCAL</span></span>   | <span data-ttu-id="54638-118">La impresora es una impresora local.</span><span class="sxs-lookup"><span data-stu-id="54638-118">The printer is a local printer.</span></span>  |
| <span data-ttu-id="54638-119">\_red de atributos de impresora \_</span><span class="sxs-lookup"><span data-stu-id="54638-119">PRINTER\_ATTRIBUTE\_NETWORK</span></span> | <span data-ttu-id="54638-120">La impresora es una impresora remota.</span><span class="sxs-lookup"><span data-stu-id="54638-120">The printer is a remote printer.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54638-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54638-121">Remarks</span></span>

<span data-ttu-id="54638-122">La estructura de la información de la **impresora \_ \_ 4** proporciona una manera fácil y sumamente rápida de recuperar los nombres de las impresoras instaladas en un equipo local, así como las conexiones remotas que ha establecido un usuario.</span><span class="sxs-lookup"><span data-stu-id="54638-122">The **PRINTER\_INFO\_4** structure provides an easy and extremely fast way to retrieve the names of the printers installed on a local machine, as well as the remote connections that a user has established.</span></span> <span data-ttu-id="54638-123">Cuando se llama a [**EnumPrinters**](enumprinters.md) con una estructura de datos de la información de la **impresora \_ \_ 4** , esa función consulta el registro para obtener la información especificada y, a continuación, vuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="54638-123">When [**EnumPrinters**](enumprinters.md) is called with a **PRINTER\_INFO\_4** data structure, that function queries the registry for the specified information, then returns immediately.</span></span> <span data-ttu-id="54638-124">Esto difiere del comportamiento de **EnumPrinters** cuando se llama con otros niveles de estructuras de datos de la información de la **impresora \_ \_ XXX** .</span><span class="sxs-lookup"><span data-stu-id="54638-124">This differs from the behavior of **EnumPrinters** when called with other levels of **PRINTER\_INFO\_xxx** data structures.</span></span> <span data-ttu-id="54638-125">En concreto, cuando se llama a **EnumPrinters** con una estructura de datos de nivel 2 (información de la **impresora \_ \_ 2** ), realiza una llamada **OpenPrinter** en cada conexión remota.</span><span class="sxs-lookup"><span data-stu-id="54638-125">In particular, when **EnumPrinters** is called with a level 2 (**PRINTER\_INFO\_2** ) data structure, it performs an **OpenPrinter** call on each remote connection.</span></span> <span data-ttu-id="54638-126">Si una conexión remota está inactiva, si el servidor remoto ya no existe, o si la impresora remota ya no existe, la función debe esperar a que se agote el tiempo de espera de RPC y, por tanto, no se puede realizar la llamada a **OpenPrinter** .</span><span class="sxs-lookup"><span data-stu-id="54638-126">If a remote connection is down, if the remote server no longer exists, or if the remote printer no longer exists, the function must wait for RPC to time out and consequently fail the **OpenPrinter** call.</span></span> <span data-ttu-id="54638-127">Esto puede tardar unos minutos.</span><span class="sxs-lookup"><span data-stu-id="54638-127">This can take a while.</span></span> <span data-ttu-id="54638-128">Pasar una estructura de la información de la **impresora \_ \_ 4** permite que una aplicación recupere un mínimo de la información necesaria; si se desea obtener información más detallada, se puede realizar una llamada posterior al nivel 2 de **EnumPrinter** .</span><span class="sxs-lookup"><span data-stu-id="54638-128">Passing a **PRINTER\_INFO\_4** structure lets an application retrieve a bare minimum of required information; if more detailed information is desired, a subsequent **EnumPrinter** level 2 call can be made.</span></span>

<span data-ttu-id="54638-129">**Los atributos** también pueden contener valores que se definen en el campo **atributos** de la información de la **impresora \_ \_ 2**.</span><span class="sxs-lookup"><span data-stu-id="54638-129">**Attributes** can also contain values that are defined in the **Attributes** field of **PRINTER\_INFO\_2**.</span></span>

<span data-ttu-id="54638-130">Algunas configuraciones de impresora, como las conexiones de impresora a algunos servidores de impresión no basados en Windows, pueden devolver el **atributo de impresora \_ \_ local** y la **red de \_ atributos \_ de impresora**.</span><span class="sxs-lookup"><span data-stu-id="54638-130">Some printer configurations, such as printer connections to some non-Windows-based print servers, might return both **PRINTER\_ATTRIBUTE\_LOCAL** and **PRINTER\_ATTRIBUTE\_NETWORK**.</span></span>

## <a name="requirements"></a><span data-ttu-id="54638-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54638-131">Requirements</span></span>



| <span data-ttu-id="54638-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="54638-132">Requirement</span></span> | <span data-ttu-id="54638-133">Value</span><span class="sxs-lookup"><span data-stu-id="54638-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54638-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54638-134">Minimum supported client</span></span><br/> | <span data-ttu-id="54638-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="54638-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="54638-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54638-136">Minimum supported server</span></span><br/> | <span data-ttu-id="54638-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="54638-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="54638-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54638-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="54638-139"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54638-139"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="54638-140">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="54638-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="54638-141">Información de la **\_ impresora \_ \_ 4W** (Unicode) y la información de la **\_ impresora \_ \_ 4A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="54638-141">**\_PRINTER\_INFO\_4W** (Unicode) and **\_PRINTER\_INFO\_4A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="54638-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="54638-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54638-143">Impresión</span><span class="sxs-lookup"><span data-stu-id="54638-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="54638-144">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="54638-144">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="54638-145">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="54638-145">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="54638-146">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="54638-146">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="54638-147">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="54638-147">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="54638-148">**Información de la impresora \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="54638-148">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="54638-149">**Información de la impresora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="54638-149">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="54638-150">**Información de la impresora \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="54638-150">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> </dl>

 

 





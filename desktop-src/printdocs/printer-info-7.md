---
description: La estructura de la información de la impresora \_ \_ 7 especifica la información de la impresora de servicios de directorio.
ms.assetid: 9443855e-df7d-41a1-a0df-5649a97b2915
title: Estructura de PRINTER_INFO_7 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_7
- _PRINTER_INFO_7A
- _PRINTER_INFO_7W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3dfa92ead4a1f7dab4f0610145e1e1dee7d04065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716943"
---
# <a name="printer_info_7-structure"></a><span data-ttu-id="cd012-103">Estructura de información de impresora \_ \_ 7</span><span class="sxs-lookup"><span data-stu-id="cd012-103">PRINTER\_INFO\_7 structure</span></span>

<span data-ttu-id="cd012-104">La estructura de la información de la **impresora \_ \_ 7** especifica la información de la impresora de servicios de directorio.</span><span class="sxs-lookup"><span data-stu-id="cd012-104">The **PRINTER\_INFO\_7** structure specifies directory services printer information.</span></span> <span data-ttu-id="cd012-105">Utilice esta estructura con la función [**SetPrinter**](setprinter.md) para publicar los datos de una impresora en el servicio de directorio (DS), o para actualizar o quitar los datos publicados de la impresora del DS.</span><span class="sxs-lookup"><span data-stu-id="cd012-105">Use this structure with the [**SetPrinter**](setprinter.md) function to publish a printer's data in the directory service (DS), or to update or remove a printer's published data from the DS.</span></span> <span data-ttu-id="cd012-106">Use esta estructura con la función [**GetPrinter**](getprinter.md) para determinar si una impresora está publicada en el DS.</span><span class="sxs-lookup"><span data-stu-id="cd012-106">Use this structure with the [**GetPrinter**](getprinter.md) function to determine whether a printer is published in the DS.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd012-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd012-107">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_7 {
  LPTSTR pszObjectGUID;
  DWORD  dwAction;
} PRINTER_INFO_7, *PPRINTER_INFO_7;
```



## <a name="members"></a><span data-ttu-id="cd012-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="cd012-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="cd012-109">**pszObjectGUID**</span><span class="sxs-lookup"><span data-stu-id="cd012-109">**pszObjectGUID**</span></span>
</dt> <dd>

<span data-ttu-id="cd012-110">Puntero a una cadena terminada en null que contiene el GUID del objeto de cola de impresión del servicio de directorio asociado a una impresora publicada.</span><span class="sxs-lookup"><span data-stu-id="cd012-110">A pointer to a null-terminated string containing the GUID of the directory service print queue object associated with a published printer.</span></span> <span data-ttu-id="cd012-111">Utilice la función [**GetPrinter**](getprinter.md) para recuperar este GUID.</span><span class="sxs-lookup"><span data-stu-id="cd012-111">Use the [**GetPrinter**](getprinter.md) function to retrieve this GUID.</span></span>

<span data-ttu-id="cd012-112">Antes de llamar a [**SetPrinter**](setprinter.md), establezca **pszObjectGUID** en **null**.</span><span class="sxs-lookup"><span data-stu-id="cd012-112">Before calling [**SetPrinter**](setprinter.md), set **pszObjectGUID** to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cd012-113">**dwAction**</span><span class="sxs-lookup"><span data-stu-id="cd012-113">**dwAction**</span></span>
</dt> <dd>

<span data-ttu-id="cd012-114">Indica la acción que va a realizar la función [**SetPrinter**](setprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="cd012-114">Indicates the action for the [**SetPrinter**](setprinter.md) function to perform.</span></span> <span data-ttu-id="cd012-115">En el caso de la función [**GetPrinter**](getprinter.md) , este miembro indica si la impresora especificada está publicada.</span><span class="sxs-lookup"><span data-stu-id="cd012-115">For the [**GetPrinter**](getprinter.md) function, this member indicates whether the specified printer is published.</span></span> <span data-ttu-id="cd012-116">Este miembro puede ser una combinación de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cd012-116">This member can be a combination of the following values.</span></span>



| <span data-ttu-id="cd012-117">Value</span><span class="sxs-lookup"><span data-stu-id="cd012-117">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="cd012-118">Significado</span><span class="sxs-lookup"><span data-stu-id="cd012-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DSPRINT_PENDING"></span><span id="dsprint_pending"></span><dl> <span data-ttu-id="cd012-119"><dt>**DSPRINT \_ FUNCIÓN**</dt> <dt>0x80000000</dt> pendiente</span><span class="sxs-lookup"><span data-stu-id="cd012-119"><dt>**DSPRINT\_PENDING**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="cd012-120">[**GetPrinter**](getprinter.md): indica que el sistema está intentando completar una operación de publicación o anulación de publicación iniciada por una llamada a [**SetPrinter**](setprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="cd012-120">[**GetPrinter**](getprinter.md): Indicates that the system is attempting to complete a publish or unpublish operation started by a [**SetPrinter**](setprinter.md) call.</span></span><br/> <span data-ttu-id="cd012-121">[**SetPrinter**](setprinter.md): este valor no es válido.</span><span class="sxs-lookup"><span data-stu-id="cd012-121">[**SetPrinter**](setprinter.md): This value is not valid.</span></span> <br/>                                                |
| <span id="DSPRINT_PUBLISH"></span><span id="dsprint_publish"></span><dl> <span data-ttu-id="cd012-122"><dt>**DSPRINT \_ PUBLICAR**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="cd012-122"><dt>**DSPRINT\_PUBLISH**</dt> <dt>0x00000001</dt></span></span> </dl>       | <span data-ttu-id="cd012-123">[**SetPrinter**](setprinter.md): publica los datos de la impresora en el DS.</span><span class="sxs-lookup"><span data-stu-id="cd012-123">[**SetPrinter**](setprinter.md): Publishes the printer's data in the DS.</span></span><br/> <span data-ttu-id="cd012-124">[**GetPrinter**](getprinter.md): indica que la impresora está publicada.</span><span class="sxs-lookup"><span data-stu-id="cd012-124">[**GetPrinter**](getprinter.md): Indicates the printer is published.</span></span> <br/>                                                                                                                                      |
| <span id="DSPRINT_REPUBLISH"></span><span id="dsprint_republish"></span><dl> <span data-ttu-id="cd012-125"><dt>**DSPRINT \_ VOLVER a publicar**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="cd012-125"><dt>**DSPRINT\_REPUBLISH**</dt> <dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="cd012-126">[**SetPrinter**](setprinter.md): los datos de DS de la impresora no se publican y, a continuación, se vuelven a publicar, actualizando todas las propiedades de la impresora publicada.</span><span class="sxs-lookup"><span data-stu-id="cd012-126">[**SetPrinter**](setprinter.md): The DS data for the printer is unpublished and then published again, refreshing all properties in the published printer.</span></span> <span data-ttu-id="cd012-127">Al volver a publicar también se cambia el GUID de la impresora publicada.</span><span class="sxs-lookup"><span data-stu-id="cd012-127">Re-publishing also changes the GUID of the published printer.</span></span><br/> <span data-ttu-id="cd012-128">[**GetPrinter**](getprinter.md): nunca devuelve este valor.</span><span class="sxs-lookup"><span data-stu-id="cd012-128">[**GetPrinter**](getprinter.md): Never returns this value.</span></span> <br/> |
| <span id="DSPRINT_UNPUBLISH"></span><span id="dsprint_unpublish"></span><dl> <span data-ttu-id="cd012-129"><dt>**DSPRINT \_ Cancelar la publicación**</dt> de <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="cd012-129"><dt>**DSPRINT\_UNPUBLISH**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="cd012-130">[**SetPrinter**](setprinter.md): quita los datos publicados de la impresora del DS.</span><span class="sxs-lookup"><span data-stu-id="cd012-130">[**SetPrinter**](setprinter.md): Removes the printer's published data from the DS.</span></span><br/> <span data-ttu-id="cd012-131">[**GetPrinter**](getprinter.md): indica que la impresora no está publicada.</span><span class="sxs-lookup"><span data-stu-id="cd012-131">[**GetPrinter**](getprinter.md): Indicates the printer is not published.</span></span> <br/>                                                                                                                        |
| <span id="DSPRINT_UPDATE"></span><span id="dsprint_update"></span><dl> <span data-ttu-id="cd012-132"><dt>**DSPRINT \_ ACTUALIZAR**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="cd012-132"><dt>**DSPRINT\_UPDATE**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="cd012-133">[**SetPrinter**](setprinter.md): actualiza los datos publicados de la impresora en el DS.</span><span class="sxs-lookup"><span data-stu-id="cd012-133">[**SetPrinter**](setprinter.md): Updates the printer's published data in the DS.</span></span><br/> <span data-ttu-id="cd012-134">[**GetPrinter**](getprinter.md): nunca devuelve este valor.</span><span class="sxs-lookup"><span data-stu-id="cd012-134">[**GetPrinter**](getprinter.md): Never returns this value.</span></span> <br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd012-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd012-135">Remarks</span></span>

<span data-ttu-id="cd012-136">La estructura de la información de la **impresora \_ \_ 7** se usa en una llamada a [**SetPrinter**](setprinter.md) para publicar información de impresora en el servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="cd012-136">The **PRINTER\_INFO\_7** structure is used in a [**SetPrinter**](setprinter.md) call to publish printer information to the directory service.</span></span> <span data-ttu-id="cd012-137">Los datos publicados incluyen todos los valores y datos de la impresora especificada que se encuentra en la clave de administrador de trabajos de SPLDS \_ \_ , \_ clave de controlador SPLDS \_ o claves de clave de usuario de SPLDS \_ \_ creadas por [**SetPrinterDataEx**](setprinterdataex.md).</span><span class="sxs-lookup"><span data-stu-id="cd012-137">The published data includes all values and data for the specified printer found under the SPLDS\_SPOOLER\_KEY, SPLDS\_DRIVER\_KEY, or SPLDS\_USER\_KEY keys created by [**SetPrinterDataEx**](setprinterdataex.md).</span></span>

<span data-ttu-id="cd012-138">En el caso de [**SetPrinter**](setprinter.md), *pszObjectGUID* debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="cd012-138">For [**SetPrinter**](setprinter.md), *pszObjectGUID* should be set to **NULL**.</span></span> <span data-ttu-id="cd012-139">Para [**GetPrinter**](getprinter.md), *PSZOBJECTGUID* devuelve el GUID del objeto cola de impresión de servicios de directorio asociado a una impresora publicada.</span><span class="sxs-lookup"><span data-stu-id="cd012-139">For [**GetPrinter**](getprinter.md), *pszObjectGUID* returns the GUID of the directory services print queue object associated with a published printer.</span></span> <span data-ttu-id="cd012-140">Puede usar este GUID con métodos de la interfaz de Active Directory Services (ADSI) para recuperar los datos publicados para la impresora.</span><span class="sxs-lookup"><span data-stu-id="cd012-140">You can use this GUID with Active Directory Services Interface (ADSI) methods to retrieve published data for the printer.</span></span> <span data-ttu-id="cd012-141">Sin embargo, el método recomendado para recuperar los datos publicados es llamar a la función [**GetPrinterDataEx**](getprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="cd012-141">However, the recommended method for retrieving published data is to call the [**GetPrinterDataEx**](getprinterdataex.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd012-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd012-142">Requirements</span></span>



| <span data-ttu-id="cd012-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd012-143">Requirement</span></span> | <span data-ttu-id="cd012-144">Value</span><span class="sxs-lookup"><span data-stu-id="cd012-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd012-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd012-145">Minimum supported client</span></span><br/> | <span data-ttu-id="cd012-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cd012-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cd012-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd012-147">Minimum supported server</span></span><br/> | <span data-ttu-id="cd012-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cd012-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cd012-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd012-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd012-150"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd012-150"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="cd012-151">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="cd012-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cd012-152">Información de la **\_ impresora \_ \_ 7W** (Unicode) y la información de la **\_ impresora \_ \_ 7A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cd012-152">**\_PRINTER\_INFO\_7W** (Unicode) and **\_PRINTER\_INFO\_7A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="cd012-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd012-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd012-154">Impresión</span><span class="sxs-lookup"><span data-stu-id="cd012-154">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="cd012-155">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="cd012-155">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 





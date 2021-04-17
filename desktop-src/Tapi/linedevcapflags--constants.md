---
description: Las \_ constantes de marcador de bits LINEDEVCAPFLAGS son una colección de valores booleanos que describen varias funcionalidades de dispositivo de línea.
ms.assetid: 0c537488-9fb9-4961-bd0a-1937aefc0b08
title: Constantes de LINEDEVCAPFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffefca75c00fdf09b1886affbff7f0ea90bab6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681064"
---
# <a name="linedevcapflags_-constants"></a><span data-ttu-id="d01a8-103">Constantes de LINEDEVCAPFLAGS \_</span><span class="sxs-lookup"><span data-stu-id="d01a8-103">LINEDEVCAPFLAGS\_ Constants</span></span>

<span data-ttu-id="d01a8-104">Las constantes de marcador de bits **LINEDEVCAPFLAGS \_** son una colección de valores booleanos que describen varias funcionalidades de dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="d01a8-104">The **LINEDEVCAPFLAGS\_** bit-flag constants are a collection of Booleans describing various line device capabilities.</span></span>

<dl> <dt>

<span data-ttu-id="d01a8-105"><span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**LINEDEVCAPFLAGS \_ CALLHUB**</span><span class="sxs-lookup"><span data-stu-id="d01a8-105"><span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**LINEDEVCAPFLAGS\_CALLHUB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d01a8-106">Indica si se admiten los concentradores de llamadas en esta línea.</span><span class="sxs-lookup"><span data-stu-id="d01a8-106">Indicates whether call hubs are supported on this line.</span></span> <span data-ttu-id="d01a8-107">Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 3,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="d01a8-107">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d01a8-108"><span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**LINEDEVCAPFLAGS \_ CALLHUBTRACKING**</span><span class="sxs-lookup"><span data-stu-id="d01a8-108"><span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**LINEDEVCAPFLAGS\_CALLHUBTRACKING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d01a8-109">Indica si se admite el seguimiento del centro de llamadas en esta línea.</span><span class="sxs-lookup"><span data-stu-id="d01a8-109">Indicates whether call hub tracking is supported on this line.</span></span> <span data-ttu-id="d01a8-110">Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 3,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="d01a8-110">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d01a8-111"><span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**LINEDEVCAPFLAGS \_ CLOSEDROP**</span><span class="sxs-lookup"><span data-stu-id="d01a8-111"><span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**LINEDEVCAPFLAGS\_CLOSEDROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d01a8-112">Especifica lo que ocurre cuando se cierra una línea abierta mientras la aplicación tiene llamadas activas en la línea.</span><span class="sxs-lookup"><span data-stu-id="d01a8-112">Specifies what happens when an open line is closed while the application has calls active on the line.</span></span> <span data-ttu-id="d01a8-113">Si **es true**, el proveedor de servicios quita (borra) todas las llamadas activas en la línea cuando la última aplicación que ha abierto la línea la cierra con [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose).</span><span class="sxs-lookup"><span data-stu-id="d01a8-113">If **TRUE**, the service provider drops (clears) all active calls on the line when the last application that has opened the line closes it with [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose).</span></span> <span data-ttu-id="d01a8-114">Si **es false**, el proveedor de servicios no quita las llamadas activas en estos casos.</span><span class="sxs-lookup"><span data-stu-id="d01a8-114">If **FALSE**, the service provider does not drop active calls in such cases.</span></span> <span data-ttu-id="d01a8-115">En su lugar, las llamadas permanecen activas y bajo el control de dispositivos externos.</span><span class="sxs-lookup"><span data-stu-id="d01a8-115">Instead, the calls remain active and under control of external devices.</span></span> <span data-ttu-id="d01a8-116">Normalmente, un proveedor de servicios establece este bit en **false** si hay algún otro dispositivo que pueda mantener activa la llamada (por ejemplo, si una línea analógica tiene el equipo y el teléfono conectados ambos) se conectan directamente a ellos en una configuración de línea de entidad, el teléfono OffHook mantendrá la llamada activa automáticamente incluso después de que el equipo se apague.</span><span class="sxs-lookup"><span data-stu-id="d01a8-116">A service provider typically sets this bit to **FALSE** if there is some other device that can keep the call alive, for example, if an analog line has the computer and phone set both connect directly to them in a party-line configuration, the offhook phone will automatically keep the call active even after the computer powers down.</span></span>

<span data-ttu-id="d01a8-117">Las aplicaciones deben comprobar esta marca para determinar si se debe advertir al usuario (con un cuadro de diálogo de aceptar o cancelar) que las llamadas activas se perderán.</span><span class="sxs-lookup"><span data-stu-id="d01a8-117">Applications should check this flag to determine whether to warn the user (with an OK/Cancel dialog box) that active calls will be lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d01a8-118"><span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**LINEDEVCAPFLAGS \_ CROSSADDRCONF**</span><span class="sxs-lookup"><span data-stu-id="d01a8-118"><span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**LINEDEVCAPFLAGS\_CROSSADDRCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d01a8-119">Especifica si se pueden realizar conferencias en las llamadas en diferentes direcciones de esta línea.</span><span class="sxs-lookup"><span data-stu-id="d01a8-119">Specifies whether calls on different addresses on this line can be conferenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d01a8-120"><span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**LINEDEVCAPFLAGS \_ DIALBILLING**</span><span class="sxs-lookup"><span data-stu-id="d01a8-120"><span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**LINEDEVCAPFLAGS\_DIALBILLING**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d01a8-121"><span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**LINEDEVCAPFLAGS \_ DIALDIALTONE**</span><span class="sxs-lookup"><span data-stu-id="d01a8-121"><span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**LINEDEVCAPFLAGS\_DIALDIALTONE**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d01a8-122"><span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**LINEDEVCAPFLAGS \_ DIALQUIET**</span><span class="sxs-lookup"><span data-stu-id="d01a8-122"><span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**LINEDEVCAPFLAGS\_DIALQUIET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d01a8-123">Estas marcas indican si se admite el modificador de cadena de marcado "$", "@" o "W" para un dispositivo de línea determinado.</span><span class="sxs-lookup"><span data-stu-id="d01a8-123">These flags indicate whether the "$", "@", or "W" dialable string modifier is supported for a given line device.</span></span> <span data-ttu-id="d01a8-124">Es **true** si se admite el modificador; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="d01a8-124">It is **TRUE** if the modifier is supported; otherwise, **FALSE**.</span></span> <span data-ttu-id="d01a8-125">El (solicitar al usuario que continúe el marcado) nunca es compatible con un dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="d01a8-125">The "?" (prompt user to continue dialing) is never supported by a line device.</span></span> <span data-ttu-id="d01a8-126">Estas marcas permiten a una aplicación determinar por adelantado qué modificadores darían lugar a la generación de un LINEERR.</span><span class="sxs-lookup"><span data-stu-id="d01a8-126">These flags allow an application to determine up front which modifiers would result in the generation of a LINEERR.</span></span> <span data-ttu-id="d01a8-127">La aplicación tiene la opción de buscar previamente cadenas marcables para los caracteres no admitidos o de pasar la cadena "sin formato" de [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) directamente al proveedor como parte de funciones como [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) o [**lineales**](/windows/desktop/api/Tapi/nf-tapi-linedial) y permitir que la función genere un error para indicar que el modificador no admitido se produce en primer lugar en la cadena.</span><span class="sxs-lookup"><span data-stu-id="d01a8-127">The application has the choice of pre-scanning dialable strings for unsupported characters or of passing the "raw" string from [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) directly to the provider as part of functions such as [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) or [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) and let the function generate an error to tell it which unsupported modifier occurs first in the string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d01a8-128"><span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**LINEDEVCAPFLAGS \_ HIGHLEVCOMP**</span><span class="sxs-lookup"><span data-stu-id="d01a8-128"><span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**LINEDEVCAPFLAGS\_HIGHLEVCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d01a8-129">Especifica si se admiten elementos de información de compatibilidad de alto nivel en esta línea.</span><span class="sxs-lookup"><span data-stu-id="d01a8-129">Specifies whether high-level compatibility information elements are supported on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d01a8-130"><span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**LINEDEVCAPFLAGS \_ LOWLEVCOMP**</span><span class="sxs-lookup"><span data-stu-id="d01a8-130"><span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**LINEDEVCAPFLAGS\_LOWLEVCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d01a8-131">Especifica si se admiten elementos de información de compatibilidad de bajo nivel en esta línea.</span><span class="sxs-lookup"><span data-stu-id="d01a8-131">Specifies whether low-level compatibility information elements are supported on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d01a8-132"><span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**LINEDEVCAPFLAGS \_ MEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="d01a8-132"><span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**LINEDEVCAPFLAGS\_MEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d01a8-133">Especifica si las operaciones de control de medios están disponibles para las llamadas en esta línea.</span><span class="sxs-lookup"><span data-stu-id="d01a8-133">Specifies whether media-control operations are available for calls at this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d01a8-134"><span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**LINEDEVCAPFLAGS \_ MSP**</span><span class="sxs-lookup"><span data-stu-id="d01a8-134"><span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**LINEDEVCAPFLAGS\_MSP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d01a8-135">Indica si un proveedor de servicios multimedia (MSP) está asociado a la línea.</span><span class="sxs-lookup"><span data-stu-id="d01a8-135">Indicates whether a Media Service Provider (MSP) is associated with the line.</span></span> <span data-ttu-id="d01a8-136">Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 3,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="d01a8-136">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d01a8-137"><span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**LINEDEVCAPFLAGS \_ MULTIPLEADDR**</span><span class="sxs-lookup"><span data-stu-id="d01a8-137"><span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**LINEDEVCAPFLAGS\_MULTIPLEADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d01a8-138">Especifica si [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineal**](/windows/desktop/api/Tapi/nf-tapi-linedial), [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)o [**TSPI es \_**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) capaz de tratar con varias direcciones a la vez (como para multiplexación inversa).</span><span class="sxs-lookup"><span data-stu-id="d01a8-138">Specifies whether [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial), [**TSPI\_lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall), or [**TSPI\_lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) is able to deal with multiple addresses at once (as for inverse multiplexing).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d01a8-139"><span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**LINEDEVCAPFLAGS \_ PRIVATEOBJECTS**</span><span class="sxs-lookup"><span data-stu-id="d01a8-139"><span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**LINEDEVCAPFLAGS\_PRIVATEOBJECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d01a8-140">Indica si se han implementado [interfaces específicas del proveedor](./provider-specific-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="d01a8-140">Indicates whether [provider-specific Interfaces](./provider-specific-interfaces.md) have been implemented.</span></span> <span data-ttu-id="d01a8-141">Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 3,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="d01a8-141">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d01a8-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d01a8-142">Remarks</span></span>

<span data-ttu-id="d01a8-143">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="d01a8-143">No extensibility.</span></span> <span data-ttu-id="d01a8-144">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="d01a8-144">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="d01a8-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d01a8-145">Requirements</span></span>



| <span data-ttu-id="d01a8-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="d01a8-146">Requirement</span></span> | <span data-ttu-id="d01a8-147">Value</span><span class="sxs-lookup"><span data-stu-id="d01a8-147">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d01a8-148">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="d01a8-148">TAPI version</span></span><br/> | <span data-ttu-id="d01a8-149">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="d01a8-149">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="d01a8-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d01a8-150">Header</span></span><br/>       | <dl> <span data-ttu-id="d01a8-151"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="d01a8-151"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d01a8-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="d01a8-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d01a8-153">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="d01a8-153">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="d01a8-154">**Fino**</span><span class="sxs-lookup"><span data-stu-id="d01a8-154">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[<span data-ttu-id="d01a8-155">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="d01a8-155">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="d01a8-156">**lineTranslateAddress**</span><span class="sxs-lookup"><span data-stu-id="d01a8-156">**lineTranslateAddress**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)
</dt> </dl>

 


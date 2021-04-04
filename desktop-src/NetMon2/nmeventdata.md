---
description: La estructura NMEVENTDATA contiene información sobre una condición de evento que se pasa a Monitor de red para insertar una línea en el visor de expertos.
ms.assetid: 35cda410-d45a-4a51-91b7-8bd4a0c9957f
title: Estructura NMEVENTDATA (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMEVENTDATA
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 6258b1b1bfde5b159165de2efb9a010053c0421a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908181"
---
# <a name="nmeventdata-structure"></a><span data-ttu-id="f398f-103">Estructura NMEVENTDATA</span><span class="sxs-lookup"><span data-stu-id="f398f-103">NMEVENTDATA structure</span></span>

<span data-ttu-id="f398f-104">La estructura **NMEVENTDATA** contiene información sobre una condición de evento que se pasa a monitor de red para insertar una línea en el visor de expertos.</span><span class="sxs-lookup"><span data-stu-id="f398f-104">The **NMEVENTDATA** structure contains information about an event condition that is passed to Network Monitor to insert a line in the expert viewer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f398f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f398f-105">Syntax</span></span>


```C++
typedef struct {
  BYTE         Version;
  DWORD        EventIdent;
  DWORD        Flags;
  DWORD        Severity;
  BYTE         NumColumns;
  LPSTR        szSourceName;
  LPSTR        szEventName;
  LPSTR        szDescription;
  LPSTR        szMachine;
  JTYPE        Justification;
  LPSTR        szUrl;
  SYSTEMTIME   SysTime;
  NMCOLUMNINFO Column[];
} NMEVENTDATA, *PNMEVENTDATA;
```



## <a name="members"></a><span data-ttu-id="f398f-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="f398f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f398f-107">**Versión**</span><span class="sxs-lookup"><span data-stu-id="f398f-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="f398f-108">Número de versión de la estructura **NMEVENTDATA** .</span><span class="sxs-lookup"><span data-stu-id="f398f-108">Version number of the **NMEVENTDATA** structure.</span></span> <span data-ttu-id="f398f-109">El número de versión debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f398f-109">The version number must be zero.</span></span> <span data-ttu-id="f398f-110">Las versiones futuras de Monitor de red pueden admitir un número de versión superior.</span><span class="sxs-lookup"><span data-stu-id="f398f-110">Future versions of Network Monitor may support a higher version number.</span></span>

</dd> <dt>

<span data-ttu-id="f398f-111">**EventIdent**</span><span class="sxs-lookup"><span data-stu-id="f398f-111">**EventIdent**</span></span>
</dt> <dd>

<span data-ttu-id="f398f-112">Identificador del evento.</span><span class="sxs-lookup"><span data-stu-id="f398f-112">Identifier of the event.</span></span> <span data-ttu-id="f398f-113">**EventIdent** es único para cada experto y hace referencia a una [Página de referencia de evento](event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="f398f-113">**EventIdent** is unique to each expert, and references an [event reference page](event-reference-page.md).</span></span>

</dd> <dt>

<span data-ttu-id="f398f-114">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="f398f-114">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="f398f-115">Un conjunto de marcas que describe quién envía los datos de evento y cómo se muestra el evento.</span><span class="sxs-lookup"><span data-stu-id="f398f-115">A set of flags that describes who sends the event data, and how the event is displayed.</span></span>



| <span data-ttu-id="f398f-116">Value</span><span class="sxs-lookup"><span data-stu-id="f398f-116">Value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="f398f-117">Significado</span><span class="sxs-lookup"><span data-stu-id="f398f-117">Meaning</span></span>                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EVENT_FLAG_EXPERT"></span><span id="event_flag_expert"></span><dl> <span data-ttu-id="f398f-118"><dt>**\_experto en marcas de evento \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f398f-118"><dt>**EVENT\_FLAG\_EXPERT**</dt></span></span> </dl>                                                                         | <span data-ttu-id="f398f-119">El evento procede de un experto.</span><span class="sxs-lookup"><span data-stu-id="f398f-119">The event came from an expert.</span></span> <br/>                                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SEVERITY"></span><span id="nmeventflag_do_not_display_severity"></span><dl> <span data-ttu-id="f398f-120"><dt>**NMEVENTFLAG \_ \_ no \_ Mostrar \_ gravedad**</dt></span><span class="sxs-lookup"><span data-stu-id="f398f-120"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_SEVERITY**</dt></span></span> </dl>                 | <span data-ttu-id="f398f-121">No mostrar el nivel de gravedad para el evento.</span><span class="sxs-lookup"><span data-stu-id="f398f-121">Do not display the severity level for the event.</span></span> <br/>                                                                                                                |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SOURCE"></span><span id="nmeventflag_do_not_display_source"></span><dl> <span data-ttu-id="f398f-122"><dt>**NMEVENTFLAG \_ \_ no \_ Mostrar el \_ origen**</dt></span><span class="sxs-lookup"><span data-stu-id="f398f-122"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_SOURCE**</dt></span></span> </dl>                       | <span data-ttu-id="f398f-123">No se muestra el nombre del origen del evento.</span><span class="sxs-lookup"><span data-stu-id="f398f-123">Do not display the source name for the event.</span></span> <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_EVENT_NAME"></span><span id="nmeventflag_do_not_display_event_name"></span><dl> <span data-ttu-id="f398f-124"><dt>**NMEVENTFLAG \_ \_ no \_ Mostrar \_ nombre de evento \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f398f-124"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_EVENT\_NAME**</dt></span></span> </dl>          | <span data-ttu-id="f398f-125">No muestre el nombre del evento.</span><span class="sxs-lookup"><span data-stu-id="f398f-125">Do not display the event name for the event.</span></span> <br/>                                                                                                                    |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_DESCRIPTION"></span><span id="nmeventflag_do_not_display_description"></span><dl> <span data-ttu-id="f398f-126"><dt>**NMEVENTFLAG \_ \_ no \_ Mostrar \_ Descripción**</dt></span><span class="sxs-lookup"><span data-stu-id="f398f-126"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_DESCRIPTION**</dt></span></span> </dl>        | <span data-ttu-id="f398f-127">No se muestra la descripción del evento.</span><span class="sxs-lookup"><span data-stu-id="f398f-127">Do not display the description for the event.</span></span> <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_MACHINE"></span><span id="nmeventflag_do_not_display_machine"></span><dl> <span data-ttu-id="f398f-128"><dt>**NMEVENTFLAG \_ \_ no \_ Mostrar \_ equipo**</dt></span><span class="sxs-lookup"><span data-stu-id="f398f-128"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_MACHINE**</dt></span></span> </dl>                    | <span data-ttu-id="f398f-129">No muestre el nombre del equipo para el evento.</span><span class="sxs-lookup"><span data-stu-id="f398f-129">Do not display the machine name for the event.</span></span> <br/>                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_TIME"></span><span id="nmeventflag_do_not_display_time"></span><dl> <span data-ttu-id="f398f-130"><dt>**NMEVENTFLAG \_ \_ no \_ Mostrar \_ hora**</dt></span><span class="sxs-lookup"><span data-stu-id="f398f-130"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_TIME**</dt></span></span> </dl>                             | <span data-ttu-id="f398f-131">No mostrar la hora del evento</span><span class="sxs-lookup"><span data-stu-id="f398f-131">Do not display the time for the event</span></span> <br/>                                                                                                                           |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_FIXED_COLUMNS"></span><span id="nmeventflag_do_not_display_fixed_columns"></span><dl> <span data-ttu-id="f398f-132"><dt>**NMEVENTFLAG \_ \_ no \_ Mostrar \_ columnas fijas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f398f-132"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_FIXED\_COLUMNS**</dt></span></span> </dl> | <span data-ttu-id="f398f-133">No muestre la gravedad, el origen, el nombre del evento, la descripción, la máquina o las columnas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f398f-133">Do not display the Severity, Source, Event Name, Description, Machine, or Time columns.</span></span> <span data-ttu-id="f398f-134">No se trata de una marca única, pero es una Unión de las seis marcas anteriores.</span><span class="sxs-lookup"><span data-stu-id="f398f-134">This is not a single flag, but it is a union of the previous six flags.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="f398f-135">**Gravedad**</span><span class="sxs-lookup"><span data-stu-id="f398f-135">**Severity**</span></span>
</dt> <dd>

<span data-ttu-id="f398f-136">Nivel de gravedad del evento.</span><span class="sxs-lookup"><span data-stu-id="f398f-136">Severity level of the event.</span></span> <span data-ttu-id="f398f-137">El nivel de gravedad puede tener uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="f398f-137">The severity level can have one of the following values:</span></span>

<span data-ttu-id="f398f-138">NMEVENT \_ gravedad \_ informativa NMEVENT \_ gravedad \_ ADVERTENCIA NMEVENT gravedad \_ \_ severa \_ ADVERTENCIA NMEVENT \_ gravedad NMEVENT gravedad grave error \_ \_ \_ \_ NMEVENT \_ gravedad \_ crítico \_ error</span><span class="sxs-lookup"><span data-stu-id="f398f-138">NMEVENT\_SEVERITY\_INFORMATIONAL NMEVENT\_SEVERITY\_WARNING NMEVENT\_SEVERITY\_STRONG\_WARNING NMEVENT\_SEVERITY\_ERROR NMEVENT\_SEVERITY\_SEVERE\_ERROR NMEVENT\_SEVERITY\_CRITICAL\_ERROR</span></span>

</dd> <dt>

<span data-ttu-id="f398f-139">**NumColumns**</span><span class="sxs-lookup"><span data-stu-id="f398f-139">**NumColumns**</span></span>
</dt> <dd>

<span data-ttu-id="f398f-140">Número de columnas designadas en la estructura actual.</span><span class="sxs-lookup"><span data-stu-id="f398f-140">Number of columns designated in the current structure.</span></span>

</dd> <dt>

<span data-ttu-id="f398f-141">**szSourceName**</span><span class="sxs-lookup"><span data-stu-id="f398f-141">**szSourceName**</span></span>
</dt> <dd>

<span data-ttu-id="f398f-142">Nombre del experto que se muestra.</span><span class="sxs-lookup"><span data-stu-id="f398f-142">Name of the expert that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="f398f-143">**szEventName**</span><span class="sxs-lookup"><span data-stu-id="f398f-143">**szEventName**</span></span>
</dt> <dd>

<span data-ttu-id="f398f-144">Nombre del evento que se muestra.</span><span class="sxs-lookup"><span data-stu-id="f398f-144">Name of the event that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="f398f-145">**szDescription**</span><span class="sxs-lookup"><span data-stu-id="f398f-145">**szDescription**</span></span>
</dt> <dd>

<span data-ttu-id="f398f-146">Descripción del evento que se muestra.</span><span class="sxs-lookup"><span data-stu-id="f398f-146">Description of the event that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="f398f-147">**szMachine**</span><span class="sxs-lookup"><span data-stu-id="f398f-147">**szMachine**</span></span>
</dt> <dd>

<span data-ttu-id="f398f-148">Obsoleto, debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="f398f-148">Obsolete, should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f398f-149">**Justificación**</span><span class="sxs-lookup"><span data-stu-id="f398f-149">**Justification**</span></span>
</dt> <dd>

<span data-ttu-id="f398f-150">Información que se muestra en la segunda ventana del Visor de eventos.</span><span class="sxs-lookup"><span data-stu-id="f398f-150">Information displayed in the second window of the Event Viewer.</span></span> <span data-ttu-id="f398f-151">El miembro de **justificación** puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="f398f-151">The **Justification** member may be **NULL**.</span></span> <span data-ttu-id="f398f-152">Si es **null**, la segunda ventana no es visible.</span><span class="sxs-lookup"><span data-stu-id="f398f-152">If it is **NULL**, the second window is not be visible.</span></span>

</dd> <dt>

<span data-ttu-id="f398f-153">**szUrl**</span><span class="sxs-lookup"><span data-stu-id="f398f-153">**szUrl**</span></span>
</dt> <dd>

<span data-ttu-id="f398f-154">Sector Este miembro debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="f398f-154">Reserved; this member must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f398f-155">**SysTime**</span><span class="sxs-lookup"><span data-stu-id="f398f-155">**SysTime**</span></span>
</dt> <dd>

<span data-ttu-id="f398f-156">Hora a la que se produce la condición de evento.</span><span class="sxs-lookup"><span data-stu-id="f398f-156">Time at which the event condition occurs.</span></span> <span data-ttu-id="f398f-157">La hora se mide en relación con el principio de la captura.</span><span class="sxs-lookup"><span data-stu-id="f398f-157">The time is measured relative to the beginning of the capture.</span></span>

</dd> <dt>

<span data-ttu-id="f398f-158">**Columna**</span><span class="sxs-lookup"><span data-stu-id="f398f-158">**Column**</span></span>
</dt> <dd>

<span data-ttu-id="f398f-159">Tabla de estructuras de columna que aparece en el panel superior del Visor de eventos.</span><span class="sxs-lookup"><span data-stu-id="f398f-159">Table of column structures that appears in the top pane of the Event Viewer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f398f-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f398f-160">Requirements</span></span>



| <span data-ttu-id="f398f-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="f398f-161">Requirement</span></span> | <span data-ttu-id="f398f-162">Value</span><span class="sxs-lookup"><span data-stu-id="f398f-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f398f-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f398f-163">Minimum supported client</span></span><br/> | <span data-ttu-id="f398f-164">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f398f-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f398f-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f398f-165">Minimum supported server</span></span><br/> | <span data-ttu-id="f398f-166">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f398f-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f398f-167">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f398f-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="f398f-168"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f398f-168"><dt>Netmon.h</dt></span></span> </dl> |



 

 





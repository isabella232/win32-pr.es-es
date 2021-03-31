---
title: Métodos de la propiedad IADsPrintQueueOperations (iAds. h)
description: Los métodos de propiedad de la interfaz IADsPrintQueueOperations leen y escriben las propiedades enumeradas en la lista siguiente. Para obtener más información sobre los métodos de propiedad, vea métodos de propiedad de interfaz.
ms.assetid: a4e6bac5-5d52-4492-b48e-f051fec6158c
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsPrintQueueOperations ADSI
topic_type:
- apiref
api_name:
- IADsPrintQueueOperations Property Methods
- IADsPrintQueueOperations.Status
- IADsPrintQueueOperations.get_Name
- IADsPrintQueueOperations.put_Name
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8af7aef94dd9453af690f0c5d83b1e978d3b058
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996828"
---
# <a name="iadsprintqueueoperations-property-methods"></a><span data-ttu-id="c09c6-105">Métodos de propiedad IADsPrintQueueOperations</span><span class="sxs-lookup"><span data-stu-id="c09c6-105">IADsPrintQueueOperations Property Methods</span></span>

<span data-ttu-id="c09c6-106">Los métodos de propiedad de la interfaz [**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations) leen y escriben las propiedades enumeradas en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="c09c6-106">The property methods of the [**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations) interface read and write the properties listed in the following list.</span></span> <span data-ttu-id="c09c6-107">Para obtener más información sobre los métodos de propiedad, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="c09c6-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="c09c6-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c09c6-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="c09c6-109">**Estado**</span><span class="sxs-lookup"><span data-stu-id="c09c6-109">**Status**</span></span>
<span data-ttu-id="c09c6-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c09c6-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="c09c6-111">Estado actual de las operaciones de cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="c09c6-111">Current status of the print queue operations.</span></span> <span data-ttu-id="c09c6-112">Los valores de código de estado válidos se muestran en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="c09c6-112">The valid status code values are listed in the following list.</span></span>

<dt>

<span id="ADS_PRINTER_PAUSED"></span><span id="ads_printer_paused"></span>

<span data-ttu-id="c09c6-113">**Anuncios \_ de IMPRESORA en \_ pausa** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="c09c6-113">**ADS\_PRINTER\_PAUSED** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PENDING_DELETION"></span><span id="ads_printer_pending_deletion"></span>

<span data-ttu-id="c09c6-114">**Anuncios \_ de \_ \_ Eliminación de impresora pendiente** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="c09c6-114">**ADS\_PRINTER\_PENDING\_DELETION** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_ERROR"></span><span id="ads_printer_error"></span>

<span data-ttu-id="c09c6-115">**Anuncios \_ de \_Error de impresora** (0x00000003)</span><span class="sxs-lookup"><span data-stu-id="c09c6-115">**ADS\_PRINTER\_ERROR** (0x00000003)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_JAM"></span><span id="ads_printer_paper_jam"></span>

<span data-ttu-id="c09c6-116">**Anuncios \_ de \_ \_ Atasco de papel** de la impresora (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="c09c6-116">**ADS\_PRINTER\_PAPER\_JAM** (0x00000004)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_OUT"></span><span id="ads_printer_paper_out"></span>

<span data-ttu-id="c09c6-117">**Anuncios \_ de \_Papel \_** de la impresora (0x00000005)</span><span class="sxs-lookup"><span data-stu-id="c09c6-117">**ADS\_PRINTER\_PAPER\_OUT** (0x00000005)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_MANUAL_FEED"></span><span id="ads_printer_manual_feed"></span>

<span data-ttu-id="c09c6-118">**Anuncios \_ de \_ \_ Alimentación manual** de la impresora (0x00000006)</span><span class="sxs-lookup"><span data-stu-id="c09c6-118">**ADS\_PRINTER\_MANUAL\_FEED** (0x00000006)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_PROBLEM"></span><span id="ads_printer_paper_problem"></span>

<span data-ttu-id="c09c6-119">**Anuncios \_ de \_ \_ Problema de papel** de la impresora (0x00000007)</span><span class="sxs-lookup"><span data-stu-id="c09c6-119">**ADS\_PRINTER\_PAPER\_PROBLEM** (0x00000007)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OFFLINE"></span><span id="ads_printer_offline"></span>

<span data-ttu-id="c09c6-120">**Anuncios \_ de IMPRESORA \_ sin conexión** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="c09c6-120">**ADS\_PRINTER\_OFFLINE** (0x00000008)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_IO_ACTIVE"></span><span id="ads_printer_io_active"></span>

<span data-ttu-id="c09c6-121">**Anuncios \_ de \_E/ \_ s de impresora activa** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="c09c6-121">**ADS\_PRINTER\_IO\_ACTIVE** (0x00000100)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_BUSY"></span><span id="ads_printer_busy"></span>

<span data-ttu-id="c09c6-122">**Anuncios \_ de IMPRESORA \_ ocupada** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="c09c6-122">**ADS\_PRINTER\_BUSY** (0x00000200)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PRINTING"></span><span id="ads_printer_printing"></span>

<span data-ttu-id="c09c6-123">**Anuncios \_ de \_Impresión de impresora** (0x00000400)</span><span class="sxs-lookup"><span data-stu-id="c09c6-123">**ADS\_PRINTER\_PRINTING** (0x00000400)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUTPUT_BIN_FULL"></span><span id="ads_printer_output_bin_full"></span>

<span data-ttu-id="c09c6-124">**Anuncios \_ de Bandeja de salida de impresora \_ \_ \_ completa** (0x00000800)</span><span class="sxs-lookup"><span data-stu-id="c09c6-124">**ADS\_PRINTER\_OUTPUT\_BIN\_FULL** (0x00000800)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NOT_AVAILABLE"></span><span id="ads_printer_not_available"></span>

<span data-ttu-id="c09c6-125">**Anuncios \_ de La impresora \_ no \_ está disponible** (0x00001000)</span><span class="sxs-lookup"><span data-stu-id="c09c6-125">**ADS\_PRINTER\_NOT\_AVAILABLE** (0x00001000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WAITING"></span><span id="ads_printer_waiting"></span>

<span data-ttu-id="c09c6-126">**Anuncios \_ de IMPRESORA en \_ espera** (0x00002000)</span><span class="sxs-lookup"><span data-stu-id="c09c6-126">**ADS\_PRINTER\_WAITING** (0x00002000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PROCESSING"></span><span id="ads_printer_processing"></span>

<span data-ttu-id="c09c6-127">**Anuncios \_ de \_Procesamiento** de la impresora (0x00004000)</span><span class="sxs-lookup"><span data-stu-id="c09c6-127">**ADS\_PRINTER\_PROCESSING** (0x00004000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_INITIALIZING"></span><span id="ads_printer_initializing"></span>

<span data-ttu-id="c09c6-128">**Anuncios \_ de \_Inicialización** de la impresora (0x00008000)</span><span class="sxs-lookup"><span data-stu-id="c09c6-128">**ADS\_PRINTER\_INITIALIZING** (0x00008000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WARMING_UP"></span><span id="ads_printer_warming_up"></span>

<span data-ttu-id="c09c6-129">**Anuncios \_ de \_Preparación \_ de la impresora** (0x00010000)</span><span class="sxs-lookup"><span data-stu-id="c09c6-129">**ADS\_PRINTER\_WARMING\_UP** (0x00010000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_TONER_LOW"></span><span id="ads_printer_toner_low"></span>

<span data-ttu-id="c09c6-130">**Anuncios \_ de Tóner de impresora \_ \_ bajo** (0x00020000)</span><span class="sxs-lookup"><span data-stu-id="c09c6-130">**ADS\_PRINTER\_TONER\_LOW** (0x00020000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NO_TONER"></span><span id="ads_printer_no_toner"></span>

<span data-ttu-id="c09c6-131">**Anuncios \_ de IMPRESORA \_ sin \_ tóner** (0x00040000)</span><span class="sxs-lookup"><span data-stu-id="c09c6-131">**ADS\_PRINTER\_NO\_TONER** (0x00040000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAGE_PUNT"></span><span id="ads_printer_page_punt"></span>

<span data-ttu-id="c09c6-132">**Anuncios \_ de Página de la impresora \_ \_ aparcan** (0x00080000)</span><span class="sxs-lookup"><span data-stu-id="c09c6-132">**ADS\_PRINTER\_PAGE\_PUNT** (0x00080000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_USER_INTERVENTION"></span><span id="ads_printer_user_intervention"></span>

<span data-ttu-id="c09c6-133">**Anuncios \_ de \_ \_ Intervención del usuario** de la impresora (0x00100000)</span><span class="sxs-lookup"><span data-stu-id="c09c6-133">**ADS\_PRINTER\_USER\_INTERVENTION** (0x00100000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUT_OF_MEMORY"></span><span id="ads_printer_out_of_memory"></span>

<span data-ttu-id="c09c6-134">**Anuncios \_ de \_ \_ \_ Memoria insuficiente de la impresora** (0x00200000)</span><span class="sxs-lookup"><span data-stu-id="c09c6-134">**ADS\_PRINTER\_OUT\_OF\_MEMORY** (0x00200000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_DOOR_OPEN"></span><span id="ads_printer_door_open"></span>

<span data-ttu-id="c09c6-135">**Anuncios \_ de IMPRESORA de \_ puerta \_ abierta** (0x00400000)</span><span class="sxs-lookup"><span data-stu-id="c09c6-135">**ADS\_PRINTER\_DOOR\_OPEN** (0x00400000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_SERVER_UNKNOWN"></span><span id="ads_printer_server_unknown"></span>

<span data-ttu-id="c09c6-136">**Anuncios \_ de Servidor de impresora \_ \_ desconocido** (0x00800000)</span><span class="sxs-lookup"><span data-stu-id="c09c6-136">**ADS\_PRINTER\_SERVER\_UNKNOWN** (0x00800000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_POWER_SAVE"></span><span id="ads_printer_power_save"></span>

<span data-ttu-id="c09c6-137">**Anuncios \_ de Ahorro \_ de \_ energía** de la impresora (0x01000000)</span><span class="sxs-lookup"><span data-stu-id="c09c6-137">**ADS\_PRINTER\_POWER\_SAVE** (0x01000000)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="c09c6-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c09c6-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c09c6-139">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="c09c6-139">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] LONG* pbstrName
);
HRESULT put_Name(
  [in] LONG bstrName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="c09c6-140">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c09c6-140">Examples</span></span>

<span data-ttu-id="c09c6-141">En el siguiente ejemplo de código Visual Basic se comprueba que se ha atascado una impresora.</span><span class="sxs-lookup"><span data-stu-id="c09c6-141">The following Visual Basic code example verifies that a printer is jammed.</span></span>


```VB
Dim pqo As IADsPrintQueueOperations
Set pqo = GetObject("WinNT://aMachine/aPrinter")
If pqo.Status = ADS_PRINTER_PAPER_JAM Then
MsgBox "Your printer is jammed."
End If
```



<span data-ttu-id="c09c6-142">En el siguiente ejemplo de código de C++ se comprueba que una impresora está atascada.</span><span class="sxs-lookup"><span data-stu-id="c09c6-142">The following C++ code example verifies that a printer is jammed.</span></span>


```C++
IADsPrintQueueOperations *pqo;
HRESULT hr = ADsGetObject(L"WinNT://aMachine/aPrinter",
IID_IADsPrintQueueOperations,
(void**)&pqo)
long status;
hr = pqo->get_Status(&status);
if(status = ADS_PRINTER_PAPER_JAM) {
printf("Your printer is jammed.\n");
}
hr = pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="c09c6-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c09c6-143">Requirements</span></span>



| <span data-ttu-id="c09c6-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="c09c6-144">Requirement</span></span> | <span data-ttu-id="c09c6-145">Value</span><span class="sxs-lookup"><span data-stu-id="c09c6-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c09c6-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c09c6-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c09c6-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c09c6-147">Windows Vista</span></span><br/>                                                                    |
| <span data-ttu-id="c09c6-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c09c6-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c09c6-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c09c6-149">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="c09c6-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c09c6-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="c09c6-151"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="c09c6-151"><dt>Iads.h</dt></span></span> </dl>           |
| <span data-ttu-id="c09c6-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c09c6-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c09c6-153"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c09c6-153"><dt>Activeds.dll</dt></span></span> </dl>     |
| <span data-ttu-id="c09c6-154">IID</span><span class="sxs-lookup"><span data-stu-id="c09c6-154">IID</span></span><br/>                      | <span data-ttu-id="c09c6-155">IID \_ IADsPrintQueueOperations se define como 124BE5C0-156E-11cf-A986-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="c09c6-155">IID\_IADsPrintQueueOperations is defined as 124BE5C0-156E-11CF-A986-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c09c6-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="c09c6-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c09c6-157">**IADsPrintQueue**</span><span class="sxs-lookup"><span data-stu-id="c09c6-157">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="c09c6-158">**IADsPrintQueueOperations**</span><span class="sxs-lookup"><span data-stu-id="c09c6-158">**IADsPrintQueueOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)
</dt> </dl>

 

 






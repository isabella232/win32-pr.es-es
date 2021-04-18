---
description: Se usa para notificar el estado o la información de error en respuesta a un comando de detección de solicitud SCSI.
ms.assetid: 43B2FE98-1468-4457-AB7D-3038C16E20B6
title: Estructura de SENSE_DATA (SCSI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SENSE_DATA
api_type:
- HeaderDef
api_location:
- Scsi.h
ms.openlocfilehash: b5eacf9bee8c2cebf93b27c97a88c691852a3841
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105649339"
---
# <a name="sense_data-structure"></a><span data-ttu-id="fca79-103">Estructura de datos de detección \_</span><span class="sxs-lookup"><span data-stu-id="fca79-103">SENSE\_DATA structure</span></span>

<span data-ttu-id="fca79-104">Se usa para notificar el estado o la información de error en respuesta a un comando de **detección de solicitud** SCSI.</span><span class="sxs-lookup"><span data-stu-id="fca79-104">Used to report status or error information in response to a SCSI **Request Sense** command.</span></span>

## <a name="syntax"></a><span data-ttu-id="fca79-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fca79-105">Syntax</span></span>


```C++
typedef struct _SENSE_DATA {
  UCHAR  ErrorCode  :7;
  UCHAR  Valid  :1;
  UCHAR  SegmentNumber;
  UCHAR  SenseKey  :4;
  UCHAR  Reserved  :1;
  UCHAR  IncorrectLength  :1;
  UCHAR  EndOfMedia  :1;
  UCHAR  FileMark  :1;
  UCHAR  Information[4];
  UCHAR  AdditionalSenseLength;
  UCHAR  CommandSpecificInformation[4];
  UCHAR  AdditionalSenseCode;
  UCHAR  AdditionalSenseCodeQualifier;
  UCHAR  FieldReplaceableUnitCode;
  UCHAR  SenseKeySpecific[3];
} SENSE_DATA, *PSENSE_DATA;
```



## <a name="members"></a><span data-ttu-id="fca79-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="fca79-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fca79-107">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="fca79-107">**ErrorCode**</span></span>
</dt> <dd>

<span data-ttu-id="fca79-108">El tipo de informe.</span><span class="sxs-lookup"><span data-stu-id="fca79-108">The report type.</span></span>



| <span data-ttu-id="fca79-109">Value</span><span class="sxs-lookup"><span data-stu-id="fca79-109">Value</span></span>                                                                           | <span data-ttu-id="fca79-110">Significado</span><span class="sxs-lookup"><span data-stu-id="fca79-110">Meaning</span></span>                     |
|---------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="fca79-111"><dt>0x70</dt></span><span class="sxs-lookup"><span data-stu-id="fca79-111"><dt>0x70</dt></span></span> </dl> | <span data-ttu-id="fca79-112">Errores actuales.</span><span class="sxs-lookup"><span data-stu-id="fca79-112">Current errors.</span></span><br/>  |
| <dl> <span data-ttu-id="fca79-113"><dt>0x71</dt></span><span class="sxs-lookup"><span data-stu-id="fca79-113"><dt>0x71</dt></span></span> </dl> | <span data-ttu-id="fca79-114">Errores diferidos.</span><span class="sxs-lookup"><span data-stu-id="fca79-114">Deferred errors.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fca79-115">**Válido**</span><span class="sxs-lookup"><span data-stu-id="fca79-115">**Valid**</span></span>
</dt> <dd>

<span data-ttu-id="fca79-116">1 si el campo de **información** se define en un estándar; de lo contrario, el campo de **información** es específico del proveedor y no está definido por un estándar.</span><span class="sxs-lookup"><span data-stu-id="fca79-116">1 if the **Information** field is defined in a standard; otherwise the **Information** field is vendor-specific and not defined by a standard.</span></span>

</dd> <dt>

<span data-ttu-id="fca79-117">**SegmentNumber**</span><span class="sxs-lookup"><span data-stu-id="fca79-117">**SegmentNumber**</span></span>
</dt> <dd>

<span data-ttu-id="fca79-118">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="fca79-118">Obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="fca79-119">**SenseKey**</span><span class="sxs-lookup"><span data-stu-id="fca79-119">**SenseKey**</span></span>
</dt> <dd>

<span data-ttu-id="fca79-120">Indica la categoría de error.</span><span class="sxs-lookup"><span data-stu-id="fca79-120">Indicates the category of error.</span></span>

<dl> <dt>

<span data-ttu-id="fca79-121"><span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**No tiene sentido** (0X0)</span><span class="sxs-lookup"><span data-stu-id="fca79-121"><span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**No Sense** (0x0)</span></span>
</dt> <dt>

<span data-ttu-id="fca79-122"><span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**Error recuperado** (0x1)</span><span class="sxs-lookup"><span data-stu-id="fca79-122"><span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**Recovered Error** (0x1)</span></span>
</dt> <dt>

<span data-ttu-id="fca79-123"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (0X2)</span><span class="sxs-lookup"><span data-stu-id="fca79-123"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (0x2)</span></span>
</dt> <dt>

<span data-ttu-id="fca79-124"><span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Error medio** (0X3)</span><span class="sxs-lookup"><span data-stu-id="fca79-124"><span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Medium Error** (0x3)</span></span>
</dt> <dt>

<span data-ttu-id="fca79-125"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Error de hardware** (0x4)</span><span class="sxs-lookup"><span data-stu-id="fca79-125"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Hardware Error** (0x4)</span></span>
</dt> <dt>

<span data-ttu-id="fca79-126"><span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>**Solicitud no válida** (0X5)</span><span class="sxs-lookup"><span data-stu-id="fca79-126"><span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>**Illegal Request** (0x5)</span></span>
</dt> <dt>

<span data-ttu-id="fca79-127"><span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Atención** de la unidad (0x6)</span><span class="sxs-lookup"><span data-stu-id="fca79-127"><span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Unit Attention** (0x6)</span></span>
</dt> <dt>

<span data-ttu-id="fca79-128"><span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Protección de datos** (0X7)</span><span class="sxs-lookup"><span data-stu-id="fca79-128"><span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Data Protect** (0x7)</span></span>
</dt> <dt>

<span data-ttu-id="fca79-129"><span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Error de firmware** (0x9)</span><span class="sxs-lookup"><span data-stu-id="fca79-129"><span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Firmware Error** (0x9)</span></span>
</dt> <dt>

<span data-ttu-id="fca79-130"><span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Comando anulado** (0xB)</span><span class="sxs-lookup"><span data-stu-id="fca79-130"><span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Aborted Command** (0xB)</span></span>
</dt> <dt>

<span data-ttu-id="fca79-131"><span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Igual** (0xc)</span><span class="sxs-lookup"><span data-stu-id="fca79-131"><span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Equal** (0xC)</span></span>
</dt> <dt>

<span data-ttu-id="fca79-132"><span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Desbordamiento de volumen** (0xd)</span><span class="sxs-lookup"><span data-stu-id="fca79-132"><span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Volume Overflow** (0xD)</span></span>
</dt> <dt>

<span data-ttu-id="fca79-133"><span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>No **comparación** (0xE)</span><span class="sxs-lookup"><span data-stu-id="fca79-133"><span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>**Miscompare** (0xE)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="fca79-134">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="fca79-134">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="fca79-135">Reservado.</span><span class="sxs-lookup"><span data-stu-id="fca79-135">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="fca79-136">**IncorrectLength**</span><span class="sxs-lookup"><span data-stu-id="fca79-136">**IncorrectLength**</span></span>
</dt> <dd>

<span data-ttu-id="fca79-137">1 si la longitud del bloque lógico solicitado no coincide con la longitud de bloque lógico de los datos en el medio.</span><span class="sxs-lookup"><span data-stu-id="fca79-137">1 if the requested logical block length does not match the logical block length of the data on the media.</span></span>

</dd> <dt>

<span data-ttu-id="fca79-138">**EndOfMedia**</span><span class="sxs-lookup"><span data-stu-id="fca79-138">**EndOfMedia**</span></span>
</dt> <dd>

<span data-ttu-id="fca79-139">1 si un dispositivo de acceso secuencial ha alcanzado el final del medio, o si una impresora no tiene papel.</span><span class="sxs-lookup"><span data-stu-id="fca79-139">1 if a sequential-access device has reached end-of-media, or a printer is out of paper.</span></span>

</dd> <dt>

<span data-ttu-id="fca79-140">**Detecta**</span><span class="sxs-lookup"><span data-stu-id="fca79-140">**FileMark**</span></span>
</dt> <dd>

<span data-ttu-id="fca79-141">1 si el comando actual ha alcanzado una marca de acceso o setmark.</span><span class="sxs-lookup"><span data-stu-id="fca79-141">1 if the current command has reached a filemark or setmark.</span></span> <span data-ttu-id="fca79-142">Solo es válido para dispositivos de acceso secuencial.</span><span class="sxs-lookup"><span data-stu-id="fca79-142">Only valid for sequential-access devices.</span></span>

</dd> <dt>

<span data-ttu-id="fca79-143">**Información**</span><span class="sxs-lookup"><span data-stu-id="fca79-143">**Information**</span></span>
</dt> <dd>

<span data-ttu-id="fca79-144">Datos específicos del tipo de dispositivo o del comando.</span><span class="sxs-lookup"><span data-stu-id="fca79-144">Device-type or command specific data.</span></span>

</dd> <dt>

<span data-ttu-id="fca79-145">**AdditionalSenseLength**</span><span class="sxs-lookup"><span data-stu-id="fca79-145">**AdditionalSenseLength**</span></span>
</dt> <dd>

<span data-ttu-id="fca79-146">La longitud en bytes del resto de la estructura.</span><span class="sxs-lookup"><span data-stu-id="fca79-146">The length in bytes of the remainder of the structure.</span></span> <span data-ttu-id="fca79-147">La longitud total menos 7.</span><span class="sxs-lookup"><span data-stu-id="fca79-147">The total length minus 7.</span></span>

</dd> <dt>

<span data-ttu-id="fca79-148">**CommandSpecificInformation**</span><span class="sxs-lookup"><span data-stu-id="fca79-148">**CommandSpecificInformation**</span></span>
</dt> <dd>

<span data-ttu-id="fca79-149">Datos específicos del comando.</span><span class="sxs-lookup"><span data-stu-id="fca79-149">Command-specific data.</span></span> <span data-ttu-id="fca79-150">Los valores se definen en el estándar de comandos adecuado.</span><span class="sxs-lookup"><span data-stu-id="fca79-150">Values are defined in the appropriate command standard.</span></span>

</dd> <dt>

<span data-ttu-id="fca79-151">**AdditionalSenseCode**</span><span class="sxs-lookup"><span data-stu-id="fca79-151">**AdditionalSenseCode**</span></span>
</dt> <dd>

<span data-ttu-id="fca79-152">Código específico del dispositivo que describe el error incluido en el campo **SenseKey** .</span><span class="sxs-lookup"><span data-stu-id="fca79-152">Device specific code that describes the error reported in the **SenseKey** field.</span></span>

</dd> <dt>

<span data-ttu-id="fca79-153">**AdditionalSenseCodeQualifier**</span><span class="sxs-lookup"><span data-stu-id="fca79-153">**AdditionalSenseCodeQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="fca79-154">Puede contener detalles adicionales sobre el campo **AdditionalSenseCode** .</span><span class="sxs-lookup"><span data-stu-id="fca79-154">Can contain additional detail about the **AdditionalSenseCode** field.</span></span>

</dd> <dt>

<span data-ttu-id="fca79-155">**FieldReplaceableUnitCode**</span><span class="sxs-lookup"><span data-stu-id="fca79-155">**FieldReplaceableUnitCode**</span></span>
</dt> <dd>

<span data-ttu-id="fca79-156">Información específica del expendedor sobre el componente asociado a estos datos de detección.</span><span class="sxs-lookup"><span data-stu-id="fca79-156">Vender-specific information about the component associated with this sense data.</span></span>

</dd> <dt>

<span data-ttu-id="fca79-157">**SenseKeySpecific**</span><span class="sxs-lookup"><span data-stu-id="fca79-157">**SenseKeySpecific**</span></span>
</dt> <dd>

<span data-ttu-id="fca79-158">El contenido y el formato de la información específica de la clave de detección viene determinado por el valor del campo **SenseKey** .</span><span class="sxs-lookup"><span data-stu-id="fca79-158">The content and format of the sense key specific information is determined by the value of the **SenseKey** field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fca79-159">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fca79-159">Remarks</span></span>

<span data-ttu-id="fca79-160">Para obtener más información sobre el formato de datos de detección, consulte [comando de sentido de solicitud SCSI](https://wikipedia.org/wiki/SCSI_command) ( https://wikipedia.org/wiki/SCSI_command) .</span><span class="sxs-lookup"><span data-stu-id="fca79-160">For more information about the sense data format, see [SCSI Request Sense Command](https://wikipedia.org/wiki/SCSI_command) (https://wikipedia.org/wiki/SCSI_command).</span></span>

## <a name="requirements"></a><span data-ttu-id="fca79-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fca79-161">Requirements</span></span>



| <span data-ttu-id="fca79-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="fca79-162">Requirement</span></span> | <span data-ttu-id="fca79-163">Value</span><span class="sxs-lookup"><span data-stu-id="fca79-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fca79-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fca79-164">Minimum supported client</span></span><br/> | <span data-ttu-id="fca79-165">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fca79-165">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="fca79-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fca79-166">Minimum supported server</span></span><br/> | <span data-ttu-id="fca79-167">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fca79-167">Windows Server 2003 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fca79-168">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fca79-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="fca79-169"><dt>SCSI. h</dt></span><span class="sxs-lookup"><span data-stu-id="fca79-169"><dt>Scsi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fca79-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="fca79-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fca79-171">Paso a través de destino iSCSI</span><span class="sxs-lookup"><span data-stu-id="fca79-171">iSCSI Target Pass-Through</span></span>](/powershell/module/iscsi)
</dt> <dt>

[<span data-ttu-id="fca79-172">\_paso \_ a través \_ directo de SCSI</span><span class="sxs-lookup"><span data-stu-id="fca79-172">SCSI\_PASS\_THROUGH\_DIRECT</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_pass_through_direct)
</dt> </dl>

 

 





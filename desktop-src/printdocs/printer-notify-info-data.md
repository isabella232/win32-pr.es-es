---
description: La estructura de datos de notificación de la impresora \_ \_ \_ identifica un campo de información de la impresora o del trabajo y proporciona los datos actuales para ese campo.
ms.assetid: 7a7b9e01-32e0-47f8-a5b1-5f7e6a663714
title: Estructura de PRINTER_NOTIFY_INFO_DATA (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO_DATA,
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4c76ffe70a8388e920b5f8576830e31ed23edc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277250"
---
# <a name="printer_notify_info_data-structure"></a><span data-ttu-id="f80a0-103">\_Estructura de \_ \_ datos de notificación de impresora</span><span class="sxs-lookup"><span data-stu-id="f80a0-103">PRINTER\_NOTIFY\_INFO\_DATA structure</span></span>

<span data-ttu-id="f80a0-104">La estructura de **\_ \_ \_ datos de notificación** de la impresora identifica un campo de información de la impresora o del trabajo y proporciona los datos actuales para ese campo.</span><span class="sxs-lookup"><span data-stu-id="f80a0-104">The **PRINTER\_NOTIFY\_INFO\_DATA** structure identifies a job or printer information field and provides the current data for that field.</span></span>

<span data-ttu-id="f80a0-105">La función [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) devuelve una estructura de [**\_ \_ información de notificación de impresora**](printer-notify-info.md) , que contiene una matriz de estructuras de **\_ \_ \_ datos de información de notificación de impresora** .</span><span class="sxs-lookup"><span data-stu-id="f80a0-105">The [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function returns a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, which contains an array of **PRINTER\_NOTIFY\_INFO\_DATA** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="f80a0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f80a0-106">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_INFO_DATA {
  WORD  Type;
  WORD  Field;
  DWORD Reserved;
  DWORD Id;
  union {
    DWORD  adwData[2];
    struct {
      DWORD  cbBuf;
      LPVOID pBuf;
    } Data;
  } NotifyData;
} PRINTER_NOTIFY_INFO_DATA, *PPRINTER_NOTIFY_INFO_DATA; ;
```



## <a name="members"></a><span data-ttu-id="f80a0-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f80a0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f80a0-108">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f80a0-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="f80a0-109">Indica el tipo de información proporcionado.</span><span class="sxs-lookup"><span data-stu-id="f80a0-109">Indicates the type of information provided.</span></span> <span data-ttu-id="f80a0-110">Este miembro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f80a0-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="f80a0-111">Value</span><span class="sxs-lookup"><span data-stu-id="f80a0-111">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="f80a0-112">Significado</span><span class="sxs-lookup"><span data-stu-id="f80a0-112">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <span data-ttu-id="f80a0-113"><dt>**Trabajo \_ de NOTIFICAr \_ tipo**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="f80a0-113"><dt>**JOB\_NOTIFY\_TYPE**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="f80a0-114">Indica que el miembro de **campo** especifica una \_ constante de campo de notificación de trabajo \_ \_ \* .</span><span class="sxs-lookup"><span data-stu-id="f80a0-114">Indicates that the **Field** member specifies a JOB\_NOTIFY\_FIELD\_\* constant.</span></span><br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <span data-ttu-id="f80a0-115"><dt>**Impresora \_ de NOTIFICAr el \_ tipo**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="f80a0-115"><dt>**PRINTER\_NOTIFY\_TYPE**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="f80a0-116">Indica que el miembro de **campo** especifica una \_ constante de campo de notificación de impresora \_ \_ \* .</span><span class="sxs-lookup"><span data-stu-id="f80a0-116">Indicates that the **Field** member specifies a PRINTER\_NOTIFY\_FIELD\_\* constant.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f80a0-117">**Campo**</span><span class="sxs-lookup"><span data-stu-id="f80a0-117">**Field**</span></span>
</dt> <dd>

<span data-ttu-id="f80a0-118">Indica el campo que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="f80a0-118">Indicates the field that changed.</span></span> <span data-ttu-id="f80a0-119">Para obtener una lista de los valores posibles, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f80a0-119">For a list of possible values, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="f80a0-120">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="f80a0-120">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="f80a0-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="f80a0-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f80a0-122">**Id**</span><span class="sxs-lookup"><span data-stu-id="f80a0-122">**Id**</span></span>
</dt> <dd>

<span data-ttu-id="f80a0-123">Indica el identificador de trabajo si el miembro de **tipo** especifica el tipo de notificación de trabajo \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f80a0-123">Indicates the job identifier if the **Type** member specifies JOB\_NOTIFY\_TYPE.</span></span> <span data-ttu-id="f80a0-124">Si el miembro de **tipo** especifica \_ el \_ tipo de notificación de la impresora, este miembro es indefinido.</span><span class="sxs-lookup"><span data-stu-id="f80a0-124">If the **Type** member specifies PRINTER\_NOTIFY\_TYPE, this member is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="f80a0-125">**NotifyData**</span><span class="sxs-lookup"><span data-stu-id="f80a0-125">**NotifyData**</span></span>
</dt> <dd>

<span data-ttu-id="f80a0-126">Unión de información de datos basada en los miembros de **campo** y **tipo** .</span><span class="sxs-lookup"><span data-stu-id="f80a0-126">A union of data information based on the **Type** and **Field** members.</span></span> <span data-ttu-id="f80a0-127">Para obtener una descripción del tipo de datos asociado a cada campo, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f80a0-127">For a description of the type of data associated with each field, see the Remarks section.</span></span>

<dl> <dt>

<span data-ttu-id="f80a0-128">**adwData \[ 2\]**</span><span class="sxs-lookup"><span data-stu-id="f80a0-128">**adwData\[2\]**</span></span>
</dt> <dd>

<span data-ttu-id="f80a0-129">Matriz de dos valores **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="f80a0-129">An array of two **DWORD** values.</span></span> <span data-ttu-id="f80a0-130">En el caso de los campos de información que usan un solo **DWORD**, los datos están en **adwData** \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="f80a0-130">For information fields that use only a single **DWORD**, the data is in **adwData** \[0\].</span></span>

</dd> <dt>

<span data-ttu-id="f80a0-131">**Data**</span><span class="sxs-lookup"><span data-stu-id="f80a0-131">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f80a0-132">**cbBuf**</span><span class="sxs-lookup"><span data-stu-id="f80a0-132">**cbBuf**</span></span>
</dt> <dd>

<span data-ttu-id="f80a0-133">Indica el tamaño, en bytes, del búfer al que apunta **pBuf**.</span><span class="sxs-lookup"><span data-stu-id="f80a0-133">Indicates the size, in bytes, of the buffer pointed to by **pBuf**.</span></span>

</dd> <dt>

<span data-ttu-id="f80a0-134">**pBuf**</span><span class="sxs-lookup"><span data-stu-id="f80a0-134">**pBuf**</span></span>
</dt> <dd>

<span data-ttu-id="f80a0-135">Puntero a un búfer que contiene los datos actuales del campo.</span><span class="sxs-lookup"><span data-stu-id="f80a0-135">Pointer to a buffer that contains the field's current data.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f80a0-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f80a0-136">Remarks</span></span>

<span data-ttu-id="f80a0-137">Si el miembro de **tipo** especifica el \_ tipo de notificación de impresora \_ , el miembro de **campo** puede tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f80a0-137">If the **Type** member specifies PRINTER\_NOTIFY\_TYPE, the **Field** member can be one of the following values.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f80a0-138">Campo</span><span class="sxs-lookup"><span data-stu-id="f80a0-138">Field</span></span></th>
<th><span data-ttu-id="f80a0-139">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f80a0-139">Type of data</span></span></th>
<th><span data-ttu-id="f80a0-140">Value</span><span class="sxs-lookup"><span data-stu-id="f80a0-140">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f80a0-141">PRINTER_NOTIFY_FIELD_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="f80a0-141">PRINTER_NOTIFY_FIELD_SERVER_NAME</span></span></td>
<td><span data-ttu-id="f80a0-142">No se admite.</span><span class="sxs-lookup"><span data-stu-id="f80a0-142">Not supported.</span></span></td>
<td><span data-ttu-id="f80a0-143">0x00</span><span class="sxs-lookup"><span data-stu-id="f80a0-143">0x00</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80a0-144">PRINTER_NOTIFY_FIELD_PRINTER_NAME</span><span class="sxs-lookup"><span data-stu-id="f80a0-144">PRINTER_NOTIFY_FIELD_PRINTER_NAME</span></span></td>
<td><span data-ttu-id="f80a0-145"><strong>pBuf</strong> es un puntero a una cadena terminada en null que contiene el nombre de la impresora.</span><span class="sxs-lookup"><span data-stu-id="f80a0-145"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the printer.</span></span></td>
<td><span data-ttu-id="f80a0-146">0x01</span><span class="sxs-lookup"><span data-stu-id="f80a0-146">0x01</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80a0-147">PRINTER_NOTIFY_FIELD_SHARE_NAME</span><span class="sxs-lookup"><span data-stu-id="f80a0-147">PRINTER_NOTIFY_FIELD_SHARE_NAME</span></span></td>
<td><span data-ttu-id="f80a0-148"><strong>pBuf</strong> es un puntero a una cadena terminada en null que identifica el punto de recurso compartido para la impresora.</span><span class="sxs-lookup"><span data-stu-id="f80a0-148"><strong>pBuf</strong> is a pointer to a null-terminated string that identifies the share point for the printer.</span></span></td>
<td><span data-ttu-id="f80a0-149">0x02</span><span class="sxs-lookup"><span data-stu-id="f80a0-149">0x02</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80a0-150">PRINTER_NOTIFY_FIELD_PORT_NAME</span><span class="sxs-lookup"><span data-stu-id="f80a0-150">PRINTER_NOTIFY_FIELD_PORT_NAME</span></span></td>
<td><span data-ttu-id="f80a0-151"><strong>pBuf</strong> es un puntero a una cadena terminada en null que contiene el nombre del puerto en el que se imprimirán los trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="f80a0-151"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the port that the print jobs will be printed to.</span></span> <span data-ttu-id="f80a0-152">Si &quot; &quot; se selecciona agrupación de impresoras, se trata de una lista separada por comas de puertos.</span><span class="sxs-lookup"><span data-stu-id="f80a0-152">If &quot;Printer Pooling&quot; is selected, this is a comma separated list of ports.</span></span></td>
<td><span data-ttu-id="f80a0-153">0x03</span><span class="sxs-lookup"><span data-stu-id="f80a0-153">0x03</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80a0-154">PRINTER_NOTIFY_FIELD_DRIVER_NAME</span><span class="sxs-lookup"><span data-stu-id="f80a0-154">PRINTER_NOTIFY_FIELD_DRIVER_NAME</span></span></td>
<td><span data-ttu-id="f80a0-155"><strong>pBuf</strong> es un puntero a una cadena terminada en null que contiene el nombre del controlador de la impresora.</span><span class="sxs-lookup"><span data-stu-id="f80a0-155"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the printer's driver.</span></span></td>
<td><span data-ttu-id="f80a0-156">0x04</span><span class="sxs-lookup"><span data-stu-id="f80a0-156">0x04</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80a0-157">PRINTER_NOTIFY_FIELD_COMMENT</span><span class="sxs-lookup"><span data-stu-id="f80a0-157">PRINTER_NOTIFY_FIELD_COMMENT</span></span></td>
<td><span data-ttu-id="f80a0-158"><strong>pBuf</strong> es un puntero a una cadena terminada en null que contiene la nueva cadena de comentario, que suele ser una breve descripción de la impresora.</span><span class="sxs-lookup"><span data-stu-id="f80a0-158"><strong>pBuf</strong> is a pointer to a null-terminated string containing the new comment string, which is typically a brief description of the printer.</span></span></td>
<td><span data-ttu-id="f80a0-159">0x05</span><span class="sxs-lookup"><span data-stu-id="f80a0-159">0x05</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80a0-160">PRINTER_NOTIFY_FIELD_LOCATION</span><span class="sxs-lookup"><span data-stu-id="f80a0-160">PRINTER_NOTIFY_FIELD_LOCATION</span></span></td>
<td><span data-ttu-id="f80a0-161"><strong>pBuf</strong> es un puntero a una cadena terminada en null que contiene la nueva ubicación física de la impresora (por ejemplo, &quot; Bldg.</span><span class="sxs-lookup"><span data-stu-id="f80a0-161"><strong>pBuf</strong> is a pointer to a null-terminated string containing the new physical location of the printer (for example, &quot;Bldg.</span></span> <span data-ttu-id="f80a0-162">38, habitación 1164 &quot; ).</span><span class="sxs-lookup"><span data-stu-id="f80a0-162">38, Room 1164&quot;).</span></span></td>
<td><span data-ttu-id="f80a0-163">0x06</span><span class="sxs-lookup"><span data-stu-id="f80a0-163">0x06</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80a0-164">PRINTER_NOTIFY_FIELD_DEVMODE</span><span class="sxs-lookup"><span data-stu-id="f80a0-164">PRINTER_NOTIFY_FIELD_DEVMODE</span></span></td>
<td><span data-ttu-id="f80a0-165"><strong>pBuf</strong> es un puntero a una estructura <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> que define los datos de impresora predeterminados, como la orientación del papel y la resolución.</span><span class="sxs-lookup"><span data-stu-id="f80a0-165"><strong>pBuf</strong> is a pointer to a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> structure that defines default printer data such as the paper orientation and the resolution.</span></span></td>
<td><span data-ttu-id="f80a0-166">0x07</span><span class="sxs-lookup"><span data-stu-id="f80a0-166">0x07</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80a0-167">PRINTER_NOTIFY_FIELD_SEPFILE</span><span class="sxs-lookup"><span data-stu-id="f80a0-167">PRINTER_NOTIFY_FIELD_SEPFILE</span></span></td>
<td><span data-ttu-id="f80a0-168"><strong>pBuf</strong> es un puntero a una cadena terminada en null que especifica el nombre del archivo usado para crear la página separadora.</span><span class="sxs-lookup"><span data-stu-id="f80a0-168"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the name of the file used to create the separator page.</span></span> <span data-ttu-id="f80a0-169">Esta página se utiliza para separar los trabajos de impresión que se envían a la impresora.</span><span class="sxs-lookup"><span data-stu-id="f80a0-169">This page is used to separate print jobs sent to the printer.</span></span></td>
<td><span data-ttu-id="f80a0-170">0x08</span><span class="sxs-lookup"><span data-stu-id="f80a0-170">0x08</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80a0-171">PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</span><span class="sxs-lookup"><span data-stu-id="f80a0-171">PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</span></span></td>
<td><span data-ttu-id="f80a0-172"><strong>pBuf</strong> es un puntero a una cadena terminada en null que especifica el nombre del procesador de impresión utilizado por la impresora.</span><span class="sxs-lookup"><span data-stu-id="f80a0-172"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the name of the print processor used by the printer.</span></span></td>
<td><span data-ttu-id="f80a0-173">0x09</span><span class="sxs-lookup"><span data-stu-id="f80a0-173">0x09</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80a0-174">PRINTER_NOTIFY_FIELD_PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f80a0-174">PRINTER_NOTIFY_FIELD_PARAMETERS</span></span></td>
<td><span data-ttu-id="f80a0-175"><strong>pBuf</strong> es un puntero a una cadena terminada en null que especifica los parámetros predeterminados del procesador de impresión.</span><span class="sxs-lookup"><span data-stu-id="f80a0-175"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the default print-processor parameters.</span></span></td>
<td><span data-ttu-id="f80a0-176">0x0A</span><span class="sxs-lookup"><span data-stu-id="f80a0-176">0x0A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80a0-177">PRINTER_NOTIFY_FIELD_DATATYPE</span><span class="sxs-lookup"><span data-stu-id="f80a0-177">PRINTER_NOTIFY_FIELD_DATATYPE</span></span></td>
<td><span data-ttu-id="f80a0-178"><strong>pBuf</strong> es un puntero a una cadena terminada en null que especifica el tipo de datos utilizado para registrar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="f80a0-178"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the data type used to record the print job.</span></span></td>
<td><span data-ttu-id="f80a0-179">0x0B</span><span class="sxs-lookup"><span data-stu-id="f80a0-179">0x0B</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80a0-180">PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</span><span class="sxs-lookup"><span data-stu-id="f80a0-180">PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</span></span></td>
<td><span data-ttu-id="f80a0-181"><strong>pBuf</strong> es un puntero a una estructura de <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> para la impresora.</span><span class="sxs-lookup"><span data-stu-id="f80a0-181"><strong>pBuf</strong> is a pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> structure for the printer.</span></span> <span data-ttu-id="f80a0-182">El puntero puede ser <strong>null</strong> si no hay ningún descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f80a0-182">The pointer may be <strong>NULL</strong> if there is no security descriptor.</span></span></td>
<td><span data-ttu-id="f80a0-183">0x0C</span><span class="sxs-lookup"><span data-stu-id="f80a0-183">0x0C</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80a0-184">PRINTER_NOTIFY_FIELD_ATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="f80a0-184">PRINTER_NOTIFY_FIELD_ATTRIBUTES</span></span></td>
<td><span data-ttu-id="f80a0-185"><strong>adwData</strong> [0] especifica los atributos de la impresora, que pueden ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="f80a0-185"><strong>adwData</strong> [0] specifies the printer attributes, which can be one of the following values:</span></span><dl> <span data-ttu-id="f80a0-186">PRINTER_ATTRIBUTE_QUEUED</span><span class="sxs-lookup"><span data-stu-id="f80a0-186">PRINTER_ATTRIBUTE_QUEUED</span></span><br />
<span data-ttu-id="f80a0-187">PRINTER_ATTRIBUTE_DIRECT</span><span class="sxs-lookup"><span data-stu-id="f80a0-187">PRINTER_ATTRIBUTE_DIRECT</span></span><br />
<span data-ttu-id="f80a0-188">PRINTER_ATTRIBUTE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="f80a0-188">PRINTER_ATTRIBUTE_DEFAULT</span></span><br />
<span data-ttu-id="f80a0-189">PRINTER_ATTRIBUTE_SHARED</span><span class="sxs-lookup"><span data-stu-id="f80a0-189">PRINTER_ATTRIBUTE_SHARED</span></span><br />
</dl></td>
<td><span data-ttu-id="f80a0-190">0x0D</span><span class="sxs-lookup"><span data-stu-id="f80a0-190">0x0D</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80a0-191">PRINTER_NOTIFY_FIELD_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="f80a0-191">PRINTER_NOTIFY_FIELD_PRIORITY</span></span></td>
<td><span data-ttu-id="f80a0-192"><strong>adwData</strong> [0] especifica un valor de prioridad que el administrador de trabajos de impresión utiliza para enrutar los trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="f80a0-192"><strong>adwData</strong> [0] specifies a priority value that the spooler uses to route print jobs.</span></span></td>
<td><span data-ttu-id="f80a0-193">0x0E</span><span class="sxs-lookup"><span data-stu-id="f80a0-193">0x0E</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80a0-194">PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="f80a0-194">PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</span></span></td>
<td><span data-ttu-id="f80a0-195"><strong>adwData</strong> [0] especifica el valor de prioridad predeterminado asignado a cada trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="f80a0-195"><strong>adwData</strong> [0] specifies the default priority value assigned to each print job.</span></span></td>
<td><span data-ttu-id="f80a0-196">0x0F</span><span class="sxs-lookup"><span data-stu-id="f80a0-196">0x0F</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80a0-197">PRINTER_NOTIFY_FIELD_START_TIME</span><span class="sxs-lookup"><span data-stu-id="f80a0-197">PRINTER_NOTIFY_FIELD_START_TIME</span></span></td>
<td><span data-ttu-id="f80a0-198"><strong>adwData</strong> [0] especifica la primera hora en la que la impresora imprimirá un trabajo.</span><span class="sxs-lookup"><span data-stu-id="f80a0-198"><strong>adwData</strong> [0] specifies the earliest time at which the printer will print a job.</span></span> <span data-ttu-id="f80a0-199">(Este valor se especifica en minutos transcurridos desde las 12:00 A.M.)</span><span class="sxs-lookup"><span data-stu-id="f80a0-199">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span></td>
<td><span data-ttu-id="f80a0-200">0x10</span><span class="sxs-lookup"><span data-stu-id="f80a0-200">0x10</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80a0-201">PRINTER_NOTIFY_FIELD_UNTIL_TIME</span><span class="sxs-lookup"><span data-stu-id="f80a0-201">PRINTER_NOTIFY_FIELD_UNTIL_TIME</span></span></td>
<td><span data-ttu-id="f80a0-202"><strong>adwData</strong> [0] especifica la hora más reciente en la que la impresora imprimirá un trabajo.</span><span class="sxs-lookup"><span data-stu-id="f80a0-202"><strong>adwData</strong> [0] specifies the latest time at which the printer will print a job.</span></span> <span data-ttu-id="f80a0-203">(Este valor se especifica en minutos transcurridos desde las 12:00 A.M.)</span><span class="sxs-lookup"><span data-stu-id="f80a0-203">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span></td>
<td><span data-ttu-id="f80a0-204">0x11</span><span class="sxs-lookup"><span data-stu-id="f80a0-204">0x11</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80a0-205">PRINTER_NOTIFY_FIELD_STATUS</span><span class="sxs-lookup"><span data-stu-id="f80a0-205">PRINTER_NOTIFY_FIELD_STATUS</span></span></td>
<td><span data-ttu-id="f80a0-206"><strong>adwData</strong> [0] especifica el estado de la impresora.</span><span class="sxs-lookup"><span data-stu-id="f80a0-206"><strong>adwData</strong> [0] specifies the printer status.</span></span> <span data-ttu-id="f80a0-207">Para obtener una lista de los valores posibles, vea la estructura <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f80a0-207">For a list of possible values, see the <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> structure.</span></span></td>
<td><span data-ttu-id="f80a0-208">0X12</span><span class="sxs-lookup"><span data-stu-id="f80a0-208">0x12</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80a0-209">PRINTER_NOTIFY_FIELD_STATUS_STRING</span><span class="sxs-lookup"><span data-stu-id="f80a0-209">PRINTER_NOTIFY_FIELD_STATUS_STRING</span></span></td>
<td><span data-ttu-id="f80a0-210">No se admite.</span><span class="sxs-lookup"><span data-stu-id="f80a0-210">Not supported.</span></span></td>
<td><span data-ttu-id="f80a0-211">0x13</span><span class="sxs-lookup"><span data-stu-id="f80a0-211">0x13</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80a0-212">PRINTER_NOTIFY_FIELD_CJOBS</span><span class="sxs-lookup"><span data-stu-id="f80a0-212">PRINTER_NOTIFY_FIELD_CJOBS</span></span></td>
<td><span data-ttu-id="f80a0-213"><strong>adwData</strong> [0] especifica el número de trabajos de impresión que se han puesto en cola para la impresora.</span><span class="sxs-lookup"><span data-stu-id="f80a0-213"><strong>adwData</strong> [0] specifies the number of print jobs that have been queued for the printer.</span></span></td>
<td><span data-ttu-id="f80a0-214">0x14</span><span class="sxs-lookup"><span data-stu-id="f80a0-214">0x14</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80a0-215">PRINTER_NOTIFY_FIELD_AVERAGE_PPM</span><span class="sxs-lookup"><span data-stu-id="f80a0-215">PRINTER_NOTIFY_FIELD_AVERAGE_PPM</span></span></td>
<td><span data-ttu-id="f80a0-216"><strong>adwData</strong> [0] especifica el número medio de páginas por minuto que se han impreso en la impresora.</span><span class="sxs-lookup"><span data-stu-id="f80a0-216"><strong>adwData</strong> [0] specifies the average number of pages per minute that have been printed on the printer.</span></span></td>
<td><span data-ttu-id="f80a0-217">0x15</span><span class="sxs-lookup"><span data-stu-id="f80a0-217">0x15</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80a0-218">PRINTER_NOTIFY_FIELD_TOTAL_PAGES</span><span class="sxs-lookup"><span data-stu-id="f80a0-218">PRINTER_NOTIFY_FIELD_TOTAL_PAGES</span></span></td>
<td><span data-ttu-id="f80a0-219">No se admite.</span><span class="sxs-lookup"><span data-stu-id="f80a0-219">Not supported.</span></span></td>
<td><span data-ttu-id="f80a0-220">0x16</span><span class="sxs-lookup"><span data-stu-id="f80a0-220">0x16</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80a0-221">PRINTER_NOTIFY_FIELD_PAGES_PRINTED</span><span class="sxs-lookup"><span data-stu-id="f80a0-221">PRINTER_NOTIFY_FIELD_PAGES_PRINTED</span></span></td>
<td><span data-ttu-id="f80a0-222">No se admite.</span><span class="sxs-lookup"><span data-stu-id="f80a0-222">Not supported.</span></span></td>
<td><span data-ttu-id="f80a0-223">0 x 17</span><span class="sxs-lookup"><span data-stu-id="f80a0-223">0x17</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80a0-224">PRINTER_NOTIFY_FIELD_TOTAL_BYTES</span><span class="sxs-lookup"><span data-stu-id="f80a0-224">PRINTER_NOTIFY_FIELD_TOTAL_BYTES</span></span></td>
<td><span data-ttu-id="f80a0-225">No se admite.</span><span class="sxs-lookup"><span data-stu-id="f80a0-225">Not supported.</span></span></td>
<td><span data-ttu-id="f80a0-226">0x18</span><span class="sxs-lookup"><span data-stu-id="f80a0-226">0x18</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80a0-227">PRINTER_NOTIFY_FIELD_BYTES_PRINTED</span><span class="sxs-lookup"><span data-stu-id="f80a0-227">PRINTER_NOTIFY_FIELD_BYTES_PRINTED</span></span></td>
<td><span data-ttu-id="f80a0-228">No se admite.</span><span class="sxs-lookup"><span data-stu-id="f80a0-228">Not supported.</span></span></td>
<td><span data-ttu-id="f80a0-229">0x19</span><span class="sxs-lookup"><span data-stu-id="f80a0-229">0x19</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80a0-230">PRINTER_NOTIFY_FIELD_OBJECT_GUID</span><span class="sxs-lookup"><span data-stu-id="f80a0-230">PRINTER_NOTIFY_FIELD_OBJECT_GUID</span></span></td>
<td><span data-ttu-id="f80a0-231">Se establece si el GUID del objeto cambia.</span><span class="sxs-lookup"><span data-stu-id="f80a0-231">This is set if the object GUID changes.</span></span></td>
<td><span data-ttu-id="f80a0-232">0x1A</span><span class="sxs-lookup"><span data-stu-id="f80a0-232">0x1A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80a0-233">PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="f80a0-233">PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</span></span></td>
<td><span data-ttu-id="f80a0-234">Se establece si se cambia el nombre de la conexión de impresora.</span><span class="sxs-lookup"><span data-stu-id="f80a0-234">This is set if the printer connection is renamed.</span></span></td>
<td><span data-ttu-id="f80a0-235">0x1B</span><span class="sxs-lookup"><span data-stu-id="f80a0-235">0x1B</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f80a0-236">Si el miembro de **tipo** especifica el \_ tipo de notificación de trabajo \_ , el miembro de **campo** puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f80a0-236">If the **Type** member specifies JOB\_NOTIFY\_TYPE, the **Field** member can be one of the following values.</span></span>



| <span data-ttu-id="f80a0-237">Campo</span><span class="sxs-lookup"><span data-stu-id="f80a0-237">Field</span></span>                                    | <span data-ttu-id="f80a0-238">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f80a0-238">Type of data</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="f80a0-239">Value</span><span class="sxs-lookup"><span data-stu-id="f80a0-239">Value</span></span> |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="f80a0-240">\_nombre de \_ impresora del campo de notificación de trabajo \_ \_</span><span class="sxs-lookup"><span data-stu-id="f80a0-240">JOB\_NOTIFY\_FIELD\_PRINTER\_NAME</span></span>        | <span data-ttu-id="f80a0-241">**pBuf** es un puntero a una cadena terminada en null que contiene el nombre de la impresora para la que se pone en cola el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f80a0-241">**pBuf** is a pointer to a null-terminated string containing the name of the printer for which the job is spooled.</span></span>                                                                                                                                      | <span data-ttu-id="f80a0-242">0x00</span><span class="sxs-lookup"><span data-stu-id="f80a0-242">0x00</span></span>  |
| <span data-ttu-id="f80a0-243">\_nombre de \_ equipo de campo de notificación de trabajo \_ \_</span><span class="sxs-lookup"><span data-stu-id="f80a0-243">JOB\_NOTIFY\_FIELD\_MACHINE\_NAME</span></span>        | <span data-ttu-id="f80a0-244">**pBuf** es un puntero a una cadena terminada en null que especifica el nombre del equipo que creó el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="f80a0-244">**pBuf** is a pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>                                                                                                                                    | <span data-ttu-id="f80a0-245">0x01</span><span class="sxs-lookup"><span data-stu-id="f80a0-245">0x01</span></span>  |
| <span data-ttu-id="f80a0-246">\_nombre de \_ Puerto de campo de notificación de trabajo \_ \_</span><span class="sxs-lookup"><span data-stu-id="f80a0-246">JOB\_NOTIFY\_FIELD\_PORT\_NAME</span></span>           | <span data-ttu-id="f80a0-247">**pBuf** es un puntero a una cadena terminada en null que identifica los puertos que se usan para transmitir datos a la impresora.</span><span class="sxs-lookup"><span data-stu-id="f80a0-247">**pBuf** is a pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="f80a0-248">Si una impresora está conectada a más de un puerto, los nombres de los puertos se separan por comas (por ejemplo, "LPT1:, LPT2:, LPT3:").</span><span class="sxs-lookup"><span data-stu-id="f80a0-248">If a printer is connected to more than one port, the names of the ports are separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span> | <span data-ttu-id="f80a0-249">0x02</span><span class="sxs-lookup"><span data-stu-id="f80a0-249">0x02</span></span>  |
| <span data-ttu-id="f80a0-250">\_nombre de \_ usuario del campo de notificación de trabajo \_ \_</span><span class="sxs-lookup"><span data-stu-id="f80a0-250">JOB\_NOTIFY\_FIELD\_USER\_NAME</span></span>           | <span data-ttu-id="f80a0-251">**pBuf** es un puntero a una cadena terminada en null que especifica el nombre del usuario que envió el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="f80a0-251">**pBuf** is a pointer to a null-terminated string that specifies the name of the user who sent the print job.</span></span>                                                                                                                                           | <span data-ttu-id="f80a0-252">0x03</span><span class="sxs-lookup"><span data-stu-id="f80a0-252">0x03</span></span>  |
| <span data-ttu-id="f80a0-253">\_nombre de \_ notificación de campo de notificación de trabajo \_ \_</span><span class="sxs-lookup"><span data-stu-id="f80a0-253">JOB\_NOTIFY\_FIELD\_NOTIFY\_NAME</span></span>         | <span data-ttu-id="f80a0-254">**pBuf** es un puntero a una cadena terminada en null que especifica el nombre del usuario al que se debe notificar cuando se ha impreso el trabajo o cuando se produce un error durante la impresión del trabajo.</span><span class="sxs-lookup"><span data-stu-id="f80a0-254">**pBuf** is a pointer to a null-terminated string that specifies the name of the user who should be notified when the job has been printed or when an error occurs while printing the job.</span></span>                                                              | <span data-ttu-id="f80a0-255">0x04</span><span class="sxs-lookup"><span data-stu-id="f80a0-255">0x04</span></span>  |
| <span data-ttu-id="f80a0-256">\_tipo de \_ campo de notificación de trabajo \_</span><span class="sxs-lookup"><span data-stu-id="f80a0-256">JOB\_NOTIFY\_FIELD\_DATATYPE</span></span>             | <span data-ttu-id="f80a0-257">**pBuf** es un puntero a una cadena terminada en null que especifica el tipo de datos que se usa para registrar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="f80a0-257">**pBuf** is a pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>                                                                                                                                         | <span data-ttu-id="f80a0-258">0x05</span><span class="sxs-lookup"><span data-stu-id="f80a0-258">0x05</span></span>  |
| <span data-ttu-id="f80a0-259">\_procesador de \_ impresión de campo de notificación de trabajo \_ \_</span><span class="sxs-lookup"><span data-stu-id="f80a0-259">JOB\_NOTIFY\_FIELD\_PRINT\_PROCESSOR</span></span>     | <span data-ttu-id="f80a0-260">**pBuf** es un puntero a una cadena terminada en null que especifica el nombre del procesador de impresión que se va a usar para imprimir el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f80a0-260">**pBuf** is a pointer to a null-terminated string that specifies the name of the print processor to be used to print the job.</span></span>                                                                                                                           | <span data-ttu-id="f80a0-261">0x06</span><span class="sxs-lookup"><span data-stu-id="f80a0-261">0x06</span></span>  |
| <span data-ttu-id="f80a0-262">\_parámetros de \_ campo de notificación de trabajo \_</span><span class="sxs-lookup"><span data-stu-id="f80a0-262">JOB\_NOTIFY\_FIELD\_PARAMETERS</span></span>           | <span data-ttu-id="f80a0-263">**pBuf** es un puntero a una cadena terminada en null que especifica los parámetros del procesador de impresión.</span><span class="sxs-lookup"><span data-stu-id="f80a0-263">**pBuf** is a pointer to a null-terminated string that specifies print-processor parameters.</span></span>                                                                                                                                                            | <span data-ttu-id="f80a0-264">0x07</span><span class="sxs-lookup"><span data-stu-id="f80a0-264">0x07</span></span>  |
| <span data-ttu-id="f80a0-265">\_nombre del \_ controlador de campo de notificación de trabajo \_ \_</span><span class="sxs-lookup"><span data-stu-id="f80a0-265">JOB\_NOTIFY\_FIELD\_DRIVER\_NAME</span></span>         | <span data-ttu-id="f80a0-266">**pBuf** es un puntero a una cadena terminada en null que especifica el nombre del controlador de impresora que se debe usar para procesar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="f80a0-266">**pBuf** is a pointer to a null-terminated string that specifies the name of the printer driver that should be used to process the print job.</span></span>                                                                                                           | <span data-ttu-id="f80a0-267">0x08</span><span class="sxs-lookup"><span data-stu-id="f80a0-267">0x08</span></span>  |
| <span data-ttu-id="f80a0-268">campo de notificación de trabajo \_ \_ \_ DEVMODE</span><span class="sxs-lookup"><span data-stu-id="f80a0-268">JOB\_NOTIFY\_FIELD\_DEVMODE</span></span>              | <span data-ttu-id="f80a0-269">**pBuf** es un puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contiene datos de entorno y de inicialización del dispositivo para el controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="f80a0-269">**pBuf** is a pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains device-initialization and environment data for the printer driver.</span></span>                                                                                                        | <span data-ttu-id="f80a0-270">0x09</span><span class="sxs-lookup"><span data-stu-id="f80a0-270">0x09</span></span>  |
| <span data-ttu-id="f80a0-271">\_Estado de \_ campo de notificación de trabajo \_</span><span class="sxs-lookup"><span data-stu-id="f80a0-271">JOB\_NOTIFY\_FIELD\_STATUS</span></span>               | <span data-ttu-id="f80a0-272">**adwData** \[ 0 \] especifica el estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="f80a0-272">**adwData** \[0\] specifies the job status.</span></span> <span data-ttu-id="f80a0-273">Para obtener una lista de los valores posibles, consulte la estructura [**Job \_ info \_ 2**](job-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="f80a0-273">For a list of possible values, see the [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>                                                                                                                        | <span data-ttu-id="f80a0-274">0x0A</span><span class="sxs-lookup"><span data-stu-id="f80a0-274">0x0A</span></span>  |
| <span data-ttu-id="f80a0-275">\_cadena de \_ Estado de campo de notificación de trabajo \_ \_</span><span class="sxs-lookup"><span data-stu-id="f80a0-275">JOB\_NOTIFY\_FIELD\_STATUS\_STRING</span></span>       | <span data-ttu-id="f80a0-276">**pBuf** es un puntero a una cadena terminada en null que especifica el estado del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="f80a0-276">**pBuf** is a pointer to a null-terminated string that specifies the status of the print job.</span></span>                                                                                                                                                           | <span data-ttu-id="f80a0-277">0x0B</span><span class="sxs-lookup"><span data-stu-id="f80a0-277">0x0B</span></span>  |
| <span data-ttu-id="f80a0-278">\_descriptor de seguridad de campo de notificación de trabajo \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="f80a0-278">JOB\_NOTIFY\_FIELD\_SECURITY\_DESCRIPTOR</span></span> | <span data-ttu-id="f80a0-279">No se admite.</span><span class="sxs-lookup"><span data-stu-id="f80a0-279">Not supported.</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="f80a0-280">0x0C</span><span class="sxs-lookup"><span data-stu-id="f80a0-280">0x0C</span></span>  |
| <span data-ttu-id="f80a0-281">\_documento de \_ campo de notificación de trabajo \_</span><span class="sxs-lookup"><span data-stu-id="f80a0-281">JOB\_NOTIFY\_FIELD\_DOCUMENT</span></span>             | <span data-ttu-id="f80a0-282">**pBuf** es un puntero a una cadena terminada en null que especifica el nombre del trabajo de impresión (por ejemplo, "MS-WORD: Review.doc").</span><span class="sxs-lookup"><span data-stu-id="f80a0-282">**pBuf** is a pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>                                                                                                                        | <span data-ttu-id="f80a0-283">0x0D</span><span class="sxs-lookup"><span data-stu-id="f80a0-283">0x0D</span></span>  |
| <span data-ttu-id="f80a0-284">\_prioridad de \_ campo de notificación de trabajo \_</span><span class="sxs-lookup"><span data-stu-id="f80a0-284">JOB\_NOTIFY\_FIELD\_PRIORITY</span></span>             | <span data-ttu-id="f80a0-285">**adwData** \[ 0 \] especifica la prioridad del trabajo.</span><span class="sxs-lookup"><span data-stu-id="f80a0-285">**adwData** \[0\] specifies the job priority.</span></span>                                                                                                                                                                                                           | <span data-ttu-id="f80a0-286">0x0E</span><span class="sxs-lookup"><span data-stu-id="f80a0-286">0x0E</span></span>  |
| <span data-ttu-id="f80a0-287">\_posición del \_ campo de notificación del trabajo \_</span><span class="sxs-lookup"><span data-stu-id="f80a0-287">JOB\_NOTIFY\_FIELD\_POSITION</span></span>             | <span data-ttu-id="f80a0-288">**adwData** \[ 0 \] especifica la posición del trabajo en la cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="f80a0-288">**adwData** \[0\] specifies the job's position in the print queue.</span></span>                                                                                                                                                                                      | <span data-ttu-id="f80a0-289">0x0F</span><span class="sxs-lookup"><span data-stu-id="f80a0-289">0x0F</span></span>  |
| <span data-ttu-id="f80a0-290">campo de notificación de trabajo \_ \_ \_ enviado</span><span class="sxs-lookup"><span data-stu-id="f80a0-290">JOB\_NOTIFY\_FIELD\_SUBMITTED</span></span>            | <span data-ttu-id="f80a0-291">**pBuf** es un puntero a una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que especifica la hora a la que se envió el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f80a0-291">**pBuf** is a pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time when the job was submitted.</span></span>                                                                                                                          | <span data-ttu-id="f80a0-292">0x10</span><span class="sxs-lookup"><span data-stu-id="f80a0-292">0x10</span></span>  |
| <span data-ttu-id="f80a0-293">\_hora de \_ Inicio del campo de notificación de trabajo \_ \_</span><span class="sxs-lookup"><span data-stu-id="f80a0-293">JOB\_NOTIFY\_FIELD\_START\_TIME</span></span>          | <span data-ttu-id="f80a0-294">**adwData** \[ 0 \] especifica la hora más temprana en que se puede imprimir el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f80a0-294">**adwData** \[0\] specifies the earliest time that the job can be printed.</span></span> <span data-ttu-id="f80a0-295">(Este valor se especifica en minutos transcurridos desde las 12:00 A.M.)</span><span class="sxs-lookup"><span data-stu-id="f80a0-295">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span>                                                                                                                | <span data-ttu-id="f80a0-296">0x11</span><span class="sxs-lookup"><span data-stu-id="f80a0-296">0x11</span></span>  |
| <span data-ttu-id="f80a0-297">campo de notificación de trabajo \_ \_ hasta la \_ \_ hora</span><span class="sxs-lookup"><span data-stu-id="f80a0-297">JOB\_NOTIFY\_FIELD\_UNTIL\_TIME</span></span>          | <span data-ttu-id="f80a0-298">**adwData** \[ 0 \] especifica la última hora a la que se puede imprimir el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f80a0-298">**adwData** \[0\] specifies the latest time that the job can be printed.</span></span> <span data-ttu-id="f80a0-299">(Este valor se especifica en minutos transcurridos desde las 12:00 A.M.)</span><span class="sxs-lookup"><span data-stu-id="f80a0-299">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span>                                                                                                                  | <span data-ttu-id="f80a0-300">0X12</span><span class="sxs-lookup"><span data-stu-id="f80a0-300">0x12</span></span>  |
| <span data-ttu-id="f80a0-301">\_tiempo de \_ campo de notificación de trabajo \_</span><span class="sxs-lookup"><span data-stu-id="f80a0-301">JOB\_NOTIFY\_FIELD\_TIME</span></span>                 | <span data-ttu-id="f80a0-302">**adwData** \[ 0 \] especifica el tiempo total, en segundos, que ha transcurrido desde que comenzó la impresión del trabajo.</span><span class="sxs-lookup"><span data-stu-id="f80a0-302">**adwData** \[0\] specifies the total time, in seconds, that has elapsed since the job began printing.</span></span>                                                                                                                                                  | <span data-ttu-id="f80a0-303">0x13</span><span class="sxs-lookup"><span data-stu-id="f80a0-303">0x13</span></span>  |
| <span data-ttu-id="f80a0-304">\_ \_ páginas totales de campo de notificación de \_ trabajo \_</span><span class="sxs-lookup"><span data-stu-id="f80a0-304">JOB\_NOTIFY\_FIELD\_TOTAL\_PAGES</span></span>         | <span data-ttu-id="f80a0-305">**adwData** \[ 0 \] especifica el tamaño, en páginas, del trabajo.</span><span class="sxs-lookup"><span data-stu-id="f80a0-305">**adwData** \[0\] specifies the size, in pages, of the job.</span></span>                                                                                                                                                                                             | <span data-ttu-id="f80a0-306">0x14</span><span class="sxs-lookup"><span data-stu-id="f80a0-306">0x14</span></span>  |
| <span data-ttu-id="f80a0-307">páginas de campo de notificación de trabajo \_ \_ \_ \_ impresas</span><span class="sxs-lookup"><span data-stu-id="f80a0-307">JOB\_NOTIFY\_FIELD\_PAGES\_PRINTED</span></span>       | <span data-ttu-id="f80a0-308">**adwData** \[ 0 \] especifica el número de páginas que se han impreso.</span><span class="sxs-lookup"><span data-stu-id="f80a0-308">**adwData** \[0\] specifies the number of pages that have printed.</span></span>                                                                                                                                                                                      | <span data-ttu-id="f80a0-309">0x15</span><span class="sxs-lookup"><span data-stu-id="f80a0-309">0x15</span></span>  |
| <span data-ttu-id="f80a0-310">\_ \_ bytes totales de campo de notificación \_ de trabajo \_</span><span class="sxs-lookup"><span data-stu-id="f80a0-310">JOB\_NOTIFY\_FIELD\_TOTAL\_BYTES</span></span>         | <span data-ttu-id="f80a0-311">**adwData** \[ 0 \] especifica el tamaño, en bytes, del trabajo.</span><span class="sxs-lookup"><span data-stu-id="f80a0-311">**adwData** \[0\] specifies the size, in bytes, of the job.</span></span>                                                                                                                                                                                             | <span data-ttu-id="f80a0-312">0x16</span><span class="sxs-lookup"><span data-stu-id="f80a0-312">0x16</span></span>  |
| <span data-ttu-id="f80a0-313">\_bytes de campo de notificación de trabajo \_ \_ \_ impresos</span><span class="sxs-lookup"><span data-stu-id="f80a0-313">JOB\_NOTIFY\_FIELD\_BYTES\_PRINTED</span></span>       | <span data-ttu-id="f80a0-314">**adwData** \[ 0 \] especifica el número de bytes que se han impreso en este trabajo.</span><span class="sxs-lookup"><span data-stu-id="f80a0-314">**adwData** \[0\] specifies the number of bytes that have been printed on this job.</span></span> <span data-ttu-id="f80a0-315">En este campo, el objeto de notificación de cambios se señaliza cuando se envían bytes a la impresora.</span><span class="sxs-lookup"><span data-stu-id="f80a0-315">For this field, the change notification object is signaled when bytes are sent to the printer.</span></span>                                                                      | <span data-ttu-id="f80a0-316">0 x 17</span><span class="sxs-lookup"><span data-stu-id="f80a0-316">0x17</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="f80a0-317">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f80a0-317">Requirements</span></span>



| <span data-ttu-id="f80a0-318">Requisito</span><span class="sxs-lookup"><span data-stu-id="f80a0-318">Requirement</span></span> | <span data-ttu-id="f80a0-319">Value</span><span class="sxs-lookup"><span data-stu-id="f80a0-319">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f80a0-320">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f80a0-320">Minimum supported client</span></span><br/> | <span data-ttu-id="f80a0-321">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f80a0-321">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f80a0-322">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f80a0-322">Minimum supported server</span></span><br/> | <span data-ttu-id="f80a0-323">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f80a0-323">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f80a0-324">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f80a0-324">Header</span></span><br/>                   | <dl> <span data-ttu-id="f80a0-325"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f80a0-325"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f80a0-326">Vea también</span><span class="sxs-lookup"><span data-stu-id="f80a0-326">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f80a0-327">Impresión</span><span class="sxs-lookup"><span data-stu-id="f80a0-327">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f80a0-328">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="f80a0-328">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="f80a0-329">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="f80a0-329">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="f80a0-330">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="f80a0-330">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="f80a0-331">**Información de trabajo \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="f80a0-331">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="f80a0-332">**Información de la impresora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="f80a0-332">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="f80a0-333">**\_información de notificación de impresora \_**</span><span class="sxs-lookup"><span data-stu-id="f80a0-333">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> <dt>

[<span data-ttu-id="f80a0-334">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="f80a0-334">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="f80a0-335">**SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="f80a0-335">**SYSTEMTIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>


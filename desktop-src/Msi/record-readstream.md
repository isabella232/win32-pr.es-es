---
description: El método ReadStream del objeto record Lee un número especificado de bytes de un campo registro que contiene los datos de la secuencia.
ms.assetid: 845e23e5-6379-4592-aee4-cd6832baf335
title: Método record. ReadStream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.ReadStream
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bc77e07231d086f15086662d60581d4c5992bf5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670966"
---
# <a name="recordreadstream-method"></a><span data-ttu-id="f224e-103">Método record. ReadStream</span><span class="sxs-lookup"><span data-stu-id="f224e-103">Record.ReadStream method</span></span>

<span data-ttu-id="f224e-104">El método **ReadStream** del objeto [**Record**](record-object.md) Lee un número especificado de bytes de un campo registro que contiene los datos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f224e-104">The **ReadStream** method of the [**Record**](record-object.md) object reads a specified number of bytes from a record field that contains stream data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f224e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f224e-105">Syntax</span></span>


```JScript
Record.ReadStream(
  field,
  length,
  format
)
```



## <a name="parameters"></a><span data-ttu-id="f224e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f224e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f224e-107">*campo*</span><span class="sxs-lookup"><span data-stu-id="f224e-107">*field*</span></span> 
</dt> <dd>

<span data-ttu-id="f224e-108">El número de campo necesario del valor dentro del registro, basado en 1.</span><span class="sxs-lookup"><span data-stu-id="f224e-108">The required field number of the value within the record, 1-based.</span></span>

</dd> <dt>

<span data-ttu-id="f224e-109">*length*</span><span class="sxs-lookup"><span data-stu-id="f224e-109">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="f224e-110">Número necesario de bytes que se van a leer de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f224e-110">The required number of bytes to read from the stream.</span></span>

</dd> <dt>

<span data-ttu-id="f224e-111">*format*</span><span class="sxs-lookup"><span data-stu-id="f224e-111">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="f224e-112">Interpretación requerida y devolución de los bytes de datos.</span><span class="sxs-lookup"><span data-stu-id="f224e-112">Required interpretation and return of the data bytes.</span></span>



| <span data-ttu-id="f224e-113">Nombre de parámetro</span><span class="sxs-lookup"><span data-stu-id="f224e-113">Parameter name</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="f224e-114">Significado</span><span class="sxs-lookup"><span data-stu-id="f224e-114">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="msiReadStreamInteger"></span><span id="msireadstreaminteger"></span><span id="MSIREADSTREAMINTEGER"></span><dl> <span data-ttu-id="f224e-115"><dt>**msiReadStreamInteger**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f224e-115"><dt>**msiReadStreamInteger**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="f224e-116">Como entero largo, la longitud debe ser de 1 a 4.</span><span class="sxs-lookup"><span data-stu-id="f224e-116">As a long integer the length must be 1 to 4.</span></span><br/>             |
| <span id="msiReadStreamBytes"></span><span id="msireadstreambytes"></span><span id="MSIREADSTREAMBYTES"></span><dl> <span data-ttu-id="f224e-117"><dt>**msiReadStreamBytes**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f224e-117"><dt>**msiReadStreamBytes**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="f224e-118">Los datos como un **BSTR**: un byte por carácter.</span><span class="sxs-lookup"><span data-stu-id="f224e-118">The data as a **BSTR**—one byte per character.</span></span><br/>           |
| <span id="msiReadStreamAnsi"></span><span id="msireadstreamansi"></span><span id="MSIREADSTREAMANSI"></span><dl> <span data-ttu-id="f224e-119"><dt>**msiReadStreamAnsi**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f224e-119"><dt>**msiReadStreamAnsi**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="f224e-120">Bytes ANSI convertidos en un **BSTR** Unicode.</span><span class="sxs-lookup"><span data-stu-id="f224e-120">The ANSI bytes translated to a Unicode **BSTR**.</span></span><br/>         |
| <span id="msiReadStreamDirect"></span><span id="msireadstreamdirect"></span><span id="MSIREADSTREAMDIRECT"></span><dl> <span data-ttu-id="f224e-121"><dt>**msiReadStreamDirect**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f224e-121"><dt>**msiReadStreamDirect**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="f224e-122">Pares de bytes que se devuelven directamente como **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="f224e-122">The byte pairs that are returned directly as a **BSTR**.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f224e-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f224e-123">Return value</span></span>

<span data-ttu-id="f224e-124">Este método devuelve una cadena que contiene el número solicitado de bytes leídos de un campo de registro.</span><span class="sxs-lookup"><span data-stu-id="f224e-124">This method returns a string that contains the requested number of bytes read from a record field.</span></span>

## <a name="remarks"></a><span data-ttu-id="f224e-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f224e-125">Remarks</span></span>

<span data-ttu-id="f224e-126">El valor devuelto de un campo inexistente es un valor vacío.</span><span class="sxs-lookup"><span data-stu-id="f224e-126">The returned value of a nonexistent field is an Empty value.</span></span> <span data-ttu-id="f224e-127">Si el flujo tiene menos bytes solicitados por el recuento, la cadena devuelta se acorta adecuadamente.</span><span class="sxs-lookup"><span data-stu-id="f224e-127">If the stream has fewer bytes that the count requested, the returned string is shortened appropriately.</span></span>

<span data-ttu-id="f224e-128">Para obtener un ejemplo de este método, vea [copiar un archivo ANSI en un campo de base de datos](copy-ansi-file-into-a-database-field.md).</span><span class="sxs-lookup"><span data-stu-id="f224e-128">For an example of this method, see [Copy ANSI File Into a Database Field](copy-ansi-file-into-a-database-field.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f224e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f224e-129">Requirements</span></span>



| <span data-ttu-id="f224e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f224e-130">Requirement</span></span> | <span data-ttu-id="f224e-131">Value</span><span class="sxs-lookup"><span data-stu-id="f224e-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f224e-132">Versión</span><span class="sxs-lookup"><span data-stu-id="f224e-132">Version</span></span><br/> | <span data-ttu-id="f224e-133">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f224e-133">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f224e-134">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f224e-134">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f224e-135">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="f224e-135">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f224e-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f224e-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="f224e-137"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f224e-137"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f224e-138">IID</span><span class="sxs-lookup"><span data-stu-id="f224e-138">IID</span></span><br/>     | <span data-ttu-id="f224e-139">IID \_ IRecord se define como 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f224e-139">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 





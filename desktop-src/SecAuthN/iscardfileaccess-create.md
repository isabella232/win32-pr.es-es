---
description: El método Create crea un archivo en una ubicación determinada dentro del sistema de archivos de la tarjeta inteligente.
ms.assetid: 6bfe0b22-6aad-4818-bb2a-d5b0af4ee3a6
title: 'ISCardFileAccess:: Create (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Create
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2cfc7e1492505191a7912f23e5471f5fa72fdcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154346"
---
# <a name="iscardfileaccesscreate-method"></a><span data-ttu-id="0ac71-103">ISCardFileAccess:: Create (método)</span><span class="sxs-lookup"><span data-stu-id="0ac71-103">ISCardFileAccess::Create method</span></span>

<span data-ttu-id="0ac71-104">\[El método **Create** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="0ac71-104">\[The **Create** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0ac71-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0ac71-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0ac71-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="0ac71-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0ac71-107">El método **Create** crea un archivo en una ubicación determinada dentro del sistema de archivos de la [*tarjeta inteligente*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="0ac71-107">The **Create** method creates a file at a given location within the [*smart card*](../secgloss/s-gly.md) file system.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ac71-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ac71-108">Syntax</span></span>


```C++
HRESULT Create(
  [in] REFTYPE      refType,
  [in] BSTR         bstrPathSpec,
  [in] TLV_TABLE    TLV,
  [in] SCARD_FLAGS  flags,
  [in] LPBYTEBUFFER pDataBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="0ac71-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ac71-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ac71-110">*refType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0ac71-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ac71-111">Tipo de referencia que se usa en *bstrPathSpec*.</span><span class="sxs-lookup"><span data-stu-id="0ac71-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="0ac71-112">**\_tipo SC \_ por \_ nombre**</span><span class="sxs-lookup"><span data-stu-id="0ac71-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="0ac71-113">**\_tipo SC \_ por \_ identificador**</span><span class="sxs-lookup"><span data-stu-id="0ac71-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="0ac71-114">**\_tipo SC \_ por \_ corto**</span><span class="sxs-lookup"><span data-stu-id="0ac71-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="0ac71-115">**\_tipo SC \_ por \_ cualquier**</span><span class="sxs-lookup"><span data-stu-id="0ac71-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="0ac71-116">*bstrPathSpec* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0ac71-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ac71-117">IDENTIFICADOR de archivo que se va a crear en el contexto actual.</span><span class="sxs-lookup"><span data-stu-id="0ac71-117">File ID to be created within the current context.</span></span>

</dd> <dt>

<span data-ttu-id="0ac71-118">*TLV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0ac71-118">*TLV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ac71-119">Lista de estructuras TLV (etiqueta, longitud, valor) que se deben establecer.</span><span class="sxs-lookup"><span data-stu-id="0ac71-119">List of TLV (tag,length,value) structures which values have to be set.</span></span>

</dd> <dt>

<span data-ttu-id="0ac71-120">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0ac71-120">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ac71-121">Especifica si se debe usar la mensajería segura y los datos preasignados.</span><span class="sxs-lookup"><span data-stu-id="0ac71-121">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="0ac71-122">**\_ \_ mensajería segura de SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="0ac71-122">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="0ac71-123">**SC \_ FL \_ preasignado**</span><span class="sxs-lookup"><span data-stu-id="0ac71-123">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="0ac71-124">*pDataBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0ac71-124">*pDataBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ac71-125">Puntero a datos asignados previamente.</span><span class="sxs-lookup"><span data-stu-id="0ac71-125">Pointer to preallocated data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ac71-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ac71-126">Return value</span></span>

<span data-ttu-id="0ac71-127">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="0ac71-127">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="0ac71-128">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0ac71-128">Return code</span></span>                                                                                   | <span data-ttu-id="0ac71-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ac71-129">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0ac71-130"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0ac71-130"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0ac71-131">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="0ac71-131">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="0ac71-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0ac71-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0ac71-133">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="0ac71-133">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="0ac71-134"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="0ac71-134"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0ac71-135">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="0ac71-135">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="0ac71-136"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0ac71-136"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0ac71-137">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="0ac71-137">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="0ac71-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ac71-138">Remarks</span></span>

<span data-ttu-id="0ac71-139">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="0ac71-139">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="0ac71-140">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0ac71-140">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="0ac71-141">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="0ac71-141">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ac71-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ac71-142">Requirements</span></span>



| <span data-ttu-id="0ac71-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ac71-143">Requirement</span></span> | <span data-ttu-id="0ac71-144">Value</span><span class="sxs-lookup"><span data-stu-id="0ac71-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0ac71-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ac71-145">Minimum supported client</span></span><br/> | <span data-ttu-id="0ac71-146">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0ac71-146">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0ac71-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ac71-147">Minimum supported server</span></span><br/> | <span data-ttu-id="0ac71-148">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0ac71-148">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0ac71-149">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="0ac71-149">End of client support</span></span><br/>    | <span data-ttu-id="0ac71-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0ac71-150">Windows XP</span></span><br/>                                |
| <span data-ttu-id="0ac71-151">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="0ac71-151">End of server support</span></span><br/>    | <span data-ttu-id="0ac71-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0ac71-152">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="0ac71-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ac71-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ac71-154">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="0ac71-154">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 

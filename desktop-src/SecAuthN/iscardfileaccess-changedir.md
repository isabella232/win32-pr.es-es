---
description: El método ChangeDir cambia el directorio de la tarjeta inteligente actual al nuevo directorio especificado.
ms.assetid: 1eb53236-c88f-4b43-ac91-de67d4029433
title: 'ISCardFileAccess:: ChangeDir (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.ChangeDir
api_type:
- COM
api_location: ''
ms.openlocfilehash: 147456bd705eea3073f2e65cb375494187ca2473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907980"
---
# <a name="iscardfileaccesschangedir-method"></a><span data-ttu-id="83ba9-103">ISCardFileAccess:: ChangeDir (método)</span><span class="sxs-lookup"><span data-stu-id="83ba9-103">ISCardFileAccess::ChangeDir method</span></span>

<span data-ttu-id="83ba9-104">\[El método **ChangeDir** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="83ba9-104">\[The **ChangeDir** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="83ba9-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="83ba9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="83ba9-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="83ba9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="83ba9-107">El método **ChangeDir** cambia el directorio de la [*tarjeta inteligente*](../secgloss/s-gly.md) actual al nuevo directorio especificado.</span><span class="sxs-lookup"><span data-stu-id="83ba9-107">The **ChangeDir** method changes the current [*smart card*](../secgloss/s-gly.md) directory to the new specified directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="83ba9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83ba9-108">Syntax</span></span>


```C++
HRESULT ChangeDir(
  [in] REFTYPE refType,
  [in] BSTR    bstrNewDir
);
```



## <a name="parameters"></a><span data-ttu-id="83ba9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83ba9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83ba9-110">*refType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="83ba9-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83ba9-111">Tipo de referencia que se usa en *bstrNewDir*.</span><span class="sxs-lookup"><span data-stu-id="83ba9-111">Type of reference used in *bstrNewDir*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="83ba9-112">**\_tipo SC \_ por \_ nombre**</span><span class="sxs-lookup"><span data-stu-id="83ba9-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="83ba9-113">**\_tipo SC \_ por \_ identificador**</span><span class="sxs-lookup"><span data-stu-id="83ba9-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="83ba9-114">**\_tipo SC \_ por \_ corto**</span><span class="sxs-lookup"><span data-stu-id="83ba9-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="83ba9-115">**\_tipo SC \_ por \_ cualquier**</span><span class="sxs-lookup"><span data-stu-id="83ba9-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="83ba9-116">*bstrNewDir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="83ba9-116">*bstrNewDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83ba9-117">Nombre del archivo o directorio (por *refType*) que se va a seleccionar.</span><span class="sxs-lookup"><span data-stu-id="83ba9-117">File/directory name (by *refType*) to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83ba9-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83ba9-118">Return value</span></span>

<span data-ttu-id="83ba9-119">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="83ba9-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="83ba9-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="83ba9-120">Return code</span></span>                                                                                   | <span data-ttu-id="83ba9-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="83ba9-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="83ba9-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="83ba9-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="83ba9-123">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="83ba9-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="83ba9-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="83ba9-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="83ba9-125">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="83ba9-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="83ba9-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="83ba9-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="83ba9-127">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="83ba9-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="83ba9-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83ba9-128">Remarks</span></span>

<span data-ttu-id="83ba9-129">Para obtener una ruta de acceso absoluta al directorio seleccionado actualmente, llame a [**GetCurrentDir**](iscardfileaccess-getcurrentdir.md).</span><span class="sxs-lookup"><span data-stu-id="83ba9-129">To get an absolute path to the currently selected directory, call [**GetCurrentDir**](iscardfileaccess-getcurrentdir.md).</span></span>

<span data-ttu-id="83ba9-130">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="83ba9-130">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="83ba9-131">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="83ba9-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="83ba9-132">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="83ba9-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83ba9-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83ba9-133">Requirements</span></span>



| <span data-ttu-id="83ba9-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="83ba9-134">Requirement</span></span> | <span data-ttu-id="83ba9-135">Value</span><span class="sxs-lookup"><span data-stu-id="83ba9-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="83ba9-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83ba9-136">Minimum supported client</span></span><br/> | <span data-ttu-id="83ba9-137">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="83ba9-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="83ba9-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83ba9-138">Minimum supported server</span></span><br/> | <span data-ttu-id="83ba9-139">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="83ba9-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="83ba9-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="83ba9-140">End of client support</span></span><br/>    | <span data-ttu-id="83ba9-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="83ba9-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="83ba9-142">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="83ba9-142">End of server support</span></span><br/>    | <span data-ttu-id="83ba9-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="83ba9-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="83ba9-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="83ba9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83ba9-145">**GetCurrentDir**</span><span class="sxs-lookup"><span data-stu-id="83ba9-145">**GetCurrentDir**</span></span>](iscardfileaccess-getcurrentdir.md)
</dt> <dt>

[<span data-ttu-id="83ba9-146">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="83ba9-146">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 

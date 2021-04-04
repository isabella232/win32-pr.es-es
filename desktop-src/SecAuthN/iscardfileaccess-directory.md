---
description: El método de directorio recupera una lista de archivos del tipo especificado del directorio actual.
ms.assetid: 0ae89811-7534-497b-af9f-ae37a48bc3e5
title: ISCardFileAccess::D método directorio
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Directory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 74293d4fa97a61133739cac75f17eaffed6e52b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908690"
---
# <a name="iscardfileaccessdirectory-method"></a><span data-ttu-id="7029b-103">ISCardFileAccess::D método directorio</span><span class="sxs-lookup"><span data-stu-id="7029b-103">ISCardFileAccess::Directory method</span></span>

<span data-ttu-id="7029b-104">\[El método de **directorio** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="7029b-104">\[The **Directory** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7029b-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7029b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7029b-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="7029b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7029b-107">El método de **directorio** recupera una lista de archivos del tipo especificado del directorio actual.</span><span class="sxs-lookup"><span data-stu-id="7029b-107">The **Directory** method retrieves a list of files of the specified type from the current directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="7029b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7029b-108">Syntax</span></span>


```C++
HRESULT Directory(
  [in]  FILETYPE    fileType,
  [out] LPSAFEARRAY *ppFileList
);
```



## <a name="parameters"></a><span data-ttu-id="7029b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7029b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7029b-110">*filetype* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7029b-110">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7029b-111">Tipo de archivos de [*tarjeta inteligente*](../secgloss/s-gly.md) que se van a mostrar.</span><span class="sxs-lookup"><span data-stu-id="7029b-111">Type of [*smart card*](../secgloss/s-gly.md) files to list.</span></span>



| <span data-ttu-id="7029b-112">Value</span><span class="sxs-lookup"><span data-stu-id="7029b-112">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="7029b-113">Significado</span><span class="sxs-lookup"><span data-stu-id="7029b-113">Meaning</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="SC_TYPE_DIRECTORIES"></span><span id="sc_type_directories"></span><dl> <span data-ttu-id="7029b-114"><dt>**\_directorios de tipo SC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7029b-114"><dt>**SC\_TYPE\_DIRECTORIES**</dt></span></span> </dl>           | <span data-ttu-id="7029b-115">Enumerar solo archivos de directorio.</span><span class="sxs-lookup"><span data-stu-id="7029b-115">List directory files only.</span></span><br/>                |
| <span id="SC_TYPE_FILES"></span><span id="sc_type_files"></span><dl> <span data-ttu-id="7029b-116"><dt>**\_archivos de tipo SC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7029b-116"><dt>**SC\_TYPE\_FILES**</dt></span></span> </dl>                             | <span data-ttu-id="7029b-117">Enumerar solo archivos elementales.</span><span class="sxs-lookup"><span data-stu-id="7029b-117">List elementary files only.</span></span><br/>               |
| <span id="SC_TYPE_ALL_FILES"></span><span id="sc_type_all_files"></span><dl> <span data-ttu-id="7029b-118"><dt>**SC \_ Type \_ All \_ files**</dt></span><span class="sxs-lookup"><span data-stu-id="7029b-118"><dt>**SC\_TYPE\_ALL\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="7029b-119">Enumere los archivos de directorio y elementales.</span><span class="sxs-lookup"><span data-stu-id="7029b-119">List both directory and elementary files.</span></span><br/> |
| <span id="SC_TYPE_DIRECTORY_FILE"></span><span id="sc_type_directory_file"></span><dl> <span data-ttu-id="7029b-120"><dt>**\_archivo de \_ Directorio de tipo SC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7029b-120"><dt>**SC\_TYPE\_DIRECTORY\_FILE**</dt></span></span> </dl> | <span data-ttu-id="7029b-121">Archivo de directorio.</span><span class="sxs-lookup"><span data-stu-id="7029b-121">Directory file.</span></span><br/>                           |
| <span id="SC_TYPE_TRANSPARENT_EF"></span><span id="sc_type_transparent_ef"></span><dl> <span data-ttu-id="7029b-122"><dt>**\_tipo SC \_ transparente \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="7029b-122"><dt>**SC\_TYPE\_TRANSPARENT\_EF**</dt></span></span> </dl> | <span data-ttu-id="7029b-123">Archivo elemental transparente.</span><span class="sxs-lookup"><span data-stu-id="7029b-123">Transparent elementary file.</span></span><br/>              |
| <span id="SC_TYPE_FIXED_EF"></span><span id="sc_type_fixed_ef"></span><dl> <span data-ttu-id="7029b-124"><dt>**\_tipo SC \_ fixed \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="7029b-124"><dt>**SC\_TYPE\_FIXED\_EF**</dt></span></span> </dl>                   | <span data-ttu-id="7029b-125">Archivo elemental fijo lineal.</span><span class="sxs-lookup"><span data-stu-id="7029b-125">Linear fixed elementary file.</span></span><br/>             |
| <span id="SC_TYPE_CYCLIC_EF"></span><span id="sc_type_cyclic_ef"></span><dl> <span data-ttu-id="7029b-126"><dt>**\_tipo SC \_ cíclico \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="7029b-126"><dt>**SC\_TYPE\_CYCLIC\_EF**</dt></span></span> </dl>                | <span data-ttu-id="7029b-127">Archivo elemental cíclico.</span><span class="sxs-lookup"><span data-stu-id="7029b-127">Cyclic elementary file.</span></span><br/>                   |
| <span id="SC_TYPE_VARIABLE_EF"></span><span id="sc_type_variable_ef"></span><dl> <span data-ttu-id="7029b-128"><dt>**\_variable de tipo SC \_ \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="7029b-128"><dt>**SC\_TYPE\_VARIABLE\_EF**</dt></span></span> </dl>          | <span data-ttu-id="7029b-129">Archivo elemental de variable lineal.</span><span class="sxs-lookup"><span data-stu-id="7029b-129">Linear variable elementary file.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="7029b-130">*ppFileList* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7029b-130">*ppFileList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7029b-131">Matriz de BSTR que representa la lista de archivos que coinciden con el especificador en *filetype*.</span><span class="sxs-lookup"><span data-stu-id="7029b-131">Array of BSTRs representing the list of files matching the specifier in *fileType*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7029b-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7029b-132">Return value</span></span>

<span data-ttu-id="7029b-133">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="7029b-133">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7029b-134">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7029b-134">Return code</span></span>                                                                                   | <span data-ttu-id="7029b-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="7029b-135">Description</span></span>                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="7029b-136"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="7029b-136"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7029b-137">La operación se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="7029b-137">Operation was completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="7029b-138"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7029b-138"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7029b-139">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="7029b-139">Invalid parameter.</span></span><br/>                             |
| <dl> <span data-ttu-id="7029b-140"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="7029b-140"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="7029b-141">La interfaz no ha implementado este método.</span><span class="sxs-lookup"><span data-stu-id="7029b-141">The interface has not implemented this method.</span></span><br/> |
| <dl> <span data-ttu-id="7029b-142"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7029b-142"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7029b-143">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="7029b-143">Out of memory.</span></span><br/>                                 |
| <dl> <span data-ttu-id="7029b-144"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="7029b-144"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7029b-145">Se pasó un puntero incorrecto para *ppFileList*.</span><span class="sxs-lookup"><span data-stu-id="7029b-145">A bad pointer was passed in for *ppFileList*.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="7029b-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7029b-146">Remarks</span></span>

<span data-ttu-id="7029b-147">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="7029b-147">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="7029b-148">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7029b-148">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7029b-149">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7029b-149">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7029b-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7029b-150">Requirements</span></span>



| <span data-ttu-id="7029b-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="7029b-151">Requirement</span></span> | <span data-ttu-id="7029b-152">Value</span><span class="sxs-lookup"><span data-stu-id="7029b-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7029b-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7029b-153">Minimum supported client</span></span><br/> | <span data-ttu-id="7029b-154">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7029b-154">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7029b-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7029b-155">Minimum supported server</span></span><br/> | <span data-ttu-id="7029b-156">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7029b-156">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7029b-157">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7029b-157">End of client support</span></span><br/>    | <span data-ttu-id="7029b-158">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7029b-158">Windows XP</span></span><br/>                                |
| <span data-ttu-id="7029b-159">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="7029b-159">End of server support</span></span><br/>    | <span data-ttu-id="7029b-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7029b-160">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="7029b-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="7029b-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7029b-162">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="7029b-162">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 

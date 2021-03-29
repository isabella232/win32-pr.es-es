---
description: El método GetFileCapabilities recupera una lista de capacidades de archivo del archivo actual.
ms.assetid: 0d24efd2-d411-4fb3-95c2-4742a58aeb5e
title: 'ISCardFileAccess:: GetFileCapabilities (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetFileCapabilities
api_type:
- COM
api_location: ''
ms.openlocfilehash: ca22f02d327cdfbea527fba3a87f3f149774c091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277535"
---
# <a name="iscardfileaccessgetfilecapabilities-method"></a><span data-ttu-id="fc372-103">ISCardFileAccess:: GetFileCapabilities (método)</span><span class="sxs-lookup"><span data-stu-id="fc372-103">ISCardFileAccess::GetFileCapabilities method</span></span>

<span data-ttu-id="fc372-104">\[El método **GetFileCapabilities** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="fc372-104">\[The **GetFileCapabilities** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fc372-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fc372-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fc372-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="fc372-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fc372-107">El método **GetFileCapabilities** recupera una lista de capacidades de archivo del archivo actual.</span><span class="sxs-lookup"><span data-stu-id="fc372-107">The **GetFileCapabilities** method retrieves a list of file capabilities from the current file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc372-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc372-108">Syntax</span></span>


```C++
HRESULT GetFileCapabilities(
  [in, out] LPTLV_TABLE *ppProperties,
  [in, out] LONG        *plProperties,
  [in]      SCARD_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="fc372-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc372-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc372-110">*ppProperties* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fc372-110">*ppProperties* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc372-111">Puntero a las estructuras TLV (etiqueta, longitud, valor).</span><span class="sxs-lookup"><span data-stu-id="fc372-111">Pointer to TLV (tag, length, value) structures.</span></span> <span data-ttu-id="fc372-112">En la entrada, este parámetro indica los archivos para los que se van a obtener propiedades. en la salida, este parámetro contiene las propiedades.</span><span class="sxs-lookup"><span data-stu-id="fc372-112">On input, this parameter indicates the files for which to get properties; on output, this parameter contains the properties.</span></span> <span data-ttu-id="fc372-113">El ejemplo siguiente es una definición de la estructura TLV.</span><span class="sxs-lookup"><span data-stu-id="fc372-113">The following example is a definition of the TLV structure.</span></span>


```C++
#include <windows.h>

typedef struct
{
  DWORD  Tag;
  DWORD  Length;
  BYTE[]  Value;
  BOOL  Valid;
} TLV;
```



<span data-ttu-id="fc372-114">Para obtener más información sobre las estructuras TLV, vea [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) .</span><span class="sxs-lookup"><span data-stu-id="fc372-114">For more information on TLV structures, see [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/).</span></span>

</dd> <dt>

<span data-ttu-id="fc372-115">*plProperties* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fc372-115">*plProperties* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc372-116">Puntero al número de entradas de TLV en *ppProperties*.</span><span class="sxs-lookup"><span data-stu-id="fc372-116">Pointer to the number of TLV entries in *ppProperties*.</span></span>

</dd> <dt>

<span data-ttu-id="fc372-117">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="fc372-117">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc372-118">Especifica si se debe usar la mensajería segura y los datos preasignados.</span><span class="sxs-lookup"><span data-stu-id="fc372-118">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="fc372-119">**\_ \_ mensajería segura de SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="fc372-119">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="fc372-120">**SC \_ FL \_ preasignado**</span><span class="sxs-lookup"><span data-stu-id="fc372-120">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc372-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc372-121">Return value</span></span>

<span data-ttu-id="fc372-122">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="fc372-122">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="fc372-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fc372-123">Return code</span></span>                                                                                   | <span data-ttu-id="fc372-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc372-124">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="fc372-125"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="fc372-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fc372-126">La operación se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="fc372-126">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="fc372-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fc372-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="fc372-128">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="fc372-128">Invalid parameter.</span></span><br/>                    |
| <dl> <span data-ttu-id="fc372-129"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="fc372-129"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fc372-130">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="fc372-130">A bad pointer was passed in.</span></span><br/>          |
| <dl> <span data-ttu-id="fc372-131"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fc372-131"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fc372-132">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="fc372-132">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="fc372-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc372-133">Remarks</span></span>

<span data-ttu-id="fc372-134">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="fc372-134">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="fc372-135">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fc372-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="fc372-136">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="fc372-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc372-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc372-137">Requirements</span></span>



| <span data-ttu-id="fc372-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc372-138">Requirement</span></span> | <span data-ttu-id="fc372-139">Value</span><span class="sxs-lookup"><span data-stu-id="fc372-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fc372-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc372-140">Minimum supported client</span></span><br/> | <span data-ttu-id="fc372-141">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fc372-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="fc372-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc372-142">Minimum supported server</span></span><br/> | <span data-ttu-id="fc372-143">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc372-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fc372-144">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="fc372-144">End of client support</span></span><br/>    | <span data-ttu-id="fc372-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fc372-145">Windows XP</span></span><br/>                                |
| <span data-ttu-id="fc372-146">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="fc372-146">End of server support</span></span><br/>    | <span data-ttu-id="fc372-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fc372-147">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="fc372-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc372-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc372-149">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="fc372-149">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 

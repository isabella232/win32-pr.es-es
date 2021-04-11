---
description: Establece el campo de datos en la unidad de datos de protocolo de aplicación (APDU).
ms.assetid: 4508e00c-2b1d-4be5-b3a7-083b367a2158
title: 'ISCardCmd: método de ut_Data de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 58c1fa7d709eff1ed0618f52a83825f5110c4457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155105"
---
# <a name="iscardcmdput_data-method"></a><span data-ttu-id="a7167-103">ISCardCmd::p \_ método de datos UT</span><span class="sxs-lookup"><span data-stu-id="a7167-103">ISCardCmd::put\_Data method</span></span>

<span data-ttu-id="a7167-104">\[El método **Put \_ Data** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="a7167-104">\[The **put\_Data** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a7167-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a7167-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a7167-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="a7167-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a7167-107">El método **Put \_ Data** establece el campo de datos en la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="a7167-107">The **put\_Data** method sets the data field in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="a7167-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7167-108">Syntax</span></span>


```C++
HRESULT put_Data(
  [in] LPBYTEBUFFER pData
);
```



## <a name="parameters"></a><span data-ttu-id="a7167-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7167-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7167-110">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a7167-110">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7167-111">Puntero al objeto de búfer de bytes (**IStream**) que se va a copiar en el campo de datos APDU.</span><span class="sxs-lookup"><span data-stu-id="a7167-111">Pointer to the byte buffer object (**IStream**) to be copied into the APDU data field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7167-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7167-112">Return value</span></span>

<span data-ttu-id="a7167-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="a7167-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a7167-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a7167-114">Return code</span></span>                                                                                   | <span data-ttu-id="a7167-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7167-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="a7167-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a7167-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a7167-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="a7167-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="a7167-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a7167-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a7167-119">El parámetro *pdata* no es válido.</span><span class="sxs-lookup"><span data-stu-id="a7167-119">The *pData* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="a7167-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="a7167-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a7167-121">Se pasó un puntero incorrecto en *pdata*.</span><span class="sxs-lookup"><span data-stu-id="a7167-121">A bad pointer was passed in *pData*.</span></span><br/> |
| <dl> <span data-ttu-id="a7167-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a7167-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a7167-123">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="a7167-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="a7167-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7167-124">Remarks</span></span>

<span data-ttu-id="a7167-125">Cuando se establece una nueva parte de datos del mensaje, la longitud del campo de datos se calcula y se almacena en el parámetro P3 de la APDU.</span><span class="sxs-lookup"><span data-stu-id="a7167-125">When you set a new data portion of the message, the length of the data field is calculated and stored in the P3 parameter of the APDU.</span></span> <span data-ttu-id="a7167-126">Para recuperar la longitud del campo de datos, llame a [**Get \_ P3**](iscardcmd-get-p3.md).</span><span class="sxs-lookup"><span data-stu-id="a7167-126">To retrieve the length of the data field, call [**get\_P3**](iscardcmd-get-p3.md).</span></span>

<span data-ttu-id="a7167-127">Para recuperar el campo de datos de APDU, llame a [**Get \_ Data**](iscardcmd-get-data.md).</span><span class="sxs-lookup"><span data-stu-id="a7167-127">To retrieve the data field from the APDU, call [**get\_Data**](iscardcmd-get-data.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a7167-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a7167-128">Examples</span></span>

<span data-ttu-id="a7167-129">En el ejemplo siguiente se muestra cómo establecer el campo de datos en la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="a7167-129">The following example shows how to set the data field in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="a7167-130">En el ejemplo se da por supuesto que pIByteData es un puntero válido a una instancia de la interfaz [**IByteBuffer**](ibytebuffer.md) y que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="a7167-130">The example assumes that pIByteData is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Set the data.
hr = pISCardCmd->put_Data(pIByteData);
if (FAILED(hr)) 
{
    printf("Failed put_Data.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="a7167-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7167-131">Requirements</span></span>



| <span data-ttu-id="a7167-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7167-132">Requirement</span></span> | <span data-ttu-id="a7167-133">Value</span><span class="sxs-lookup"><span data-stu-id="a7167-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7167-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7167-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a7167-135">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a7167-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a7167-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7167-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a7167-137">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a7167-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a7167-138">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a7167-138">End of client support</span></span><br/>    | <span data-ttu-id="a7167-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a7167-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a7167-140">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="a7167-140">End of server support</span></span><br/>    | <span data-ttu-id="a7167-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a7167-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a7167-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7167-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7167-143"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7167-143"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7167-144">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a7167-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="a7167-145"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a7167-145"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a7167-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a7167-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7167-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7167-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a7167-148">IID</span><span class="sxs-lookup"><span data-stu-id="a7167-148">IID</span></span><br/>                      | <span data-ttu-id="a7167-149">IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a7167-149">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="a7167-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7167-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7167-151">**obtener \_ datos**</span><span class="sxs-lookup"><span data-stu-id="a7167-151">**get\_Data**</span></span>](iscardcmd-get-data.md)
</dt> <dt>

[<span data-ttu-id="a7167-152">**obtener \_ P3**</span><span class="sxs-lookup"><span data-stu-id="a7167-152">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="a7167-153">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="a7167-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 

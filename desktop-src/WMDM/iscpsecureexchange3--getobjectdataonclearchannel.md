---
title: Método GetObjectDataOnClearChannel
description: El método GetObjectDataOnClearChannel transfiere de nuevo un bloque de datos de objeto de un canal claro a Windows Media Administrador de dispositivos.
ms.assetid: 62122415-b45b-436e-8c5f-28be759ba8c0
keywords:
- Método GetObjectDataOnClearChannel de Windows Media Administrador de dispositivos
topic_type:
- apiref
api_name:
- GetObjectDataOnClearChannel
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25b72df0dd27289153a97221fefbcb58f3a5ad13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698518"
---
# <a name="getobjectdataonclearchannel-method"></a><span data-ttu-id="38666-104">Método GetObjectDataOnClearChannel</span><span class="sxs-lookup"><span data-stu-id="38666-104">GetObjectDataOnClearChannel method</span></span>

<span data-ttu-id="38666-105">El método **GetObjectDataOnClearChannel** transfiere de nuevo un bloque de datos de objeto de un canal claro a Windows Media administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="38666-105">The **GetObjectDataOnClearChannel** method transfers a block of object data on a clear channel back to Windows Media Device Manager.</span></span>

<span data-ttu-id="38666-106">Este método es idéntico a [**ISCPSecureExchange:: ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , salvo que los datos devueltos por este método no están cifrados.</span><span class="sxs-lookup"><span data-stu-id="38666-106">This method is identical to [**ISCPSecureExchange::ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) except that the data returned by this method is not encrypted.</span></span> <span data-ttu-id="38666-107">Por consiguiente, este método es más eficaz.</span><span class="sxs-lookup"><span data-stu-id="38666-107">Consequently this method is more efficient.</span></span>

## <a name="syntax"></a><span data-ttu-id="38666-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38666-108">Syntax</span></span>


```C++
HRESULT GetObjectDataOnClearChannel(
   IMDSPDevice *pDevice,
   BYTE        *pData,
   DWORD       *pdwSize
);
```



## <a name="parameters"></a><span data-ttu-id="38666-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38666-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38666-110">*pDevice*</span><span class="sxs-lookup"><span data-stu-id="38666-110">*pDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="38666-111">Puntero al objeto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="38666-111">Pointer to the device object.</span></span>

</dd> <dt>

<span data-ttu-id="38666-112">*pData*</span><span class="sxs-lookup"><span data-stu-id="38666-112">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="38666-113">Puntero a un búfer para recibir datos.</span><span class="sxs-lookup"><span data-stu-id="38666-113">Pointer to a buffer to receive data.</span></span>

</dd> <dt>

<span data-ttu-id="38666-114">*pdwSize*</span><span class="sxs-lookup"><span data-stu-id="38666-114">*pdwSize*</span></span> 
</dt> <dd>

<span data-ttu-id="38666-115">Puntero a un **valor DWORD** que contiene el tamaño de la transferencia.</span><span class="sxs-lookup"><span data-stu-id="38666-115">Pointer to a **DWORD** containing the transfer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38666-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38666-116">Return value</span></span>

<span data-ttu-id="38666-117">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="38666-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="38666-118">Si se produce un error en el método, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="38666-118">If the method fails, it returns an **HRESULT** error code.</span></span>



| <span data-ttu-id="38666-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="38666-119">Return code</span></span>                                                                                                | <span data-ttu-id="38666-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="38666-120">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="38666-121"><dt>**\_error de \_ comprobación de Mac \_ \_ de WMDM**</dt></span><span class="sxs-lookup"><span data-stu-id="38666-121"><dt>**WMDM\_E\_MAC\_CHECK\_FAILED**</dt></span></span> </dl> | <span data-ttu-id="38666-122">El código de autenticación del mensaje no es válido.</span><span class="sxs-lookup"><span data-stu-id="38666-122">The message authentication code is not valid.</span></span><br/>                                    |
| <dl> <span data-ttu-id="38666-123"><dt>**\_E/s de WMDM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38666-123"><dt>**WMDM\_E\_NORIGHTS**</dt></span></span> </dl>           | <span data-ttu-id="38666-124">El autor de la llamada no tiene los derechos necesarios para realizar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="38666-124">The caller does not have the rights required to perform the requested operation.</span></span><br/> |
| <dl> <span data-ttu-id="38666-125"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="38666-125"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="38666-126">Error en el método.</span><span class="sxs-lookup"><span data-stu-id="38666-126">The method failed.</span></span> <span data-ttu-id="38666-127">Finalice la interacción con el proveedor de contenido.</span><span class="sxs-lookup"><span data-stu-id="38666-127">Terminate interaction with the content provider.</span></span><br/>              |
| <dl> <span data-ttu-id="38666-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="38666-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="38666-129">Un parámetro es un puntero **nulo** o no válido.</span><span class="sxs-lookup"><span data-stu-id="38666-129">A parameter is an invalid or **NULL** pointer.</span></span><br/>                                   |
| <dl> <span data-ttu-id="38666-130"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="38666-130"><dt>**E\_FAIL**</dt></span></span> </dl>                     | <span data-ttu-id="38666-131">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="38666-131">An unspecified error occurred.</span></span><br/>                                                   |



 

## <a name="remarks"></a><span data-ttu-id="38666-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38666-132">Remarks</span></span>

<span data-ttu-id="38666-133">Para transferir datos, Windows Media Administrador de dispositivos llama al método [TransferContainerDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) para obtener los datos del contenedor.</span><span class="sxs-lookup"><span data-stu-id="38666-133">To transfer data, Windows Media Device Manager calls the [TransferContainerDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) method to obtain the container data.</span></span> <span data-ttu-id="38666-134">A continuación, se llama a **GetObjectDataOnClearChannel** para transferir bloques de datos de objeto del proveedor de contenido a Windows Media administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="38666-134">**GetObjectDataOnClearChannel** is then called to transfer blocks of object data from the content provider to Windows Media Device Manager.</span></span> <span data-ttu-id="38666-135">Si \_ se devuelve S OK con *pdwSize* establecido en cero, Windows Media administrador de dispositivos no solicitará más datos.</span><span class="sxs-lookup"><span data-stu-id="38666-135">If S\_OK is returned with *pdwSize* set to zero, Windows Media Device Manager will request no further data.</span></span>

<span data-ttu-id="38666-136">Este método es idéntico a [**ISCPSecureExchange:: ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , salvo que los datos devueltos por este método no están cifrados.</span><span class="sxs-lookup"><span data-stu-id="38666-136">This method is identical to [**ISCPSecureExchange::ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) except that the data returned by this method is not encrypted.</span></span> <span data-ttu-id="38666-137">Por consiguiente, este método es más eficaz.</span><span class="sxs-lookup"><span data-stu-id="38666-137">Consequently this method is more efficient.</span></span>

## <a name="requirements"></a><span data-ttu-id="38666-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38666-138">Requirements</span></span>



| <span data-ttu-id="38666-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="38666-139">Requirement</span></span> | <span data-ttu-id="38666-140">Value</span><span class="sxs-lookup"><span data-stu-id="38666-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38666-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38666-141">Header</span></span><br/>  | <dl> <span data-ttu-id="38666-142"><dt>WMSCP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="38666-142"><dt>WMSCP.idl</dt></span></span> </dl>    |
| <span data-ttu-id="38666-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="38666-143">Library</span></span><br/> | <dl> <span data-ttu-id="38666-144"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38666-144"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38666-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="38666-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38666-146">**ISCPSecureExchange:: ObjectData**</span><span class="sxs-lookup"><span data-stu-id="38666-146">**ISCPSecureExchange::ObjectData**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata)
</dt> <dt>

[<span data-ttu-id="38666-147">**Interfaz ISCPSecureExchange3**</span><span class="sxs-lookup"><span data-stu-id="38666-147">**ISCPSecureExchange3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)
</dt> </dl>

 

 






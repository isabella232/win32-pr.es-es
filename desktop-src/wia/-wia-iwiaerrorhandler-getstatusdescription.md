---
description: Devuelve una cadena que describe el código de estado.
ms.assetid: d3007f3e-46e1-4ab6-8ce3-c4e38f87ce61
title: 'IWiaErrorHandler:: GetStatusDescription (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.GetStatusDescription
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: da23e413ee238f43ae577a51b18a542dc1b0768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696616"
---
# <a name="iwiaerrorhandlergetstatusdescription-method"></a><span data-ttu-id="63e4f-103">IWiaErrorHandler:: GetStatusDescription (método)</span><span class="sxs-lookup"><span data-stu-id="63e4f-103">IWiaErrorHandler::GetStatusDescription method</span></span>

<span data-ttu-id="63e4f-104">Devuelve una cadena que describe el código de estado.</span><span class="sxs-lookup"><span data-stu-id="63e4f-104">Returns a string that describes the status code.</span></span>

## <a name="syntax"></a><span data-ttu-id="63e4f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63e4f-105">Syntax</span></span>


```C++
HRESULT GetStatusDescription(
  [in]  IUnknown *punkItem,
  [in]  HRESULT  hrStatus,
  [in]  LONG     cbResLength,
  [in]  BYTE     *pbData,
  [out] BSTR     *pbstrDescription
);
```



## <a name="parameters"></a><span data-ttu-id="63e4f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63e4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63e4f-107">*punkItem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63e4f-107">*punkItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63e4f-108">Tipo: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="63e4f-108">Type: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="63e4f-109">Puntero a la [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) del elemento que se va a transferir.</span><span class="sxs-lookup"><span data-stu-id="63e4f-109">Pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) of the item being transferred.</span></span> <span data-ttu-id="63e4f-110">Este objeto implementa mínimamente [_ *IWiaItem2* \*](-wia-iwiaitem2.md) y [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span><span class="sxs-lookup"><span data-stu-id="63e4f-110">This object minimally implements [_ *IWiaItem2*\*](-wia-iwiaitem2.md) and [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span></span>

</dd> <dt>

<span data-ttu-id="63e4f-111">*hrStatus* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63e4f-111">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63e4f-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="63e4f-112">Type: **HRESULT**</span></span>

<span data-ttu-id="63e4f-113">**HRESULT** que es el código de estado recibido por [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="63e4f-113">**HRESULT** that is the status code received by [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="63e4f-114">*cbResLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63e4f-114">*cbResLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63e4f-115">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="63e4f-115">Type: **LONG**</span></span>

<span data-ttu-id="63e4f-116">**Long** que es el tamaño de los datos a los que hace referencia *pbData*.</span><span class="sxs-lookup"><span data-stu-id="63e4f-116">**LONG** that is the size of the data referred to by *pbData*.</span></span>

</dd> <dt>

<span data-ttu-id="63e4f-117">*pbData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63e4f-117">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63e4f-118">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="63e4f-118">Type: \**BYTE\** _</span></span>

<span data-ttu-id="63e4f-119">Puntero al búfer de datos tal y como lo recibe [_ *BandedDataCallback* \*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="63e4f-119">Pointer to the data buffer as received by [_ *BandedDataCallback*\*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="63e4f-120">*pbstrDescription* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="63e4f-120">*pbstrDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63e4f-121">Tipo: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="63e4f-121">Type: \**BSTR\** _</span></span>

<span data-ttu-id="63e4f-122">_ *BSTR*\* que recibe una descripción del estado o error detectado durante la transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="63e4f-122">_ *BSTR*\* that receives a description of the status or error encountered during the data transfer.</span></span> <span data-ttu-id="63e4f-123">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="63e4f-123">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="63e4f-124">El autor de la llamada debe liberar la cadena mediante [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)y el implementador debe asignar la cadena mediante [SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).</span><span class="sxs-lookup"><span data-stu-id="63e4f-124">The caller must free the string using [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring), and the implementor must allocate the string using [SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63e4f-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63e4f-125">Return value</span></span>

<span data-ttu-id="63e4f-126">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="63e4f-126">Type: **HRESULT**</span></span>

<span data-ttu-id="63e4f-127">Devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="63e4f-127">Returns one of the following values.</span></span>



| <span data-ttu-id="63e4f-128">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="63e4f-128">Return code</span></span>                                                                             | <span data-ttu-id="63e4f-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="63e4f-129">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="63e4f-130"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="63e4f-130"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="63e4f-131">*pbstrDescription* contiene un puntero **BSTR** válido.</span><span class="sxs-lookup"><span data-stu-id="63e4f-131">*pbstrDescription* contains a valid **BSTR** pointer.</span></span> <br/>  |
| <dl> <span data-ttu-id="63e4f-132"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="63e4f-132"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="63e4f-133">*hrStatus* es desconocido y no hay ninguna descripción disponible.</span><span class="sxs-lookup"><span data-stu-id="63e4f-133">*hrStatus* is unknown and no description is available.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="63e4f-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63e4f-134">Requirements</span></span>



| <span data-ttu-id="63e4f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="63e4f-135">Requirement</span></span> | <span data-ttu-id="63e4f-136">Value</span><span class="sxs-lookup"><span data-stu-id="63e4f-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63e4f-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63e4f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="63e4f-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="63e4f-138">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="63e4f-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63e4f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="63e4f-140">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="63e4f-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="63e4f-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63e4f-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="63e4f-142"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="63e4f-142"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="63e4f-143">IDL</span><span class="sxs-lookup"><span data-stu-id="63e4f-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="63e4f-144"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="63e4f-144"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="63e4f-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="63e4f-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="63e4f-146"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63e4f-146"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 

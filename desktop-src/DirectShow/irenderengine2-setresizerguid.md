---
description: El método SetResizerGUID especifica el CLSID de un filtro de cambio de tamaño de vídeo personalizado.
ms.assetid: 709a6e7f-64ae-406d-bb6d-29f6c65b63a8
title: 'IRenderEngine2:: SetResizerGUID (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2.SetResizerGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 864053c2c5def6ef1b23ca2c2ee712664e132079
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681026"
---
# <a name="irenderengine2setresizerguid-method"></a><span data-ttu-id="9b294-103">IRenderEngine2:: SetResizerGUID (método)</span><span class="sxs-lookup"><span data-stu-id="9b294-103">IRenderEngine2::SetResizerGUID method</span></span>

> [!Note]  
> <span data-ttu-id="9b294-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="9b294-104">\[Deprecated.</span></span> <span data-ttu-id="9b294-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9b294-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9b294-106">El `SetResizerGUID` método especifica el CLSID de un filtro de cambio de tamaño de vídeo personalizado.</span><span class="sxs-lookup"><span data-stu-id="9b294-106">The `SetResizerGUID` method specifies the CLSID of a custom video resizing filter.</span></span> <span data-ttu-id="9b294-107">Llame a este método para reemplazar el filtro de cambio de tamaño predeterminado utilizado por los servicios de edición de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9b294-107">Call this method to replace the default resizing filter used by DirectShow Editing Services.</span></span> <span data-ttu-id="9b294-108">El filtro debe registrarse como un objeto COM en el sistema del usuario y debe ser compatible con la interfaz [**IResize**](iresize.md) .</span><span class="sxs-lookup"><span data-stu-id="9b294-108">Your filter must be registered as a COM object on the user's system, and it must support the [**IResize**](iresize.md) interface.</span></span>

<span data-ttu-id="9b294-109">Llame a este método antes de llamar a [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md).</span><span class="sxs-lookup"><span data-stu-id="9b294-109">Call this method before calling [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9b294-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b294-110">Syntax</span></span>


```C++
HRESULT SetResizerGUID(
  [in] GUID ResizerGuid
);
```



## <a name="parameters"></a><span data-ttu-id="9b294-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b294-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b294-112">*ResizerGuid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9b294-112">*ResizerGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b294-113">CLSID del filtro.</span><span class="sxs-lookup"><span data-stu-id="9b294-113">The CLSID of the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b294-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b294-114">Return value</span></span>

<span data-ttu-id="9b294-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9b294-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9b294-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9b294-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b294-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b294-117">Remarks</span></span>

<span data-ttu-id="9b294-118">Para revertir al tamaño DES predeterminado, use el siguiente CLSID:</span><span class="sxs-lookup"><span data-stu-id="9b294-118">To revert to the default DES resizer, use the following CLSID:</span></span>


```C++
// {F97B8A60-31AD-11CF-B2DE-00DD01101B85}
DEFINE_GUID(CLSID_Resize, 
0xF97B8A60, 0x31AD, 0x11CF, 0xB2, 0xDE, 0x00, 0xDD, 0x01, 0x10, 0x1B, 0x85);
```



> [!Note]  
> <span data-ttu-id="9b294-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="9b294-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9b294-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9b294-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9b294-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9b294-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9b294-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b294-122">Requirements</span></span>



| <span data-ttu-id="9b294-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b294-123">Requirement</span></span> | <span data-ttu-id="9b294-124">Value</span><span class="sxs-lookup"><span data-stu-id="9b294-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b294-125">Versión</span><span class="sxs-lookup"><span data-stu-id="9b294-125">Version</span></span><br/> | <span data-ttu-id="9b294-126">DirectX 9,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="9b294-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="9b294-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b294-127">Header</span></span><br/>  | <dl> <span data-ttu-id="9b294-128"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b294-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9b294-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b294-129">Library</span></span><br/> | <dl> <span data-ttu-id="9b294-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b294-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b294-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b294-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b294-132">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="9b294-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="9b294-133">**Interfaz IRenderEngine2**</span><span class="sxs-lookup"><span data-stu-id="9b294-133">**IRenderEngine2 Interface**</span></span>](irenderengine2.md)
</dt> </dl>

 

 





---
description: Especifica un filtro de compresión que se va a utilizar al representar el grupo especificado.
ms.assetid: ba717cac-c5a8-4821-a5f0-dd9d5fe4834e
title: 'ISmartRenderEngine:: SetGroupCompressor (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.SetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9cb02a9d8daf7e6ba74a45299daa9d45ab63d5db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681186"
---
# <a name="ismartrenderenginesetgroupcompressor-method"></a><span data-ttu-id="61a8d-103">ISmartRenderEngine:: SetGroupCompressor (método)</span><span class="sxs-lookup"><span data-stu-id="61a8d-103">ISmartRenderEngine::SetGroupCompressor method</span></span>

> [!Note]  
> <span data-ttu-id="61a8d-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="61a8d-104">\[Deprecated.</span></span> <span data-ttu-id="61a8d-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="61a8d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="61a8d-106">Especifica un filtro de compresión que se va a utilizar al representar el grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="61a8d-106">Specifies a compression filter to use when rendering the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="61a8d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61a8d-107">Syntax</span></span>


```C++
HRESULT SetGroupCompressor(
   long        Group,
   IBaseFilter *pCompressor
);
```



## <a name="parameters"></a><span data-ttu-id="61a8d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61a8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61a8d-109">*Grupo*</span><span class="sxs-lookup"><span data-stu-id="61a8d-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="61a8d-110">Índice de base cero del grupo.</span><span class="sxs-lookup"><span data-stu-id="61a8d-110">Zero-based index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="61a8d-111">*pCompressor*</span><span class="sxs-lookup"><span data-stu-id="61a8d-111">*pCompressor*</span></span> 
</dt> <dd>

<span data-ttu-id="61a8d-112">Puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro de compresión.</span><span class="sxs-lookup"><span data-stu-id="61a8d-112">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the compression filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61a8d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61a8d-113">Return value</span></span>

<span data-ttu-id="61a8d-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="61a8d-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="61a8d-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="61a8d-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="61a8d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61a8d-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="61a8d-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="61a8d-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="61a8d-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="61a8d-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="61a8d-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="61a8d-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="61a8d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61a8d-120">Requirements</span></span>



| <span data-ttu-id="61a8d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="61a8d-121">Requirement</span></span> | <span data-ttu-id="61a8d-122">Value</span><span class="sxs-lookup"><span data-stu-id="61a8d-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61a8d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61a8d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="61a8d-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="61a8d-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="61a8d-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="61a8d-125">Library</span></span><br/> | <dl> <span data-ttu-id="61a8d-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61a8d-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61a8d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="61a8d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61a8d-128">**Interfaz ISmartRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="61a8d-128">**ISmartRenderEngine Interface**</span></span>](ismartrenderengine.md)
</dt> <dt>

[<span data-ttu-id="61a8d-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="61a8d-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





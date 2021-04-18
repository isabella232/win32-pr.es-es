---
description: El método SetSubObjectGUID especifica el GUID del subobjeto asociado a este objeto.
ms.assetid: 1f21e242-306e-4b28-8655-511b7db495ab
title: 'IAMTimelineObj:: SetSubObjectGUID (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObjectGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac5e7631b447d28c92bc94cb64cfeabde0e6cd6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690717"
---
# <a name="iamtimelineobjsetsubobjectguid-method"></a><span data-ttu-id="9194c-103">IAMTimelineObj:: SetSubObjectGUID (método)</span><span class="sxs-lookup"><span data-stu-id="9194c-103">IAMTimelineObj::SetSubObjectGUID method</span></span>

> [!Note]  
> <span data-ttu-id="9194c-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="9194c-104">\[Deprecated.</span></span> <span data-ttu-id="9194c-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9194c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9194c-106">El `SetSubObjectGUID` método especifica el GUID del subobjeto asociado a este objeto.</span><span class="sxs-lookup"><span data-stu-id="9194c-106">The `SetSubObjectGUID` method specifies the GUID of the subobject associated with this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9194c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9194c-107">Syntax</span></span>


```C++
HRESULT SetSubObjectGUID(
   GUID newVal
);
```



## <a name="parameters"></a><span data-ttu-id="9194c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9194c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9194c-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="9194c-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="9194c-110">GUID del subobjeto.</span><span class="sxs-lookup"><span data-stu-id="9194c-110">GUID of the subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9194c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9194c-111">Return value</span></span>

<span data-ttu-id="9194c-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9194c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9194c-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9194c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9194c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9194c-114">Remarks</span></span>

<span data-ttu-id="9194c-115">El motor de representación crea una instancia del subobjeto según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9194c-115">The render engine creates an instance of the subobject as needed.</span></span>

> [!Note]  
> <span data-ttu-id="9194c-116">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="9194c-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9194c-117">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9194c-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9194c-118">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9194c-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9194c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9194c-119">Requirements</span></span>



| <span data-ttu-id="9194c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9194c-120">Requirement</span></span> | <span data-ttu-id="9194c-121">Value</span><span class="sxs-lookup"><span data-stu-id="9194c-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9194c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9194c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9194c-123"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="9194c-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9194c-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9194c-124">Library</span></span><br/> | <dl> <span data-ttu-id="9194c-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9194c-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9194c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="9194c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9194c-127">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="9194c-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="9194c-128">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="9194c-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





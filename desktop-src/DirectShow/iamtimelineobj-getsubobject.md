---
description: El método GetSubObject recupera el subobjeto asociado a este objeto.
ms.assetid: 478597d6-ae13-4fa9-a928-19893f378f1a
title: 'IAMTimelineObj:: GetSubObject (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 74f14658db5ffbaf100925f26573a08b592f6510
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680193"
---
# <a name="iamtimelineobjgetsubobject-method"></a><span data-ttu-id="53c96-103">IAMTimelineObj:: GetSubObject (método)</span><span class="sxs-lookup"><span data-stu-id="53c96-103">IAMTimelineObj::GetSubObject method</span></span>

> [!Note]  
> <span data-ttu-id="53c96-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="53c96-104">\[Deprecated.</span></span> <span data-ttu-id="53c96-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="53c96-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="53c96-106">El `GetSubObject` método recupera el subobjeto asociado a este objeto.</span><span class="sxs-lookup"><span data-stu-id="53c96-106">The `GetSubObject` method retrieves the subobject associated with this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="53c96-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53c96-107">Syntax</span></span>


```C++
HRESULT GetSubObject(
  [out, retval] IUnknown **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="53c96-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53c96-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53c96-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="53c96-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="53c96-110">Recibe un puntero a la interfaz **IUnknown** del subobjeto.</span><span class="sxs-lookup"><span data-stu-id="53c96-110">Receives a pointer to the subobject's **IUnknown** interface.</span></span> <span data-ttu-id="53c96-111">Si el objeto no tiene un subobjeto, el valor se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="53c96-111">If the object does not have a subobject, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53c96-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53c96-112">Return value</span></span>

<span data-ttu-id="53c96-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="53c96-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="53c96-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="53c96-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="53c96-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53c96-115">Remarks</span></span>

<span data-ttu-id="53c96-116">Cada objeto Timeline puede contener un puntero a un subobjeto asociado.</span><span class="sxs-lookup"><span data-stu-id="53c96-116">Every timeline object can hold a pointer to an associated subobject.</span></span>

<span data-ttu-id="53c96-117">Si el valor devuelto en *pval* no es **null**, la interfaz **IUnknown** tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="53c96-117">If the value returned in *pVal* is not **NULL**, the **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="53c96-118">Asegúrese de liberar la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="53c96-118">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="53c96-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="53c96-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="53c96-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="53c96-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="53c96-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="53c96-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="53c96-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53c96-122">Requirements</span></span>



| <span data-ttu-id="53c96-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="53c96-123">Requirement</span></span> | <span data-ttu-id="53c96-124">Value</span><span class="sxs-lookup"><span data-stu-id="53c96-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53c96-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53c96-125">Header</span></span><br/>  | <dl> <span data-ttu-id="53c96-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="53c96-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="53c96-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="53c96-127">Library</span></span><br/> | <dl> <span data-ttu-id="53c96-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53c96-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53c96-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="53c96-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53c96-130">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="53c96-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="53c96-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="53c96-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





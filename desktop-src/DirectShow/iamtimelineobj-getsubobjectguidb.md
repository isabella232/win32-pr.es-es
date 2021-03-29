---
description: 'El método GetSubObjectGUIDB recupera el GUID del subobjeto asociado a este objeto Timeline. Este método es equivalente a IAMTimelineObj:: GetSubObjectGUID, pero recibe un valor BSTR.'
ms.assetid: 693cafda-78c8-4ba4-90d7-23fedcd1fc52
title: 'IAMTimelineObj:: GetSubObjectGUIDB (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 903c6638eececd635af2facd964adabe26f0c106
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679330"
---
# <a name="iamtimelineobjgetsubobjectguidb-method"></a><span data-ttu-id="9dfca-104">IAMTimelineObj:: GetSubObjectGUIDB (método)</span><span class="sxs-lookup"><span data-stu-id="9dfca-104">IAMTimelineObj::GetSubObjectGUIDB method</span></span>

> [!Note]  
> <span data-ttu-id="9dfca-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="9dfca-105">\[Deprecated.</span></span> <span data-ttu-id="9dfca-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9dfca-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9dfca-107">El `GetSubObjectGUIDB` método recupera el GUID del subobjeto asociado a este objeto Timeline.</span><span class="sxs-lookup"><span data-stu-id="9dfca-107">The `GetSubObjectGUIDB` method retrieves the GUID of the subobject associated with this timeline object.</span></span> <span data-ttu-id="9dfca-108">Este método es equivalente a [**IAMTimelineObj:: GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md), pero recibe un valor **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="9dfca-108">This method is equivalent to [**IAMTimelineObj::GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md), but receives a **BSTR** value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dfca-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9dfca-109">Syntax</span></span>


```C++
HRESULT GetSubObjectGUIDB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="9dfca-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9dfca-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dfca-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9dfca-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9dfca-112">Recibe una cadena que representa el GUID del subobjeto.</span><span class="sxs-lookup"><span data-stu-id="9dfca-112">Receives a string representing the subobject GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dfca-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9dfca-113">Return value</span></span>

<span data-ttu-id="9dfca-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9dfca-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9dfca-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9dfca-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dfca-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9dfca-116">Remarks</span></span>

<span data-ttu-id="9dfca-117">El método asigna memoria para la cadena.</span><span class="sxs-lookup"><span data-stu-id="9dfca-117">The method allocates memory for the string.</span></span> <span data-ttu-id="9dfca-118">La aplicación debe llamar a **SysFreeString** para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="9dfca-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="9dfca-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="9dfca-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9dfca-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9dfca-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9dfca-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9dfca-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9dfca-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dfca-122">Requirements</span></span>



| <span data-ttu-id="9dfca-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dfca-123">Requirement</span></span> | <span data-ttu-id="9dfca-124">Value</span><span class="sxs-lookup"><span data-stu-id="9dfca-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9dfca-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9dfca-125">Header</span></span><br/>  | <dl> <span data-ttu-id="9dfca-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dfca-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9dfca-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9dfca-127">Library</span></span><br/> | <dl> <span data-ttu-id="9dfca-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9dfca-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dfca-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9dfca-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dfca-130">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="9dfca-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="9dfca-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="9dfca-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





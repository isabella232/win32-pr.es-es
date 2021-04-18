---
description: El método SetGroupName establece el nombre definido por la aplicación del grupo.
ms.assetid: e1d8a91b-d5b9-42a4-9b98-582e1a57ac51
title: 'IAMTimelineGroup:: SetGroupName (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetGroupName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 327bf0384ce484353ac41c069ddf580c674b0b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690104"
---
# <a name="iamtimelinegroupsetgroupname-method"></a><span data-ttu-id="68734-103">IAMTimelineGroup:: SetGroupName (método)</span><span class="sxs-lookup"><span data-stu-id="68734-103">IAMTimelineGroup::SetGroupName method</span></span>

> [!Note]  
> <span data-ttu-id="68734-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="68734-104">\[Deprecated.</span></span> <span data-ttu-id="68734-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="68734-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="68734-106">El `SetGroupName` método establece el nombre definido por la aplicación del grupo.</span><span class="sxs-lookup"><span data-stu-id="68734-106">The `SetGroupName` method sets the application-defined name of the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="68734-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68734-107">Syntax</span></span>


```C++
HRESULT SetGroupName(
   BSTR pGroupName
);
```



## <a name="parameters"></a><span data-ttu-id="68734-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68734-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68734-109">*pGroupName*</span><span class="sxs-lookup"><span data-stu-id="68734-109">*pGroupName*</span></span> 
</dt> <dd>

<span data-ttu-id="68734-110">**BSTR** que especifica el nombre del grupo.</span><span class="sxs-lookup"><span data-stu-id="68734-110">**BSTR** that specifies the name of the group.</span></span> <span data-ttu-id="68734-111">La longitud máxima del nombre es de 256 caracteres, incuding el terminador null.</span><span class="sxs-lookup"><span data-stu-id="68734-111">The maximum length of the name is 256 characters, incuding the null terminator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68734-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68734-112">Return value</span></span>

<span data-ttu-id="68734-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="68734-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="68734-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="68734-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="68734-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68734-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="68734-116">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="68734-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="68734-117">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="68734-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="68734-118">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="68734-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="68734-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68734-119">Requirements</span></span>



| <span data-ttu-id="68734-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="68734-120">Requirement</span></span> | <span data-ttu-id="68734-121">Value</span><span class="sxs-lookup"><span data-stu-id="68734-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68734-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68734-122">Header</span></span><br/>  | <dl> <span data-ttu-id="68734-123"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="68734-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="68734-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68734-124">Library</span></span><br/> | <dl> <span data-ttu-id="68734-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68734-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68734-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="68734-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68734-127">**Interfaz IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="68734-127">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="68734-128">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="68734-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





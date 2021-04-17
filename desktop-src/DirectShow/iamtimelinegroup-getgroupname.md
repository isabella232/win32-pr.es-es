---
description: El método GetGroupName recupera el nombre definido por la aplicación del grupo.
ms.assetid: 402e97d9-abb5-4d8e-8735-1b06d60ab225
title: 'IAMTimelineGroup:: GetGroupName (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetGroupName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 78e3fc736ece3f4a8ebea1c688ce2bc5099f497c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681251"
---
# <a name="iamtimelinegroupgetgroupname-method"></a><span data-ttu-id="1e936-103">IAMTimelineGroup:: GetGroupName (método)</span><span class="sxs-lookup"><span data-stu-id="1e936-103">IAMTimelineGroup::GetGroupName method</span></span>

> [!Note]  
> <span data-ttu-id="1e936-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="1e936-104">\[Deprecated.</span></span> <span data-ttu-id="1e936-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1e936-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1e936-106">El `GetGroupName` método recupera el nombre definido por la aplicación del grupo.</span><span class="sxs-lookup"><span data-stu-id="1e936-106">The `GetGroupName` method retrieves the application-defined name of the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e936-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e936-107">Syntax</span></span>


```C++
HRESULT GetGroupName(
  [out, retval] BSTR *pGroupName
);
```



## <a name="parameters"></a><span data-ttu-id="1e936-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e936-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e936-109">*pGroupName* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1e936-109">*pGroupName* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1e936-110">Recibe el nombre del grupo.</span><span class="sxs-lookup"><span data-stu-id="1e936-110">Receives the name of the group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e936-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e936-111">Return value</span></span>

<span data-ttu-id="1e936-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1e936-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1e936-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1e936-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e936-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e936-114">Remarks</span></span>

<span data-ttu-id="1e936-115">El método asigna memoria para la cadena.</span><span class="sxs-lookup"><span data-stu-id="1e936-115">The method allocates memory for the string.</span></span> <span data-ttu-id="1e936-116">La aplicación debe llamar a **SysFreeString** para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="1e936-116">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="1e936-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="1e936-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1e936-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1e936-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1e936-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1e936-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1e936-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e936-120">Requirements</span></span>



| <span data-ttu-id="1e936-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e936-121">Requirement</span></span> | <span data-ttu-id="1e936-122">Value</span><span class="sxs-lookup"><span data-stu-id="1e936-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e936-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e936-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1e936-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e936-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1e936-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e936-125">Library</span></span><br/> | <dl> <span data-ttu-id="1e936-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e936-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e936-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e936-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e936-128">**Interfaz IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="1e936-128">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="1e936-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="1e936-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





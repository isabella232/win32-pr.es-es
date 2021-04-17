---
description: El método SetMediaName especifica el nombre del archivo de origen representado por este objeto de origen.
ms.assetid: 60307c87-9dce-4e60-b14b-07d2c8604dd8
title: 'IAMTimelineSrc:: SetMediaName (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6a770c697f72c8776e9ec7070272ab09fc0dd6af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690936"
---
# <a name="iamtimelinesrcsetmedianame-method"></a><span data-ttu-id="fdf29-103">IAMTimelineSrc:: SetMediaName (método)</span><span class="sxs-lookup"><span data-stu-id="fdf29-103">IAMTimelineSrc::SetMediaName method</span></span>

> [!Note]  
> <span data-ttu-id="fdf29-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="fdf29-104">\[Deprecated.</span></span> <span data-ttu-id="fdf29-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fdf29-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fdf29-106">El `SetMediaName` método especifica el nombre del archivo de código fuente representado por este objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="fdf29-106">The `SetMediaName` method specifies the name of the source file represented by this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdf29-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fdf29-107">Syntax</span></span>


```C++
HRESULT SetMediaName(
   BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="fdf29-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fdf29-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdf29-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="fdf29-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="fdf29-110">Cadena que especifica el nombre del archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="fdf29-110">String that specifies the name of the media file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdf29-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fdf29-111">Return value</span></span>

<span data-ttu-id="fdf29-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="fdf29-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fdf29-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fdf29-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdf29-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fdf29-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fdf29-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="fdf29-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fdf29-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fdf29-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fdf29-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="fdf29-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fdf29-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdf29-118">Requirements</span></span>



| <span data-ttu-id="fdf29-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdf29-119">Requirement</span></span> | <span data-ttu-id="fdf29-120">Value</span><span class="sxs-lookup"><span data-stu-id="fdf29-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdf29-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fdf29-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fdf29-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdf29-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fdf29-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fdf29-123">Library</span></span><br/> | <dl> <span data-ttu-id="fdf29-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fdf29-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdf29-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="fdf29-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdf29-126">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="fdf29-126">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="fdf29-127">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="fdf29-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





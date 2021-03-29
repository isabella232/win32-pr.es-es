---
description: El método GetMediaName recupera el nombre del archivo de código fuente representado por este objeto de origen.
ms.assetid: 6f468628-10e1-4746-9c3a-6dae9aa3f6ad
title: 'IAMTimelineSrc:: GetMediaName (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3727d57371e5c7bab4f9d693a247b6b62a3ada17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678938"
---
# <a name="iamtimelinesrcgetmedianame-method"></a><span data-ttu-id="9177c-103">IAMTimelineSrc:: GetMediaName (método)</span><span class="sxs-lookup"><span data-stu-id="9177c-103">IAMTimelineSrc::GetMediaName method</span></span>

> [!Note]  
> <span data-ttu-id="9177c-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="9177c-104">\[Deprecated.</span></span> <span data-ttu-id="9177c-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9177c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9177c-106">El `GetMediaName` método recupera el nombre del archivo de código fuente representado por este objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="9177c-106">The `GetMediaName` method retrieves the name of the source file represented by this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9177c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9177c-107">Syntax</span></span>


```C++
HRESULT GetMediaName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="9177c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9177c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9177c-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9177c-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9177c-110">Recibe el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="9177c-110">Receives the name of the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9177c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9177c-111">Return value</span></span>

<span data-ttu-id="9177c-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9177c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9177c-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9177c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9177c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9177c-114">Remarks</span></span>

<span data-ttu-id="9177c-115">El método asigna memoria para la cadena.</span><span class="sxs-lookup"><span data-stu-id="9177c-115">The method allocates memory for the string.</span></span> <span data-ttu-id="9177c-116">La aplicación debe llamar a **SysFreeString** para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="9177c-116">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="9177c-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="9177c-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9177c-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9177c-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9177c-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9177c-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9177c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9177c-120">Requirements</span></span>



| <span data-ttu-id="9177c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9177c-121">Requirement</span></span> | <span data-ttu-id="9177c-122">Value</span><span class="sxs-lookup"><span data-stu-id="9177c-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9177c-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9177c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9177c-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="9177c-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9177c-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9177c-125">Library</span></span><br/> | <dl> <span data-ttu-id="9177c-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9177c-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9177c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9177c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9177c-128">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="9177c-128">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="9177c-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="9177c-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





---
description: El método SetUserName establece un nombre definido por la aplicación para el objeto.
ms.assetid: 6f071884-519a-465f-8273-ab1be58dda8b
title: 'IAMTimelineObj:: SetUserName (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8ec39aece23d38be6fbe2e69f7ded8bc738e04c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690714"
---
# <a name="iamtimelineobjsetusername-method"></a><span data-ttu-id="a9499-103">IAMTimelineObj:: SetUserName (método)</span><span class="sxs-lookup"><span data-stu-id="a9499-103">IAMTimelineObj::SetUserName method</span></span>

> [!Note]  
> <span data-ttu-id="a9499-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="a9499-104">\[Deprecated.</span></span> <span data-ttu-id="a9499-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a9499-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a9499-106">El `SetUserName` método establece un nombre definido por la aplicación para el objeto.</span><span class="sxs-lookup"><span data-stu-id="a9499-106">The `SetUserName` method sets an application-defined name for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9499-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9499-107">Syntax</span></span>


```C++
HRESULT SetUserName(
   BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="a9499-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a9499-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9499-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="a9499-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="a9499-110">Cadena de caracteres anchos que contiene el nombre.</span><span class="sxs-lookup"><span data-stu-id="a9499-110">Wide-character string that contains the name.</span></span> <span data-ttu-id="a9499-111">Es posible que se trunquen las cadenas con más de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a9499-111">Strings longer than 256 characters might be truncated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9499-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a9499-112">Return value</span></span>

<span data-ttu-id="a9499-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a9499-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a9499-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a9499-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9499-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9499-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a9499-116">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="a9499-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a9499-117">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a9499-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a9499-118">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a9499-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a9499-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9499-119">Requirements</span></span>



| <span data-ttu-id="a9499-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9499-120">Requirement</span></span> | <span data-ttu-id="a9499-121">Value</span><span class="sxs-lookup"><span data-stu-id="a9499-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9499-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9499-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a9499-123"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9499-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a9499-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a9499-124">Library</span></span><br/> | <dl> <span data-ttu-id="a9499-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9499-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9499-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9499-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9499-127">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="a9499-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="a9499-128">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="a9499-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





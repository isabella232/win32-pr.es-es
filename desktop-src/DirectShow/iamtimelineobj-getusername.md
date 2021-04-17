---
description: El método GetUserName recupera el nombre definido por la aplicación del objeto.
ms.assetid: 7d172ec5-9cb7-4418-a628-a109944077a6
title: 'IAMTimelineObj:: GetUserName (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: efca014493cb5631e058927256bd1586aaca7ab7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680732"
---
# <a name="iamtimelineobjgetusername-method"></a><span data-ttu-id="ce397-103">IAMTimelineObj:: GetUserName (método)</span><span class="sxs-lookup"><span data-stu-id="ce397-103">IAMTimelineObj::GetUserName method</span></span>

> [!Note]  
> <span data-ttu-id="ce397-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="ce397-104">\[Deprecated.</span></span> <span data-ttu-id="ce397-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ce397-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ce397-106">El `GetUserName` método recupera el nombre definido por la aplicación del objeto.</span><span class="sxs-lookup"><span data-stu-id="ce397-106">The `GetUserName` method retrieves the object's application-defined name.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce397-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce397-107">Syntax</span></span>


```C++
HRESULT GetUserName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="ce397-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce397-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce397-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ce397-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ce397-110">Recibe el nombre del objeto como **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="ce397-110">Receives the name of the object as a **BSTR**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce397-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce397-111">Return value</span></span>

<span data-ttu-id="ce397-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="ce397-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ce397-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ce397-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce397-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce397-114">Remarks</span></span>

<span data-ttu-id="ce397-115">El método asigna memoria para la cadena.</span><span class="sxs-lookup"><span data-stu-id="ce397-115">The method allocates memory for the string.</span></span> <span data-ttu-id="ce397-116">La aplicación debe llamar a **SysFreeString** para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="ce397-116">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="ce397-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="ce397-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ce397-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ce397-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ce397-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ce397-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ce397-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce397-120">Requirements</span></span>



| <span data-ttu-id="ce397-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce397-121">Requirement</span></span> | <span data-ttu-id="ce397-122">Value</span><span class="sxs-lookup"><span data-stu-id="ce397-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce397-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce397-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ce397-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce397-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ce397-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce397-125">Library</span></span><br/> | <dl> <span data-ttu-id="ce397-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce397-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce397-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce397-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce397-128">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="ce397-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="ce397-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="ce397-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





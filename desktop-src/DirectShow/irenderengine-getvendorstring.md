---
description: El método GetVendorString recupera el nombre del proveedor. En el caso de los objetos del motor de representación que se proporcionan en DirectShow, la cadena del proveedor es &\# 0034; Microsoft Corporation&\# 0034;.
ms.assetid: d0a4c525-67dc-419a-b4d6-8cd51888fd8a
title: 'IRenderEngine:: GetVendorString (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetVendorString
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: abf339b73fa058c6554965c16428774ad1fdd32c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680718"
---
# <a name="irenderenginegetvendorstring-method"></a><span data-ttu-id="89d51-104">IRenderEngine:: GetVendorString (método)</span><span class="sxs-lookup"><span data-stu-id="89d51-104">IRenderEngine::GetVendorString method</span></span>

> [!Note]  
> <span data-ttu-id="89d51-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="89d51-105">\[Deprecated.</span></span> <span data-ttu-id="89d51-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="89d51-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="89d51-107">El `GetVendorString` método recupera el nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="89d51-107">The `GetVendorString` method retrieves the name of the vendor.</span></span> <span data-ttu-id="89d51-108">En el caso de los objetos del motor de representación que se proporcionan en DirectShow, la cadena del proveedor es "Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="89d51-108">For the render engine objects that are provided by DirectShow, the vendor string is "Microsoft Corporation".</span></span>

## <a name="syntax"></a><span data-ttu-id="89d51-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89d51-109">Syntax</span></span>


```C++
HRESULT GetVendorString(
  [out, retval] BSTR *pVendorID
);
```



## <a name="parameters"></a><span data-ttu-id="89d51-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89d51-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89d51-111">*pVendorID* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="89d51-111">*pVendorID* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="89d51-112">Recibe un **BSTR** que contiene la cadena del proveedor.</span><span class="sxs-lookup"><span data-stu-id="89d51-112">Receives a **BSTR** containing the vendor string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89d51-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89d51-113">Return value</span></span>

<span data-ttu-id="89d51-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="89d51-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="89d51-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="89d51-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="89d51-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89d51-116">Remarks</span></span>

<span data-ttu-id="89d51-117">El método asigna memoria para la cadena.</span><span class="sxs-lookup"><span data-stu-id="89d51-117">The method allocates memory for the string.</span></span> <span data-ttu-id="89d51-118">La aplicación debe llamar a **SysFreeString** para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="89d51-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="89d51-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="89d51-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="89d51-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="89d51-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="89d51-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="89d51-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="89d51-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89d51-122">Requirements</span></span>



| <span data-ttu-id="89d51-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="89d51-123">Requirement</span></span> | <span data-ttu-id="89d51-124">Value</span><span class="sxs-lookup"><span data-stu-id="89d51-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89d51-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89d51-125">Header</span></span><br/>  | <dl> <span data-ttu-id="89d51-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="89d51-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="89d51-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="89d51-127">Library</span></span><br/> | <dl> <span data-ttu-id="89d51-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89d51-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89d51-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="89d51-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89d51-130">**Interfaz IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="89d51-130">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="89d51-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="89d51-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





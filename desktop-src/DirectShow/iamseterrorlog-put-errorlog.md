---
description: El \_ método put ErrorLog especifica un registro de errores para el objeto.
ms.assetid: 39da3fb0-57d3-452f-b2ae-6dcd84fa5c8e
title: 'IAMSetErrorLog: método de ut_ErrorLog de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog.put_ErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 189f0fed57d67d7632d07839ee82dd13494eb418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679390"
---
# <a name="iamseterrorlogput_errorlog-method"></a><span data-ttu-id="b7d04-103">IAMSetErrorLog: \_ método ErrorLog:p UT</span><span class="sxs-lookup"><span data-stu-id="b7d04-103">IAMSetErrorLog::put\_ErrorLog method</span></span>

> [!Note]  
> <span data-ttu-id="b7d04-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="b7d04-104">\[Deprecated.</span></span> <span data-ttu-id="b7d04-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b7d04-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b7d04-106">El `put_ErrorLog` método especifica un registro de errores para el objeto.</span><span class="sxs-lookup"><span data-stu-id="b7d04-106">The `put_ErrorLog` method specifies an error log for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7d04-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7d04-107">Syntax</span></span>


```C++
HRESULT put_ErrorLog(
  [in] IAMErrorLog *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="b7d04-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7d04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7d04-109">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b7d04-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d04-110">Puntero a la interfaz [**IAMErrorLog**](iamerrorlog.md) del registro de errores.</span><span class="sxs-lookup"><span data-stu-id="b7d04-110">Pointer to the error log's [**IAMErrorLog**](iamerrorlog.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7d04-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7d04-111">Return value</span></span>

<span data-ttu-id="b7d04-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="b7d04-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b7d04-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b7d04-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7d04-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7d04-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b7d04-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="b7d04-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b7d04-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b7d04-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b7d04-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b7d04-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b7d04-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7d04-118">Requirements</span></span>



| <span data-ttu-id="b7d04-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7d04-119">Requirement</span></span> | <span data-ttu-id="b7d04-120">Value</span><span class="sxs-lookup"><span data-stu-id="b7d04-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d04-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7d04-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b7d04-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7d04-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b7d04-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b7d04-123">Library</span></span><br/> | <dl> <span data-ttu-id="b7d04-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7d04-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7d04-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7d04-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d04-126">**Interfaz IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="b7d04-126">**IAMSetErrorLog Interface**</span></span>](iamseterrorlog.md)
</dt> <dt>

[<span data-ttu-id="b7d04-127">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="b7d04-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





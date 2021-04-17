---
description: El \_ método get ErrorLog recupera el registro de errores actual de este objeto.
ms.assetid: 580b8a06-6bf2-49ef-a5fb-5e6df2f09793
title: 'Método IAMSetErrorLog:: get_ErrorLog (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog.get_ErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 508a73d6475698dca628de7e3bb96001fe13bcd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653523"
---
# <a name="iamseterrorlogget_errorlog-method"></a><span data-ttu-id="3b24e-103">IAMSetErrorLog:: get \_ ErrorLog (método)</span><span class="sxs-lookup"><span data-stu-id="3b24e-103">IAMSetErrorLog::get\_ErrorLog method</span></span>

> [!Note]  
> <span data-ttu-id="3b24e-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="3b24e-104">\[Deprecated.</span></span> <span data-ttu-id="3b24e-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3b24e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3b24e-106">El `get_ErrorLog` método recupera el registro de errores actual de este objeto.</span><span class="sxs-lookup"><span data-stu-id="3b24e-106">The `get_ErrorLog` method retrieves the current error log for this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b24e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b24e-107">Syntax</span></span>


```C++
HRESULT get_ErrorLog(
  [out, retval] IAMErrorLog **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="3b24e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b24e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b24e-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3b24e-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3b24e-110">Recibe un puntero a la interfaz [**IAMErrorLog**](iamerrorlog.md) del registro de errores.</span><span class="sxs-lookup"><span data-stu-id="3b24e-110">Receives a pointer to the error log's [**IAMErrorLog**](iamerrorlog.md) interface.</span></span> <span data-ttu-id="3b24e-111">Si la escala de tiempo no tiene un registro de errores, el valor se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="3b24e-111">If the timeline does not have an error log, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b24e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b24e-112">Return value</span></span>

<span data-ttu-id="3b24e-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="3b24e-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3b24e-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3b24e-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b24e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b24e-115">Remarks</span></span>

<span data-ttu-id="3b24e-116">Si el valor devuelto en *pval* no es **null**, la interfaz [**IAMErrorLog**](iamerrorlog.md) tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="3b24e-116">If the value returned in *pVal* is not **NULL**, the [**IAMErrorLog**](iamerrorlog.md) interface has an outstanding reference count.</span></span> <span data-ttu-id="3b24e-117">Asegúrese de liberar la interfaz cuando haya terminado de usarla.</span><span class="sxs-lookup"><span data-stu-id="3b24e-117">Be sure to release the interface when you are done using it.</span></span>

> [!Note]  
> <span data-ttu-id="3b24e-118">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="3b24e-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3b24e-119">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3b24e-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3b24e-120">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3b24e-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3b24e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b24e-121">Requirements</span></span>



| <span data-ttu-id="3b24e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b24e-122">Requirement</span></span> | <span data-ttu-id="3b24e-123">Value</span><span class="sxs-lookup"><span data-stu-id="3b24e-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b24e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b24e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3b24e-125"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b24e-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3b24e-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b24e-126">Library</span></span><br/> | <dl> <span data-ttu-id="3b24e-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b24e-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b24e-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b24e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b24e-129">**Interfaz IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="3b24e-129">**IAMSetErrorLog Interface**</span></span>](iamseterrorlog.md)
</dt> <dt>

[<span data-ttu-id="3b24e-130">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="3b24e-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





---
description: El \_ método put FILENAME especifica el nombre del archivo de código fuente que va a usar el detector de medios.
ms.assetid: 37bcc7ed-d2c1-4182-b85a-03bad92c5ba7
title: 'IMediaDet: método de ut_Filename de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filename
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 542b84d3a1eec79b8408c7642bc08680fdc036ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679533"
---
# <a name="imediadetput_filename-method"></a><span data-ttu-id="d1bf3-103">IMediaDet::p \_ método FILENAME.</span><span class="sxs-lookup"><span data-stu-id="d1bf3-103">IMediaDet::put\_Filename method</span></span>

> [!Note]  
> <span data-ttu-id="d1bf3-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="d1bf3-104">\[Deprecated.</span></span> <span data-ttu-id="d1bf3-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d1bf3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d1bf3-106">El `put_Filename` método especifica el nombre del archivo de código fuente que va a usar el detector de medios.</span><span class="sxs-lookup"><span data-stu-id="d1bf3-106">The `put_Filename` method specifies the name of the source file for the media detector to use.</span></span>

<span data-ttu-id="d1bf3-107">No llame a este método dos veces en el mismo objeto MediaDet.</span><span class="sxs-lookup"><span data-stu-id="d1bf3-107">Do not call this method twice on the same MediaDet object.</span></span> <span data-ttu-id="d1bf3-108">Para usar esta interfaz con más de un archivo de código fuente, cree instancias independientes del objeto MediaDet.</span><span class="sxs-lookup"><span data-stu-id="d1bf3-108">To use this interface with more than one source file, create separate instances of the MediaDet object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1bf3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1bf3-109">Syntax</span></span>


```C++
HRESULT put_Filename(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="d1bf3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1bf3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1bf3-111">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d1bf3-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1bf3-112">Nombre del archivo de origen.</span><span class="sxs-lookup"><span data-stu-id="d1bf3-112">File name of the source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1bf3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1bf3-113">Return value</span></span>

<span data-ttu-id="d1bf3-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d1bf3-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d1bf3-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d1bf3-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1bf3-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1bf3-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d1bf3-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="d1bf3-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d1bf3-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d1bf3-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d1bf3-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d1bf3-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d1bf3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1bf3-120">Requirements</span></span>



| <span data-ttu-id="d1bf3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1bf3-121">Requirement</span></span> | <span data-ttu-id="d1bf3-122">Value</span><span class="sxs-lookup"><span data-stu-id="d1bf3-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1bf3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1bf3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d1bf3-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1bf3-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d1bf3-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1bf3-125">Library</span></span><br/> | <dl> <span data-ttu-id="d1bf3-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1bf3-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1bf3-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1bf3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1bf3-128">**Interfaz IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="d1bf3-128">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="d1bf3-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="d1bf3-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





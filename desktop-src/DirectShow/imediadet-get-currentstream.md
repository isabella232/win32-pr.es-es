---
description: El \_ método get CurrentStream recupera el número de secuencia que usa actualmente el detector de medios.
ms.assetid: 0f590498-e639-4b6b-be1d-f1e4a36282cb
title: 'Método IMediaDet:: get_CurrentStream (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_CurrentStream
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 98e664e88862a6bc124a88ac23cedf29e687d51e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680230"
---
# <a name="imediadetget_currentstream-method"></a><span data-ttu-id="1a3f6-103">IMediaDet:: get \_ CurrentStream (método)</span><span class="sxs-lookup"><span data-stu-id="1a3f6-103">IMediaDet::get\_CurrentStream method</span></span>

> [!Note]  
> <span data-ttu-id="1a3f6-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-104">\[Deprecated.</span></span> <span data-ttu-id="1a3f6-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1a3f6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1a3f6-106">El `get_CurrentStream` método recupera el número de secuencia utilizado actualmente por el detector de medios.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-106">The `get_CurrentStream` method retrieves the stream number currently used by the media detector.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a3f6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a3f6-107">Syntax</span></span>


```C++
HRESULT get_CurrentStream(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="1a3f6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a3f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a3f6-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1a3f6-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1a3f6-110">Recibe el número de secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-110">Receives the current stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a3f6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a3f6-111">Return value</span></span>

<span data-ttu-id="1a3f6-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1a3f6-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1a3f6-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a3f6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a3f6-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1a3f6-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1a3f6-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1a3f6-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1a3f6-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1a3f6-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1a3f6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a3f6-118">Requirements</span></span>



| <span data-ttu-id="1a3f6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a3f6-119">Requirement</span></span> | <span data-ttu-id="1a3f6-120">Value</span><span class="sxs-lookup"><span data-stu-id="1a3f6-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a3f6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a3f6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1a3f6-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a3f6-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1a3f6-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1a3f6-123">Library</span></span><br/> | <dl> <span data-ttu-id="1a3f6-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a3f6-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a3f6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a3f6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a3f6-126">**Interfaz IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="1a3f6-126">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="1a3f6-127">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="1a3f6-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





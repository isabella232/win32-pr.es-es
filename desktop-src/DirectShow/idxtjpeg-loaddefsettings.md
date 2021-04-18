---
description: El método LoadDefSettings restaura la configuración predeterminada de la transición de borrado.
ms.assetid: 3f81002a-ecac-4d5a-8d2a-ada4d4884d7d
title: 'IDxtJpeg:: LoadDefSettings (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.LoadDefSettings
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 51438a21782d1a703a3b43134517e8337ce9f75e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680669"
---
# <a name="idxtjpegloaddefsettings-method"></a><span data-ttu-id="e7f43-103">IDxtJpeg:: LoadDefSettings (método)</span><span class="sxs-lookup"><span data-stu-id="e7f43-103">IDxtJpeg::LoadDefSettings method</span></span>

> [!Note]  
> <span data-ttu-id="e7f43-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="e7f43-104">\[Deprecated.</span></span> <span data-ttu-id="e7f43-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e7f43-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e7f43-106">El `LoadDefSettings` método restaura la configuración predeterminada de la transición de borrado.</span><span class="sxs-lookup"><span data-stu-id="e7f43-106">The `LoadDefSettings` method restores the default settings of the Wipe transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7f43-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7f43-107">Syntax</span></span>


```C++
HRESULT LoadDefSettings();
```



## <a name="parameters"></a><span data-ttu-id="e7f43-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7f43-108">Parameters</span></span>

<span data-ttu-id="e7f43-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e7f43-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7f43-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7f43-110">Return value</span></span>

<span data-ttu-id="e7f43-111">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e7f43-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e7f43-112">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e7f43-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7f43-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7f43-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e7f43-114">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="e7f43-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e7f43-115">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e7f43-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e7f43-116">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e7f43-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e7f43-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7f43-117">Requirements</span></span>



| <span data-ttu-id="e7f43-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7f43-118">Requirement</span></span> | <span data-ttu-id="e7f43-119">Value</span><span class="sxs-lookup"><span data-stu-id="e7f43-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7f43-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7f43-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e7f43-121"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7f43-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e7f43-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7f43-122">Library</span></span><br/> | <dl> <span data-ttu-id="e7f43-123"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7f43-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7f43-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7f43-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7f43-125">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="e7f43-125">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 





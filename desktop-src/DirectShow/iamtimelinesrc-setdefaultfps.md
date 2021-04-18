---
description: El método SetDefaultFPS establece la velocidad de fotogramas predeterminada del objeto de origen.
ms.assetid: ea93acde-3e05-43d5-8130-9ab2ee841b4e
title: 'IAMTimelineSrc:: SetDefaultFPS (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd15f0606b1a4e4ee1aacdb1b3f56d63a024708b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680572"
---
# <a name="iamtimelinesrcsetdefaultfps-method"></a><span data-ttu-id="f0c70-103">IAMTimelineSrc:: SetDefaultFPS (método)</span><span class="sxs-lookup"><span data-stu-id="f0c70-103">IAMTimelineSrc::SetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="f0c70-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="f0c70-104">\[Deprecated.</span></span> <span data-ttu-id="f0c70-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f0c70-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f0c70-106">El `SetDefaultFPS` método establece la velocidad de fotogramas predeterminada del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="f0c70-106">The `SetDefaultFPS` method sets the source object's default frame rate.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0c70-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0c70-107">Syntax</span></span>


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a><span data-ttu-id="f0c70-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0c70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0c70-109">*FPS*</span><span class="sxs-lookup"><span data-stu-id="f0c70-109">*FPS*</span></span> 
</dt> <dd>

<span data-ttu-id="f0c70-110">Velocidad de fotogramas predeterminada, en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="f0c70-110">Default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0c70-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0c70-111">Return value</span></span>

<span data-ttu-id="f0c70-112">Devuelve S \_ correcto si es correcto, o E \_ INVALIDARG si la velocidad de fotogramas especificada es menor que cero.</span><span class="sxs-lookup"><span data-stu-id="f0c70-112">Returns S\_OK if successful, or E\_INVALIDARG if the specified frame rate is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0c70-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0c70-113">Remarks</span></span>

<span data-ttu-id="f0c70-114">El motor de representación utiliza este valor si no puede determinar la velocidad de fotogramas del archivo de código fuente original.</span><span class="sxs-lookup"><span data-stu-id="f0c70-114">The render engine uses this value if it cannot determine the frame rate from the original source file.</span></span>

<span data-ttu-id="f0c70-115">Llame a este método solo para los archivos de código fuente sin una velocidad de fotogramas predefinida.</span><span class="sxs-lookup"><span data-stu-id="f0c70-115">Call this method only for source files without a predefined frame rate.</span></span> <span data-ttu-id="f0c70-116">En el caso de los archivos de mapa de bits y JPEG, la velocidad de fotogramas predeterminada es cero, lo que hace que el origen se represente como una imagen fija.</span><span class="sxs-lookup"><span data-stu-id="f0c70-116">For bitmap and JPEG files, the default frame rate is zero, which causes the source to be rendered as a still image.</span></span> <span data-ttu-id="f0c70-117">Para usar la imagen como primer fotograma en una secuencia DIB, establezca la velocidad de fotogramas en un valor mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="f0c70-117">To use the image as the first frame in a DIB sequence set the frame rate to a value greater than zero.</span></span> <span data-ttu-id="f0c70-118">Para obtener más información, vea [trabajar con orígenes](working-with-sources.md).</span><span class="sxs-lookup"><span data-stu-id="f0c70-118">For more information, see [Working with Sources](working-with-sources.md).</span></span>

> [!Note]  
> <span data-ttu-id="f0c70-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="f0c70-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f0c70-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f0c70-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f0c70-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f0c70-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f0c70-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0c70-122">Requirements</span></span>



| <span data-ttu-id="f0c70-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0c70-123">Requirement</span></span> | <span data-ttu-id="f0c70-124">Value</span><span class="sxs-lookup"><span data-stu-id="f0c70-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c70-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0c70-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f0c70-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0c70-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f0c70-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0c70-127">Library</span></span><br/> | <dl> <span data-ttu-id="f0c70-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0c70-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0c70-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0c70-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c70-130">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="f0c70-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="f0c70-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="f0c70-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





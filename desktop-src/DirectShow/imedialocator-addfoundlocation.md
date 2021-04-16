---
description: El método AddFoundLocation agrega un directorio a la memoria caché del directorio.
ms.assetid: 0323c4ea-2e86-433b-87d0-34d1800a5627
title: 'IMediaLocator:: AddFoundLocation (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.AddFoundLocation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76d878e5b013b8c6a061d777d4ec837bca85f8e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679070"
---
# <a name="imedialocatoraddfoundlocation-method"></a><span data-ttu-id="eef13-103">IMediaLocator:: AddFoundLocation (método)</span><span class="sxs-lookup"><span data-stu-id="eef13-103">IMediaLocator::AddFoundLocation method</span></span>

> [!Note]  
> <span data-ttu-id="eef13-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="eef13-104">\[Deprecated.</span></span> <span data-ttu-id="eef13-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="eef13-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="eef13-106">El `AddFoundLocation` método agrega un directorio a la memoria caché del directorio.</span><span class="sxs-lookup"><span data-stu-id="eef13-106">The `AddFoundLocation` method adds a directory to the directory cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="eef13-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eef13-107">Syntax</span></span>


```C++
HRESULT AddFoundLocation(
   BSTR DirectoryName
);
```



## <a name="parameters"></a><span data-ttu-id="eef13-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eef13-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eef13-109">*DirectoryName*</span><span class="sxs-lookup"><span data-stu-id="eef13-109">*DirectoryName*</span></span> 
</dt> <dd>

<span data-ttu-id="eef13-110">Ruta de acceso al directorio que se va a agregar a la caché.</span><span class="sxs-lookup"><span data-stu-id="eef13-110">Directory path to add to the cache.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eef13-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eef13-111">Return value</span></span>

<span data-ttu-id="eef13-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="eef13-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eef13-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eef13-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="eef13-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eef13-114">Remarks</span></span>

<span data-ttu-id="eef13-115">El localizador de medios mantiene una memoria caché de rutas de acceso de directorio donde ha encontrado correctamente archivos en búsquedas anteriores.</span><span class="sxs-lookup"><span data-stu-id="eef13-115">The media locator keeps a cache of directory paths where it has successfully found files in past searches.</span></span> <span data-ttu-id="eef13-116">Cuando localiza correctamente un archivo, agrega el directorio a la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="eef13-116">When it successfully locates a file, it adds the directory to the cache.</span></span>

> [!Note]  
> <span data-ttu-id="eef13-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="eef13-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="eef13-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="eef13-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="eef13-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="eef13-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eef13-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eef13-120">Requirements</span></span>



| <span data-ttu-id="eef13-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="eef13-121">Requirement</span></span> | <span data-ttu-id="eef13-122">Value</span><span class="sxs-lookup"><span data-stu-id="eef13-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eef13-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eef13-123">Header</span></span><br/>  | <dl> <span data-ttu-id="eef13-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="eef13-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="eef13-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eef13-125">Library</span></span><br/> | <dl> <span data-ttu-id="eef13-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eef13-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eef13-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="eef13-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eef13-128">**Interfaz IMediaLocator**</span><span class="sxs-lookup"><span data-stu-id="eef13-128">**IMediaLocator Interface**</span></span>](imedialocator.md)
</dt> <dt>

[<span data-ttu-id="eef13-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="eef13-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





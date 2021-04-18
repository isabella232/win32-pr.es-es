---
description: El \_ método get FILENAME recupera el nombre del archivo de código fuente utilizado actualmente por el detector de medios.
ms.assetid: 68f0f1ea-74a2-4b65-9f1d-8699326d9d04
title: 'Método IMediaDet:: get_Filename (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filename
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 95a350dde3dfdc1c6046c8e31b8a2d9e62684788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680668"
---
# <a name="imediadetget_filename-method"></a><span data-ttu-id="7497a-103">IMediaDet:: get \_ filename (método)</span><span class="sxs-lookup"><span data-stu-id="7497a-103">IMediaDet::get\_Filename method</span></span>

> [!Note]  
> <span data-ttu-id="7497a-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="7497a-104">\[Deprecated.</span></span> <span data-ttu-id="7497a-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7497a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7497a-106">El `get_Filename` método recupera el nombre del archivo de código fuente utilizado actualmente por el detector de medios.</span><span class="sxs-lookup"><span data-stu-id="7497a-106">The `get_Filename` method retrieves the name of the source file currently used by the media detector.</span></span>

## <a name="syntax"></a><span data-ttu-id="7497a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7497a-107">Syntax</span></span>


```C++
HRESULT get_Filename(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="7497a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7497a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7497a-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="7497a-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7497a-110">Recibe el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="7497a-110">Receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7497a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7497a-111">Return value</span></span>

<span data-ttu-id="7497a-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="7497a-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7497a-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7497a-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7497a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7497a-114">Remarks</span></span>

<span data-ttu-id="7497a-115">El método asigna memoria para la cadena.</span><span class="sxs-lookup"><span data-stu-id="7497a-115">The method allocates memory for the string.</span></span> <span data-ttu-id="7497a-116">La aplicación debe llamar a **SysFreeString** para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="7497a-116">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="7497a-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="7497a-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7497a-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7497a-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7497a-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7497a-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7497a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7497a-120">Requirements</span></span>



| <span data-ttu-id="7497a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7497a-121">Requirement</span></span> | <span data-ttu-id="7497a-122">Value</span><span class="sxs-lookup"><span data-stu-id="7497a-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7497a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7497a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7497a-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="7497a-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7497a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7497a-125">Library</span></span><br/> | <dl> <span data-ttu-id="7497a-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7497a-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7497a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="7497a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7497a-128">**Interfaz IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="7497a-128">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="7497a-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="7497a-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 





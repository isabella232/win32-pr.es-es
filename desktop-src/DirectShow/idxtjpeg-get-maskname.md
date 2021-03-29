---
description: El \_ método get MaskName recupera el nombre de un archivo JPEG que se usará como máscara de borrado.
ms.assetid: b21913c0-4269-41f9-b2f0-ae69be9c0871
title: 'Método IDxtJpeg:: get_MaskName (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a00c8104ee19cac33a00ff9062006338a19e283b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679212"
---
# <a name="idxtjpegget_maskname-method"></a><span data-ttu-id="53840-103">IDxtJpeg:: get \_ MaskName (método)</span><span class="sxs-lookup"><span data-stu-id="53840-103">IDxtJpeg::get\_MaskName method</span></span>

> [!Note]  
> <span data-ttu-id="53840-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="53840-104">\[Deprecated.</span></span> <span data-ttu-id="53840-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="53840-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="53840-106">El `get_MaskName` método recupera el nombre de un archivo JPEG que se usará como máscara de borrado.</span><span class="sxs-lookup"><span data-stu-id="53840-106">The `get_MaskName` method retrieves the name of a JPEG file to be used as the wipe mask.</span></span>

## <a name="syntax"></a><span data-ttu-id="53840-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53840-107">Syntax</span></span>


```C++
HRESULT get_MaskName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="53840-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53840-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53840-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="53840-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="53840-110">Recibe el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="53840-110">Receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53840-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53840-111">Return value</span></span>

<span data-ttu-id="53840-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="53840-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="53840-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="53840-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="53840-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53840-114">Remarks</span></span>

<span data-ttu-id="53840-115">Si la transición de borrado usa uno de los borradores de SMPTE integrados que admite, el valor de esta propiedad es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="53840-115">If the wipe transition is using one of the built-in SMPTE wipes that it supports, the value of this property is an empty string.</span></span>

<span data-ttu-id="53840-116">El autor de la llamada debe liberar la cadena devuelta mediante la función **SysFreeString** .</span><span class="sxs-lookup"><span data-stu-id="53840-116">The caller must release the returned string, using the **SysFreeString** function.</span></span>

> [!Note]  
> <span data-ttu-id="53840-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="53840-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="53840-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="53840-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="53840-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="53840-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="53840-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53840-120">Requirements</span></span>



| <span data-ttu-id="53840-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="53840-121">Requirement</span></span> | <span data-ttu-id="53840-122">Value</span><span class="sxs-lookup"><span data-stu-id="53840-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53840-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53840-123">Header</span></span><br/>  | <dl> <span data-ttu-id="53840-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="53840-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="53840-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="53840-125">Library</span></span><br/> | <dl> <span data-ttu-id="53840-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53840-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53840-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="53840-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53840-128">**Interfaz IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="53840-128">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> <dt>

[<span data-ttu-id="53840-129">**IDxtJpeg:: get \_ MaskNum**</span><span class="sxs-lookup"><span data-stu-id="53840-129">**IDxtJpeg::get\_MaskNum**</span></span>](idxtjpeg-get-masknum.md)
</dt> </dl>

 

 





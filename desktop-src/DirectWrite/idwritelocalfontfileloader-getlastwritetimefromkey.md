---
title: IDWriteLocalFontFileLoader GetLastWriteTimeFromKey, método
description: Obtiene la hora de la última escritura del archivo a partir de la clave de referencia del archivo de fuente.
ms.assetid: ce7f5321-8ad8-4412-a54c-7102790e99c0
keywords:
- Método GetLastWriteTimeFromKey de escritura directa
- Método GetLastWriteTimeFromKey de escritura directa, interfaz IDWriteLocalFontFileLoader
- Interfaz IDWriteLocalFontFileLoader Direct Write, método GetLastWriteTimeFromKey
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea9817917a59761278a961a6fcafcdeaea5fda32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690603"
---
# <a name="idwritelocalfontfileloadergetlastwritetimefromkey-method"></a><span data-ttu-id="8c498-106">IDWriteLocalFontFileLoader:: GetLastWriteTimeFromKey (método)</span><span class="sxs-lookup"><span data-stu-id="8c498-106">IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey method</span></span>

<span data-ttu-id="8c498-107">Obtiene la hora de la última escritura del archivo a partir de la clave de referencia del archivo de fuente.</span><span class="sxs-lookup"><span data-stu-id="8c498-107">Obtains the last write time of the file from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c498-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c498-108">Syntax</span></span>


```C++
virtual HRESULT GetLastWriteTimeFromKey(
  [in]  const void     *fontFileReferenceKey,
              UINT32   fontFileReferenceKeySize,
  [out]       FILETIME *lastWriteTime
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="8c498-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c498-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c498-110">*fontFileReferenceKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c498-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c498-111">Tipo: **const void \***</span><span class="sxs-lookup"><span data-stu-id="8c498-111">Type: **const void\***</span></span>

<span data-ttu-id="8c498-112">Clave de referencia del archivo de fuente que identifica de forma única el archivo de fuente local dentro del ámbito del cargador de fuentes que se utiliza.</span><span class="sxs-lookup"><span data-stu-id="8c498-112">The font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="8c498-113">*fontFileReferenceKeySize*</span><span class="sxs-lookup"><span data-stu-id="8c498-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="8c498-114">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="8c498-114">Type: **UINT32**</span></span>

<span data-ttu-id="8c498-115">Tamaño de la clave de referencia del archivo de fuentes en bytes.</span><span class="sxs-lookup"><span data-stu-id="8c498-115">The size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8c498-116">*lastWriteTime* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8c498-116">*lastWriteTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c498-117">Tipo: **FILETIME \***</span><span class="sxs-lookup"><span data-stu-id="8c498-117">Type: **FILETIME\***</span></span>

<span data-ttu-id="8c498-118">Hora de la última modificación del archivo de fuentes.</span><span class="sxs-lookup"><span data-stu-id="8c498-118">The time of the last font file modification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c498-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c498-119">Return value</span></span>

<span data-ttu-id="8c498-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8c498-120">Type: **HRESULT**</span></span>

<span data-ttu-id="8c498-121">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8c498-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8c498-122">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8c498-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c498-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c498-123">Requirements</span></span>



| <span data-ttu-id="8c498-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c498-124">Requirement</span></span> | <span data-ttu-id="8c498-125">Value</span><span class="sxs-lookup"><span data-stu-id="8c498-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c498-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c498-126">Library</span></span><br/> | <dl> <span data-ttu-id="8c498-127"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c498-127"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="8c498-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c498-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="8c498-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c498-129"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c498-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c498-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c498-131">**IDWriteLocalFontFileLoader**</span><span class="sxs-lookup"><span data-stu-id="8c498-131">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 






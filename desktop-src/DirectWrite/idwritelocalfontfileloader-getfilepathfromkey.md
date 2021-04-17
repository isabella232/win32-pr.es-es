---
title: IDWriteLocalFontFileLoader GetFilePathFromKey, método
description: Obtiene la ruta de acceso del archivo de fuentes absolutas de la clave de referencia del archivo de fuente.
ms.assetid: a61cfe80-100d-4813-b04f-a39f626893dd
keywords:
- Método GetFilePathFromKey de escritura directa
- Método GetFilePathFromKey de escritura directa, interfaz IDWriteLocalFontFileLoader
- Interfaz IDWriteLocalFontFileLoader Direct Write, método GetFilePathFromKey
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14fb3070ddc2f0d82554c86f005343faa3c087fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690516"
---
# <a name="idwritelocalfontfileloadergetfilepathfromkey-method"></a><span data-ttu-id="5b8d5-106">IDWriteLocalFontFileLoader:: GetFilePathFromKey (método)</span><span class="sxs-lookup"><span data-stu-id="5b8d5-106">IDWriteLocalFontFileLoader::GetFilePathFromKey method</span></span>

<span data-ttu-id="5b8d5-107">Obtiene la ruta de acceso del archivo de fuentes absolutas de la clave de referencia del archivo de fuente.</span><span class="sxs-lookup"><span data-stu-id="5b8d5-107">Obtains the absolute font file path from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b8d5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b8d5-108">Syntax</span></span>


```C++
virtual HRESULT GetFilePathFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       WCHAR  *filePath,
              UINT32 filePathSize
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="5b8d5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b8d5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b8d5-110">*fontFileReferenceKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5b8d5-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b8d5-111">Tipo: **const void \***</span><span class="sxs-lookup"><span data-stu-id="5b8d5-111">Type: **const void\***</span></span>

<span data-ttu-id="5b8d5-112">Clave de referencia del archivo de fuente que identifica de forma única el archivo de fuente local dentro del ámbito del cargador de fuentes que se utiliza.</span><span class="sxs-lookup"><span data-stu-id="5b8d5-112">The font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="5b8d5-113">*fontFileReferenceKeySize*</span><span class="sxs-lookup"><span data-stu-id="5b8d5-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="5b8d5-114">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="5b8d5-114">Type: **UINT32**</span></span>

<span data-ttu-id="5b8d5-115">Tamaño de la clave de referencia del archivo de fuentes en bytes.</span><span class="sxs-lookup"><span data-stu-id="5b8d5-115">The size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5b8d5-116">*filePath* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5b8d5-116">*filePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b8d5-117">Tipo: **WCHAR \***</span><span class="sxs-lookup"><span data-stu-id="5b8d5-117">Type: **WCHAR\***</span></span>

<span data-ttu-id="5b8d5-118">Matriz de caracteres que recibe la ruta de acceso del archivo local.</span><span class="sxs-lookup"><span data-stu-id="5b8d5-118">The character array that receives the local file path.</span></span>

</dd> <dt>

<span data-ttu-id="5b8d5-119">*filePathSize*</span><span class="sxs-lookup"><span data-stu-id="5b8d5-119">*filePathSize*</span></span> 
</dt> <dd>

<span data-ttu-id="5b8d5-120">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="5b8d5-120">Type: **UINT32**</span></span>

<span data-ttu-id="5b8d5-121">Longitud de la matriz de caracteres de la ruta de acceso del archivo.</span><span class="sxs-lookup"><span data-stu-id="5b8d5-121">The length of the file path character array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b8d5-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b8d5-122">Return value</span></span>

<span data-ttu-id="5b8d5-123">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5b8d5-123">Type: **HRESULT**</span></span>

<span data-ttu-id="5b8d5-124">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="5b8d5-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5b8d5-125">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5b8d5-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b8d5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b8d5-126">Requirements</span></span>



| <span data-ttu-id="5b8d5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b8d5-127">Requirement</span></span> | <span data-ttu-id="5b8d5-128">Value</span><span class="sxs-lookup"><span data-stu-id="5b8d5-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b8d5-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5b8d5-129">Library</span></span><br/> | <dl> <span data-ttu-id="5b8d5-130"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b8d5-130"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="5b8d5-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5b8d5-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="5b8d5-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b8d5-132"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b8d5-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b8d5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b8d5-134">**IDWriteLocalFontFileLoader**</span><span class="sxs-lookup"><span data-stu-id="5b8d5-134">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 






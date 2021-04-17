---
title: IDWriteLocalFontFileLoader GetFilePathLengthFromKey, método
description: Obtiene la longitud de la ruta de acceso absoluta del archivo a partir de la clave de referencia del archivo de fuente.
ms.assetid: bdd84d75-5a7a-448a-a52c-0f5997ab07b9
keywords:
- Método GetFilePathLengthFromKey de escritura directa
- Método GetFilePathLengthFromKey de escritura directa, interfaz IDWriteLocalFontFileLoader
- Interfaz IDWriteLocalFontFileLoader Direct Write, método GetFilePathLengthFromKey
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathLengthFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091c3cd5f1e13c40d364a3db005793f1dd0bf5f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671206"
---
# <a name="idwritelocalfontfileloadergetfilepathlengthfromkey-method"></a><span data-ttu-id="f3eb8-106">IDWriteLocalFontFileLoader:: GetFilePathLengthFromKey (método)</span><span class="sxs-lookup"><span data-stu-id="f3eb8-106">IDWriteLocalFontFileLoader::GetFilePathLengthFromKey method</span></span>

<span data-ttu-id="f3eb8-107">Obtiene la longitud de la ruta de acceso absoluta del archivo a partir de la clave de referencia del archivo de fuente.</span><span class="sxs-lookup"><span data-stu-id="f3eb8-107">Obtains the length of the absolute file path from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3eb8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3eb8-108">Syntax</span></span>


```C++
HRESULT GetFilePathLengthFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       UINT32 *filePathLength
);
```



## <a name="parameters"></a><span data-ttu-id="f3eb8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3eb8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3eb8-110">*fontFileReferenceKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3eb8-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3eb8-111">Tipo: **const void \***</span><span class="sxs-lookup"><span data-stu-id="f3eb8-111">Type: **const void\***</span></span>

<span data-ttu-id="f3eb8-112">Clave de referencia del archivo de fuente que identifica de forma única el archivo de fuente local dentro del ámbito del cargador de fuentes que se está usando.</span><span class="sxs-lookup"><span data-stu-id="f3eb8-112">Font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb8-113">*fontFileReferenceKeySize*</span><span class="sxs-lookup"><span data-stu-id="f3eb8-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="f3eb8-114">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="f3eb8-114">Type: **UINT32**</span></span>

<span data-ttu-id="f3eb8-115">Tamaño de la clave de referencia del archivo de fuentes en bytes.</span><span class="sxs-lookup"><span data-stu-id="f3eb8-115">Size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb8-116">*filePathLength* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f3eb8-116">*filePathLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3eb8-117">Tipo: **UINT32 \***</span><span class="sxs-lookup"><span data-stu-id="f3eb8-117">Type: **UINT32\***</span></span>

<span data-ttu-id="f3eb8-118">Longitud de la cadena de ruta de acceso del archivo, sin incluir el carácter **nulo** terminado.</span><span class="sxs-lookup"><span data-stu-id="f3eb8-118">Length of the file path string, not including the terminated **NULL** character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3eb8-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3eb8-119">Return value</span></span>

<span data-ttu-id="f3eb8-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f3eb8-120">Type: **HRESULT**</span></span>

<span data-ttu-id="f3eb8-121">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f3eb8-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f3eb8-122">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f3eb8-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3eb8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3eb8-123">Requirements</span></span>



| <span data-ttu-id="f3eb8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3eb8-124">Requirement</span></span> | <span data-ttu-id="f3eb8-125">Value</span><span class="sxs-lookup"><span data-stu-id="f3eb8-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3eb8-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f3eb8-126">Library</span></span><br/> | <dl> <span data-ttu-id="f3eb8-127"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3eb8-127"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="f3eb8-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f3eb8-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="f3eb8-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3eb8-129"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3eb8-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3eb8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3eb8-131">**IDWriteLocalFontFileLoader**</span><span class="sxs-lookup"><span data-stu-id="f3eb8-131">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 






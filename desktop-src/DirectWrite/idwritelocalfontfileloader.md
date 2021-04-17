---
title: Interfaz IDWriteLocalFontFileLoader
description: Implementación integrada de la interfaz IDWriteFontFileLoader, que funciona en archivos de fuentes locales y expone información del archivo de fuentes local a partir de la clave de referencia del archivo de fuente.
ms.assetid: acb777c8-24c6-452e-8f58-8fb2ad8c0b6c
keywords:
- Interfaz IDWriteLocalFontFileLoader de escritura directa
- IDWriteLocalFontFileLoader interface Direct Write, descrito
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c65f537dc2a4a96161a11d85ae0a4e1869a331e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671035"
---
# <a name="idwritelocalfontfileloader-interface"></a><span data-ttu-id="c6f26-105">Interfaz IDWriteLocalFontFileLoader</span><span class="sxs-lookup"><span data-stu-id="c6f26-105">IDWriteLocalFontFileLoader interface</span></span>

<span data-ttu-id="c6f26-106">Implementación integrada de la interfaz [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) , que funciona en archivos de fuentes locales y expone información del archivo de fuentes local a partir de la clave de referencia del archivo de fuente.</span><span class="sxs-lookup"><span data-stu-id="c6f26-106">A built-in implementation of the [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) interface, that operates on local font files and exposes local font file information from the font file reference key.</span></span> <span data-ttu-id="c6f26-107">Las referencias de archivo de fuentes creadas con [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) usan este cargador de archivos de fuentes.</span><span class="sxs-lookup"><span data-stu-id="c6f26-107">Font file references created using [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) use this font file loader.</span></span>

## <a name="members"></a><span data-ttu-id="c6f26-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c6f26-108">Members</span></span>

<span data-ttu-id="c6f26-109">La interfaz **IDWriteLocalFontFileLoader** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c6f26-109">The **IDWriteLocalFontFileLoader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c6f26-110">**IDWriteLocalFontFileLoader** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c6f26-110">**IDWriteLocalFontFileLoader** also has these types of members:</span></span>

-   [<span data-ttu-id="c6f26-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c6f26-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c6f26-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="c6f26-112">Methods</span></span>

<span data-ttu-id="c6f26-113">La interfaz **IDWriteLocalFontFileLoader** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c6f26-113">The **IDWriteLocalFontFileLoader** interface has these methods.</span></span>



| <span data-ttu-id="c6f26-114">Método</span><span class="sxs-lookup"><span data-stu-id="c6f26-114">Method</span></span>                                                                                  | <span data-ttu-id="c6f26-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6f26-115">Description</span></span>                                                                               |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6f26-116">**GetFilePathFromKey**</span><span class="sxs-lookup"><span data-stu-id="c6f26-116">**GetFilePathFromKey**</span></span>](idwritelocalfontfileloader-getfilepathfromkey.md)             | <span data-ttu-id="c6f26-117">Obtiene la ruta de acceso del archivo de fuentes absolutas de la clave de referencia del archivo de fuente.</span><span class="sxs-lookup"><span data-stu-id="c6f26-117">Obtains the absolute font file path from the font file reference key.</span></span><br/>          |
| [<span data-ttu-id="c6f26-118">**GetFilePathLengthFromKey**</span><span class="sxs-lookup"><span data-stu-id="c6f26-118">**GetFilePathLengthFromKey**</span></span>](idwritelocalfontfileloader-getfilepathlengthfromkey.md) | <span data-ttu-id="c6f26-119">Obtiene la longitud de la ruta de acceso absoluta del archivo a partir de la clave de referencia del archivo de fuente.</span><span class="sxs-lookup"><span data-stu-id="c6f26-119">Obtains the length of the absolute file path from the font file reference key.</span></span><br/> |
| [<span data-ttu-id="c6f26-120">**GetLastWriteTimeFromKey**</span><span class="sxs-lookup"><span data-stu-id="c6f26-120">**GetLastWriteTimeFromKey**</span></span>](idwritelocalfontfileloader-getlastwritetimefromkey.md)   | <span data-ttu-id="c6f26-121">Obtiene la hora de la última escritura del archivo a partir de la clave de referencia del archivo de fuente.</span><span class="sxs-lookup"><span data-stu-id="c6f26-121">Obtains the last write time of the file from the font file reference key.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="c6f26-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6f26-122">Requirements</span></span>



| <span data-ttu-id="c6f26-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6f26-123">Requirement</span></span> | <span data-ttu-id="c6f26-124">Value</span><span class="sxs-lookup"><span data-stu-id="c6f26-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6f26-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c6f26-125">Library</span></span><br/> | <dl> <span data-ttu-id="c6f26-126"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6f26-126"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="c6f26-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c6f26-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="c6f26-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6f26-128"><dt>Dwrite.dll</dt></span></span> </dl> |



 


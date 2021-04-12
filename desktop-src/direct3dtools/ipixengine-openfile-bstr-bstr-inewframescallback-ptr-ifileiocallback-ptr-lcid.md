---
description: Abre un registro de gráficos.
MS-HAID: vspixengine.IPixEngine\_OpenFile\_BSTR\_BSTR\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_LCID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine:: OpenFile (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8E0E1336-9FC7-4C32-AF3C-F3BDF39A36D9
api_name:
- IPixEngine.OpenFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d18b0ff4d6d2301c6d52d2bc855d48a3db124ccb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152275"
---
# <a name="span-idvspixengineipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcidspanipixengineopenfile-method"></a><span data-ttu-id="a8954-103"><span id="vspixengine.ipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcid"></span>IPixEngine:: OpenFile (método)</span><span class="sxs-lookup"><span data-stu-id="a8954-103"><span id="vspixengine.ipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcid"></span>IPixEngine::OpenFile method</span></span>

<span data-ttu-id="a8954-104">Abre un registro de gráficos.</span><span class="sxs-lookup"><span data-stu-id="a8954-104">Opens a graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8954-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8954-105">Syntax</span></span>


```C++
HRESULT OpenFile(
   BSTR                FileName,
   BSTR                registryBoot,
   INewFramesCallback* callbacks,
   IFileIOCallback*    pFileIOCallback,
   LCID                uiLocale
);
```

## <a name="parameters"></a><span data-ttu-id="a8954-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8954-106">Parameters</span></span>

<span data-ttu-id="a8954-107">*Extensión* </span><span class="sxs-lookup"><span data-stu-id="a8954-107">*FileName* </span></span>  
<span data-ttu-id="a8954-108">Cadena COM que contiene el nombre del registro de gráficos.</span><span class="sxs-lookup"><span data-stu-id="a8954-108">A COM string containing the name of the graphics log.</span></span>

<span data-ttu-id="a8954-109">*registryBoot* </span><span class="sxs-lookup"><span data-stu-id="a8954-109">*registryBoot* </span></span>  
<span data-ttu-id="a8954-110">Cadena COM que contiene la raíz del registro.</span><span class="sxs-lookup"><span data-stu-id="a8954-110">A COM string containing the registry root.</span></span> <span data-ttu-id="a8954-111">El motor busca aquí el DIA y otras claves del registro.</span><span class="sxs-lookup"><span data-stu-id="a8954-111">The engine looks here for DIA and other registry keys.</span></span>

<span data-ttu-id="a8954-112">*devoluciones* </span><span class="sxs-lookup"><span data-stu-id="a8954-112">*callbacks* </span></span>  
<span data-ttu-id="a8954-113">La dirección de una función que se usa para notificar al host que se han analizado nuevos fotogramas.</span><span class="sxs-lookup"><span data-stu-id="a8954-113">The address of a function used to notify the host that new frames have been parsed.</span></span>

<span data-ttu-id="a8954-114">*pFileIOCallback* </span><span class="sxs-lookup"><span data-stu-id="a8954-114">*pFileIOCallback* </span></span>  
<span data-ttu-id="a8954-115">La dirección de una función que se usa para notificar al host de errores de e/s de archivo durante el análisis.</span><span class="sxs-lookup"><span data-stu-id="a8954-115">The address of a function used to notify the host of file IO errors during parsing.</span></span>

<span data-ttu-id="a8954-116">*uiLocale* </span><span class="sxs-lookup"><span data-stu-id="a8954-116">*uiLocale* </span></span>  
<span data-ttu-id="a8954-117">IDENTIFICADOR de configuración regional que se usa para presentar los mensajes de error según la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="a8954-117">The locale ID used to present error messages according to locale settings.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8954-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8954-118">Return value</span></span>

<span data-ttu-id="a8954-119">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a8954-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a8954-120">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a8954-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8954-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8954-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a8954-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8954-122">Header</span></span></p></td><td><span data-ttu-id="a8954-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a8954-123">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a8954-124"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="a8954-124"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a8954-125">**IPixEngine**</span><span class="sxs-lookup"><span data-stu-id="a8954-125">**IPixEngine**</span></span>](/windows/desktop/direct3dtools/ipixengine)

 

 

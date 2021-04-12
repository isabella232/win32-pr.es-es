---
description: Carga una textura desde un archivo y lo notifica al host de forma asincrónica cuando se completa.
MS-HAID: vspixengine.IPixEngine5\_LoadTextureFromFileAsync\_BSTR\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5:: LoadTextureFromFileAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DF10C209-B6B5-4692-81D7-7FD59CE49F56
api_name:
- IPixEngine5.LoadTextureFromFileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bef4e4e5117680f7c18f13cc99f801c8e8b8bdfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152622"
---
# <a name="span-idvspixengineipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadtexturefromfileasync-method"></a><span data-ttu-id="617be-103"><span id="vspixengine.ipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5:: LoadTextureFromFileAsync (método)</span><span class="sxs-lookup"><span data-stu-id="617be-103"><span id="vspixengine.ipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::LoadTextureFromFileAsync method</span></span>

<span data-ttu-id="617be-104">Carga una textura desde un archivo y lo notifica al host de forma asincrónica cuando se completa.</span><span class="sxs-lookup"><span data-stu-id="617be-104">Loads a texture from a file and notifies the host asynchronously when it completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="617be-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="617be-105">Syntax</span></span>


```C++
HRESULT LoadTextureFromFileAsync(
   BSTR                  fileName,
   BSTR                  histogramDataFileName,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="617be-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="617be-106">Parameters</span></span>

<span data-ttu-id="617be-107">*Extensión* </span><span class="sxs-lookup"><span data-stu-id="617be-107">*fileName* </span></span>  
<span data-ttu-id="617be-108">Cadena COM que contiene el nombre del archivo de textura.</span><span class="sxs-lookup"><span data-stu-id="617be-108">A COM string containing the name of the texture file.</span></span>

<span data-ttu-id="617be-109">*histogramDataFileName* </span><span class="sxs-lookup"><span data-stu-id="617be-109">*histogramDataFileName* </span></span>  
<span data-ttu-id="617be-110">Cadena COM que contiene el nombre del archivo de datos de histograma asociado a la textura.</span><span class="sxs-lookup"><span data-stu-id="617be-110">A COM string containing the name of the histogram data file associated with the texture.</span></span>

<span data-ttu-id="617be-111">*devoluciones* </span><span class="sxs-lookup"><span data-stu-id="617be-111">*callbacks* </span></span>  
<span data-ttu-id="617be-112">La dirección de un objeto que proporciona la interfaz de devoluciones de llamada IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="617be-112">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="617be-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="617be-113">*requestCookie* </span></span>  
<span data-ttu-id="617be-114">Una cookie que idenfies la solicitud de forma única y se puede usar para indicar que se cancele.</span><span class="sxs-lookup"><span data-stu-id="617be-114">A cookie that uniquely idenfies the request, and can be used to signal for it to be canceled.</span></span>

<span data-ttu-id="617be-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="617be-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="617be-116">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="617be-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="617be-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="617be-117">Return value</span></span>

<span data-ttu-id="617be-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="617be-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="617be-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="617be-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="617be-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="617be-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="617be-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="617be-121">Header</span></span></p></td><td><span data-ttu-id="617be-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="617be-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="617be-123"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="617be-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="617be-124">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="617be-124">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 

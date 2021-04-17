---
description: Representa una textura en un archivo y devuelve el resultado al host asynchrnously.
MS-HAID: vspixengine.IPixEngine5\_RenderTextureAsync\_UINT\_PixEngineTextureSliceIndex\_int\_float\_arr4\_float\_arr4\_BSTR\_UINT\_BSTR\_arr\_float\_arr\_UINT\_BSTR\_arr\_BOOL\_arr\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5:: RenderTextureAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd16214887514fa348a672c45d5eb85c2df6bca5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537294"
---
# <a name="span-idvspixengineipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5rendertextureasync-method"></a><span data-ttu-id="1bd02-103"><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5:: RenderTextureAsync (método)</span><span class="sxs-lookup"><span data-stu-id="1bd02-103"><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::RenderTextureAsync method</span></span>

<span data-ttu-id="1bd02-104">Representa una textura en un archivo y devuelve el resultado al host asynchrnously.</span><span class="sxs-lookup"><span data-stu-id="1bd02-104">Renders a texture to a file and returns the result to the host asynchrnously.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bd02-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1bd02-105">Syntax</span></span>


```C++
HRESULT RenderTextureAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   float [4]                  lower,
   float [4]                  upper,
   BSTR                       shaderFileName,
   UINT                       numFloatShaderVars,
   BSTR []                    count6_shaderFloatVarName,
   float []                   count6_shaderFloatVarValue,
   UINT                       numBoolShaderVars,
   BSTR []                    count9_shaderBoolVarName,
   BOOL []                    count9_shaderBoolVarValue,
   BSTR                       renderContentFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="1bd02-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1bd02-106">Parameters</span></span>

<span data-ttu-id="1bd02-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="1bd02-107">*textureId* </span></span>  
<span data-ttu-id="1bd02-108">IDENTIFICADOR de la textura que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="1bd02-108">The ID of the texture to render.</span></span>

<span data-ttu-id="1bd02-109">*sliceIndex* </span><span class="sxs-lookup"><span data-stu-id="1bd02-109">*sliceIndex* </span></span>  
<span data-ttu-id="1bd02-110">Índice del segmento dentro de la textura que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="1bd02-110">The index of the slice within the texture to render.</span></span>

<span data-ttu-id="1bd02-111">*formatOverride* </span><span class="sxs-lookup"><span data-stu-id="1bd02-111">*formatOverride* </span></span>  
<span data-ttu-id="1bd02-112">Invalidación del formato de color.</span><span class="sxs-lookup"><span data-stu-id="1bd02-112">The color format override.</span></span>

<span data-ttu-id="1bd02-113">*inferiores*</span><span class="sxs-lookup"><span data-stu-id="1bd02-113">*lower*</span></span>   

<span data-ttu-id="1bd02-114">*esquina superior*</span><span class="sxs-lookup"><span data-stu-id="1bd02-114">*upper*</span></span>   

<span data-ttu-id="1bd02-115">*shaderFileName* </span><span class="sxs-lookup"><span data-stu-id="1bd02-115">*shaderFileName* </span></span>  
<span data-ttu-id="1bd02-116">Cadena COM que contiene la ruta de acceso del archivo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1bd02-116">A COM string containing the pathname of the shader file.</span></span>

<span data-ttu-id="1bd02-117">*numFloatShaderVars* </span><span class="sxs-lookup"><span data-stu-id="1bd02-117">*numFloatShaderVars* </span></span>  
<span data-ttu-id="1bd02-118">El número de variables de sombreador de punto flotante</span><span class="sxs-lookup"><span data-stu-id="1bd02-118">The number of floating-point shader variables</span></span>

<span data-ttu-id="1bd02-119">*count6 \_ shaderFloatVarName* </span><span class="sxs-lookup"><span data-stu-id="1bd02-119">*count6\_shaderFloatVarName* </span></span>  
<span data-ttu-id="1bd02-120">Las cadenas COM contianing los nombres de las variables de sombreador de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="1bd02-120">COM strings contianing the names of the floating-point shader variables.</span></span>

<span data-ttu-id="1bd02-121">*count6 \_ shaderFloatVarValue* </span><span class="sxs-lookup"><span data-stu-id="1bd02-121">*count6\_shaderFloatVarValue* </span></span>  
<span data-ttu-id="1bd02-122">Variables de sombreador de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="1bd02-122">The floating-point shader variables.</span></span>

<span data-ttu-id="1bd02-123">*numBoolShaderVars* </span><span class="sxs-lookup"><span data-stu-id="1bd02-123">*numBoolShaderVars* </span></span>  
<span data-ttu-id="1bd02-124">El número de variables de sombreador booleanas.</span><span class="sxs-lookup"><span data-stu-id="1bd02-124">The number of boolean shader variables.</span></span>

<span data-ttu-id="1bd02-125">*count9 \_ shaderBoolVarName* </span><span class="sxs-lookup"><span data-stu-id="1bd02-125">*count9\_shaderBoolVarName* </span></span>  
<span data-ttu-id="1bd02-126">Las cadenas COM contianing los nombres de las variables de sombreador booleanos.</span><span class="sxs-lookup"><span data-stu-id="1bd02-126">COM strings contianing the names of the boolean shader variables.</span></span>

<span data-ttu-id="1bd02-127">*count9 \_ shaderBoolVarValue* </span><span class="sxs-lookup"><span data-stu-id="1bd02-127">*count9\_shaderBoolVarValue* </span></span>  
<span data-ttu-id="1bd02-128">Variables de sombreador booleanos.</span><span class="sxs-lookup"><span data-stu-id="1bd02-128">The boolean shader variables.</span></span>

<span data-ttu-id="1bd02-129">*renderContentFileName* </span><span class="sxs-lookup"><span data-stu-id="1bd02-129">*renderContentFileName* </span></span>  
<span data-ttu-id="1bd02-130">Cadena COM que contiene la ruta de acceso del archivo donde se escribió la textura representada.</span><span class="sxs-lookup"><span data-stu-id="1bd02-130">A COM string containing the pathname of the file where the rendered texture was written.</span></span>

<span data-ttu-id="1bd02-131">*devoluciones* </span><span class="sxs-lookup"><span data-stu-id="1bd02-131">*callbacks* </span></span>  
<span data-ttu-id="1bd02-132">La dirección de un objeto que proporciona la interfaz de devoluciones de llamada IPixEngine5.</span><span class="sxs-lookup"><span data-stu-id="1bd02-132">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="1bd02-133">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="1bd02-133">*requestCookie* </span></span>  
<span data-ttu-id="1bd02-134">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="1bd02-134">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="1bd02-135">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="1bd02-135">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="1bd02-136">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="1bd02-136">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="1bd02-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1bd02-137">Return value</span></span>

<span data-ttu-id="1bd02-138">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1bd02-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1bd02-139">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1bd02-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bd02-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bd02-140">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1bd02-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1bd02-141">Header</span></span></p></td><td><span data-ttu-id="1bd02-142">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="1bd02-142">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="1bd02-143"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="1bd02-143"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="1bd02-144">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="1bd02-144">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 

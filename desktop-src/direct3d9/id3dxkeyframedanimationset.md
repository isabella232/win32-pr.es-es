---
description: Una aplicación usa los métodos de esta interfaz para implementar un conjunto de animaciones de fotogramas clave.
ms.assetid: eeb7acd8-1017-4aca-9813-188fc6703837
title: Interfaz ID3DXKeyframedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0e45ab69b3a91461c947ce9c8a63885bb5ab0a8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698381"
---
# <a name="id3dxkeyframedanimationset-interface"></a><span data-ttu-id="02a81-103">Interfaz ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="02a81-103">ID3DXKeyframedAnimationSet interface</span></span>

<span data-ttu-id="02a81-104">Una aplicación usa los métodos de esta interfaz para implementar un conjunto de animaciones de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="02a81-104">An application uses the methods of this interface to implement a key frame animation set.</span></span>

## <a name="members"></a><span data-ttu-id="02a81-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="02a81-105">Members</span></span>

<span data-ttu-id="02a81-106">La interfaz **ID3DXKeyframedAnimationSet** hereda de [**ID3DXAnimationSet**](id3dxanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="02a81-106">The **ID3DXKeyframedAnimationSet** interface inherits from [**ID3DXAnimationSet**](id3dxanimationset.md).</span></span> <span data-ttu-id="02a81-107">**ID3DXKeyframedAnimationSet** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="02a81-107">**ID3DXKeyframedAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="02a81-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="02a81-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="02a81-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="02a81-109">Methods</span></span>

<span data-ttu-id="02a81-110">La interfaz **ID3DXKeyframedAnimationSet** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="02a81-110">The **ID3DXKeyframedAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="02a81-111">Método</span><span class="sxs-lookup"><span data-stu-id="02a81-111">Method</span></span>                                                                                   | <span data-ttu-id="02a81-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="02a81-112">Description</span></span>                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02a81-113">**Compress**</span><span class="sxs-lookup"><span data-stu-id="02a81-113">**Compress**</span></span>](id3dxkeyframedanimationset--compress.md)                                 | <span data-ttu-id="02a81-114">Transforma las animaciones de una animación establecida en un formato comprimido y devuelve un puntero al búfer que almacena los datos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="02a81-114">Transforms animations in an animation set into a compressed format and returns a pointer to the buffer that stores the compressed data.</span></span><br/> |
| [<span data-ttu-id="02a81-115">**GetCallbackKey**</span><span class="sxs-lookup"><span data-stu-id="02a81-115">**GetCallbackKey**</span></span>](id3dxkeyframedanimationset--getcallbackkey.md)                     | <span data-ttu-id="02a81-116">Obtiene información sobre una devolución de llamada específica en el conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="02a81-116">Gets information about a specific callback in the animation set.</span></span><br/>                                                                        |
| [<span data-ttu-id="02a81-117">**GetCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="02a81-117">**GetCallbackKeys**</span></span>](id3dxkeyframedanimationset--getcallbackkeys.md)                   | <span data-ttu-id="02a81-118">Rellena una matriz con los datos de clave de devolución de llamada utilizados para la animación de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="02a81-118">Fills an array with callback key data used for key frame animation.</span></span><br/>                                                                     |
| [<span data-ttu-id="02a81-119">**GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="02a81-119">**GetNumCallbackKeys**</span></span>](id3dxkeyframedanimationset--getnumcallbackkeys.md)             | <span data-ttu-id="02a81-120">Obtiene el número de claves de devolución de llamada del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="02a81-120">Gets the number of callback keys in the animation set.</span></span><br/>                                                                                  |
| [<span data-ttu-id="02a81-121">**GetNumRotationKeys**</span><span class="sxs-lookup"><span data-stu-id="02a81-121">**GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)             | <span data-ttu-id="02a81-122">Obtiene el número de claves de rotación en la animación de fotogramas clave especificada.</span><span class="sxs-lookup"><span data-stu-id="02a81-122">Gets the number of rotation keys in the specified key frame animation.</span></span><br/>                                                                  |
| [<span data-ttu-id="02a81-123">**GetNumScaleKeys**</span><span class="sxs-lookup"><span data-stu-id="02a81-123">**GetNumScaleKeys**</span></span>](id3dxkeyframedanimationset--getnumscalekeys.md)                   | <span data-ttu-id="02a81-124">Obtiene el número de claves de escala en la animación de fotogramas clave especificada.</span><span class="sxs-lookup"><span data-stu-id="02a81-124">Gets the number of scale keys in the specified key frame animation.</span></span><br/>                                                                     |
| [<span data-ttu-id="02a81-125">**GetNumTranslationKeys**</span><span class="sxs-lookup"><span data-stu-id="02a81-125">**GetNumTranslationKeys**</span></span>](id3dxkeyframedanimationset--getnumtranslationkeys.md)       | <span data-ttu-id="02a81-126">Obtiene el número de claves de traducción en la animación de fotogramas clave especificada.</span><span class="sxs-lookup"><span data-stu-id="02a81-126">Gets the number of translation keys in the specified key frame animation.</span></span><br/>                                                               |
| [<span data-ttu-id="02a81-127">**GetPlaybackType**</span><span class="sxs-lookup"><span data-stu-id="02a81-127">**GetPlaybackType**</span></span>](id3dxkeyframedanimationset--getplaybacktype.md)                   | <span data-ttu-id="02a81-128">Obtiene el tipo del bucle de reproducción establecido de la animación.</span><span class="sxs-lookup"><span data-stu-id="02a81-128">Gets the type of the animation set playback loop.</span></span><br/>                                                                                       |
| [<span data-ttu-id="02a81-129">**GetRotationKey**</span><span class="sxs-lookup"><span data-stu-id="02a81-129">**GetRotationKey**</span></span>](id3dxkeyframedanimationset--getrotationkey.md)                     | <span data-ttu-id="02a81-130">Obtiene la información de rotación de un fotograma clave específico en el conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="02a81-130">Get rotation information for a specific key frame in the animation set.</span></span><br/>                                                                 |
| [<span data-ttu-id="02a81-131">**GetRotationKeys**</span><span class="sxs-lookup"><span data-stu-id="02a81-131">**GetRotationKeys**</span></span>](id3dxkeyframedanimationset--getrotationkeys.md)                   | <span data-ttu-id="02a81-132">Rellena una matriz con datos de clave de rotación utilizados para la animación de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="02a81-132">Fills an array with rotational key data used for key frame animation.</span></span><br/>                                                                   |
| [<span data-ttu-id="02a81-133">**GetScaleKey**</span><span class="sxs-lookup"><span data-stu-id="02a81-133">**GetScaleKey**</span></span>](id3dxkeyframedanimationset--getscalekey.md)                           | <span data-ttu-id="02a81-134">Obtiene la información de escala de un fotograma clave específico en el conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="02a81-134">Get scale information for a specific key frame in the animation set.</span></span><br/>                                                                    |
| [<span data-ttu-id="02a81-135">**GetScaleKeys**</span><span class="sxs-lookup"><span data-stu-id="02a81-135">**GetScaleKeys**</span></span>](id3dxkeyframedanimationset--getscalekeys.md)                         | <span data-ttu-id="02a81-136">Rellena una matriz con los datos de clave de escala que se usan para la animación de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="02a81-136">Fills an array with scale key data used for key frame animation.</span></span><br/>                                                                        |
| [<span data-ttu-id="02a81-137">**GetSourceTicksPerSecond**</span><span class="sxs-lookup"><span data-stu-id="02a81-137">**GetSourceTicksPerSecond**</span></span>](id3dxkeyframedanimationset--getsourcetickspersecond.md)   | <span data-ttu-id="02a81-138">Obtiene el número de TICs de fotogramas clave de animación que se producen por segundo.</span><span class="sxs-lookup"><span data-stu-id="02a81-138">Gets the number of animation key frame ticks that occur per second.</span></span><br/>                                                                     |
| [<span data-ttu-id="02a81-139">**GetTranslationKey**</span><span class="sxs-lookup"><span data-stu-id="02a81-139">**GetTranslationKey**</span></span>](id3dxkeyframedanimationset--gettranslationkey.md)               | <span data-ttu-id="02a81-140">Obtiene la información de traducción de un fotograma clave específico en el conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="02a81-140">Get translation information for a specific key frame in the animation set.</span></span><br/>                                                              |
| [<span data-ttu-id="02a81-141">**GetTranslationKeys**</span><span class="sxs-lookup"><span data-stu-id="02a81-141">**GetTranslationKeys**</span></span>](id3dxkeyframedanimationset--gettranslationkeys.md)             | <span data-ttu-id="02a81-142">Rellena una matriz con datos de clave de traducción usados para la animación de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="02a81-142">Fills an array with translational key data used for key frame animation.</span></span><br/>                                                                |
| [<span data-ttu-id="02a81-143">**RegisterAnimationSRTKeys**</span><span class="sxs-lookup"><span data-stu-id="02a81-143">**RegisterAnimationSRTKeys**</span></span>](id3dxkeyframedanimationset--registeranimationsrtkeys.md) | <span data-ttu-id="02a81-144">Registre los datos del fotograma clave de escala, rotación y traducción (SRT) de una animación.</span><span class="sxs-lookup"><span data-stu-id="02a81-144">Register the scale, rotate, and translate (SRT) key frame data for an animation.</span></span><br/>                                                        |
| [<span data-ttu-id="02a81-145">**SetCallbackKey**</span><span class="sxs-lookup"><span data-stu-id="02a81-145">**SetCallbackKey**</span></span>](id3dxkeyframedanimationset--setcallbackkey.md)                     | <span data-ttu-id="02a81-146">Establece información sobre una devolución de llamada específica en el conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="02a81-146">Sets information about a specific callback in the animation set.</span></span><br/>                                                                        |
| [<span data-ttu-id="02a81-147">**SetRotationKey**</span><span class="sxs-lookup"><span data-stu-id="02a81-147">**SetRotationKey**</span></span>](id3dxkeyframedanimationset--setrotationkey.md)                     | <span data-ttu-id="02a81-148">Establezca la información de rotación de un fotograma clave específico en el conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="02a81-148">Set rotation information for a specific key frame in the animation set.</span></span><br/>                                                                 |
| [<span data-ttu-id="02a81-149">**SetScaleKey**</span><span class="sxs-lookup"><span data-stu-id="02a81-149">**SetScaleKey**</span></span>](id3dxkeyframedanimationset--setscalekey.md)                           | <span data-ttu-id="02a81-150">Establezca la información de escala para un fotograma clave específico en el conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="02a81-150">Set scale information for a specific key frame in the animation set.</span></span><br/>                                                                    |
| [<span data-ttu-id="02a81-151">**SetTranslationKey**</span><span class="sxs-lookup"><span data-stu-id="02a81-151">**SetTranslationKey**</span></span>](id3dxkeyframedanimationset--settranslationkey.md)               | <span data-ttu-id="02a81-152">Establezca la información de traducción de un fotograma clave específico en el conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="02a81-152">Set translation information for a specific key frame in the animation set.</span></span><br/>                                                              |
| [<span data-ttu-id="02a81-153">**UnregisterAnimation**</span><span class="sxs-lookup"><span data-stu-id="02a81-153">**UnregisterAnimation**</span></span>](id3dxkeyframedanimationset--unregisteranimation.md)           | <span data-ttu-id="02a81-154">Quitar los datos de animación del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="02a81-154">Remove the animation data from the animation set.</span></span><br/>                                                                                       |
| [<span data-ttu-id="02a81-155">**UnregisterRotationKey**</span><span class="sxs-lookup"><span data-stu-id="02a81-155">**UnregisterRotationKey**</span></span>](id3dxkeyframedanimationset--unregisterrotationkey.md)       | <span data-ttu-id="02a81-156">Quita los datos de rotación en el fotograma clave especificado.</span><span class="sxs-lookup"><span data-stu-id="02a81-156">Removes the rotation data at the specified key frame.</span></span><br/>                                                                                   |
| [<span data-ttu-id="02a81-157">**UnregisterScaleKey**</span><span class="sxs-lookup"><span data-stu-id="02a81-157">**UnregisterScaleKey**</span></span>](id3dxkeyframedanimationset--unregisterscalekey.md)             | <span data-ttu-id="02a81-158">Quita los datos de escala en el fotograma clave especificado.</span><span class="sxs-lookup"><span data-stu-id="02a81-158">Removes the scale data at the specified key frame.</span></span><br/>                                                                                      |
| [<span data-ttu-id="02a81-159">**UnregisterTranslationKey**</span><span class="sxs-lookup"><span data-stu-id="02a81-159">**UnregisterTranslationKey**</span></span>](id3dxkeyframedanimationset--unregistertranslationkey.md) | <span data-ttu-id="02a81-160">Quita los datos de traducción en el fotograma clave especificado.</span><span class="sxs-lookup"><span data-stu-id="02a81-160">Removes the translation data at the specified key frame.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="02a81-161">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02a81-161">Remarks</span></span>

<span data-ttu-id="02a81-162">Cree un conjunto de animaciones fotogramas clave con [**D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="02a81-162">Create a keyframed animation set with [**D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md).</span></span>

<span data-ttu-id="02a81-163">El tipo LPD3DXKEYFRAMEDANIMATIONSET se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="02a81-163">The LPD3DXKEYFRAMEDANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXKeyframedAnimationSet ID3DXKeyframedAnimationSet;
typedef interface ID3DXKeyframedAnimationSet *LPD3DXKEYFRAMEDANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="02a81-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02a81-164">Requirements</span></span>



| <span data-ttu-id="02a81-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="02a81-165">Requirement</span></span> | <span data-ttu-id="02a81-166">Value</span><span class="sxs-lookup"><span data-stu-id="02a81-166">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="02a81-167">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02a81-167">Header</span></span><br/>  | <dl> <span data-ttu-id="02a81-168"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="02a81-168"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="02a81-169">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="02a81-169">Library</span></span><br/> | <dl> <span data-ttu-id="02a81-170"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02a81-170"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="02a81-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="02a81-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02a81-172">**ID3DXAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="02a81-172">**ID3DXAnimationSet**</span></span>](id3dxanimationset.md)
</dt> <dt>

[<span data-ttu-id="02a81-173">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="02a81-173">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 





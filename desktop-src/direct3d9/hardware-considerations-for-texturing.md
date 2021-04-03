---
description: El hardware actual no implementa necesariamente toda la funcionalidad que la interfaz Direct3D habilita. La aplicación debe probar el hardware del usuario y ajustar sus estrategias de representación en consecuencia.
ms.assetid: 7b5f586c-616c-4351-b6b9-5c0179db5d8b
title: Consideraciones de hardware para la texturización (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f1ba8bea85cc3657478767aac7c7ffc2abebbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906292"
---
# <a name="hardware-considerations-for-texturing-direct3d-9"></a><span data-ttu-id="b9de5-104">Consideraciones de hardware para la texturización (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b9de5-104">Hardware Considerations for Texturing (Direct3D 9)</span></span>

<span data-ttu-id="b9de5-105">El hardware actual no implementa necesariamente toda la funcionalidad que la interfaz Direct3D habilita.</span><span class="sxs-lookup"><span data-stu-id="b9de5-105">Current hardware does not necessarily implement all the functionality that the Direct3D interface enables.</span></span> <span data-ttu-id="b9de5-106">La aplicación debe probar el hardware del usuario y ajustar sus estrategias de representación en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="b9de5-106">Your application must test user hardware and adjust its rendering strategies accordingly.</span></span>

<span data-ttu-id="b9de5-107">Muchas tarjetas aceleradoras 3D no admiten valores iterados difusos como argumentos para las unidades de mezcla.</span><span class="sxs-lookup"><span data-stu-id="b9de5-107">Many 3D accelerator cards do not support diffuse iterated values as arguments to blending units.</span></span> <span data-ttu-id="b9de5-108">Sin embargo, la aplicación puede introducir datos de color iterados cuando realiza la combinación de texturas.</span><span class="sxs-lookup"><span data-stu-id="b9de5-108">However, your application can introduce iterated color data when it performs texture blending.</span></span>

<span data-ttu-id="b9de5-109">Es posible que algún hardware 3D no tenga una fase de fusión asociada a la primera textura.</span><span class="sxs-lookup"><span data-stu-id="b9de5-109">Some 3D hardware may not have a blending stage associated with the first texture.</span></span> <span data-ttu-id="b9de5-110">En estos adaptadores, la aplicación debe realizar la combinación en la segunda y tercera fase de textura en el conjunto de texturas actuales.</span><span class="sxs-lookup"><span data-stu-id="b9de5-110">On these adapters, your application must perform blending in the second and third texture stages in the set of current textures.</span></span>

<span data-ttu-id="b9de5-111">Debido a las limitaciones de gran parte del hardware de hoy en día, algunos adaptadores de pantalla pueden realizar la interpolación de mipmap trilineal a través de la interfaz de combinación de texturas múltiple ofrecida por [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="b9de5-111">Because of limitations in much of today's hardware, few display adapters can perform trilinear mipmap interpolation through the multiple texture blending interface offered by [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span> <span data-ttu-id="b9de5-112">La aplicación puede utilizar la combinación de texturas de Multipass para lograr los mismos efectos, o bien degradarse al \_ modo de filtro MIP del punto de D3DTEXF, que es ampliamente compatible.</span><span class="sxs-lookup"><span data-stu-id="b9de5-112">Your application can use multipass texture blending to achieve the same effects, or degrade to the D3DTEXF\_POINT mipmap filter mode, which is widely supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9de5-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b9de5-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9de5-114">Texturas de Direct3D</span><span class="sxs-lookup"><span data-stu-id="b9de5-114">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 

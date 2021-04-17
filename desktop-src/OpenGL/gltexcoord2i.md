---
title: función glTexCoord2i (GL. h)
description: Establece las coordenadas de textura actuales. | función glTexCoord2i (GL. h)
ms.assetid: 7a5ff9a7-8dcd-47a0-868c-3909e011a592
keywords:
- glTexCoord2i (función) OpenGL
topic_type:
- apiref
api_name:
- glTexCoord2i
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa4d710f49d55e8aa0379bfc83f79f877d3cc906
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670193"
---
# <a name="gltexcoord2i-function"></a><span data-ttu-id="be7f6-105">glTexCoord2i función)</span><span class="sxs-lookup"><span data-stu-id="be7f6-105">glTexCoord2i function</span></span>

<span data-ttu-id="be7f6-106">Establece las coordenadas de textura actuales.</span><span class="sxs-lookup"><span data-stu-id="be7f6-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="be7f6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be7f6-107">Syntax</span></span>


```C++
void WINAPI glTexCoord2i(
   GLint s,
   GLint t
);
```



## <a name="parameters"></a><span data-ttu-id="be7f6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be7f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be7f6-109">*s*</span><span class="sxs-lookup"><span data-stu-id="be7f6-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="be7f6-110">Coordenada de textura s.</span><span class="sxs-lookup"><span data-stu-id="be7f6-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="be7f6-111">*t*</span><span class="sxs-lookup"><span data-stu-id="be7f6-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="be7f6-112">Coordenada de textura de t.</span><span class="sxs-lookup"><span data-stu-id="be7f6-112">The t texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be7f6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be7f6-113">Return value</span></span>

<span data-ttu-id="be7f6-114">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="be7f6-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be7f6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be7f6-115">Remarks</span></span>

<span data-ttu-id="be7f6-116">La función [**glTexCoord**](gltexcoord-functions.md) establece las coordenadas de textura actuales que forman parte de los datos asociados a los vértices del polígono.</span><span class="sxs-lookup"><span data-stu-id="be7f6-116">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="be7f6-117">La función **glTexCoord** especifica coordenadas de textura en una, dos, tres o cuatro dimensiones.</span><span class="sxs-lookup"><span data-stu-id="be7f6-117">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="be7f6-118">La función glTexCoord1 establece las coordenadas de textura actuales en (s, 0, 0, 1); una llamada a glTexCoord2 lo establece en (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="be7f6-118">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="be7f6-119">Del mismo modo, glTexCoord3 especifica las coordenadas de textura como (s, t, r, 1) y glTexCoord4 define los cuatro componentes explícitamente como (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="be7f6-119">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="be7f6-120">Puede actualizar las coordenadas de textura actuales en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="be7f6-120">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="be7f6-121">En concreto, puede llamar a glTexCoord entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="be7f6-121">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="be7f6-122">La siguiente función recupera información relacionada con **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="be7f6-122">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="be7f6-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento \_ coordenadas de \_ textura \_ actual de GL</span><span class="sxs-lookup"><span data-stu-id="be7f6-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="be7f6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be7f6-124">Requirements</span></span>



| <span data-ttu-id="be7f6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="be7f6-125">Requirement</span></span> | <span data-ttu-id="be7f6-126">Value</span><span class="sxs-lookup"><span data-stu-id="be7f6-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be7f6-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be7f6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="be7f6-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="be7f6-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="be7f6-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be7f6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="be7f6-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="be7f6-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="be7f6-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be7f6-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="be7f6-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="be7f6-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="be7f6-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be7f6-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="be7f6-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be7f6-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="be7f6-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="be7f6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be7f6-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be7f6-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be7f6-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="be7f6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be7f6-138">glVertex</span><span class="sxs-lookup"><span data-stu-id="be7f6-138">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 






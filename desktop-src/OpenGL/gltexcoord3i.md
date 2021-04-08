---
title: función glTexCoord3i (GL. h)
description: Establece las coordenadas de textura actuales. | función glTexCoord3i (GL. h)
ms.assetid: a153bbce-9f8c-48e1-a33a-a4474efe3ffd
keywords:
- glTexCoord3i (función) OpenGL
topic_type:
- apiref
api_name:
- glTexCoord3i
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 757921bc1a3298b31be9cbcd76263dc6aa98593d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003593"
---
# <a name="gltexcoord3i-function"></a><span data-ttu-id="4d863-105">glTexCoord3i función)</span><span class="sxs-lookup"><span data-stu-id="4d863-105">glTexCoord3i function</span></span>

<span data-ttu-id="4d863-106">Establece las coordenadas de textura actuales.</span><span class="sxs-lookup"><span data-stu-id="4d863-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d863-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d863-107">Syntax</span></span>


```C++
void WINAPI glTexCoord3i(
   GLint s,
   GLint t,
   GLint r
);
```



## <a name="parameters"></a><span data-ttu-id="4d863-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d863-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d863-109">*s*</span><span class="sxs-lookup"><span data-stu-id="4d863-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="4d863-110">Coordenada de textura s.</span><span class="sxs-lookup"><span data-stu-id="4d863-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="4d863-111">*t*</span><span class="sxs-lookup"><span data-stu-id="4d863-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="4d863-112">Coordenada de textura de t.</span><span class="sxs-lookup"><span data-stu-id="4d863-112">The t texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="4d863-113">*r*</span><span class="sxs-lookup"><span data-stu-id="4d863-113">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="4d863-114">Coordenada de textura de r.</span><span class="sxs-lookup"><span data-stu-id="4d863-114">The r texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d863-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d863-115">Return value</span></span>

<span data-ttu-id="4d863-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4d863-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d863-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d863-117">Remarks</span></span>

<span data-ttu-id="4d863-118">La función [**glTexCoord**](gltexcoord-functions.md) establece las coordenadas de textura actuales que forman parte de los datos asociados a los vértices del polígono.</span><span class="sxs-lookup"><span data-stu-id="4d863-118">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="4d863-119">La función **glTexCoord** especifica coordenadas de textura en una, dos, tres o cuatro dimensiones.</span><span class="sxs-lookup"><span data-stu-id="4d863-119">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="4d863-120">La función glTexCoord1 establece las coordenadas de textura actuales en (s, 0, 0, 1); una llamada a glTexCoord2 lo establece en (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="4d863-120">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="4d863-121">Del mismo modo, glTexCoord3 especifica las coordenadas de textura como (s, t, r, 1) y glTexCoord4 define los cuatro componentes explícitamente como (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="4d863-121">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="4d863-122">Puede actualizar las coordenadas de textura actuales en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="4d863-122">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="4d863-123">En concreto, puede llamar a glTexCoord entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="4d863-123">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="4d863-124">La siguiente función recupera información relacionada con **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="4d863-124">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="4d863-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento \_ coordenadas de \_ textura \_ actual de GL</span><span class="sxs-lookup"><span data-stu-id="4d863-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="4d863-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d863-126">Requirements</span></span>



| <span data-ttu-id="4d863-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d863-127">Requirement</span></span> | <span data-ttu-id="4d863-128">Value</span><span class="sxs-lookup"><span data-stu-id="4d863-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d863-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d863-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4d863-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4d863-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4d863-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d863-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4d863-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4d863-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4d863-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d863-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d863-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d863-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4d863-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4d863-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="4d863-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d863-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4d863-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4d863-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d863-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d863-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d863-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d863-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d863-140">glVertex</span><span class="sxs-lookup"><span data-stu-id="4d863-140">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 






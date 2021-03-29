---
title: función glTexCoord4i (GL. h)
description: Establece las coordenadas de textura actuales. | función glTexCoord4i (GL. h)
ms.assetid: b2b49102-5129-49cc-9043-22ba46fbf08f
keywords:
- glTexCoord4i (función) OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4i
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86ecdcddc7a62a2cce4adf595321c72dd877aa69
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678724"
---
# <a name="gltexcoord4i-function"></a><span data-ttu-id="07b47-105">glTexCoord4i función)</span><span class="sxs-lookup"><span data-stu-id="07b47-105">glTexCoord4i function</span></span>

<span data-ttu-id="07b47-106">Establece las coordenadas de textura actuales.</span><span class="sxs-lookup"><span data-stu-id="07b47-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="07b47-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07b47-107">Syntax</span></span>


```C++
void WINAPI glTexCoord4i(
   GLint s,
   GLint t,
   GLint r,
   GLint q
);
```



## <a name="parameters"></a><span data-ttu-id="07b47-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07b47-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07b47-109">*s*</span><span class="sxs-lookup"><span data-stu-id="07b47-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="07b47-110">Coordenada de textura s.</span><span class="sxs-lookup"><span data-stu-id="07b47-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="07b47-111">*t*</span><span class="sxs-lookup"><span data-stu-id="07b47-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="07b47-112">Coordenada de textura de t.</span><span class="sxs-lookup"><span data-stu-id="07b47-112">The t texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="07b47-113">*r*</span><span class="sxs-lookup"><span data-stu-id="07b47-113">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="07b47-114">Coordenada de textura de r.</span><span class="sxs-lookup"><span data-stu-id="07b47-114">The r texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="07b47-115">*respuestas*</span><span class="sxs-lookup"><span data-stu-id="07b47-115">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="07b47-116">Coordenada de textura q.</span><span class="sxs-lookup"><span data-stu-id="07b47-116">The q texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07b47-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07b47-117">Return value</span></span>

<span data-ttu-id="07b47-118">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="07b47-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="07b47-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07b47-119">Remarks</span></span>

<span data-ttu-id="07b47-120">La función [**glTexCoord**](gltexcoord-functions.md) establece las coordenadas de textura actuales que forman parte de los datos asociados a los vértices del polígono.</span><span class="sxs-lookup"><span data-stu-id="07b47-120">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="07b47-121">La función **glTexCoord** especifica coordenadas de textura en una, dos, tres o cuatro dimensiones.</span><span class="sxs-lookup"><span data-stu-id="07b47-121">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="07b47-122">La función glTexCoord1 establece las coordenadas de textura actuales en (s, 0, 0, 1); una llamada a glTexCoord2 lo establece en (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="07b47-122">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="07b47-123">Del mismo modo, glTexCoord3 especifica las coordenadas de textura como (s, t, r, 1) y glTexCoord4 define los cuatro componentes explícitamente como (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="07b47-123">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="07b47-124">Puede actualizar las coordenadas de textura actuales en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="07b47-124">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="07b47-125">En concreto, puede llamar a glTexCoord entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="07b47-125">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="07b47-126">La siguiente función recupera información relacionada con **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="07b47-126">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="07b47-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento \_ coordenadas de \_ textura \_ actual de GL</span><span class="sxs-lookup"><span data-stu-id="07b47-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="07b47-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07b47-128">Requirements</span></span>



| <span data-ttu-id="07b47-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="07b47-129">Requirement</span></span> | <span data-ttu-id="07b47-130">Value</span><span class="sxs-lookup"><span data-stu-id="07b47-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07b47-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07b47-131">Minimum supported client</span></span><br/> | <span data-ttu-id="07b47-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="07b47-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="07b47-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07b47-133">Minimum supported server</span></span><br/> | <span data-ttu-id="07b47-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="07b47-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="07b47-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07b47-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="07b47-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="07b47-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="07b47-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="07b47-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="07b47-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07b47-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="07b47-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="07b47-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07b47-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07b47-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07b47-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="07b47-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07b47-142">glVertex</span><span class="sxs-lookup"><span data-stu-id="07b47-142">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 






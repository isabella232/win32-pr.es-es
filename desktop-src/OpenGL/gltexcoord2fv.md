---
title: función glTexCoord2fv (GL. h)
description: Establece las coordenadas de textura actuales. | función glTexCoord2fv (GL. h)
ms.assetid: ee7976ae-cea8-4116-8810-20d0995ff569
keywords:
- glTexCoord2fv (función) OpenGL
topic_type:
- apiref
api_name:
- glTexCoord2fv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88138a18627f90d8752c37335f1d3f611ce41ec6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689817"
---
# <a name="gltexcoord2fv-function"></a><span data-ttu-id="f2d9a-105">glTexCoord2fv función)</span><span class="sxs-lookup"><span data-stu-id="f2d9a-105">glTexCoord2fv function</span></span>

<span data-ttu-id="f2d9a-106">Establece las coordenadas de textura actuales.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2d9a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2d9a-107">Syntax</span></span>


```C++
void WINAPI glTexCoord2fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="f2d9a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2d9a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2d9a-109">*v*</span><span class="sxs-lookup"><span data-stu-id="f2d9a-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="f2d9a-110">Puntero a una matriz de dos elementos, que A su vez especifica las coordenadas de textura s y t.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-110">A pointer to an array of two elements, which in turn specifies the s and t texture coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2d9a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2d9a-111">Return value</span></span>

<span data-ttu-id="f2d9a-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2d9a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2d9a-113">Remarks</span></span>

<span data-ttu-id="f2d9a-114">La función [**glTexCoord**](gltexcoord-functions.md) establece las coordenadas de textura actuales que forman parte de los datos asociados a los vértices del polígono.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-114">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="f2d9a-115">La función **glTexCoord** especifica coordenadas de textura en una, dos, tres o cuatro dimensiones.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-115">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="f2d9a-116">La función glTexCoord1 establece las coordenadas de textura actuales en (s, 0, 0, 1); una llamada a glTexCoord2 lo establece en (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="f2d9a-116">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="f2d9a-117">Del mismo modo, glTexCoord3 especifica las coordenadas de textura como (s, t, r, 1) y glTexCoord4 define los cuatro componentes explícitamente como (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="f2d9a-117">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="f2d9a-118">Puede actualizar las coordenadas de textura actuales en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="f2d9a-118">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="f2d9a-119">En concreto, puede llamar a glTexCoord entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="f2d9a-119">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="f2d9a-120">La siguiente función recupera información relacionada con **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="f2d9a-120">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="f2d9a-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento \_ coordenadas de \_ textura \_ actual de GL</span><span class="sxs-lookup"><span data-stu-id="f2d9a-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="f2d9a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2d9a-122">Requirements</span></span>



| <span data-ttu-id="f2d9a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2d9a-123">Requirement</span></span> | <span data-ttu-id="f2d9a-124">Value</span><span class="sxs-lookup"><span data-stu-id="f2d9a-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2d9a-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2d9a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f2d9a-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f2d9a-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f2d9a-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2d9a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f2d9a-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f2d9a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f2d9a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2d9a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2d9a-130"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2d9a-130"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f2d9a-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f2d9a-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2d9a-132"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2d9a-132"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f2d9a-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f2d9a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2d9a-134"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2d9a-134"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2d9a-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2d9a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2d9a-136">glVertex</span><span class="sxs-lookup"><span data-stu-id="f2d9a-136">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 






---
description: Describe las definiciones de preprocesador usadas por un objeto Effect.
ms.assetid: 43413b79-e331-4466-b288-bd4439c135a2
title: Estructura D3DXMACRO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMACRO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 7fd6c52b94c3fb6f36c9b3a8e2b4b513fb8903f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708010"
---
# <a name="d3dxmacro-structure"></a><span data-ttu-id="499e0-103">Estructura D3DXMACRO</span><span class="sxs-lookup"><span data-stu-id="499e0-103">D3DXMACRO structure</span></span>

<span data-ttu-id="499e0-104">Describe las definiciones de preprocesador usadas por un objeto Effect.</span><span class="sxs-lookup"><span data-stu-id="499e0-104">Describes preprocessor definitions used by an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="499e0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="499e0-105">Syntax</span></span>


```C++
typedef struct D3DXMACRO {
  LPCSTR Name;
  LPCSTR Definition;
} D3DXMACRO, *LPD3DXMACRO;
```



## <a name="members"></a><span data-ttu-id="499e0-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="499e0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="499e0-107">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="499e0-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="499e0-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="499e0-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="499e0-109">Nombre del preprocesador.</span><span class="sxs-lookup"><span data-stu-id="499e0-109">Preprocessor name.</span></span>

</dd> <dt>

<span data-ttu-id="499e0-110">**Definición**</span><span class="sxs-lookup"><span data-stu-id="499e0-110">**Definition**</span></span>
</dt> <dd>

<span data-ttu-id="499e0-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="499e0-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="499e0-112">Nombre de definición.</span><span class="sxs-lookup"><span data-stu-id="499e0-112">Definition name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="499e0-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="499e0-113">Remarks</span></span>

<span data-ttu-id="499e0-114">Para usar **D3DXMACRO** s en más de una línea, Prefije cada carácter de línea nueva con una barra diagonal inversa (como una \# definición en el lenguaje C).</span><span class="sxs-lookup"><span data-stu-id="499e0-114">To use **D3DXMACRO** s in more than one line, prefix each new line character with a backslash (like a \#define in the C language).</span></span> <span data-ttu-id="499e0-115">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="499e0-115">For example:</span></span>


```
sample=
macro.Name = "DO_CODE_BLOCK";
macro.Definition =
    "/* here is a block of code */\\\n"
    "{ do something ... }\\\n";
```



<span data-ttu-id="499e0-116">Observe los tres caracteres de barra diagonal inversa al final de la línea.</span><span class="sxs-lookup"><span data-stu-id="499e0-116">Notice the 3 backslash characters at the end of the line.</span></span> <span data-ttu-id="499e0-117">Los dos primeros son necesarios para generar un solo ' \\ ', seguido del carácter de nueva línea ' \\ n '.</span><span class="sxs-lookup"><span data-stu-id="499e0-117">The first two are required to output a single '\\', followed by the newline character "\\n".</span></span> <span data-ttu-id="499e0-118">Opcionalmente, puede que también desee terminar las líneas con " \\ \\ \\ r \\ n".</span><span class="sxs-lookup"><span data-stu-id="499e0-118">Optionally, you may also want to terminate your lines using "\\\\\\r\\n".</span></span>

## <a name="requirements"></a><span data-ttu-id="499e0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="499e0-119">Requirements</span></span>



| <span data-ttu-id="499e0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="499e0-120">Requirement</span></span> | <span data-ttu-id="499e0-121">Value</span><span class="sxs-lookup"><span data-stu-id="499e0-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="499e0-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="499e0-122">Header</span></span><br/> | <dl> <span data-ttu-id="499e0-123"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="499e0-123"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="499e0-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="499e0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="499e0-125">Estructuras de efectos</span><span class="sxs-lookup"><span data-stu-id="499e0-125">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[<span data-ttu-id="499e0-126">**D3DXCreateEffectFromFile**</span><span class="sxs-lookup"><span data-stu-id="499e0-126">**D3DXCreateEffectFromFile**</span></span>](d3dxcreateeffectfromfile.md)
</dt> </dl>

 

 

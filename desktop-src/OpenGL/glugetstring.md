---
title: función gluGetString (GLU. h)
description: La función gluGetString obtiene una cadena que describe el número de versión GLU o las llamadas de extensión GLU compatibles.
ms.assetid: e6d9ce03-3218-4145-8bb5-3989afe62436
keywords:
- gluGetString (función) OpenGL
topic_type:
- apiref
api_name:
- gluGetString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574ed93c9c6f8d1f964e38ee14541d57bd5c34da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422214"
---
# <a name="glugetstring-function"></a><span data-ttu-id="d6f56-104">gluGetString función)</span><span class="sxs-lookup"><span data-stu-id="d6f56-104">gluGetString function</span></span>

<span data-ttu-id="d6f56-105">La función **gluGetString** obtiene una cadena que describe el número de versión Glu o las llamadas de extensión Glu compatibles.</span><span class="sxs-lookup"><span data-stu-id="d6f56-105">The **gluGetString** function gets a string that describes the GLU version number or supported GLU extension calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6f56-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6f56-106">Syntax</span></span>


```C++
const GLubyte* WINAPI gluGetString(
   GLenum name
);
```



## <a name="parameters"></a><span data-ttu-id="d6f56-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6f56-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6f56-108">*name*</span><span class="sxs-lookup"><span data-stu-id="d6f56-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="d6f56-109">El número de versión de GLU (versión de GLU \_ ) o las llamadas de extensión específicas del proveedor disponibles (extensiones de Glu \_ ).</span><span class="sxs-lookup"><span data-stu-id="d6f56-109">Either the version number of GLU (GLU\_VERSION) or available vendor-specific extension calls (GLU\_EXTENSIONS).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6f56-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d6f56-110">Remarks</span></span>

<span data-ttu-id="d6f56-111">La función **gluGetString** devuelve un puntero a una cadena estática terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="d6f56-111">The **gluGetString** function returns a pointer to a static, null-terminated string.</span></span> <span data-ttu-id="d6f56-112">Cuando el *nombre* es Glu \_ version, la cadena devuelta es un valor que representa el número de versión de Glu.</span><span class="sxs-lookup"><span data-stu-id="d6f56-112">When *name* is GLU\_VERSION, the returned string is a value that represents the version number of GLU.</span></span> <span data-ttu-id="d6f56-113">El formato del número de versión es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="d6f56-113">The format of the version number is as follows:</span></span>

``` syntax
<version number><space><vendor-specific information> 
(for example, "1.2.11 Microsoft Windows")
```

<span data-ttu-id="d6f56-114">El número de versión tiene el formato " \_ número principal. \_ número secundario" o " \_ número principal. \_ número secundario. número de versión \_ ".</span><span class="sxs-lookup"><span data-stu-id="d6f56-114">The version number has the form "major\_number.minor\_number" or "major\_number.minor\_number.release\_number".</span></span> <span data-ttu-id="d6f56-115">La información específica del proveedor es opcional y el formato y el contenido dependen de la implementación.</span><span class="sxs-lookup"><span data-stu-id="d6f56-115">The vendor-specific information is optional, and the format and contents depend on the implementation.</span></span>

<span data-ttu-id="d6f56-116">Cuando *Name* es Glu \_ extensions, la cadena devuelta contiene una lista de nombres de las extensiones de Glu admitidas que están separadas por espacios.</span><span class="sxs-lookup"><span data-stu-id="d6f56-116">When *name* is GLU\_EXTENSIONS, the returned string contains a list of names of supported GLU extensions that are separated by spaces.</span></span> <span data-ttu-id="d6f56-117">El formato de la lista de nombres devuelto es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="d6f56-117">The format of the returned list of names is as follows:</span></span>

``` syntax
<extension_name><space><extension_name><space> . . .
(for example, "GLU_NURBS GL_TESSELATION")
```

<span data-ttu-id="d6f56-118">Los nombres de extensión no pueden contener espacios.</span><span class="sxs-lookup"><span data-stu-id="d6f56-118">The extension names cannot contain any spaces.</span></span>

<span data-ttu-id="d6f56-119">La función **gluGetString** es válida para la versión 1,1 de Glu o posterior.</span><span class="sxs-lookup"><span data-stu-id="d6f56-119">The **gluGetString** function is valid for GLU version 1.1 or later.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6f56-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6f56-120">Requirements</span></span>



| <span data-ttu-id="d6f56-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6f56-121">Requirement</span></span> | <span data-ttu-id="d6f56-122">Value</span><span class="sxs-lookup"><span data-stu-id="d6f56-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f56-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6f56-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d6f56-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d6f56-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d6f56-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6f56-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d6f56-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d6f56-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d6f56-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6f56-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6f56-128"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6f56-128"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="d6f56-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d6f56-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="d6f56-130"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6f56-130"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d6f56-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d6f56-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6f56-132"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6f56-132"><dt>Glu32.dll</dt></span></span> </dl> |



 

 






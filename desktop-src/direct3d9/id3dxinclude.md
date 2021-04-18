---
description: ID3DXInclude es una interfaz implementada por el usuario para proporcionar devoluciones de llamada para las \# directivas de inclusión durante la compilación del sombreador.
ms.assetid: 8e0bfff1-8d6d-4381-b9fd-f5f64f854712
title: Interfaz ID3DXInclude (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d4b0a34eb5b4c3ab20a57a5089de1d6d1ebbdf51
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708079"
---
# <a name="id3dxinclude-interface"></a><span data-ttu-id="fb0e7-103">Interfaz ID3DXInclude</span><span class="sxs-lookup"><span data-stu-id="fb0e7-103">ID3DXInclude interface</span></span>

<span data-ttu-id="fb0e7-104">ID3DXInclude es una interfaz implementada por el usuario para proporcionar devoluciones de llamada para las \# directivas de inclusión durante la compilación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="fb0e7-104">ID3DXInclude is a user-implemented interface to provide callbacks for \#include directives during shader compilation.</span></span> <span data-ttu-id="fb0e7-105">Cada uno de los métodos de esta interfaz debe ser implementado por el usuario, que se utilizará como devoluciones de llamada para la aplicación cuando se produzca uno de los siguientes casos:</span><span class="sxs-lookup"><span data-stu-id="fb0e7-105">Each of the methods in this interface must be implemented by the user which will then be used as callbacks to the application when one of the following occurs:</span></span>

-   <span data-ttu-id="fb0e7-106">Un sombreador HLSL que contiene un \# include se compila mediante una llamada a una de las funciones de D3DXCompileShader \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="fb0e7-106">An HLSL shader that contains a \#include is compiled by calling one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="fb0e7-107">Un sombreador de ensamblado \# incluye el ensamblado llamando a cualquiera de las funciones de D3DXAssembleShader \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="fb0e7-107">An assembly shader \#include is assembled by calling any of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="fb0e7-108">Un efecto que contiene un \# include se compila mediante una llamada a cualquiera de las \* \* \* funciones D3DXCreateEffect o D3DXCreateEffectCompiler \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="fb0e7-108">An effect that contains a \#include is compiled by by calling any of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="members"></a><span data-ttu-id="fb0e7-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="fb0e7-109">Members</span></span>

<span data-ttu-id="fb0e7-110">La interfaz **ID3DXInclude** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fb0e7-110">The **ID3DXInclude** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fb0e7-111">**ID3DXInclude** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fb0e7-111">**ID3DXInclude** also has these types of members:</span></span>

-   [<span data-ttu-id="fb0e7-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="fb0e7-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fb0e7-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="fb0e7-113">Methods</span></span>

<span data-ttu-id="fb0e7-114">La interfaz **ID3DXInclude** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fb0e7-114">The **ID3DXInclude** interface has these methods.</span></span>



| <span data-ttu-id="fb0e7-115">Método</span><span class="sxs-lookup"><span data-stu-id="fb0e7-115">Method</span></span>                               | <span data-ttu-id="fb0e7-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb0e7-116">Description</span></span>                                                                                           |
|:-------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb0e7-117">**Cercanos**</span><span class="sxs-lookup"><span data-stu-id="fb0e7-117">**Close**</span></span>](id3dxinclude--close.md) | <span data-ttu-id="fb0e7-118">Método implementado por el usuario para cerrar un archivo de inclusión de sombreador \# .</span><span class="sxs-lookup"><span data-stu-id="fb0e7-118">A user-implemented method for closing a shader \#include file.</span></span><br/>                             |
| [<span data-ttu-id="fb0e7-119">**Ábra**</span><span class="sxs-lookup"><span data-stu-id="fb0e7-119">**Open**</span></span>](id3dxinclude--open.md)   | <span data-ttu-id="fb0e7-120">Método implementado por el usuario para abrir y leer el contenido de un archivo de inclusión de sombreador \# .</span><span class="sxs-lookup"><span data-stu-id="fb0e7-120">A user-implemented method for opening and reading the contents of a shader \#include file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fb0e7-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb0e7-121">Remarks</span></span>

<span data-ttu-id="fb0e7-122">Un usuario crea una interfaz ID3DXInclude implementando una clase que deriva de esta interfaz e implementando todos los métodos de interfaz.</span><span class="sxs-lookup"><span data-stu-id="fb0e7-122">A user creates an ID3DXInclude interface by implementing a class that derives from this interface, and implementing all the interface methods.</span></span>

<span data-ttu-id="fb0e7-123">El tipo LPD3DXINCLUDE se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="fb0e7-123">The LPD3DXINCLUDE type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXInclude ID3DXInclude;
typedef interface ID3DXInclude *LPD3DXINCLUDE;
```



## <a name="requirements"></a><span data-ttu-id="fb0e7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb0e7-124">Requirements</span></span>



| <span data-ttu-id="fb0e7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb0e7-125">Requirement</span></span> | <span data-ttu-id="fb0e7-126">Value</span><span class="sxs-lookup"><span data-stu-id="fb0e7-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb0e7-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb0e7-127">Header</span></span><br/>  | <dl> <span data-ttu-id="fb0e7-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb0e7-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fb0e7-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb0e7-129">Library</span></span><br/> | <dl> <span data-ttu-id="fb0e7-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb0e7-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fb0e7-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb0e7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb0e7-132">Interfaces de efectos</span><span class="sxs-lookup"><span data-stu-id="fb0e7-132">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 

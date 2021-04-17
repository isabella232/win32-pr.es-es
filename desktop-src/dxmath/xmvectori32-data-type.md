---
description: Un tipo opaco y portátil para admitir el uso de la sintaxis de inicializador de C/C++ para cargar valores enteros en una instancia de tipo XMVECTOR.
ms.assetid: 6564030e-b6e9-0c4f-4e2a-4132e4264c94
title: Tipo de datos XMVECTORI32 (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ac36caf97a62037223840e9220876f1c7a1f09a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650181"
---
# <a name="xmvectori32-data-type"></a><span data-ttu-id="0a231-103">XMVECTORI32, tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0a231-103">XMVECTORI32 Data Type</span></span>

<span data-ttu-id="0a231-104">Un tipo opaco y portátil para admitir el uso de la sintaxis de inicializador de C/C++ para cargar valores enteros en una instancia de tipo [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="0a231-104">An opaque, portable type to support the use of C/C++ initializer syntax to load integer values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTORI32 vectori32;
```



## <a name="remarks"></a><span data-ttu-id="0a231-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a231-105">Remarks</span></span>

<span data-ttu-id="0a231-106">Para obtener una lista de funcionalidad adicional, como constructores y operadores, disponible `XMVECTORI32` al programar en C++, vea [extensiones de XMVECTORI32](ovw-xmvectori32-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="0a231-106">For a list of additional functionality, such as constructors and operators, available using `XMVECTORI32` when programming in C++, see [XMVECTORI32 Extensions](ovw-xmvectori32-extensions.md).</span></span>

<span data-ttu-id="0a231-107">Las estructuras [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), **XMVECTORI32** y [**XMVECTORU8**](xmvectoru8-data-type.md) se proporcionan como un mecanismo para crear [**XMVECTOR**](xmvector-data-type.md) de diferentes tipos de datos constantes (punto flotante, entero sin signo, entero y byte) mediante inicializadores.</span><span class="sxs-lookup"><span data-stu-id="0a231-107">The [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), **XMVECTORI32**, and [**XMVECTORU8**](xmvectoru8-data-type.md) structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="0a231-108">Esto es necesario para admitir [**XMVECTOR**](xmvector-data-type.md), ya que no admite inicializadores, por motivos de portabilidad y optimización.</span><span class="sxs-lookup"><span data-stu-id="0a231-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="0a231-109">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0a231-109">For example:</span></span>


```
XMVECTOR data;
XMVECTORI32 intVector = { -1, 5, 33, 0 };
data = intVector;
```



<span data-ttu-id="0a231-110">**Espacio de nombres**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="0a231-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="0a231-111">Requisitos de la plataforma</span><span class="sxs-lookup"><span data-stu-id="0a231-111">Platform Requirements</span></span>

<span data-ttu-id="0a231-112">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el Windows SDK para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0a231-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="0a231-113">Se admite para aplicaciones de escritorio de Win32, aplicaciones de la tienda Windows y Windows Phone 8 aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="0a231-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a231-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a231-114">Requirements</span></span>



| <span data-ttu-id="0a231-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a231-115">Requirement</span></span> | <span data-ttu-id="0a231-116">Value</span><span class="sxs-lookup"><span data-stu-id="0a231-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a231-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a231-117">Header</span></span><br/> | <dl> <span data-ttu-id="0a231-118"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a231-118"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a231-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a231-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a231-120">Tipos de biblioteca de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="0a231-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="0a231-121">**XMVECTOR, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="0a231-121">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="0a231-122">**XMVECTORF32, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="0a231-122">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="0a231-123">**XMVECTORU32, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="0a231-123">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="0a231-124">**XMVECTORU8, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="0a231-124">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="0a231-125">**XMVECTORI32, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="0a231-125">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> </dl>

 

 





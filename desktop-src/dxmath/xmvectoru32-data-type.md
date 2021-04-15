---
description: Un tipo opaco y portátil para admitir el uso de la sintaxis de inicializador de C/C++ para cargar \_ valores UInt32 t en una instancia de tipo XMVECTOR.
ms.assetid: 1ac1f48a-cd7f-7741-933f-c341fc42a21c
title: Tipo de datos XMVECTORU32 (Directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90c7a64d42bc4638573b987642c0cd77c37cc12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708958"
---
# <a name="xmvectoru32-data-type"></a><span data-ttu-id="0c22a-103">XMVECTORU32, tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0c22a-103">XMVECTORU32 Data Type</span></span>

<span data-ttu-id="0c22a-104">Un tipo opaco y portátil para admitir el uso de la sintaxis de inicializador de C/C++ para cargar \_ valores UInt32 t en una instancia de tipo [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="0c22a-104">An opaque, portable type to support the use of C/C++ initializer syntax to load uint32\_t values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTOR32 vectoru32;
```



## <a name="remarks"></a><span data-ttu-id="0c22a-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c22a-105">Remarks</span></span>

<span data-ttu-id="0c22a-106">Para obtener una lista de funcionalidad adicional, como constructores y operadores, disponible mediante XMVECTORU32 al programar en C++, vea [extensiones de XMVECTORU32](ovw-xmvectoru32-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="0c22a-106">For a list of additional functionality, such as constructors and operators, available using XMVECTORU32 when programming in C++, see [XMVECTORU32 Extensions](ovw-xmvectoru32-extensions.md).</span></span>

<span data-ttu-id="0c22a-107">Las estructuras [**XMVECTORF32**](xmvectorf32-data-type.md), **XMVECTORU32**, [**XMVECTORI32**](xmvectori32-data-type.md)y [**XMVECTORU8**](xmvectoru8-data-type.md) se proporcionan como un mecanismo para crear [**XMVECTOR**](xmvector-data-type.md) de diferentes tipos de datos constantes (punto flotante, entero sin signo, entero y byte) mediante inicializadores.</span><span class="sxs-lookup"><span data-stu-id="0c22a-107">The [**XMVECTORF32**](xmvectorf32-data-type.md), **XMVECTORU32**, [**XMVECTORI32**](xmvectori32-data-type.md), and [**XMVECTORU8**](xmvectoru8-data-type.md) structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="0c22a-108">Esto es necesario para admitir [**XMVECTOR**](xmvector-data-type.md), ya que no admite inicializadores, por motivos de portabilidad y optimización.</span><span class="sxs-lookup"><span data-stu-id="0c22a-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="0c22a-109">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0c22a-109">For example:</span></span>

``` syntax
XMVECTOR data;
XMVECTORU32 uintVector = { 0xf7000000, 0x8310000, 0x1000000, 0 };
data = uintVector;
```

<span data-ttu-id="0c22a-110">**Espacio de nombres**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="0c22a-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="0c22a-111">Requisitos de la plataforma</span><span class="sxs-lookup"><span data-stu-id="0c22a-111">Platform Requirements</span></span>

<span data-ttu-id="0c22a-112">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el Windows SDK para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0c22a-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="0c22a-113">Se admite para aplicaciones de escritorio de Win32, aplicaciones de la tienda Windows y Windows Phone 8 aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="0c22a-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c22a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c22a-114">Requirements</span></span>



| <span data-ttu-id="0c22a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c22a-115">Requirement</span></span> | <span data-ttu-id="0c22a-116">Value</span><span class="sxs-lookup"><span data-stu-id="0c22a-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c22a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c22a-117">Header</span></span><br/> | <dl> <span data-ttu-id="0c22a-118"><dt>Directxmath. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c22a-118"><dt>Directxmath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c22a-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c22a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c22a-120">Tipos de biblioteca de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="0c22a-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="0c22a-121">**XMVECTORI32, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="0c22a-121">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="0c22a-122">**XMVECTORF32, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="0c22a-122">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="0c22a-123">**XMVECTOR, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="0c22a-123">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="0c22a-124">**XMVECTORU8, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="0c22a-124">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="0c22a-125">Extensiones de XMVECTORU32</span><span class="sxs-lookup"><span data-stu-id="0c22a-125">XMVECTORU32 Extensions</span></span>](ovw-xmvectoru32-extensions.md)
</dt> </dl>

 

 





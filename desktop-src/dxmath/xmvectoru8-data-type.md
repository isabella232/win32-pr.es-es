---
description: Un tipo opaco y portátil para admitir el uso de la sintaxis de inicializador de C/C++ para cargar \_ valores de Uint8 t en una instancia de tipo XMVECTOR.
ms.assetid: ab73ac2c-f178-1bb9-910d-9eef5fc6f5df
title: Tipo de datos XMVECTORU8 (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4428cdd78206bfa17c295a9578653bb0a66f0c6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708199"
---
# <a name="xmvectoru8-data-type"></a><span data-ttu-id="4fbb2-103">XMVECTORU8, tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4fbb2-103">XMVECTORU8 Data Type</span></span>

<span data-ttu-id="4fbb2-104">Un tipo opaco y portátil para admitir el uso de la sintaxis de inicializador de C/C++ para cargar \_ valores de Uint8 t en una instancia de tipo [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="4fbb2-104">An opaque, portable type to support the use of C/C++ initializer syntax to load uint8\_t values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTORU8 vectoru8;
```



## <a name="remarks"></a><span data-ttu-id="4fbb2-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4fbb2-105">Remarks</span></span>

<span data-ttu-id="4fbb2-106">Para obtener una lista de funcionalidad adicional, como constructores y operadores, disponible mediante XMVECTORU8 al programar en C++, vea [extensiones de XMVECTORU8](ovw-xmvectoru8-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="4fbb2-106">For a list of additional functionality, such as constructors and operators, available using XMVECTORU8 when programming in C++, see [XMVECTORU8 Extensions](ovw-xmvectoru8-extensions.md).</span></span>

<span data-ttu-id="4fbb2-107">Las estructuras [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md)y **XMVECTORU8** se proporcionan como un mecanismo para crear [**XMVECTOR**](xmvector-data-type.md) de diferentes tipos de datos constantes (punto flotante, entero sin signo, entero y byte) mediante inicializadores.</span><span class="sxs-lookup"><span data-stu-id="4fbb2-107">The [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md), and **XMVECTORU8** structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="4fbb2-108">Esto es necesario para admitir [**XMVECTOR**](xmvector-data-type.md), ya que no admite inicializadores, por motivos de portabilidad y optimización.</span><span class="sxs-lookup"><span data-stu-id="4fbb2-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="4fbb2-109">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="4fbb2-109">For example:</span></span>

``` syntax
XMVECTOR data;
XMVECTORU8  byteVector = { (uint8_t)  1,(uint8_t) 16,(uint8_t)101,(uint8_t) 62,
                           (uint8_t)  4,(uint8_t)  0,(uint8_t)  2,(uint8_t) 99,
                           (uint8_t)  9,(uint8_t) 18,(uint8_t)  0,(uint8_t)  0,
                           (uint8_t)100,(uint8_t) 51,(uint8_t) 23,(uint8_t)117};

data = floatingVector;
```

<span data-ttu-id="4fbb2-110">**Espacio de nombres**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="4fbb2-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="4fbb2-111">Requisitos de la plataforma</span><span class="sxs-lookup"><span data-stu-id="4fbb2-111">Platform Requirements</span></span>

<span data-ttu-id="4fbb2-112">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el Windows SDK para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4fbb2-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="4fbb2-113">Se admite para aplicaciones de escritorio de Win32, aplicaciones de la tienda Windows y Windows Phone 8 aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4fbb2-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fbb2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fbb2-114">Requirements</span></span>



| <span data-ttu-id="4fbb2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fbb2-115">Requirement</span></span> | <span data-ttu-id="4fbb2-116">Value</span><span class="sxs-lookup"><span data-stu-id="4fbb2-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fbb2-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4fbb2-117">Header</span></span><br/> | <dl> <span data-ttu-id="4fbb2-118"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fbb2-118"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fbb2-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fbb2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fbb2-120">Tipos de biblioteca de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="4fbb2-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="4fbb2-121">**XMVECTOR, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="4fbb2-121">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="4fbb2-122">**XMVECTORF32, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="4fbb2-122">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="4fbb2-123">**XMVECTORI32, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="4fbb2-123">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="4fbb2-124">**XMVECTORU32, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="4fbb2-124">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="4fbb2-125">Extensiones de XMVECTORU8</span><span class="sxs-lookup"><span data-stu-id="4fbb2-125">XMVECTORU8 Extensions</span></span>](ovw-xmvectoru8-extensions.md)
</dt> </dl>

 

 





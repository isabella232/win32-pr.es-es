---
description: Un tipo opaco y portátil para admitir el uso de la sintaxis de inicializador de C/C++ para cargar valores de punto flotante en una instancia de tipo XMVECTOR.
ms.assetid: bafaa59f-fd1b-e252-cbbd-903df796fde0
title: Tipo de datos XMVECTORF32 (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e56e79ea678ede0afcac3523c09da725ede00d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649899"
---
# <a name="xmvectorf32-data-type"></a><span data-ttu-id="a968b-103">XMVECTORF32, tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a968b-103">XMVECTORF32 Data Type</span></span>

<span data-ttu-id="a968b-104">Un tipo opaco y portátil para admitir el uso de la sintaxis de inicializador de C/C++ para cargar valores de punto flotante en una instancia de tipo [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="a968b-104">An opaque, portable type to support the use of C/C++ initializer syntax to load floating-point values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTORF32 vectorf32;
```



## <a name="remarks"></a><span data-ttu-id="a968b-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a968b-105">Remarks</span></span>

<span data-ttu-id="a968b-106">Para obtener una lista de funcionalidad adicional, como constructores y operadores, disponible `XMVECTORF32` al programar en C++, vea [extensiones de XMVECTORF32](ovw-xmvectorf32-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="a968b-106">For a list of additional functionality, such as constructors and operators, available using `XMVECTORF32` when programming in C++, see [XMVECTORF32 Extensions](ovw-xmvectorf32-extensions.md).</span></span>

<span data-ttu-id="a968b-107">Las estructuras **XMVECTORF32**, [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md)y [**XMVECTORU8**](xmvectoru8-data-type.md) se proporcionan como un mecanismo para crear [**XMVECTOR**](xmvector-data-type.md) de diferentes tipos de datos constantes (punto flotante, entero sin signo, entero y byte) mediante inicializadores.</span><span class="sxs-lookup"><span data-stu-id="a968b-107">The **XMVECTORF32**, [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md), and [**XMVECTORU8**](xmvectoru8-data-type.md) structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="a968b-108">Esto es necesario para admitir [**XMVECTOR**](xmvector-data-type.md), ya que no admite inicializadores, por motivos de portabilidad y optimización.</span><span class="sxs-lookup"><span data-stu-id="a968b-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="a968b-109">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a968b-109">For example:</span></span>


```
XMVECTOR data;
XMVECTORF32 floatingVector = { 0.f, 0.f, 0.1f, 1.f };
data = floatingVector;
```



<span data-ttu-id="a968b-110">**Espacio de nombres**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="a968b-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="a968b-111">Requisitos de la plataforma</span><span class="sxs-lookup"><span data-stu-id="a968b-111">Platform Requirements</span></span>

<span data-ttu-id="a968b-112">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el Windows SDK para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a968b-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="a968b-113">Se admite para aplicaciones de escritorio de Win32, aplicaciones de la tienda Windows y Windows Phone 8 aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a968b-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="a968b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a968b-114">Requirements</span></span>



| <span data-ttu-id="a968b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a968b-115">Requirement</span></span> | <span data-ttu-id="a968b-116">Value</span><span class="sxs-lookup"><span data-stu-id="a968b-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a968b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a968b-117">Header</span></span><br/> | <dl> <span data-ttu-id="a968b-118"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="a968b-118"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a968b-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="a968b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a968b-120">Tipos de biblioteca de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="a968b-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="a968b-121">**XMVECTORI32, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="a968b-121">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="a968b-122">**XMVECTOR, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="a968b-122">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="a968b-123">**XMVECTORU32, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="a968b-123">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="a968b-124">**XMVECTORU8, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="a968b-124">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="a968b-125">**XMVECTORF32, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="a968b-125">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> </dl>

 

 





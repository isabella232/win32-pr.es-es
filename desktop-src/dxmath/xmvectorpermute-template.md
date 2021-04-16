---
description: Permute los componentes de dos vectores para crear un nuevo vector.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorpermute(xmvector,xmvector)
title: Plantilla XMVectorPermute (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37271cbb165f1e9c1769ef3a55e47f1e07310a81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650180"
---
# <a name="xmvectorpermute-template"></a>Plantilla XMVectorPermute

Permute los componentes de dos vectores para crear un nuevo vector.

## <a name="syntax"></a>Sintaxis

``` syntax
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW> XMVECTOR XMVectorPermute(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="V1"></span><span id="v1"></span>*V1*
</dt> <dd>

\[en el \] primer vector.

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*2*
</dt> <dd>

\[en el \] segundo vector.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el vector permuted que resultó de combinar los vectores de origen.

## <a name="remarks"></a>Observaciones

Si los 4 índices solo hacen referencia a un único vector (es decir, están todos en el intervalo 0-3 o todos en el intervalo 4-7), use [**XMVectorSwizzle**](xmvectorswizzle-template.md) en su lugar para mejorar el rendimiento.

Tenga en cuenta que la biblioteca utiliza especializaciones de plantilla en algunas plataformas para mejorar el rendimiento. No se implementan todos los casos de reflejo posibles en estos casos especiales, por lo que es preferible que el elemento X del vector resultante proceda del parámetro V1 en lugar del parámetro V2. Por ejemplo, prefiere usar `XMVectorPermute<0,1,4,5>(A,B);` para `XMVectorPermute(4,5,0,1)(B,A);` .

Esta función es una versión de plantilla de [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) en la que los argumentos *permute \** son valores de plantilla.

Las constantes de [ \_ permute \_ de XM](ovw-xnamath-reference-constants.md) se proporcionan para usar como valores de entrada para *PERMUTEX*,*permutey*,*PermuteZ* y *PermuteW*.

> [!Note]  
> La `XMVectorPermute` plantilla es nueva para DirectXMath y no está disponible para XNAMath 2. x.

 

**Espacio de nombres**: usar DirectX

### <a name="platform-requirements"></a>Requisitos de la plataforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el Windows SDK para Windows 8. Se admite para aplicaciones de escritorio de Win32, aplicaciones de la tienda Windows y Windows Phone 8 aplicaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DirectXMath. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de plantilla de la biblioteca de DirectXMath](ovw-xnamath-templates.md)
</dt> <dt>

[**XMVectorSwizzle**](xmvectorswizzle-template.md)
</dt> </dl>

 

 

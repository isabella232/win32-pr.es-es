---
description: Permuta los componentes de dos vectores para crear un nuevo vector.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorpermute(xmvector,xmvector)
title: Plantilla XMVectorPermute (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37271cbb165f1e9c1769ef3a55e47f1e07310a81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170409"
---
# <a name="xmvectorpermute-template"></a>Plantilla XMVectorPermute

Permuta los componentes de dos vectores para crear un nuevo vector.

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

\[en \] Primer vector.

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*V2*
</dt> <dd>

\[en \] el segundo vector.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el vector permutado resultante de combinar los vectores de origen.

## <a name="remarks"></a>Observaciones

Si los 4 índices hacen referencia a un solo vector (es decir, todos están en el intervalo 0-3 o todos en el intervalo 4-7), use [**XMVectorSwcial en**](xmvectorswizzle-template.md) su lugar para mejorar el rendimiento.

Tenga en cuenta que la biblioteca usa especializaciones de plantilla en algunas plataformas para mejorar el rendimiento. No todos los casos reflejados posibles se implementan para estos casos especiales, por lo que prefiere permutas donde el elemento X del vector resultante procede del parámetro V1 en lugar del parámetro V2. Por ejemplo, prefiere usar `XMVectorPermute<0,1,4,5>(A,B);` a `XMVectorPermute(4,5,0,1)(B,A);` .

Esta función es una versión de plantilla de [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) donde los argumentos *de Permute \** son valores de plantilla.

Las [constantes \_ \_ PERMUTE](ovw-xnamath-reference-constants.md) de XM se proporcionan para usar como valores de entrada para *PermuteX,**PermuteY,**PermuteZ* y *PermuteW.*

> [!Note]  
> La `XMVectorPermute` plantilla es nueva para DirectXMath y no está disponible para XNAMath 2.x.

 

**Espacio de** nombres: uso de DirectX

### <a name="platform-requirements"></a>Requisitos de la plataforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el SDK Windows para Windows 8. Compatible con aplicaciones de escritorio Win32, Windows store y Windows Phone 8 aplicaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DirectXMath.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de plantilla de biblioteca de DirectXMath](ovw-xnamath-templates.md)
</dt> <dt>

[**XMVectorSwzzle**](xmvectorswizzle-template.md)
</dt> </dl>

 

 

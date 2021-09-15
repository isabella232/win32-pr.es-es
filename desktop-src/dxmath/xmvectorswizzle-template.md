---
description: Desliza un vector.
ms.assetid: 75608e80-5911-45a8-beca-ceac1f4d2c1c
title: Plantilla XMVectorSwcela (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e872d76f3251eccc8616c143c645b388e2dca4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465887"
---
# <a name="xmvectorswizzle-template"></a>Plantilla XMVectorSwzzle

Desliza un vector.

## <a name="syntax"></a>Sintaxis

``` syntax
template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW> XMVECTOR XMVectorSwizzle(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="V"></span><span id="v"></span>*V*
</dt> <dd>

\[en \] Vector a swzzle.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el [**XMVECTOR girado.**](xmvector-data-type.md)

## <a name="remarks"></a>Observaciones

Esta función es una versión de plantilla de [**XMVectorSwzzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) donde los argumentos *swzzle \** son valores de plantilla.

`XM_SWIZZLE_X`, , y son constantes que se evalúan `XM_SWIZZLE_Y` `XM_SWIZZLE_Z` como `XM_SWIZZLE_W` 0, 1, 2 y 3 respectivamente para su uso con `XMVectorSwizzle` . Es idéntico a `XM_PERMUTE_0X` , `XM_PERMUTE_0Y` , y `XM_PERMUTE_0Z` `XM_PERMUTE_0W` .

> [!Note]  
> La `XMVectorSwizzle` plantilla es nueva para DirectXMath y no está disponible para XNAMath 2.x.

 

**Espacio de** nombres: uso de DirectX

### <a name="platform-requirements"></a>Requisitos de la plataforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el SDK de Windows para Windows 8. Compatible con aplicaciones de escritorio Win32, Windows store y Windows Phone 8 aplicaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DirectXMath.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de plantilla de biblioteca de DirectXMath](ovw-xnamath-templates.md)
</dt> <dt>

[**XMVectorPermute**](xmvectorpermute-template.md)
</dt> </dl>

 

 

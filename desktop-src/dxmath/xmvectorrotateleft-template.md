---
description: Gira el vector a la izquierda por un número determinado de elementos de 32 bits.
ms.assetid: ba3698ed-212d-4ef0-846a-4099d0e1abec
title: Plantilla XMVectorRotateLeft (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b52fccebeb93803fdc33346fa4ee5e873c1d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170406"
---
# <a name="xmvectorrotateleft-template"></a>Plantilla XMVectorRotateLeft

Gira el vector a la izquierda por un número determinado de elementos de 32 bits.

## <a name="syntax"></a>Sintaxis

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateLeft(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="V"></span><span id="v"></span>*V*
</dt> <dd>

\[en \] Vector para girar a la izquierda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el [**XMVECTOR girado.**](xmvector-data-type.md)

## <a name="remarks"></a>Observaciones

Esta función es una versión de plantilla de [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) donde el *argumento Elements* es un valor de plantilla.

> [!Note]  
> La `XMVectorRotateLeft` plantilla es nueva para DirectXMath y no está disponible para XNAMath 2.x.

 

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
</dt> <dt>

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 

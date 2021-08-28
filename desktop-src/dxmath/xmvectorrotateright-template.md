---
description: Gira el vector a la derecha en un número determinado de elementos de 32 bits.
ms.assetid: 7493c1fe-2c3d-4eb6-bec1-02c066a70b9f
title: Plantilla XMVectorRotateRight (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47017982af6bb61212129665010d403bd9db898c65056110c4d2f40a5f8a9362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984495"
---
# <a name="xmvectorrotateright-template"></a>Plantilla XMVectorRotateRight

Gira el vector a la derecha en un número determinado de elementos de 32 bits.

## <a name="syntax"></a>Sintaxis

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateRight(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="V"></span><span id="v"></span>*V*
</dt> <dd>

\[en \] Vector para girar a la derecha.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el [**XMVECTOR girado.**](xmvector-data-type.md)

## <a name="remarks"></a>Comentarios

Esta función es una versión de plantilla de [**XMVectorRotateRight donde**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) el *argumento Elements* es un valor de plantilla.

> [!Note]  
> La `XMVectorRotateRight` plantilla es nueva para DirectXMath y no está disponible para XNAMath 2.x.

 

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

[**XMVectorPermute**](xmvectorpermute-template.md)
</dt> <dt>

[**XMVectorRotateLeft**](xmvectorrotateleft-template.md)
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 

---
description: Desplaza un vector a la izquierda de un número determinado de elementos de 32 bits y rellena los elementos vacantes con elementos de un segundo vector.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorshiftleft(xmvector,xmvector)
title: Plantilla XMVectorShiftLeft (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115604871d9e8402157a82bf3c420e5762b3a424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649892"
---
# <a name="xmvectorshiftleft-template"></a>Plantilla XMVectorShiftLeft

Desplaza un vector a la izquierda de un número determinado de elementos de 32 bits y rellena los elementos vacantes con elementos de un segundo vector.

## <a name="syntax"></a>Sintaxis

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorShiftLeft(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="V1"></span><span id="v1"></span>*V1*
</dt> <dd>

\[en \] vector para desplazarse a la izquierda.

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*2*
</dt> <dd>

\[en \] Vector se usa para rellenar los componentes vacantes de v1 después de desplazarse a la izquierda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el desplazado y rellenado en [**XMVECTOR**](xmvector-data-type.md).

## <a name="remarks"></a>Observaciones

Esta función es una versión de plantilla de [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) , donde el argumento *Elements* es un valor de plantilla.

> [!Note]  
> La `XMVectorShiftLeft` plantilla es nueva para DirectXMath y no está disponible para XNAMath 2. x.

 

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

[**XMVectorPermute**](xmvectorpermute-template.md)
</dt> <dt>

[**XMVectorRotateLeft**](xmvectorrotateleft-template.md)
</dt> <dt>

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> </dl>

 

 

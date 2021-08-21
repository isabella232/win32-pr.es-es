---
description: Desplaza un vector a la izquierda por un número determinado de elementos de 32 bits, rellenando los elementos desocupados con elementos de un segundo vector.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorshiftleft(xmvector,xmvector)
title: Plantilla XMVectorShiftLeft (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab92e2fb64a101251a7531ca1d96b8b06f3e9af6e2b7dabe7958673a61bd8c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499284"
---
# <a name="xmvectorshiftleft-template"></a>Plantilla XMVectorShiftLeft

Desplaza un vector a la izquierda por un número determinado de elementos de 32 bits, rellenando los elementos desocupados con elementos de un segundo vector.

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

\[en \] Vector para desplazar a la izquierda.

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*V2*
</dt> <dd>

\[en \] Vector usado para rellenar los componentes desocupados de V1 después de desplazarse a la izquierda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el desplazamiento y rellenado en [**XMVECTOR.**](xmvector-data-type.md)

## <a name="remarks"></a>Comentarios

Esta función es una versión de plantilla de [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) donde el *argumento Elements* es un valor de plantilla.

> [!Note]  
> La `XMVectorShiftLeft` plantilla es nueva para DirectXMath y no está disponible para XNAMath 2.x.

 

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

[**XMVectorRotateLeft**](xmvectorrotateleft-template.md)
</dt> <dt>

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> </dl>

 

 

---
description: Gira un vector a la izquierda por un número determinado de componentes de 32 bits e inserta los elementos seleccionados de ese resultado en otro vector.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorinsert(xmvector,xmvector)
title: Plantilla XMVectorInsert (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3250ad52ab19a127b110b02ecf71543f44708681
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170410"
---
# <a name="xmvectorinsert-template"></a>Plantilla XMVectorInsert

Gira un vector a la izquierda por un número determinado de componentes de 32 bits e inserta los elementos seleccionados de ese resultado en otro vector.

## <a name="syntax"></a>Sintaxis

``` syntax
template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3> XMVECTOR XMVectorInsert(
  [in]  XMVECTOR VD,
  [in]  XMVECTOR VS
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="VD"></span><span id="vd"></span>*VD*
</dt> <dd>

\[en \] Vector en el que se insertará.

</dd> <dt>

<span id="VS"></span><span id="vs"></span>*VS*
</dt> <dd>

\[en \] Vector para girar a la izquierda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el [**XMVECTOR**](xmvector-data-type.md) que resulta de la rotación y la inserción.

## <a name="remarks"></a>Observaciones

Esta función es una versión de plantilla de [**XMVectorInsert donde**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) los *argumentos Select \** son valores de plantilla.

Para obtener el mejor rendimiento, el resultado `XMVectorInsert` de debe asignarse de nuevo a *VD*.

> [!Note]  
> La `XMVectorInsert` plantilla es nueva para DirectXMath y no está disponible para XNAMath 2.x.

 

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

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 

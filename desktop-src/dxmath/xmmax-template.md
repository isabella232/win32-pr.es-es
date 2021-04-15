---
description: Compara dos instancias de tipos de datos numéricos, o dos instancias de un objeto que admite una sobrecarga de <, y devuelve el mayor de las dos instancias. El tipo de datos de los argumentos y el valor devuelto es el mismo.
ms.assetid: m:microsoft.directx_sdk.reference.xmmax(t,t)
title: Plantilla XMMax (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f8de32a32004289249cea269400d711831d640
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708935"
---
# <a name="xmmax-template"></a>Plantilla XMMax

Compara dos instancias de tipos de datos numéricos, o dos instancias de un objeto que admite una sobrecarga de <, y devuelve el mayor de las dos instancias. El tipo de datos de los argumentos y el valor devuelto es el mismo.

## <a name="syntax"></a>Sintaxis

``` syntax
template<class T> T XMMax(
  [in]  T a,
  [in]  T b
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="a"></span><span id="A"></span>*un*
</dt> <dd>

\[en \] especifica el primero de dos objetos.

</dd> <dt>

<span id="b"></span><span id="B"></span>*b*
</dt> <dd>

\[en \] especifica dos de los dos objetos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el mayor de los dos objetos de entrada.

## <a name="remarks"></a>Observaciones

`XMMax` es una plantilla y el tipo T se especifica cuando se crea una instancia de la plantilla.

> [!Note]  
> La `XMMax` plantilla es nueva para DirectXMath y no está disponible para XNAMath 2. x. `XMMax` está disponible como una macro en XNAMath 2. x.

 

> [!Note]  
> Idealmente, se usa STD:: Max en lugar de `XMMax` . Para evitar conflictos con los encabezados de Windows con STD:: Max, debe \# definir NOMINMAX antes de incluir los encabezados de Windows.

 

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

[**XMMin**](xmmin-template.md)
</dt> </dl>

 

 





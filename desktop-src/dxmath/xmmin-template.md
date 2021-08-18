---
description: Compara dos instancias de tipo de datos numéricos o dos instancias de un objeto que admite una sobrecarga de < y devuelve la más pequeña de las dos instancias. El tipo de datos de los argumentos y el valor devuelto es el mismo.
ms.assetid: m:microsoft.directx_sdk.reference.xmmin(t,t)
title: Plantilla XMMin (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c2d78b64a66411c31570267c66a7e75171dcf9da039871c07c8bfc31df49149
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499860"
---
# <a name="xmmin-template"></a>Plantilla XMMin

Compara dos instancias de tipo de datos numéricos o dos instancias de un objeto que admite una sobrecarga de < y devuelve la más pequeña de las dos instancias. El tipo de datos de los argumentos y el valor devuelto es el mismo.

## <a name="syntax"></a>Sintaxis

``` syntax
template<class T> T XMMin(
  [in]  T a,
  [in]  T b
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="a"></span><span id="A"></span>*Un*
</dt> <dd>

\[en \] Especifica el primero de dos objetos.

</dd> <dt>

<span id="b"></span><span id="B"></span>*B*
</dt> <dd>

\[en \] Especifica los dos objetos de .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el menor de los dos objetos de entrada.

## <a name="remarks"></a>Comentarios

`XMMin` es una plantilla y se especifica el tipo T cuando se crea una instancia de la plantilla.

> [!Note]  
> La `XMMin` plantilla es nueva para DirectXMath y no está disponible para XNAMath 2.x. `XMMin` está disponible como macro en XNAMath 2.x.

 

> [!Note]  
> Lo ideal es usar std::min en lugar de `XMMin` . Para evitar conflictos con Windows encabezados con std::min, debe definir NOMINMAX antes de incluir Windows \# encabezados.

 

**Espacio de** nombres: uso de DirectX

### <a name="platform-requirements"></a>Requisitos de la plataforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el SDK Windows para Windows 8. Compatible con aplicaciones de escritorio Win32, Windows store y Windows Phone 8 aplicaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DirectXMath.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de plantilla de biblioteca de DirectXMath](ovw-xnamath-templates.md)
</dt> <dt>

[**XMMax**](xmmax-template.md)
</dt> </dl>

 

 





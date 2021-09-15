---
description: Compara dos instancias de tipo de datos numéricos o dos instancias de un objeto que admite una sobrecarga de < y devuelve la mayor de las dos instancias. El tipo de datos de los argumentos y el valor devuelto es el mismo.
ms.assetid: m:microsoft.directx_sdk.reference.xmmax(t,t)
title: Plantilla XMMax (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f8de32a32004289249cea269400d711831d640
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360504"
---
# <a name="xmmax-template"></a>Plantilla XMMax

Compara dos instancias de tipo de datos numéricos o dos instancias de un objeto que admite una sobrecarga de < y devuelve la mayor de las dos instancias. El tipo de datos de los argumentos y el valor devuelto es el mismo.

## <a name="syntax"></a>Sintaxis

``` syntax
template<class T> T XMMax(
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

Devuelve el mayor de los dos objetos de entrada.

## <a name="remarks"></a>Observaciones

`XMMax` es una plantilla y se especifica el tipo T cuando se crea una instancia de la plantilla.

> [!Note]  
> La `XMMax` plantilla es nueva para DirectXMath y no está disponible para XNAMath 2.x. `XMMax` está disponible como macro en XNAMath 2.x.

 

> [!Note]  
> Lo ideal es usar std::max en lugar de `XMMax` . Para evitar conflictos con Windows encabezados con std::max, debe definir NOMINMAX antes de incluir Windows \# encabezados.

 

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

[**XMMin**](xmmin-template.md)
</dt> </dl>

 

 





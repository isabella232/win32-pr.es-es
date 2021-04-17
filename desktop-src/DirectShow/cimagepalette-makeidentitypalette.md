---
description: El método MakeIdentityPalette intenta crear un &\# 0034; paleta de identidad, &\# 0034; definido como uno que se asigna directamente a la paleta seleccionada en el dispositivo de pantalla.
ms.assetid: 08a0cf67-f43f-44c0-bfb3-6527fd434ea4
title: Método CImagePalette. MakeIdentityPalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakeIdentityPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e105652108e74907375408f0bd8946c69194202
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670495"
---
# <a name="cimagepalettemakeidentitypalette-method"></a>CImagePalette. MakeIdentityPalette, método

El `MakeIdentityPalette` método intenta crear una "paleta de identidad" definida como una que se asigna directamente a la paleta seleccionada en el dispositivo de pantalla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MakeIdentityPalette(
   PALETTEENTRY *pEntry,
   INT          iColours,
   LPSTR        szDevice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pEntry* 
</dt> <dd>

Puntero a una matriz de entradas de la paleta.

</dd> <dt>

*iColours* 
</dt> <dd>

Número de entradas de la paleta en *pEntry*.

</dd> <dt>

*szDevice* 
</dt> <dd>

Puntero a una cadena que contiene el nombre del dispositivo de pantalla, devuelto por la función **EnumDisplayDevices** de GDI. Para usar el dispositivo de pantalla principal, establezca este parámetro en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto si es correcto o s \_ false si no se realiza correctamente.

## <a name="remarks"></a>Observaciones

Este método compara las entradas reservadas en la paleta del sistema con las entradas correspondientes de la matriz *pEntry* . Si coinciden exactamente, el método establece la \_ marca PC nocollapse en las entradas de la paleta restantes (no reservadas) en *pEntry*. Esta marca evita que GDI intente asignar las entradas de la paleta lógica a las entradas de la paleta del sistema.

El método [**CImagePalette:: MakePalette**](cimagepalette-makepalette.md) llama a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 





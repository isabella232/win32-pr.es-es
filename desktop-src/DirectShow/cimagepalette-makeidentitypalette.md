---
description: El método MakeIdentityPalette intenta crear un &\# 0034;paleta de identidades,&0034; definido como uno que se asigna directamente a la paleta seleccionada en el dispositivo para \# mostrar.
ms.assetid: 08a0cf67-f43f-44c0-bfb3-6527fd434ea4
title: Método CImagePalette.MakeIdentityPalette (Winutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973865"
---
# <a name="cimagepalettemakeidentitypalette-method"></a>CImagePalette.MakeIdentityPalette (método)

El método intenta crear una "paleta de identidades", definida como una que se asigna directamente a la `MakeIdentityPalette` paleta seleccionada en el dispositivo para mostrar.

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

Puntero a una matriz de entradas de paleta.

</dd> <dt>

*iColours* 
</dt> <dd>

Número de entradas de paleta en *pEntry*.

</dd> <dt>

*szDevice* 
</dt> <dd>

Puntero a una cadena que contiene el nombre del dispositivo para mostrar, tal como lo devuelve la función **EnumDisplayDevices de** GDI. Para usar el dispositivo de pantalla principal, establezca este parámetro en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o S FALSE si no se realiza \_ correctamente.

## <a name="remarks"></a>Observaciones

Este método compara las entradas reservadas de la paleta del sistema con las entradas correspondientes de la *matriz pEntry.* Si coinciden exactamente, el método establece la marca PC NOCOLLAPSE en las entradas de paleta restantes \_ (no reservadas) en *pEntry*. Esta marca impide que GDI intente asignar entradas de la paleta lógica a las entradas de la paleta del sistema.

El [**método CImagePalette::MakePalette**](cimagepalette-makepalette.md) llama a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CImagePalette (clase)**](cimagepalette.md)
</dt> </dl>

 

 





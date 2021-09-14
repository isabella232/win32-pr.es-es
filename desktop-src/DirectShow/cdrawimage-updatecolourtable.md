---
description: El método UpdateColourTable actualiza la tabla de colores con una nueva paleta.
ms.assetid: 61ad98c6-a526-4aac-ad68-d44fadc668de
title: Método CDrawImage.UpdateColourTable (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.UpdateColourTable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fcffdf9e7deaaac5a01f6559ee557c978fcda88f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061273"
---
# <a name="cdrawimageupdatecolourtable-method"></a>Método CDrawImage.UpdateColourTable

El `UpdateColourTable` método actualiza la tabla de colores con una nueva paleta.

## <a name="syntax"></a>Sintaxis


```C++
void UpdateColourTable(
   HDC              hdc,
   BITMAPINFOHEADER *pbmi
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hdc* 
</dt> <dd>

Contexto del dispositivo que contiene la imagen.

</dd> <dt>

*pbmi* 
</dt> <dd>

Puntero a una [**estructura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) que contiene la nueva paleta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDrawImage (clase)**](cdrawimage.md)
</dt> </dl>

 

 





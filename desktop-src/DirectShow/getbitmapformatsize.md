---
description: La función GetBitmapFormatSize calcula el tamaño necesario para una estructura VIDEOINFO que puede contener una estructura BITMAPINFOHEADER especificada.
ms.assetid: a559415a-070f-4674-be12-a65a46025809
title: Función GetBitmapFormatSize (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapFormatSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39a64f6d975e403de6c177906b23ef7e09f29ddf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063255"
---
# <a name="getbitmapformatsize-function"></a>Función GetBitmapFormatSize

La `GetBitmapFormatSize` función calcula el tamaño necesario para una estructura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) que puede contener una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) especificada.

## <a name="syntax"></a>Sintaxis


```C++
LONG GetBitmapFormatSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pHeader* 
</dt> <dd>

Puntero a una [**estructura BITMAPINFOHEADER.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el tamaño, en bytes.

## <a name="remarks"></a>Observaciones

Una [**estructura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) puede ir seguida de máscaras de color o entradas de paleta, por lo que puede ser difícil determinar el número de bytes necesarios para construir una estructura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) a partir de una estructura **BITMAPINFOHEADER existente.**

Para copiar una [**estructura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) en una [**estructura VIDEOINFO,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) use la macro [**HEADER,**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header) que calcula el desplazamiento correcto.

## <a name="examples"></a>Ejemplos


```
LONG size = GetBitmapFormatSize(&bmi);

VIDEOINFO *pVi = static_cast<VIDEOINFO*>(CoTaskMemAlloc(size));

if (pVi != NULL)
{
    CopyMemory(HEADER(pVi), &bmi, sizeof(BITMAPINFOHEADER));
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de vídeo e imagen](video-and-image-functions.md)
</dt> </dl>

 

 





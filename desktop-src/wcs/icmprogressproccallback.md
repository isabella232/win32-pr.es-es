---
title: Función de devolución de llamada ICMProgressProcCallback
description: La función ICMProgressProcCallback es una función de devolución de llamada proporcionada por la aplicación que informa del progreso y permite que la aplicación cancele el procesamiento de color.
ms.assetid: 4e0bfa4c-f0eb-4776-98d6-90d9adf71bee
keywords:
- Función de devolución de llamada ICMProgressProcCallback sistema de color de Windows
topic_type:
- apiref
api_name:
- ICMProgressProcCallback
api_location:
- Icm.h
api_type:
- UserDefined
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8acf790a135a41e4eabb4a67c2498f1ed914c4c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721573"
---
# <a name="icmprogressproccallback-callback-function"></a>Función de devolución de llamada ICMProgressProcCallback

La función **ICMProgressProcCallback** es una función de devolución de llamada proporcionada por la aplicación que informa del progreso y permite que la aplicación cancele el procesamiento de color.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI ICMProgressProcCallback(
   ULONG  ulMax,
   ULONG  ulCurrent,
   LPARAM ulCallbackData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulMax* 
</dt> <dd>

Especifica el valor máximo del contador de progreso (que se usa para estimar la finalización del procesamiento de mapas de bits).

</dd> <dt>

*ulCurrent* 
</dt> <dd>

Especifica el valor actual del contador de progreso (cuando se divide por el valor máximo, proporciona una estimación aproximada del porcentaje de finalización).

</dd> <dt>

*ulCallbackData* 
</dt> <dd>

Especifica los datos que pasa la aplicación a una función ICM2, que después lo pasa a la función de devolución de llamada. Estos datos se pueden utilizar, por ejemplo, para identificar el mapa de bits y el proceso sobre el que se está informando del progreso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **true** para continuar el procesamiento de mapas de bits. El valor devuelto es **false** para cancelar el procesamiento. Si se cancela el procesamiento, la función de llamada devuelve cero para indicar un error, aunque es posible que el búfer de salida se llene parcialmente.

## <a name="remarks"></a>Observaciones

La aplicación proporciona el nombre de esta función de devolución de llamada. Un número de funciones WCS, incluidas [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) y [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits), llama a esta función periódicamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>ICM. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Conceptos básicos de la administración del color](basic-color-management-concepts.md)
</dt> <dt>

[Funciones](functions.md)
</dt> <dt>

[**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)
</dt> <dt>

[**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits)
</dt> </dl>

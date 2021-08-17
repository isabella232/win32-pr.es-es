---
title: Función de devolución de llamada ICMProgressProcCallback
description: La función ICMProgressProcCallback es una función de devolución de llamada proporcionada por la aplicación que informa del progreso y permite que la aplicación cancele el procesamiento de color.
ms.assetid: 4e0bfa4c-f0eb-4776-98d6-90d9adf71bee
keywords:
- Función de devolución de llamada ICMProgressProcCallback Windows Color System
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
ms.openlocfilehash: d697bb09b4871f6debb1a41a7ecc3e795307ee544ec30bfaf4b5b44ba0328578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117671391"
---
# <a name="icmprogressproccallback-callback-function"></a>Función de devolución de llamada ICMProgressProcCallback

La **función ICMProgressProcCallback** es una función de devolución de llamada proporcionada por la aplicación que informa del progreso y permite que la aplicación cancele el procesamiento de color.

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

Especifica el valor máximo del contador de progreso (que se usa para calcular la finalización del procesamiento del mapa de bits).

</dd> <dt>

*ulCurrent* 
</dt> <dd>

Especifica el valor actual del contador de progreso (cuando se divide entre el valor máximo, proporciona una estimación aproximada del porcentaje de finalización).

</dd> <dt>

*ulCallbackData* 
</dt> <dd>

Especifica los datos que pasa la aplicación a una función ICM2, que luego los pasa a la función de devolución de llamada. Estos datos se pueden usar, por ejemplo, para identificar el mapa de bits y el proceso sobre el que se notifica el progreso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **TRUE para continuar** con el procesamiento del mapa de bits. El valor devuelto es **FALSE para** cancelar el procesamiento. Si se cancela el procesamiento, la función que realiza la llamada devuelve cero para indicar un error, aunque su búfer de salida se puede rellenar parcialmente.

## <a name="remarks"></a>Comentarios

La aplicación proporciona el nombre de esta función de devolución de llamada. Varias funciones de WCS, como [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) y [**CheckBitmapBits,**](/windows/win32/api/icm/nf-icm-checkbitmapbits)llaman a esta función periódicamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Icm.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Conceptos básicos de administración de colores](basic-color-management-concepts.md)
</dt> <dt>

[Funciones](functions.md)
</dt> <dt>

[**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)
</dt> <dt>

[**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits)
</dt> </dl>

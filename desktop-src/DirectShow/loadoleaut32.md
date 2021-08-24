---
description: La función LoadOLEAut32 carga la biblioteca de vínculos dinámicos de Automation (OleAut32.dll).
ms.assetid: af907341-1e2c-4c63-bf4e-d6c49b4f6a6e
title: Función LoadOLEAut32 (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadOLEAut32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ca5832246e90e1df207754dc33380547b8193829394d81e6b2b757fccf79a91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502315"
---
# <a name="loadoleaut32-function"></a>Función LoadOLEAut32

La **función LoadOLEAut32** carga la biblioteca de vínculos dinámicos de Automation (OleAut32.dll).

## <a name="syntax"></a>Sintaxis


```C++
HINSTANCE LoadOLEAut32(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un identificador a una instancia dll de Automation.

## <a name="remarks"></a>Comentarios

Cuando el destructor [**CBaseObject**](cbaseobject.md) destruye el objeto que cargó OleAut32.dll, descargará la biblioteca si todavía está cargado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones auxiliares COM**](com-helper-functions.md)
</dt> </dl>

 

 





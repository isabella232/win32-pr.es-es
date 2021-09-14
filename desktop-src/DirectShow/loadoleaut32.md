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
ms.openlocfilehash: b23bad7e445eebc78ecf8a849ddde8fc23746131
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063198"
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

## <a name="remarks"></a>Observaciones

Cuando el destructor [**CBaseObject**](cbaseobject.md) destruye el objeto que cargó OleAut32.dll, descargará la biblioteca si todavía está cargado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones auxiliares COM**](com-helper-functions.md)
</dt> </dl>

 

 





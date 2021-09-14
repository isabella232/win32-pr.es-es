---
description: Recupera la versión de software para esta secuencia.
ms.assetid: f54153df-5593-4784-acc5-3e0dcef424b5
title: Método CPersistStream.GetSoftwareVersion (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSoftwareVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0954e9a113342217dd389c64ec4fc6c04a6f767
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062415"
---
# <a name="cpersiststreamgetsoftwareversion-method"></a>Método CPersistStream.GetSoftwareVersion

Recupera la versión de software para esta secuencia.

## <a name="syntax"></a>Sintaxis


```C++
virtual DWORD GetSoftwareVersion();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **DWORD que** contiene el número de versión. Cada vez que se cambia el formato de la secuencia, esta función debe modificarse para devolver un número mayor que antes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pstream.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CPersistStream (clase)**](cpersiststream.md)
</dt> </dl>

 

 





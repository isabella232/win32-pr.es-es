---
description: 'Constructor CPersistStream.CPersistStream: método constructor.'
ms.assetid: 48143a61-5ba7-4bf9-bffa-244f2769144d
title: Constructor CPersistStream.CPersistStream (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.CPersistStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 00745dab5d851f05bf3df99dcdb7b6e8574518a970f8a79466a291cbec13997a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813395"
---
# <a name="cpersiststreamcpersiststream-constructor"></a>Constructor CPersistStream.CPersistStream

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CPersistStream(
   IUnknown *pUnk,
   HRESULT  *phr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Punk* 
</dt> <dd>

Puntero a la **interfaz IUnknown** del objeto de delegación.

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero al valor devuelto com general. Este valor solo se cambia si se produce un error en esta función.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pstream.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPersistStream (clase)**](cpersiststream.md)
</dt> </dl>

 

 





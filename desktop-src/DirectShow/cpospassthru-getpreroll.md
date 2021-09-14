---
description: El método GetPreroll recupera la cantidad de datos que se pondrán en cola antes de la posición inicial. Este método implementa el método IMediaSeeking::GetPreroll.
ms.assetid: b00de2fa-ba3c-4a16-ad67-adf3df52ef9a
title: Método CPosPassThru.GetPreroll (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e72d7c83c8cdb0fa08a4b395fd65c80edbe3fb05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063334"
---
# <a name="cpospassthrugetpreroll-method"></a>Método CPosPassThru.GetPreroll

El `GetPreroll` método recupera la cantidad de datos que se pondrán en cola antes de la posición inicial. Este método implementa el [**método IMediaSeeking::GetPreroll.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPreroll(
   LONGLONG *pllPreroll
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pllPreroll* 
</dt> <dd>

Puntero a una variable que recibe el tiempo de inscripción previa, en unidades del formato de hora actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el **valor HRESULT** del pin conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CPosPassThru (clase)**](cpospassthru.md)
</dt> </dl>

 

 





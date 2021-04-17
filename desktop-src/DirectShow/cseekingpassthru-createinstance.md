---
description: El método CreateInstance crea una instancia del objeto. Este método admite la creación del objeto a través de un generador de clases. Para obtener más información, vea CFactoryTemplate.
ms.assetid: 88dfa933-6fa1-4b57-8b0d-579233fa960c
title: Método CSeekingPassThru. CreateInstance (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3640cbd6a0a3e582899e7f5cd349ca48498f3532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660550"
---
# <a name="cseekingpassthrucreateinstance-method"></a>CSeekingPassThru. CreateInstance (método)

El `CreateInstance` método crea una instancia del objeto. Este método admite la creación del objeto a través de un generador de clases. Para obtener más información, vea [**CFactoryTemplate**](cfactorytemplate.md).

## <a name="syntax"></a>Sintaxis


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pUnk* 
</dt> <dd>

Puntero al propietario de este objeto. Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación. De lo contrario, establezca este parámetro en **null**.

</dd> <dt>

*phr* 
</dt> <dd>

Puntero a un valor **HRESULT** . ignorado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a un nuevo objeto **CSeekingPassThru** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Seekpt. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSeekingPassThru**](cseekingpassthru.md)
</dt> </dl>

 

 





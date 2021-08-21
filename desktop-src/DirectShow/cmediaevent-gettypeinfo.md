---
description: 'Método CMediaEvent.GetTypeInfo: recupera un objeto type-information, que puede recuperar la información de tipo de una interfaz.'
ms.assetid: d54042d5-e9d3-415c-b90d-1fe7d38164f5
title: Método CMediaEvent.GetTypeInfo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3ef3f84cce1bad88b0f1103be3584ff350afac0fd7047b5a75a5fb473a4bedcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156993"
---
# <a name="cmediaeventgettypeinfo-method"></a>Método CMediaEvent.GetTypeInfo

Recupera un objeto de información de tipos, que puede recuperar la información de tipo de una interfaz.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*itinfo* 
</dt> <dd>

Escriba la información que se devolverá. Pase cero para recuperar información de tipo para **la implementación de IDispatch.**

</dd> <dt>

*lcid* 
</dt> <dd>

Identificador de configuración regional para la información de tipo. Para las clases que admiten nombres de miembros localizados, un objeto puede devolver información de tipo diferente para distintos idiomas. En el caso de las clases que no admiten nombres de miembros localizados, este parámetro se puede omitir.

</dd> <dt>

*pptinfo* 
</dt> <dd>

Dirección de un puntero al objeto de información de tipo solicitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero E \_ si *pptinfo* no es válido. Devuelve TYPE \_ E \_ ELEMENTNOTFOUND si *itinfo* no es cero. Devuelve S \_ OK si se realiza correctamente. De lo contrario, devuelve **un HRESULT** de una de las llamadas para recuperar el tipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaEvent (clase)**](cmediaevent.md)
</dt> </dl>

 

 





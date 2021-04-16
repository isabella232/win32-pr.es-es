---
description: Recupera un objeto de información de tipo, que puede recuperar la información de tipo de una interfaz.
ms.assetid: d54042d5-e9d3-415c-b90d-1fe7d38164f5
title: Método CMediaEvent. GetTypeInfo (Ctlutil. h)
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
ms.openlocfilehash: e351d3b8b06bea4f6f9a1a160802972a8fa50f82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671558"
---
# <a name="cmediaeventgettypeinfo-method"></a>CMediaEvent. GetTypeInfo, método

Recupera un objeto de información de tipo, que puede recuperar la información de tipo de una interfaz.

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

Información de tipo que se va a devolver. Pase cero para recuperar la información de tipo de la implementación de **IDispatch** .

</dd> <dt>

*lcid* 
</dt> <dd>

IDENTIFICADOR de configuración regional de la información de tipo. En el caso de las clases que admiten nombres de miembro localizados, es posible que un objeto pueda devolver información de tipo diferente para distintos idiomas. En el caso de las clases que no admiten nombres de miembro localizados, este parámetro se puede omitir.

</dd> <dt>

*pptinfo* 
</dt> <dd>

Dirección de un puntero al objeto de información de tipo solicitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un \_ puntero E si *pptinfo* no es válido. Devuelve el tipo \_ E \_ ELEMENTNOTFOUND si *itinfo* no es cero. Devuelve S \_ correcto si se realiza correctamente. De lo contrario, devuelve un **valor HRESULT** de una de las llamadas para recuperar el tipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaEvent**](cmediaevent.md)
</dt> </dl>

 

 





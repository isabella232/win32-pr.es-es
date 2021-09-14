---
description: El método ConnectionMediaType recupera el tipo de medio para la conexión de pin actual, si la hay. Este método implementa el método IPin::ConnectionMediaType.
ms.assetid: 57d100ba-4171-4caa-ab98-66a0a327a53b
title: Método CBasePin.ConnectionMediaType (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectionMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62bd211b6c93e44c571d822ccc86104a5a6fdcab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061369"
---
# <a name="cbasepinconnectionmediatype-method"></a>Método CBasePin.ConnectionMediaType

El **método ConnectionMediaType** recupera el tipo de medio para la conexión de pin actual, si la hay. Este método implementa el [**método IPin::ConnectionMediaType.**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConnectionMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntero a una [**estructura \_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) que recibe el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los de la tabla siguiente.



| Código devuelto                                                                                           | Descripción                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Correcto.<br/>                   |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>             | **Argumento de** puntero NULL.<br/> |
| <dl> <dt>**VFW \_ E \_ NO \_ CONECTADO**</dt> </dl> | El pin no está conectado.<br/>      |



 

## <a name="remarks"></a>Observaciones

Si el pin está conectado, este método copia el tipo de medio en la estructura [**\_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) especificada por *pmt*. El autor de la llamada debe liberar el bloque de formato del tipo de medio. Puede usar la [**función CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) o la [**función auxiliar FreeMediaType.**](freemediatype.md)

Si el pin no está conectado, este método cero el bloque de memoria especificado por *pmt* y devuelve un código de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 


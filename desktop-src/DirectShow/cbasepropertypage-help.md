---
description: 'El método de ayuda invoca la ayuda de la página de propiedades. Este método implementa el método IPropertyPage:: help.'
ms.assetid: 8fe72b2e-a9f1-435d-8eda-27056f112c6d
title: Método CBasePropertyPage. Help (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Help
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b87c8ba76928fbf0e465a8b6a3a0aaf4730759f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671320"
---
# <a name="cbasepropertypagehelp-method"></a>CBasePropertyPage. Help (método)

El `Help` método invoca la ayuda de la página de propiedades. Este método implementa el método **IPropertyPage:: help** .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Help(
   LPCWSTR lpszHelpDir
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszHelpDir* 
</dt> <dd>

Puntero a la cadena bajo la clave **HelpDir** en la información de CLSID de la página de propiedades en el registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ NOTIMPL.

## <a name="remarks"></a>Observaciones

En la clase base, el método siempre devuelve E \_ NOTIMPL. Cuando se produce un error en el método, el marco llama a **IPropertyPage:: GetPageInfo** para obtener el nombre del archivo de ayuda y el identificador de contexto. De forma predeterminada, son **null**. Para proporcionar ayuda, por lo tanto, la clase derivada puede invalidar el método `Help` o el método [**CBasePropertyPage:: GetPageInfo**](cbasepropertypage-getpageinfo.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 





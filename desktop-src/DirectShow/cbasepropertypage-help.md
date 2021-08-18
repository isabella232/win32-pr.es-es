---
description: El método Help invoca la ayuda de la página de propiedades. Este método implementa el método IPropertyPage::Help.
ms.assetid: 8fe72b2e-a9f1-435d-8eda-27056f112c6d
title: Método CBasePropertyPage.Help (Cprop.h)
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
ms.openlocfilehash: e2f97f7edd1e719eb44ff1d41929d7cb3864d8117eabb383b4318688adfa537f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955094"
---
# <a name="cbasepropertypagehelp-method"></a>Método CBasePropertyPage.Help

El `Help` método invoca la ayuda de la página de propiedades. Este método implementa el método **IPropertyPage::Help.**

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

Puntero a la cadena bajo la **clave HelpDir** en la información de CLSID de la página de propiedades en el Registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ NOTIMPL.

## <a name="remarks"></a>Comentarios

En la clase base, el método siempre devuelve E \_ NOTIMPL. Cuando se produce un error en el método , el marco llama **a IPropertyPage::GetPageInfo** para obtener el nombre del archivo de ayuda y el identificador de contexto. De forma predeterminada, son **NULL.** Por lo tanto, para proporcionar ayuda, la clase derivada puede invalidar el método o `Help` [**el método CBasePropertyPage::GetPageInfo.**](cbasepropertypage-getpageinfo.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePropertyPage (clase)**](cbasepropertypage.md)
</dt> </dl>

 

 





---
description: Método de constructor.
ms.assetid: 5d9863e7-fdd9-4df2-a603-34a240a2286c
title: Constructor CBasePropertyPage. CBasePropertyPage (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 915bc42cfb7f152cc061dab76caede6c998edf8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670429"
---
# <a name="cbasepropertypagecbasepropertypage-constructor"></a>Constructor CBasePropertyPage. CBasePropertyPage

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CBasePropertyPage(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   int       DialogId,
   int       TitleId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* 
</dt> <dd>

Cadena que contiene el nombre del objeto, con fines de depuración. Para obtener más información, vea [**CBaseObject:: CBaseObject**](cbaseobject-cbaseobject.md).

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntero a la interfaz **IUnknown** de agregación.

</dd> <dt>

*DialogId* 
</dt> <dd>

IDENTIFICADOR de recurso del cuadro de diálogo.

</dd> <dt>

*TitleId* 
</dt> <dd>

IDENTIFICADOR de recurso de la cadena que contiene el título del cuadro de diálogo.

</dd> </dl>

## <a name="examples"></a>Ejemplos


```C++
CMyProp::CMyProp(IUnknown *pUnk) : 
    CBasePropertyPage(NAME("MyPropPage"), pUnk, IDD_PROPPAGE, IDS_TITLE),
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 





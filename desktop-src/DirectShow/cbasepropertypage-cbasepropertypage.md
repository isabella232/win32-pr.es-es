---
description: 'Constructor CBasePropertyPage.CBasePropertyPage: método constructor.'
ms.assetid: 5d9863e7-fdd9-4df2-a603-34a240a2286c
title: Constructor CBasePropertyPage.CBasePropertyPage (Cprop.h)
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
ms.openlocfilehash: 95821062b6b1199ea98a5329934d76e2197901d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119953"
---
# <a name="cbasepropertypagecbasepropertypage-constructor"></a>Constructor CBasePropertyPage.CBasePropertyPage

Método constructor.

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

Cadena que contiene el nombre del objeto, con fines de depuración. Para obtener más información, [**vea CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).

</dd> <dt>

*Punk* 
</dt> <dd>

Puntero a la interfaz **IUnknown de agregación.**

</dd> <dt>

*DialogId* 
</dt> <dd>

Identificador de recurso para el cuadro de diálogo.

</dd> <dt>

*TitleId* 
</dt> <dd>

Identificador de recurso de la cadena que contiene el título del cuadro de diálogo.

</dd> </dl>

## <a name="examples"></a>Ejemplos


```C++
CMyProp::CMyProp(IUnknown *pUnk) : 
    CBasePropertyPage(NAME("MyPropPage"), pUnk, IDD_PROPPAGE, IDS_TITLE),
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop.h (incluir Streams.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePropertyPage (clase)**](cbasepropertypage.md)
</dt> </dl>

 

 





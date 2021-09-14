---
description: 'Constructor CTransInPlaceFilter.CTransInPlaceFilter: método constructor.'
ms.assetid: f0d30125-5d16-470c-a5fb-a7df96814dad
title: Constructor CTransInPlaceFilter.CTransInPlaceFilter (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6b14af4b0d1f33933db8ca2fd1835e9711edad9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255290"
---
# <a name="ctransinplacefilterctransinplacefilter-constructor"></a>Constructor CTransInPlaceFilter.CTransInPlaceFilter

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CTransInPlaceFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   REFCLSID  clsid,
   HRESULT   *phr,
   bool      bModifiesData = TRUE
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pObjectName* 
</dt> <dd>

Cadena que contiene el nombre de depuración del filtro. Para obtener más información, vea [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*lpUnk* 
</dt> <dd>

Puntero al propietario de este objeto. Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación. De lo contrario, establezca este parámetro en **NULL.**

</dd> <dt>

*Clsid* 
</dt> <dd>

Identificador de clase del filtro.

</dd> <dt>

*Phr* 
</dt> <dd>

ignorado.

</dd> <dt>

*bModifiesData* 
</dt> <dd>

Valor booleano que especifica si el filtro modifica los datos de entrada. Si **es TRUE,** el filtro modifica los datos. De lo contrario, el filtro pasa los datos de nivel inferior sin modificar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransInPlaceFilter (clase)**](ctransinplacefilter.md)
</dt> </dl>

 

 





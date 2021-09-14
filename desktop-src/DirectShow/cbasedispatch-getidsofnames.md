---
description: 'Método CBaseDispatch.GetIDsOfNames: el método GetIDsOfNames asigna un conjunto de nombres a un conjunto correspondiente de DISPIDs.'
ms.assetid: 0c0a2726-e89a-4eaf-aab0-e7e9e82e3c34
title: Método CBaseDispatch.GetIDsOfNames (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f3b718c95d588ffdc7fa63902e6b26ffbf11fd6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361405"
---
# <a name="cbasedispatchgetidsofnames-method"></a>CBaseDispatch.GetIDsOfNames (método)

El `GetIDsOfNames` método asigna un conjunto de nombres a un conjunto correspondiente de DISPID.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*riid* 
</dt> <dd>

Referencia a un identificador de interfaz (IID) que especifica la interfaz.

</dd> <dt>

*rgszNames* 
</dt> <dd>

Dirección de una matriz de cadenas de caracteres anchos que contienen los nombres que se asignarán.

</dd> <dt>

*cNames* 
</dt> <dd>

Tamaño de la matriz especificada por el *parámetro rgszNames.*

</dd> <dt>

*lcid* 
</dt> <dd>

Contexto de configuración regional en el que se interpretarán los nombres. Puede ser **NULL.**

</dd> <dt>

*rgdispid* 
</dt> <dd>

Puntero a una matriz que recibe los DISPID. Cada elemento de recibe un identificador que corresponde a uno de los nombres pasados en el *parámetro rgszNames.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                         | Descripción                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Correcto.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Memoria insuficiente.<br/>                     |
| <dl> <dt>**DISP \_ E \_ UNKNOWNNAME**</dt> </dl> | No se conocían uno o varios de los nombres.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método se comporta como el método **IDispatch::GetIDsOfNames,** pero el *parámetro riid* especifica la interfaz en la que se recuperan DISPID. (En la **versión de IDispatch,** el *parámetro riid* está reservado).

Si el método devuelve DISP \_ E UNKNOWNNAME, los DISPID devueltos contienen DISPID UNKNOWN para cada entrada que \_ corresponde a un nombre \_ desconocido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseDispatch (clase)**](cbasedispatch.md)
</dt> </dl>

 

 





---
description: La función AMovieSetupRegisterFilter2 registra los valores, las marcas y los tipos de medios de un filtro en el registro mediante la interfaz IFilterMapper2.
ms.assetid: 8e0f3485-9e5d-4b22-853d-4ad9b1fb71d2
title: Función AMovieSetupRegisterFilter2 (Dllsetup.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 272b781cf70f1dede9d4eea64b45d3d9d793a119
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162297"
---
# <a name="amoviesetupregisterfilter2-function"></a>Función AMovieSetupRegisterFilter2

La **función AMovieSetupRegisterFilter2** registra los valores, las marcas y los tipos de medios de un filtro en el registro mediante la [**interfaz IFilterMapper2.**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AMovieDllRegisterServer(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper2             *pIFM2,
         BOOL                       bRegister
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*psetupdata* 
</dt> <dd>

Puntero a los [**datos filter \_ de AMOVIESETUP.**](amoviesetup-filter.md)

</dd> <dt>

*pIFM2* 
</dt> <dd>

Puntero a [**la interfaz IFilterMapper2.**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)

</dd> <dt>

*bRegister* 
</dt> <dd>

Valor que indica si se va a registrar el filtro; **TRUE** indica registrar el filtro, **FALSE** indica anular el registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

La [**función AMovieDllRegisterServer2**](amoviedllregisterserver2.md) llama a esta función auxiliar para registrar un filtro una vez registrado el servidor COM.

Normalmente, un filtro usará [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) y no llamará a esta función directamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dllsetup.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones de instalación de DLL**](dll-setup-functions.md)
</dt> </dl>

 

 





---
description: La función AMovieSetupRegisterFilter2 registra los valores, los pines y los tipos de medios de un filtro en el Registro mediante la interfaz IFilterMapper2.
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
ms.openlocfilehash: 69b37fcf3e680cb8a64155aaf1474a8234934fe34bb5349151252ec7500e87a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118001870"
---
# <a name="amoviesetupregisterfilter2-function"></a>Función AMovieSetupRegisterFilter2

La **función AMovieSetupRegisterFilter2** registra los valores, los pines y los tipos de medios de un filtro en el Registro mediante la [**interfaz IFilterMapper2.**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)

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

Puntero a los [**datos del filtro \_ de AMOVIESETUP.**](amoviesetup-filter.md)

</dd> <dt>

*pIFM2* 
</dt> <dd>

Puntero a [**la interfaz IFilterMapper2.**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)

</dd> <dt>

*bRegister* 
</dt> <dd>

Valor que indica si se debe registrar el filtro; **TRUE** indica registrar el filtro, **FALSE** indica anular el registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

La [**función AMovieDllRegisterServer2**](amoviedllregisterserver2.md) llama a esta función auxiliar para registrar un filtro una vez registrado el servidor COM.

Normalmente, un filtro usará [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) y no llamará directamente a esta función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dllsetup.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones de instalación de DLL**](dll-setup-functions.md)
</dt> </dl>

 

 





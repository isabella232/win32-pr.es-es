---
description: La función AMovieSetupRegisterFilter2 registra los tipos de méritos, PIN y medios de un filtro en el registro mediante la interfaz IFilterMapper2.
ms.assetid: 8e0f3485-9e5d-4b22-853d-4ad9b1fb71d2
title: Función AMovieSetupRegisterFilter2 (Dllsetup. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661115"
---
# <a name="amoviesetupregisterfilter2-function"></a>AMovieSetupRegisterFilter2 función)

La función **AMovieSetupRegisterFilter2** registra los tipos de méritos, PIN y medios de un filtro en el registro mediante la interfaz [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .

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

Puntero a los datos del [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) .

</dd> <dt>

*pIFM2* 
</dt> <dd>

Puntero a la interfaz [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .

</dd> <dt>

*bRegister* 
</dt> <dd>

Valor que indica si se debe registrar el filtro; **True** indica que se registra el filtro; **false** indica que se anula el registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

La función [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) llama a esta función auxiliar para registrar un filtro después de que se haya registrado el servidor com.

Normalmente, un filtro usará [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) y no llamará directamente a esta función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dllsetup. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones de instalación de DLL**](dll-setup-functions.md)
</dt> </dl>

 

 





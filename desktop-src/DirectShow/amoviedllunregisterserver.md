---
description: Obsoleto. Use AMovieDllRegisterServer2 en su lugar.
ms.assetid: 80f52109-6239-4e3d-a395-eb69f5278cd2
title: Función AMovieDllUnregisterServer (Dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllUnregisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cab526a69f14cdd4c4f48767ca34722f61002eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690799"
---
# <a name="amoviedllunregisterserver-function"></a>AMovieDllUnregisterServer función)

Obsoleto. Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) en su lugar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AMovieDllUnregisterServer(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dllsetup. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones de instalación de DLL**](dll-setup-functions.md)
</dt> </dl>

 

 





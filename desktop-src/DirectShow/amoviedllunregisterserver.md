---
description: 'Función AMovieDllUnregisterServer: obsoleta. Use AMovieDllRegisterServer2 en su lugar.'
ms.assetid: 80f52109-6239-4e3d-a395-eb69f5278cd2
title: Función AMovieDllUnregisterServer (Dllsetup.h)
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
ms.openlocfilehash: df7fb34246249298efc143b7ccc8e6332540867c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099933"
---
# <a name="amoviedllunregisterserver-function"></a>Función AMovieDllUnregisterServer

Obsoleto. Use [**AMovieDllRegisterServer2 en**](amoviedllregisterserver2.md) su lugar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AMovieDllUnregisterServer(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dllsetup.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones de instalación de DLL**](dll-setup-functions.md)
</dt> </dl>

 

 





---
title: Función WMDRMShutdown (wmdrmsdk. h)
description: La función WMDRMShutdown libera los recursos utilizados por las API extendidas del cliente DRM de Windows Media.
ms.assetid: fa99a07a-2f07-464b-b7a2-e8f3110389b5
keywords:
- Función WMDRMShutdown formato de Windows Media
topic_type:
- apiref
api_name:
- WMDRMShutdown
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb49049a593699a4071eefea9c5cf7c61571fc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678985"
---
# <a name="wmdrmshutdown-function"></a>WMDRMShutdown función)

La función **WMDRMShutdown** libera los recursos utilizados por las API extendidas del cliente DRM de Windows Media.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE WMDRMShutdown(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Para evitar pérdidas de memoria, debe llamar a esta función para cada llamada de la función [**WMDRMStartup**](wmdrmstartup.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Wmdrmsdk.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones**](drm-functions.md)
</dt> </dl>

 

 






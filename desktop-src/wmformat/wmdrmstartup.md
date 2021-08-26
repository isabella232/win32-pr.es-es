---
title: Función WMDRMStartup (Wmdrmsdk.h)
description: La función WMDRMStartup inicializa los recursos usados por las API extendidas de Windows DRM multimedia.
ms.assetid: 2fd26bcc-8106-4356-933a-d4cf3536f4fb
keywords:
- Formato multimedia de la función WMDRMStartup
topic_type:
- apiref
api_name:
- WMDRMStartup
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c194a8c060ad1626fde796510c25c83e3e163dafffe9c17df17a7dcec890be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928754"
---
# <a name="wmdrmstartup-function"></a>Función WMDRMStartup

La **función WMDRMStartup** inicializa los recursos usados por las API extendidas de Windows DRM multimedia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE WMDRMStartup(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Para cada llamada de esta función, debe llamar a [**WMDRMShutdown para**](wmdrmshutdown.md) liberar los recursos usados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Wmdrmsdk.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones**](drm-functions.md)
</dt> </dl>

 

 






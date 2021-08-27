---
title: Función WMDRMCreateProtectedProvider (Wmdrmsdk.h)
description: La función WMDRMCreateProtectedProvider crea un generador de clases que puede crear los demás objetos de las API extendidas Windows cliente DRM multimedia.
ms.assetid: 0882062f-48a2-43bc-8853-a8a3d6bc2f52
keywords:
- Formato multimedia de la función WMDRMCreateProtectedProvider
topic_type:
- apiref
api_name:
- WMDRMCreateProtectedProvider
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4b5d71ff1deed01cc10d7342286b443b9f64b1a1c192af575a599a2fc8d8c9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026933"
---
# <a name="wmdrmcreateprotectedprovider-function"></a>Función WMDRMCreateProtectedProvider

La **función WMDRMCreateProtectedProvider** crea un generador de clases que puede crear los demás objetos de las API extendidas Windows cliente DRM multimedia. Esta función requiere una biblioteca de código auxiliar de Microsoft y crea objetos que admiten las características de DRM protegidas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProtectedProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppDRMProvider* \[ out\]
</dt> <dd>

Recibe un puntero a la [**interfaz IWMDRMProvider**](iwmdrmprovider.md) del objeto recién creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones**](drm-functions.md)
</dt> <dt>

[**WMDRMCreateProvider**](wmdrmcreateprovider.md)
</dt> </dl>

 

 






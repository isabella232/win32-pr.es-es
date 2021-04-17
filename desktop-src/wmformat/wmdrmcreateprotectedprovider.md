---
title: Función WMDRMCreateProtectedProvider (wmdrmsdk. h)
description: La función WMDRMCreateProtectedProvider crea un generador de clases que puede crear los demás objetos de las API extendidas del cliente DRM de Windows Media.
ms.assetid: 0882062f-48a2-43bc-8853-a8a3d6bc2f52
keywords:
- Función WMDRMCreateProtectedProvider formato de Windows Media
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
ms.openlocfilehash: f1f046de906c7753fa200de5075cf2064721940b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698648"
---
# <a name="wmdrmcreateprotectedprovider-function"></a>WMDRMCreateProtectedProvider función)

La función **WMDRMCreateProtectedProvider** crea un generador de clases que puede crear los demás objetos de las API extendidas del cliente DRM de Windows Media. Esta función requiere una biblioteca de código auxiliar de Microsoft y crea objetos que admiten las características DRM protegidas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProtectedProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppDRMProvider* \[ enuncia\]
</dt> <dd>

Recibe un puntero a la interfaz [**IWMDRMProvider**](iwmdrmprovider.md) del objeto recién creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones**](drm-functions.md)
</dt> <dt>

[**WMDRMCreateProvider**](wmdrmcreateprovider.md)
</dt> </dl>

 

 






---
title: Función WMDRMCreateProvider (wmdrmsdk. h)
description: La función WMDRMCreateProvider crea un generador de clases que puede crear los demás objetos de las API extendidas del cliente DRM de Windows Media.
ms.assetid: 25ec2fbf-136a-4f40-b2d3-f35b42178c60
keywords:
- Función WMDRMCreateProvider formato de Windows Media
topic_type:
- apiref
api_name:
- WMDRMCreateProvider
api_location:
- Wmdrmsdk.dll
- Ext-MS-Win-mm-wmdrmsdk-l1-1-0.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cdf7a102d969ce916f8a5692d994c183305409a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718671"
---
# <a name="wmdrmcreateprovider-function"></a>WMDRMCreateProvider función)

La función **WMDRMCreateProvider** crea un generador de clases que puede crear los demás objetos de las API extendidas del cliente DRM de Windows Media. Esta función no requiere una biblioteca de código auxiliar de Microsoft y crea objetos que no admiten las características DRM protegidas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProvider(
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



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Wmdrmsdk.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones**](drm-functions.md)
</dt> <dt>

[**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md)
</dt> </dl>

 

 






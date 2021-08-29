---
title: Función WMDRMCreateProvider (Wmdrmsdk.h)
description: La función WMDRMCreateProvider crea un generador de clases que puede crear los demás objetos de las API extendidas del cliente DRM de Windows media.
ms.assetid: 25ec2fbf-136a-4f40-b2d3-f35b42178c60
keywords:
- Formato multimedia de la función WMDRMCreateProvider
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
ms.openlocfilehash: 82de65423d5bc6ad2fbd55e3d8e4c97e8f63f6f7d6b6203e092176a4afc0183c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006565"
---
# <a name="wmdrmcreateprovider-function"></a>Función WMDRMCreateProvider

La **función WMDRMCreateProvider** crea un generador de clases que puede crear los demás objetos de las API extendidas de Windows DRM multimedia. Esta función no requiere una biblioteca de código auxiliar de Microsoft y crea objetos que no admiten las características de DRM protegidas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppDRMProvider* \[ out\]
</dt> <dd>

Recibe un puntero a [**la interfaz IWMDRMProvider**](iwmdrmprovider.md) del objeto recién creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Wmdrmsdk.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones**](drm-functions.md)
</dt> <dt>

[**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md)
</dt> </dl>

 

 






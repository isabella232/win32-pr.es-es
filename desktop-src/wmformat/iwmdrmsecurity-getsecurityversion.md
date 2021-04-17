---
title: Método IWMDRMSecurity GetSecurityVersion (wmdrmsdk. h)
description: El método GetSecurityVersion recupera la versión del subsistema DRM en el equipo cliente.
ms.assetid: ec97dec8-61ba-4424-b5eb-2e6885cc1f48
keywords:
- Método GetSecurityVersion formato de Windows Media
- Método GetSecurityVersion formato de Windows Media, interfaz IWMDRMSecurity
- Interfaz IWMDRMSecurity formato de Windows Media, método GetSecurityVersion
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetSecurityVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33be994383a7e16d136aac340a77deef8256d62f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670741"
---
# <a name="iwmdrmsecuritygetsecurityversion-method"></a>IWMDRMSecurity:: GetSecurityVersion (método)

El método **GetSecurityVersion** recupera la versión del subsistema DRM en el equipo cliente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSecurityVersion(
  [out] BSTR *pbstrVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbstrVersion* \[ enuncia\]
</dt> <dd>

Dirección de una variable que recibe el número de versión del subsistema DRM.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

El número de versión se expresa como una cadena que consta de cuatro números separados por puntos. El primer número es el número de versión principal, que normalmente se establece en 2. El segundo número es el número de versión secundaria, comprendido entre 2 y 10. El tercer número siempre se establece en 0. El cuarto número se establece en 0 o 1, y es un valor booleano que indica si el subsistema se ha individualizado. Por ejemplo, un número de versión "2.4.0.1" indica la cuarta versión secundaria individual de la segunda versión principal.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 






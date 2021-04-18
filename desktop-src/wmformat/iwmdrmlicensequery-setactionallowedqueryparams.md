---
title: Método IWMDRMLicenseQuery SetActionAllowedQueryParams (wmdrmsdk. h)
description: El método SetActionAllowedQueryParams establece la información específica del entorno para obtener resultados de consulta más precisos cuando se usa el método QueryActionAllowed.
ms.assetid: 1c8f9d4e-999d-4d7c-87fd-9d30e432350c
keywords:
- Método SetActionAllowedQueryParams formato de Windows Media
- Método SetActionAllowedQueryParams formato de Windows Media, interfaz IWMDRMLicenseQuery
- Interfaz IWMDRMLicenseQuery formato de Windows Media, método SetActionAllowedQueryParams
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.SetActionAllowedQueryParams
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a83a28c4d9f3758b711c43ddd83a509c58f8ea8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679146"
---
# <a name="iwmdrmlicensequerysetactionallowedqueryparams-method"></a>IWMDRMLicenseQuery:: SetActionAllowedQueryParams (método)

El método **SetActionAllowedQueryParams** establece la información específica del entorno para obtener resultados de consulta más precisos cuando se usa el método [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetActionAllowedQueryParams(
  [in] BOOL  fIsMF,
  [in] DWORD dwAppSecLevel,
  [in] BOOL  fHasSerialNumber,
  [in] BSTR  bstrDeviceCert
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fIsMF* \[ de\]
</dt> <dd>

Especifica si el contenido se representará mediante los objetos del SDK de Microsoft Media Foundation. **False** indica la representación de los objetos del SDK de Windows Media Format. Este parámetro es opcional.

</dd> <dt>

*dwAppSecLevel* \[ de\]
</dt> <dd>

Nivel de seguridad de la aplicación que se consulta. Este valor solo es importante si se van a utilizar los objetos del SDK de Windows Media Format, en cuyo caso *fIsMF* debe establecerse en **false**. Este parámetro es opcional.

</dd> <dt>

*fHasSerialNumber* \[ de\]
</dt> <dd>

Especifica si el dispositivo de destino para una operación de copia tiene un número de serie. Este parámetro es opcional y solo se aplica a las consultas de operaciones de copia.

</dd> <dt>

*bstrDeviceCert* \[ de\]
</dt> <dd>

Certificado de dispositivo del dispositivo de destino al usar DRM de Windows Media para dispositivos portátiles. Este parámetro es opcional y solo se aplica a las consultas de operaciones de copia.

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
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMLicenseQuery**](iwmdrmlicensequery.md)
</dt> <dt>

[**Consulta para obtener información detallada sobre los derechos**](querying-for-detailed-rights-information.md)
</dt> </dl>

 

 






---
title: Método IWMDRMLicenseQuery SetActionAllowedQueryParams (Wmdrmsdk.h)
description: El método SetActionAllowedQueryParams establece información específica del entorno para obtener resultados de consulta más precisos cuando se usa el método QueryActionAllowed.
ms.assetid: 1c8f9d4e-999d-4d7c-87fd-9d30e432350c
keywords:
- Método SetActionAllowedQueryParams windows Media Format
- Método SetActionAllowedQueryParams formato multimedia de windows, interfaz IWMDRMLicenseQuery
- IWMDRMLicenseQuery interface windows Media Format , SetActionAllowedQueryParams (método)
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
ms.openlocfilehash: 54dfa59300c9d222b13067524d2e9e174e1600adff98bbaaed3973a0168942ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655042"
---
# <a name="iwmdrmlicensequerysetactionallowedqueryparams-method"></a>IWMDRMLicenseQuery::SetActionAllowedQueryParams (método)

El **método SetActionAllowedQueryParams** establece información específica del entorno para obtener resultados de consulta más precisos cuando se usa [**el método QueryActionAllowed.**](iwmdrmlicensequery-queryactionallowed.md)

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

*fIsMF* \[ En\]
</dt> <dd>

Especifica si el contenido se representará mediante los objetos del SDK Microsoft Media Foundation sdk. **FALSE** indica la representación por parte de los objetos del SDK Windows Media Format. Este parámetro es opcional.

</dd> <dt>

*dwAppSecLevel* \[ En\]
</dt> <dd>

Nivel de seguridad de la aplicación de consulta. Este valor solo es importante si se usarán los objetos del SDK Windows Media Format, en cuyo caso *fIsMF* debe establecerse en **FALSE.** Este parámetro es opcional.

</dd> <dt>

*fHasSerialNumber* \[ En\]
</dt> <dd>

Especifica si el dispositivo de destino de una operación de copia tiene un número de serie. Este parámetro es opcional y solo se aplica a las consultas para las operaciones de copia.

</dd> <dt>

*bstrDeviceCert* \[ En\]
</dt> <dd>

Certificado de dispositivo del dispositivo de destino cuando se usa Windows DRM multimedia para dispositivos portátiles. Este parámetro es opcional y solo se aplica a las consultas para las operaciones de copia.

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
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDRMLicenseQuery (interfaz)**](iwmdrmlicensequery.md)
</dt> <dt>

[**Consulta de información detallada sobre los derechos**](querying-for-detailed-rights-information.md)
</dt> </dl>

 

 






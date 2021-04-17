---
title: Método IWMDRMLicenseQuery QueryActionAllowed (wmdrmsdk. h)
description: El método QueryActionAllowed realiza una consulta en el almacén de licencias local para recuperar el estado de la licencia de una o varias acciones DRM que se aplican a un identificador de clave especificado.
ms.assetid: 814c2850-c036-4c44-a64e-861e88f16fb1
keywords:
- Método QueryActionAllowed formato de Windows Media
- Método QueryActionAllowed formato de Windows Media, interfaz IWMDRMLicenseQuery
- Interfaz IWMDRMLicenseQuery formato de Windows Media, método QueryActionAllowed
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryActionAllowed
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6564062fc9f76a840b37f6e134e960480d67a2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680445"
---
# <a name="iwmdrmlicensequeryqueryactionallowed-method"></a>IWMDRMLicenseQuery:: QueryActionAllowed (método)

El método **QueryActionAllowed** realiza una consulta en el almacén de licencias local para recuperar el estado de la licencia de una o varias acciones DRM que se aplican a un identificador de clave especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT QueryActionAllowed(
  [in]  BSTR  bstrKID,
  [in]  BSTR  bstrMinReqIndivVersion,
  [in]  DWORD cActionsToQuery,
  [in]  BSTR  rgbstrActionsToQuery[],
  [out] DWORD rgdwQueryResult[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrKID* \[ de\]
</dt> <dd>

IDENTIFICADOR de clave que se va a consultar. Solo se evaluarán las licencias que se apliquen a este ID. de clave.

</dd> <dt>

*bstrMinReqIndivVersion* \[ de\]
</dt> <dd>

La versión de seguridad mínima especificada en el encabezado del archivo ASF. Este parámetro es opcional. Pase **null** para realizar la consulta sin esta información.

</dd> <dt>

*cActionsToQuery* \[ de\]
</dt> <dd>

Número de acciones que se van a consultar. Este valor debe establecerse en el número de elementos de las matrices que se pasan para los parámetros *rgbstrActionsToQuery* y *rgdwQueryResult* .

</dd> <dt>

*\[ rgbstrActionsToQuery \]* \[en\]
</dt> <dd>

Matriz de uno o más derechos que se van a consultar. Esta matriz debe contener tantos elementos como especifique el *cActionsToQuery*. Cada elemento debe establecerse en una de las constantes siguientes:



| Constante                                         | Descripción                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------|
| g \_ wszWMDRM \_ ActionAllowed \_ reproducción             | Incluir para consultar el derecho a reproducir el contenido.                              |
| g \_ wszWMDRM \_ ActionAllowed \_                 | Incluir para consultar el derecho a copiar el contenido en dispositivos o medios externos. |
| g \_ wszWMDRM \_ ActionAllowed \_ PlaylistBurn         | Incluir para consultar el derecho a copiar el contenido en CD como parte de una lista de reproducción.  |
| g \_ wszWMDRM \_ ActionAllowed \_ CreateThumbnailImage | Incluir para consultar el derecho a crear una imagen en miniatura a partir del contenido.     |
| g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD             | Incluir para consultar el derecho a copiar el contenido en el CD.                        |



 

</dd> <dt>

*\[ rgdwQueryResult \]* \[fuera de\]
</dt> <dd>

Matriz de una o varias variables DWORD que reciben los resultados de la consulta para los derechos especificados por *rgbstrActionsToQuery*. Si se permite una acción, el elemento correspondiente se establece en cero. Si no se permite una acción, el elemento se establece en uno o más valores de la enumeración de [**\_ \_ \_ \_ resultados de consulta permitidos de la acción DRM**](drm-action-allowed-query-results.md) combinados mediante la operación OR bit a bit. Esta matriz debe contener tantos elementos como especifique el *cActionsToQuery*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Al consultar los derechos de reproducción y copia, obtendrá resultados más precisos estableciendo primero los parámetros de entorno. Use el método [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) para establecer los parámetros de entorno. Los resultados de las consultas para el derecho de grabación no se ven afectados por los parámetros del entorno. puede usar los valores predeterminados de forma segura.

Los resultados devueltos por el método **QueryActionAllowed** se agregan a partir de cero o más licencias en el almacén de licencias local. El método no puede buscar en todas las licencias que se aplican al identificador de clave si encuentra un resultado habilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMLicenseQuery**](iwmdrmlicensequery.md)
</dt> <dt>

[**Consulta de información de derechos simples**](querying-for-simple-rights-information.md)
</dt> </dl>

 

 






---
title: Método IWMDRMLicenseQuery QueryActionAllowed (Wmdrmsdk.h)
description: El método QueryActionAllowed realiza una consulta en el almacén de licencias local para recuperar el estado de licencia de una o varias acciones drm que se aplican a un identificador de clave especificado.
ms.assetid: 814c2850-c036-4c44-a64e-861e88f16fb1
keywords:
- Método QueryActionAllowed windows Media Format
- Método QueryActionAllowed windows Media Format , IWMDRMLicenseQuery (interfaz)
- IWMDRMLicenseQuery interface windows Media Format , QueryActionAllowed (método)
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
ms.openlocfilehash: 9f6974a04f92852ef9e56b473126eb8e0cc2d92a9bdcf5192e10abe800978bcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846879"
---
# <a name="iwmdrmlicensequeryqueryactionallowed-method"></a>IWMDRMLicenseQuery::QueryActionAllowed (método)

El **método QueryActionAllowed** realiza una consulta en el almacén de licencias local para recuperar el estado de licencia de una o varias acciones drm que se aplican a un identificador de clave especificado.

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

*bstrKID* \[ En\]
</dt> <dd>

Identificador de clave para el que se va a consultar. Solo se evaluarán las licencias que se apliquen a este identificador de clave.

</dd> <dt>

*bstrMinReqIndivVersion* \[ En\]
</dt> <dd>

Versión de seguridad mínima especificada en el encabezado del archivo ASF. Este parámetro es opcional. Pase **NULL** para realizar la consulta sin esta información.

</dd> <dt>

*cActionsToQuery* \[ En\]
</dt> <dd>

Número de acciones para las que se va a consultar. Este valor debe establecerse en el número de elementos de las matrices pasadas para los parámetros *rgbstrActionsToQuery* y *rgdwQueryResult.*

</dd> <dt>

*rgbstrActionsToQuery \[ \]* \[en\]
</dt> <dd>

Matriz de uno o varios derechos para los que se va a consultar. Esta matriz debe contener tantos elementos como haya especificado *cActionsToQuery.* Cada elemento debe establecerse en una de las siguientes constantes:



| Constante                                         | Descripción                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------|
| g \_ wszWMDRM \_ ActionAllowed \_ Playback             | Incluya para consultar el derecho a reproducir el contenido.                              |
| g \_ wszWMDRM \_ ActionAllowed \_ Copy                 | Incluya para consultar el derecho a copiar el contenido en dispositivos o medios externos. |
| g \_ wszWMDRM ActionAllowed Playlist (Acción wszWMDRM)Lista \_ de reproducción \_ permitido         | Incluya para consultar el derecho a copiar el contenido en CD como parte de una lista de reproducción.  |
| g \_ wszWMDRM \_ ActionAllowed \_ CreateThumbnailImage | Incluya para consultar el derecho a crear una imagen en miniatura a partir del contenido.     |
| g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD             | Incluya para consultar el derecho a copiar el contenido en CD.                        |



 

</dd> <dt>

*rgdwQueryResult \[ \]* \[out\]
</dt> <dd>

Matriz de una o varias variables DWORD que reciben los resultados de la consulta para los derechos especificados por *rgbstrActionsToQuery*. Si se permite una acción, el elemento correspondiente se establece en cero. Si no se permite una acción, el elemento se establece en uno o varios valores de la enumeración [**DRM ACTION ALLOWED QUERY \_ \_ \_ \_ RESULTS**](drm-action-allowed-query-results.md) combinada mediante la operación OR bit a bit. Esta matriz debe contener tantos elementos como haya especificado *cActionsToQuery.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Al consultar los derechos de reproducción y copia, se obtienen resultados más precisos estableciendo primero los parámetros del entorno. Use el [**método SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) para establecer los parámetros del entorno. Los resultados de las consultas para la derecha de la grabación no se ven afectados por los parámetros del entorno; puede usar los valores predeterminados de forma segura.

Los resultados devueltos **por el método QueryActionAllowed** se agregan desde cero o más licencias en el almacén de licencias local. Es posible que el método no busque todas las licencias que se aplican al identificador de clave si encuentra un resultado habilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWMDRMLicenseQuery (interfaz)**](iwmdrmlicensequery.md)
</dt> <dt>

[**Consulta de información de derechos simples**](querying-for-simple-rights-information.md)
</dt> </dl>

 

 






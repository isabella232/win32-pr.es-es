---
description: El método QuerySupported determina si un objeto admite un conjunto de propiedades especificado.
ms.assetid: eda0325c-dba4-4d9f-81e2-7fd67d5b9873
title: 'Método IKsPropertySet:: QuerySupported (KS. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.QuerySupported
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: a13c8523d45278ad403ee08d0822fb853b301520
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274709"
---
# <a name="ikspropertysetquerysupported-method"></a>IKsPropertySet:: QuerySupported (método)

El `QuerySupported` método determina si un objeto admite un conjunto de propiedades especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT QuerySupported(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [out] DWORD   *pTypeSupport
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*guidPropSet* \[ de\]
</dt> <dd>

GUID del conjunto de propiedades.

</dd> <dt>

*dwPropID* \[ de\]
</dt> <dd>

Identificador de la propiedad dentro del conjunto de propiedades.

</dd> <dt>

*pTypeSupport* \[ enuncia\]
</dt> <dd>

Puntero a un valor en el que se van a almacenar marcas que indican la compatibilidad proporcionada por el controlador. Entre las marcas admitidas se incluyen las siguientes.



| Value                    | Descripción                                                                                            |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| \_obtención de soporte técnico de KSPROPERTY \_ | Puede recuperar la propiedad llamando al método [**IKsPropertySet:: get**](ikspropertyset-get.md) . |
| \_conjunto de soporte de KSPROPERTY \_ | Puede cambiar la propiedad llamando a [**IKsPropertySet:: set**](ikspropertyset-set.md).              |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                                              | Descripción                                                                     |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                     | Se admiten el conjunto de propiedades especificado y la combinación de ID. de propiedad.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                | No se admite el conjunto de propiedades.<br/>                                       |
| <dl> <dt>**E \_ \_ ID. de prop \_ no compatible**</dt> </dl>  | No se admite el identificador de propiedad para el conjunto de propiedades especificado.<br/>         |
| <dl> <dt>**E \_ prop \_ set \_ no compatible**</dt> </dl> | No se admite el conjunto de propiedades.<br/>                                       |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> Existe otra interfaz con este nombre en el archivo de encabezado dsound. h. Las dos interfaces no son compatibles. La interfaz **IKsControl** , documentada en el DDK de DirectShow, es ahora la interfaz recomendada para pasar conjuntos de propiedades entre controladores WDM y componentes de modo de usuario.

 

Debe incluir KS. h antes de ksproxy. h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                             |
| Encabezado<br/>                   | <dl> <dt>KS. h; </dt> <dt>Ksproxy. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Strmiids. lib</dt> </dl>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> <dt>

[**Interfaz IKsPropertySet**](ikspropertyset.md)
</dt> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 





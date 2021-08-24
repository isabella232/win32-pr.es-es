---
description: El método QuerySupported determina si un objeto admite un conjunto de propiedades especificado.
ms.assetid: eda0325c-dba4-4d9f-81e2-7fd67d5b9873
title: Método IKsPropertySet::QuerySupported (Ks.h)
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
ms.openlocfilehash: 7c79e81171349e2c481535eeab212717de072b17778b052dac3fc377cea0e094
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792325"
---
# <a name="ikspropertysetquerysupported-method"></a>Método IKsPropertySet::QuerySupported

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

*guidPropSet* \[ En\]
</dt> <dd>

GUID del conjunto de propiedades.

</dd> <dt>

*dwPropID* \[ En\]
</dt> <dd>

Identificador de la propiedad dentro del conjunto de propiedades.

</dd> <dt>

*pTypeSupport* \[ out\]
</dt> <dd>

Puntero a un valor en el que se almacenan las marcas que indican la compatibilidad proporcionada por el controlador. Entre las marcas admitidas se incluyen las siguientes.



| Value                    | Descripción                                                                                            |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| KSPROPERTY \_ SUPPORT \_ GET | Puede recuperar la propiedad llamando al [**método IKsPropertySet::Get.**](ikspropertyset-get.md) |
| CONJUNTO DE COMPATIBILIDAD CON KSPROPERTY \_ \_ | Puede cambiar la propiedad llamando a [**IKsPropertySet::Set**](ikspropertyset-set.md).              |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                              | Descripción                                                                     |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Se admite la combinación de identificadores de propiedad y conjunto de propiedades especificados.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                | No se admite el conjunto de propiedades.<br/>                                       |
| <dl> <dt>**E \_ PROP \_ ID \_ UNSUPPORTED**</dt> </dl>  | No se admite el identificador de propiedad para el conjunto de propiedades especificado.<br/>         |
| <dl> <dt>**E \_ PROP \_ SET \_ UNSUPPORTED**</dt> </dl> | No se admite el conjunto de propiedades.<br/>                                       |



 

## <a name="remarks"></a>Comentarios

> [!Note]  
> Existe otra interfaz por este nombre en el archivo de encabezado d sound.h. Las dos interfaces no son compatibles. La **interfaz IKsControl,** documentada en el DDK de DirectShow, es ahora la interfaz recomendada para pasar conjuntos de propiedades entre los controladores WDM y los componentes del modo de usuario.

 

Debe incluir Ks.h antes que Ksproxy.h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                             |
| Encabezado<br/>                   | <dl> <dt>Ks.h; </dt> <dt>Ksproxy.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Strmiids.lib</dt> </dl>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> <dt>

[**IKsPropertySet (Interfaz)**](ikspropertyset.md)
</dt> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 





---
description: El método Set establece una propiedad identificada por un GUID de conjunto de propiedades y un identificador de propiedad.
ms.assetid: 78f506dc-7fb4-446d-863e-cffee9da5280
title: 'IKsPropertySet:: set (método) (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Set
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: b233cea7e131919d94b00afeb5a6e2ea3703c738
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422890"
---
# <a name="ikspropertysetset-method"></a>IKsPropertySet:: set (método)

El `Set` método establece una propiedad identificada por un GUID de conjunto de propiedades y un identificador de propiedad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Set(
  [in] REFGUID guidPropSet,
  [in] DWORD   dwPropID,
  [in] LPVOID  pInstanceData,
  [in] DWORD   cbInstanceData,
  [in] LPVOID  pPropData,
  [in] DWORD   cbPropData
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

*pInstanceData* \[ de\]
</dt> <dd>

Puntero a un búfer que contiene datos de instancia para la propiedad.

</dd> <dt>

*cbInstanceData* \[ de\]
</dt> <dd>

Tamaño del búfer de *pInstanceData* , en bytes.

</dd> <dt>

*pPropData* \[ de\]
</dt> <dd>

Puntero a un búfer que contiene el valor de la propiedad.

</dd> <dt>

*cbPropData* \[ de\]
</dt> <dd>

Sise del búfer *pPropData* , en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                                              | Descripción                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                     | Correcto.<br/>                                                         |
| <dl> <dt>**E \_ prop \_ set \_ no compatible**</dt> </dl> | No se admite el conjunto de propiedades.<br/>                               |
| <dl> <dt>**E \_ \_ ID. de prop \_ no compatible**</dt> </dl>  | El identificador de propiedad no es compatible con el conjunto de propiedades especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> Existe otra interfaz con este nombre en el archivo de encabezado dsound. h. Las dos interfaces no son compatibles. La interfaz **IKsControl** , documentada en el DDK de DirectShow, es ahora la interfaz recomendada para pasar conjuntos de propiedades entre controladores WDM y componentes de modo de usuario.

 

Debe incluir KS. h antes de ksproxy. h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Ksproxy. h</dt> </dl>    |
| Biblioteca<br/>                  | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> <dt>

[**Interfaz IKsPropertySet**](ikspropertyset.md)
</dt> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 





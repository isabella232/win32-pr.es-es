---
description: El método Set establece una propiedad identificada por un GUID del conjunto de propiedades y un identificador de propiedad.
ms.assetid: 78f506dc-7fb4-446d-863e-cffee9da5280
title: Método IKsPropertySet::Set (Ksproxy.h)
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
ms.openlocfilehash: f3669acb7f2d3049b909a4dc2c24363bf478c9b44ad0a91528e1e8ea466399fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639195"
---
# <a name="ikspropertysetset-method"></a>IKsPropertySet::Set (Método)

El `Set` método establece una propiedad identificada por un GUID del conjunto de propiedades y un identificador de propiedad.

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

*guidPropSet* \[ En\]
</dt> <dd>

GUID del conjunto de propiedades.

</dd> <dt>

*dwPropID* \[ En\]
</dt> <dd>

Identificador de la propiedad dentro del conjunto de propiedades.

</dd> <dt>

*pInstanceData* \[ En\]
</dt> <dd>

Puntero a un búfer que contiene datos de instancia para la propiedad .

</dd> <dt>

*cbInstanceData* \[ En\]
</dt> <dd>

Tamaño del búfer *pInstanceData,* en bytes.

</dd> <dt>

*pPropData* \[ En\]
</dt> <dd>

Puntero a un búfer que contiene el valor de la propiedad .

</dd> <dt>

*cbPropData* \[ En\]
</dt> <dd>

Sise del búfer *pPropData,* en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                              | Descripción                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Correcto.<br/>                                                         |
| <dl> <dt>**E \_ PROP \_ SET \_ UNSUPPORTED**</dt> </dl> | No se admite el conjunto de propiedades.<br/>                               |
| <dl> <dt>**E \_ PROP \_ ID \_ UNSUPPORTED**</dt> </dl>  | El identificador de propiedad no se admite para el conjunto de propiedades especificado.<br/> |



 

## <a name="remarks"></a>Comentarios

> [!Note]  
> Existe otra interfaz con este nombre en el archivo de encabezado dsound.h. Las dos interfaces no son compatibles. La **interfaz IKsControl,** documentada en DirectShow DDK, es ahora la interfaz recomendada para pasar conjuntos de propiedades entre los controladores WDM y los componentes del modo de usuario.

 

Debe incluir Ks.h antes de Ksproxy.h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Ksproxy.h</dt> </dl>    |
| Biblioteca<br/>                  | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> <dt>

[**IKsPropertySet (Interfaz)**](ikspropertyset.md)
</dt> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 





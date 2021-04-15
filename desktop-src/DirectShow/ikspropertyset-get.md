---
description: El método get recupera una propiedad identificada por un GUID de conjunto de propiedades y un identificador de propiedad.
ms.assetid: f39862db-0659-4533-8cee-aee2f778e085
title: 'IKsPropertySet:: get (método) (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Get
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 9c4461e8c5886d84bcf3b7faa6675b749bc0c37d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495076"
---
# <a name="ikspropertysetget-method"></a>IKsPropertySet:: get (método)

El método **Get** recupera una propiedad identificada por un GUID de conjunto de propiedades y un identificador de propiedad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Get(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [in]  LPVOID  pInstanceData,
  [in]  DWORD   cbInstanceData,
  [out] LPVOID  pPropData,
  [in]  DWORD   cbPropData,
  [out] DWORD   *pcbReturned
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

Puntero a una matriz de bytes que contiene datos de instancia para la propiedad.

</dd> <dt>

*cbInstanceData* \[ de\]
</dt> <dd>

Tamaño de la matriz proporcionado en *pInstanceData*, en bytes.

</dd> <dt>

*pPropData* \[ enuncia\]
</dt> <dd>

Puntero a una matriz de bytes que recibe los datos de la propiedad.

</dd> <dt>

*cbPropData* \[ de\]
</dt> <dd>

Tamaño de la matriz proporcionado en *pPropData*, en bytes.

</dd> <dt>

*pcbReturned* \[ enuncia\]
</dt> <dd>

Recibe el número de bytes que el método copia en la matriz *pPropData* .

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
> Existe otra interfaz con este nombre en el archivo de encabezado dsound. h. Las dos interfaces no son compatibles. La interfaz [IKsControl](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) , documentada en el DDK de DirectShow, es ahora la interfaz recomendada para pasar conjuntos de propiedades entre controladores WDM y componentes de modo de usuario.

 

Para recuperar una propiedad, asigne un búfer que este método rellenará. Para determinar el tamaño de búfer necesario, especifique **null** para *pPropData* y cero (0) para *cbPropData*. Este método devuelve el tamaño de búfer necesario en *pcbReturned*.

Debe incluir KS. h antes de ksproxy. h.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se consulta un PIN para su categoría de PIN mediante la recuperación de la propiedad de **\_ \_ categoría AMPROPERTY PIN** . (Consulte [conjunto de propiedades del PIN](pin-property-set.md)).


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



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

 

 

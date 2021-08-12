---
description: El método Get recupera una propiedad identificada por un GUID del conjunto de propiedades y un identificador de propiedad.
ms.assetid: f39862db-0659-4533-8cee-aee2f778e085
title: Método IKsPropertySet::Get (Ksproxy.h)
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
ms.openlocfilehash: fbfd44002270209c055b5a4003d9062a6821aeffb3ce71de7977fc20d0c64e81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652247"
---
# <a name="ikspropertysetget-method"></a>IKsPropertySet::Get (método)

El **método Get** recupera una propiedad identificada por un GUID del conjunto de propiedades y un identificador de propiedad.

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

*guidPropSet* \[ En\]
</dt> <dd>

GUID del conjunto de propiedades .

</dd> <dt>

*dwPropID* \[ En\]
</dt> <dd>

Identificador de la propiedad dentro del conjunto de propiedades.

</dd> <dt>

*pInstanceData* \[ En\]
</dt> <dd>

Puntero a una matriz de bytes que contiene datos de instancia para la propiedad .

</dd> <dt>

*cbInstanceData* \[ En\]
</dt> <dd>

Tamaño de la matriz especificada en *pInstanceData*, en bytes.

</dd> <dt>

*pPropData* \[ out\]
</dt> <dd>

Puntero a una matriz de bytes que recibe los datos de propiedad.

</dd> <dt>

*cbPropData* \[ En\]
</dt> <dd>

Tamaño de la matriz especificada en *pPropData*, en bytes.

</dd> <dt>

*pwReturned* \[ out\]
</dt> <dd>

Recibe el número de bytes que el método copia en la *matriz pPropData.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                              | Descripción                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Correcto.<br/>                                                         |
| <dl> <dt>**E \_ PROP \_ SET \_ UNSUPPORTED**</dt> </dl> | No se admite el conjunto de propiedades.<br/>                               |
| <dl> <dt>**E \_ PROP \_ ID \_ UNSUPPORTED**</dt> </dl>  | El identificador de propiedad no se admite para el conjunto de propiedades especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> Existe otra interfaz con este nombre en el archivo de encabezado dsound.h. Las dos interfaces no son compatibles. La [interfaz IKsControl,](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) documentada en DirectShow DDK, es ahora la interfaz recomendada para pasar conjuntos de propiedades entre los controladores WDM y los componentes del modo de usuario.

 

Para recuperar una propiedad, asigne un búfer que este método rellenará. Para determinar el tamaño de búfer necesario, especifique **NULL** para *pPropData* y cero (0) para *cbPropData.* Este método devuelve el tamaño de búfer necesario *en pwReturned.*

Debe incluir Ks.h antes de Ksproxy.h.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se consulta un pin para su categoría pin, recuperando la **propiedad AMPROPERTY \_ PIN \_ CATEGORY.** (Vea [Anclar conjunto de propiedades](pin-property-set.md)).


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

 

 

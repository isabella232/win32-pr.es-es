---
description: El método KsQueryMediums recupera los medios admitidos por un PIN.
ms.assetid: 554bf968-6054-4f9d-95db-facf0444641f
title: 'IKsPin:: KsQueryMediums (método) (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin.KsQueryMediums
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: f037317b49bc54f5ea9db5b7a4ae039ec0a9970d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806080"
---
# <a name="ikspinksquerymediums-method"></a>IKsPin:: KsQueryMediums (método)

El `KsQueryMediums` método recupera los medios admitidos por un PIN.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT KsQueryMediums(
  [out] KSMULTIPLE_ITEM **ppmi
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PPMI* \[ enuncia\]
</dt> <dd>

Dirección de un puntero a una estructura de [**\_ elementos KSMULTIPLE**](ksmultiple-item.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve S \_ correcto. Si se produce un error, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método devuelve una estructura de [**\_ elemento KSMULTIPLE**](ksmultiple-item.md) asignada por la tarea, seguida de cero o más estructuras [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) . El miembro **Count** de la estructura del **\_ elemento KSMULTIPLE** especifica el número de estructuras **REGPINMEDIUM** . Cada estructura **REGPINMEDIUM** define un medio admitido por el PIN.

El llamador debe liberar las estructuras devueltas mediante la función **CoTaskMemFree** .

Debe incluir KS. h antes de ksproxy. h.

## <a name="examples"></a>Ejemplos

La siguiente función auxiliar intenta hacer coincidir un pin con un medio especificado.


```C++
HRESULT FindMatchingMedium(
    IPin *pPin, 
    REGPINMEDIUM *pMedium, 
    bool *pfMatch)
{
    IKsPin* pKsPin = NULL;
    KSMULTIPLE_ITEM *pmi;

    *pfMatch = false;
    HRESULT hr = pPin->QueryInterface(IID_IKsPin, (void **)&pKsPin);
    if (FAILED(hr)) 
        return hr;  // Pin does not support IKsPin.

    hr = pKsPin->KsQueryMediums(&pmi);
    pKsPin->Release();
    if (FAILED(hr))
        return hr;  // Pin does not support mediums.

    if (pmi->Count) 
    {
        // Use pointer arithmetic to reference the first medium structure.
        REGPINMEDIUM *pTemp = (REGPINMEDIUM*)(pmi + 1);
        for (ULONG i = 0; i < pmi->Count; i++, pTemp++) 
        {
            if (pMedium->clsMedium == pTemp->clsMedium) 
            {
                *pfMatch = true;
                break;
            }
        }
    }        
    CoTaskMemFree(pmi);
    return S_OK;
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

[**Interfaz IKsPin**](ikspin.md)
</dt> <dt>

[Filtros de controlador de clase WDM](wdm-class-driver-filters.md)
</dt> </dl>

 

 





---
description: El método KsQueryMediums recupera los medios admitidos por un pin.
ms.assetid: 554bf968-6054-4f9d-95db-facf0444641f
title: Método IKsPin::KsQueryMediums (Ksproxy.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361321"
---
# <a name="ikspinksquerymediums-method"></a>Método IKsPin::KsQueryMediums

El `KsQueryMediums` método recupera los medios admitidos por un pin.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT KsQueryMediums(
  [out] KSMULTIPLE_ITEM **ppmi
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppmi* \[ out\]
</dt> <dd>

Dirección de un puntero a una [**estructura KSMULTIPLE \_ ITEM.**](ksmultiple-item.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve S \_ OK. Si se produce un error, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Este método devuelve una estructura [**KSMULTIPLE \_ ITEM**](ksmultiple-item.md) asignada por tareas, seguida de cero o más estructuras [**REGPINMEDIUM.**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) El **miembro Count** de la estructura **KSMULTIPLE \_ ITEM** especifica el número de **estructuras REGPINMEDIUM.** Cada **estructura REGPINMEDIUM** define un medio admitido por el pin.

El autor de la llamada debe liberar las estructuras devueltas mediante la **función CoTaskMemFree.**

Debe incluir Ks.h antes de Ksproxy.h.

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
| Encabezado<br/>                   | <dl> <dt>Ksproxy.h</dt> </dl>    |
| Biblioteca<br/>                  | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> <dt>

[**Interfaz IKsPin**](ikspin.md)
</dt> <dt>

[Filtros de controlador de clase WDM](wdm-class-driver-filters.md)
</dt> </dl>

 

 





---
description: El método CheckCapabilities consulta si la secuencia ha especificado funcionalidades de búsqueda. Este método implementa el método IMediaSeeking::CheckCapabilities.
ms.assetid: 5d37e179-9e04-44e1-acbc-dfd2682830c0
title: Método CSourceSeeking.CheckCapabilities (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 332e5fc461a39eff7ebfc70aa32a9a4d1a28a6928c15f6222e3804e2a542f6ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087055"
---
# <a name="csourceseekingcheckcapabilities-method"></a>Método CSourceSeeking.CheckCapabilities

El `CheckCapabilities` método consulta si la secuencia ha especificado funcionalidades de búsqueda. Este método implementa el [**método IMediaSeeking::CheckCapabilities.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCapabilities* 
</dt> <dd>

Puntero a una combinación bit a bit de uno o varios atributos [**DE AM SEEKING SEEKING \_ \_ \_ CAPABILITIES.**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** enumerados en la tabla siguiente.



| Código devuelto                                                                               | Descripción                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | No todas las funcionalidades de *pCapabilities* están presentes.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Todas las funcionalidades *de pCapabilities* están presentes.<br/>            |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | **Argumento de** puntero NULL.<br/>                                  |



 

## <a name="remarks"></a>Comentarios

Tal y como se implementó, este método comprueba el valor de *\* pCapabilities* con la variable miembro [**CSourceSeeking::m \_ dwSeekingCaps.**](csourceseeking-m-dwseekingcaps.md) Sin embargo, no establece *\* pCapabilities* igual a **m \_ dwSeekingCaps,** como se describe para el [**método IMediaSeeking::CheckCapabilities.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) Además, en el caso de que ninguna de las funcionalidades especificadas esté disponible, el método no devuelve E \_ FAIL. Una implementación más completa sería la siguiente:


```C++
STDMETHODIMP CheckCapabilities(DWORD *pCapabilities)
{
    CheckPointer(pCapabilities, E_POINTER)
;
    DWORD dwCaps;
    HRESULT hr = GetCapabilities(&dwCaps);
    if (SUCCEEDED(hr))
    {
        dwCaps &= *pCapabilities;
        if (dwCaps)
        {
            hr =  (dwCaps == *pCapabilities ? S_OK : S_FALSE );
        }
        else 
        {
            hr = E_FAIL;
        }
        *pCapabilities = dwCaps;
    }
    else 
    {
        *pCapabilities = 0;
    }
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 





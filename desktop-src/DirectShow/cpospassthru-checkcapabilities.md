---
description: El método CheckCapabilities consulta si una secuencia ha especificado funcionalidades de búsqueda. Este método implementa el método IMediaSeeking::CheckCapabilities.
ms.assetid: 48096af6-bbce-4a1f-be9a-fd150ed4536e
title: Método CPosPassThru.CheckCapabilities (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f1146e11097dbb2d717bd025d414b4510a219cc5f131e2fa7d56687128ddfd98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108425"
---
# <a name="cpospassthrucheckcapabilities-method"></a>Método CPosPassThru.CheckCapabilities

El `CheckCapabilities` método consulta si una secuencia ha especificado funcionalidades de búsqueda. Este método implementa el [**método IMediaSeeking::CheckCapabilities.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities)

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

Puntero a una combinación bit a bit de uno o varios atributos [**DE AM SEEKING SEEKING \_ \_ \_ CAPABILITIES.**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) Cuando el método vuelve, el valor indica cuál de esos atributos está disponible.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el **valor HRESULT** del pin conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPosPassThru (clase)**](cpospassthru.md)
</dt> </dl>

 

 





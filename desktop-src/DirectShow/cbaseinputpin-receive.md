---
description: 'Método CBaseInputPin.Receive: el método Receive recibe el siguiente ejemplo multimedia en la secuencia. Este método implementa el método IMemInputPin::Receive.'
ms.assetid: 30fefc7b-7c9c-44cd-b58b-2b275dfa2520
title: Método CBaseInputPin.Receive (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b9a3ec028b121cfcb76dfe857d4d12b34dca57410ffee177dd45a19e358e29a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341675"
---
# <a name="cbaseinputpinreceive-method"></a>Método CBaseInputPin.Receive

El `Receive` método recibe el siguiente ejemplo multimedia en la secuencia. Este método implementa el [**método IMemInputPin::Receive.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample del**](/windows/desktop/api/Strmif/nn-strmif-imediasample) ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los enumerados en la tabla siguiente.



| Código devuelto                                                                                             | Descripción                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Correcto.<br/>                                        |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                 | El pin se está vacíando actualmente; se rechazó el ejemplo.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>               | **Argumento de** puntero NULL.<br/>                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo de medio no válido.<br/>                             |
| <dl> <dt>**ERROR EN TIEMPO DE EJECUCIÓN DE VFW \_ E \_ \_**</dt> </dl>   | Se produjo un error en tiempo de ejecución.<br/>                      |
| <dl> <dt>**VFW \_ E \_ ESTADO \_ INCORRECTO**</dt> </dl>     | El pin se detiene.<br/>                             |



 

## <a name="remarks"></a>Comentarios

El pin de salida ascendente llama a este método para entregar una muestra al pin de entrada. El pin de entrada debe realizar una de las siguientes acciones:

-   Procese el ejemplo antes de volver.
-   Devuelve y procesa el ejemplo en un subproceso de trabajo.
-   Rechace el ejemplo.

Si el pin usa un subproceso de trabajo para procesar el ejemplo, agregue un recuento de referencias al ejemplo dentro de este método. Una vez que el método vuelve, el pin ascendente libera el ejemplo. Cuando el recuento de referencias de la muestra alcanza cero, el ejemplo vuelve al asignador para volver a usarlo.

Este método es sincrónico y puede bloquearse. Si el método puede bloquearse, el método [**CBaseInputPin::ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) del pin debe devolver S \_ OK.

En la clase base, este método realiza los pasos siguientes:

1.  Llama al [**método CBaseInputPin::CheckStreaming**](cbaseinputpin-checkstreaming.md) para comprobar que el pin puede procesar ejemplos ahora. Si no puede, por ejemplo, si se detiene el pin, se produce un error en el método.
2.  Recupera las propiedades de ejemplo y comprueba si el formato ha cambiado (consulte a continuación).
3.  Si el formato ha cambiado, el método llama al método [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) para determinar si el nuevo formato es aceptable.
4.  Si el nuevo formato no es aceptable, el método llama al método [**CBasePin::EndOfStream,**](cbasepin-endofstream.md) publica un evento EC ERRORABORT y devuelve un \_ código de error.
5.  Suponiendo que no haya errores, el método devuelve S \_ OK.

Pruebe un cambio de formato como se muestra a continuación:

-   Si el ejemplo admite la [**interfaz IMediaSample2,**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) compruebe el **miembro dwSampleFlags** de la [**estructura PROPERTIES de AM \_ SAMPLE2. \_**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) Si la marca \_ TYPECHANGED DE AM SAMPLE \_ está presente, el formato ha cambiado.
-   De lo contrario, si el ejemplo no admite **IMediaSample2,** llame al [**método IMediaSample::GetMediaType.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) Si el método devuelve un valor distinto de **NULL,** el formato ha cambiado.

En la clase base, este método no procesa el ejemplo. La clase derivada debe invalidar este método para realizar el procesamiento. (Lo que esto conlleva depende completamente del filtro). La clase derivada debe llamar al método de clase base para comprobar los errores descritos anteriormente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseInputPin (clase)**](cbaseinputpin.md)
</dt> </dl>

 

 





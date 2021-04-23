---
description: El conjunto de propiedades Rate Change permite que los filtros de origen o analizador MPEG-2 cambien la velocidad de reproducción. Los descodificadores MPEG-2 deben admitir este conjunto de propiedades. Tanto el navegador de DVD como el motor de búfer de flujo usan este conjunto de propiedades para controlar las velocidades de reproducción.
ms.assetid: f88c64ce-af76-49fe-8ebd-029928506243
title: Conjunto de propiedades de cambio de frecuencia (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb222f8a2fe388d8ea582448d2ba5aa6c9d7e80
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909614"
---
# <a name="rate-change-property-set"></a>Conjunto de propiedades de cambio de frecuencia

El conjunto de propiedades Rate Change permite que los filtros de origen o analizador MPEG-2 cambien la velocidad de reproducción. Los descodificadores MPEG-2 deben admitir este conjunto de propiedades. Tanto el navegador de DVD como el motor de búfer de flujo usan este conjunto de propiedades para controlar las velocidades de reproducción.



| Etiqueta | Value |
|-------------------|-------------------------------|
| GUID del conjunto de propiedades | AM \_ KSPROPSETID \_ TSRateChange |



 



| Id. de propiedad                                                                   | Descripción                                                                            |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**AM \_ RATE \_ CorrectTS**](am-rate-correctts-property.md)                     | Informa al descodificador de que el navegador está estableciendo las marcas de tiempo correctas.             |
| AM \_ RATE \_ ExactRateChange                                                     | Obsoleto.                                                                              |
| [**AM \_ RATE \_ MaxFullDataRate**](am-rate-maxfulldatarate-property.md)         | Consulta al descodificador la velocidad de datos máxima del descodificador.                               |
| [**Consulta \_ DE \_ AM RATEFullFrameRate**](am-rate-queryfullframerate-property.md)   | Consulta al descodificador la velocidad máxima de fotogramas completos del descodificador.                         |
| [**Consulta \_ AM \_ RATELastRateSegPTS**](am-rate-querylastratesegpts-property.md) | Consulta el descodificador para la hora de inicio del segmento de velocidad que se estableció más recientemente. |
| [**AM \_ RATE \_ SimpleRateChange**](am-rate-simpleratechange-property.md)       | Envía un cambio de frecuencia al descodificador.                                                    |
| Paso DE \_ VELOCIDAD \_ DE AM                                                                | Obsoleto. Vea Frame Stepping Property Set ( [Conjunto de propiedades paso a paso de marco).](frame-stepping-property-set.md)          |
| [**UseRateVersion de AM \_ RATE \_**](am-rate-userateversion-property.md)           | Especifica la versión del mecanismo de cambio de velocidad que se va a usar.                           |



 

## <a name="remarks"></a>Comentarios

En el contexto de este conjunto de propiedades, rate mide la velocidad a la que avanzan las marcas de tiempo con respecto al reloj de referencia. Velocidad inversa de la velocidad de reproducción. Por ejemplo, si la velocidad de reproducción es 2 veces mayor, las marcas de tiempo deben aumentar a 1/2 la velocidad normal. Esto se traduce en una velocidad de reproducción más rápida, ya que las muestras se representan antes de lo normal.

Las muestras se envían al descodificador con una marca de tiempo igual al tiempo de presentación a una velocidad de 1x. El descodificador debe escalar las marcas de tiempo de los ejemplos de salida al tiempo de presentación correcto para la velocidad actual. Por ejemplo, si la velocidad es 1/2 (lo que significa que la velocidad de reproducción es 2x), el descodificador debe escalar las marcas de tiempo en 1/2. Por lo general, solo los fotogramas tienen marcas de tiempo. El descodificador debe interpolar las marcas de tiempo para los fotogramas B y P. Tenga en cuenta que durante la reproducción inversa, las marcas de tiempo siguen aumentando; las marcas de tiempo nunca retrocede.

Se definen dos versiones del conjunto de propiedades Rate Change, la versión 1.0 y la versión 1.1. La versión 1.0 ofrece el comportamiento predeterminado. Se recomienda a los proveedores de descodificadores que admitan la versión 1.1, ya que proporciona una experiencia de reproducción más fluida. El navegador de DVD usa actualmente la versión 1.0. El motor de búfer de flujo usa la versión 1.1.

### <a name="rate-change-version-10"></a>Cambio de velocidad versión 1.0

La versión 1.0 del conjunto de propiedades Rate Change define el comportamiento predeterminado de los descodificadores MPEG-2.

El filtro de origen señala un cambio de frecuencia estableciendo la [**\_ propiedad \_ SimpleRateChange de AM RATE.**](am-rate-simpleratechange-property.md) Los datos de esta propiedad son la nueva tasa, más la hora de inicio en el ejemplo de entrada cuando la tasa entra en vigor. El descodificador mantiene una cola de cambios de velocidad pendientes, ordenados por hora de inicio.

Antes de que el navegador de DVD cambie a una velocidad que no sea 1x, entrega todas las muestras pendientes, establece temporalmente la velocidad en 1,0 y vacía el gráfico. A continuación, establece la nueva velocidad. Todos los cambios de velocidad se programan para el final de la VOBU actual (unidad de objeto de vídeo). Tenga en cuenta que al vaciar el gráfico se restablece el tiempo de presentación a cero.

El navegador de DVD funciona en modo *sin problemas* o en modo *de examen.* En modo smooth, envía cada fotograma al descodificador, incluidos los fotogramas B y los fotogramas P. El navegador de DVD usa el modo smooth siempre que la velocidad de reproducción sea mayor que cero pero menor que la velocidad de datos maxmimum del descodificador. Si la velocidad de reproducción es menor que cero (reproducción inversa) o supera la velocidad de datos máxima del descodificador, el navegador de DVD usa el modo de examen, donde envía solo los fotogramas I al descodificador. A velocidades muy altas, puede omitir algunos fotogramas I; Por ejemplo, puede enviar todos los demás fotogramas.

De forma predeterminada, el navegador de DVD silencia la secuencia de audio para velocidades que no son 1.0. Para cambiar esto, llame a [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) con la marca DVD \_ AudioDuringFFwdRew.

### <a name="rate-change-version-11"></a>Cambio de velocidad versión 1.1

La versión 1.1 del conjunto de propiedades Cambio de frecuencia sigue los mismos principios básicos que la versión 1.0, con las siguientes diferencias:

-   El filtro de origen indica al descodificador que use la versión 1.1 estableciendo la [**propiedad \_ \_ UseRateVersion de AM RATE.**](am-rate-userateversion-property.md) De lo contrario, el descodificador debe usar el comportamiento de la versión 1.0.
-   El filtro de origen no vacía el gráfico entre los cambios de velocidad. Por lo tanto, las marcas de tiempo aumentan de forma monónica a través de los límites de cambio de velocidad, en lugar de restablecerse a cero.
-   En lugar de poner en cola un cambio de velocidad durante un tiempo de referencia determinado, el filtro de origen puede especificar que un cambio de velocidad se aplica al ejemplo más adelante del descodificador, definido como el ejemplo en la parte principal de la cola saliente del descodificador. Para ello, el filtro de origen usa la propiedad [**\_ \_ SimpleRateChange**](am-rate-simpleratechange-property.md) de AM RATE, pero establece la hora de inicio igual a -1.
-   El filtro de origen puede consultar el descodificador para la hora de inicio del cambio de velocidad que se ha poner en cola más recientemente. Para ello, [**usa la \_ propiedad \_ QueryLastRateSegPTS**](am-rate-querylastratesegpts-property.md) de AM RATE.
-   El filtro de origen no coloca ejemplos. Si la velocidad supera la velocidad máxima de datos del descodificador, el descodificador debe quitar fotogramas según sea necesario.
-   El filtro de origen no silencia la secuencia de audio, independientemente de la velocidad de datos máxima del descodificador de audio. El descodificador de audio puede quitar muestras si la velocidad de reproducción supera la velocidad máxima del descodificador. Sin embargo, todavía debe mantener la cola de cambios de velocidad programados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 





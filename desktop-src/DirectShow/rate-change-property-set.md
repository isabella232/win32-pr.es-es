---
description: El conjunto de propiedades Rate Change permite que los filtros de origen/analizador de MPEG-2 cambien la velocidad de reproducción. Los descodificadores MPEG-2 deben admitir este conjunto de propiedades. El navegador de DVD y el motor de búfer de secuencia usan esta propiedad establecida para controlar las velocidades de reproducción.
ms.assetid: f88c64ce-af76-49fe-8ebd-029928506243
title: Conjunto de propiedades de cambio de velocidad (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e56b679b0ce9b0127b15c69cd02b016a4990b6f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690408"
---
# <a name="rate-change-property-set"></a>Conjunto de propiedades de cambio de velocidad

El conjunto de propiedades Rate Change permite que los filtros de origen/analizador de MPEG-2 cambien la velocidad de reproducción. Los descodificadores MPEG-2 deben admitir este conjunto de propiedades. El navegador de DVD y el motor de búfer de secuencia usan esta propiedad establecida para controlar las velocidades de reproducción.



|                   |                               |
|-------------------|-------------------------------|
| GUID del conjunto de propiedades | \_TSRateChange KSPROPSETID \_ AM |



 



| Id. de propiedad                                                                   | Descripción                                                                            |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**Frecuencia de las \_ \_ correcciones de AM**](am-rate-correctts-property.md)                     | Informa al descodificador de que el navegador está configurando las marcas de tiempo correctas.             |
| Tasa de AM \_ \_ ExactRateChange                                                     | Obsoleto.                                                                              |
| [**Tasa de AM \_ \_ MaxFullDataRate**](am-rate-maxfulldatarate-property.md)         | Consulta el descodificador para la velocidad de datos máxima del descodificador.                               |
| [**Tasa de AM \_ \_ QueryFullFrameRate**](am-rate-queryfullframerate-property.md)   | Consulta el descodificador para la velocidad máxima de fotogramas completa del descodificador.                         |
| [**Tasa de AM \_ \_ QueryLastRateSegPTS**](am-rate-querylastratesegpts-property.md) | Consulta el descodificador para la hora de inicio del segmento de frecuencia que se estableció más recientemente. |
| [**Tasa de AM \_ \_ SimpleRateChange**](am-rate-simpleratechange-property.md)       | Envía un cambio de frecuencia al descodificador.                                                    |
| \_Paso de frecuencia de AM \_                                                                | Obsoleto. Vea [conjunto de propiedades de ejecución de fotogramas](frame-stepping-property-set.md).          |
| [**Tasa de AM \_ \_ UseRateVersion**](am-rate-userateversion-property.md)           | Especifica la versión del mecanismo de cambio de velocidad que se va a usar.                           |



 

## <a name="remarks"></a>Observaciones

En el contexto de este conjunto de propiedades, Rate mide la velocidad a la que las marcas de tiempo avanzan en relación con el reloj de referencia. Valore el inverso de la velocidad de reproducción. Por ejemplo, si la velocidad de reproducción es 2x, las marcas de tiempo deben aumentar a 1/2 la tarifa normal. Esto se traduce en una velocidad de reproducción más rápida, ya que los ejemplos se representan antes de lo normal.

Los ejemplos se envían al descodificador con una marca de tiempo igual al tiempo de presentación a la velocidad 1x. El descodificador debe escalar las marcas de tiempo de los ejemplos de salida al tiempo de presentación correcto para la velocidad actual. Por ejemplo, si la velocidad es 1/2 (lo que significa que la velocidad de reproducción es 2x), el descodificador debe escalar las marcas de tiempo en 1/2. Por lo general, solo las tramas tienen marcas de tiempo. El descodificador debe interpolar las marcas de tiempo de los fotogramas B y P. Tenga en cuenta que durante la reproducción inversa, las marcas de tiempo continúan aumentando; las marcas de tiempo nunca se retroceden.

Se han definido dos versiones del conjunto de propiedades Rate Change, versión 1,0 y versión 1,1. El comportamiento predeterminado viene dado por la versión 1,0. Se recomienda a los proveedores del descodificador que admitan la versión 1,1, ya que proporciona una experiencia de reproducción más fluida. El navegador de DVD usa actualmente la versión 1,0. El motor de búfer de secuencia usa la versión 1,1.

### <a name="rate-change-version-10"></a>Versión de cambio de tasa 1,0

La versión 1,0 del conjunto de propiedades Rate Change define el comportamiento predeterminado de los descodificadores MPEG-2.

El filtro de origen señala un cambio de velocidad estableciendo la propiedad [**\_ \_ SimpleRateChange de la tasa AM**](am-rate-simpleratechange-property.md) . Los datos de esta propiedad son la nueva velocidad, más la hora de inicio de la muestra de entrada cuando la tasa surte efecto. El descodificador mantiene una cola de cambios de velocidad pendientes, ordenados por hora de inicio.

Antes de que el navegador de DVD cambie a una velocidad que no sea 1x, ofrece todos los ejemplos pendientes, establece temporalmente la velocidad en 1,0 y vacía el gráfico. A continuación, establece la nueva velocidad. Todos los cambios de velocidad se programan para el final de la VOBU actual (unidad de objeto de vídeo). Tenga en cuenta que el vaciado del gráfico restablece el tiempo de presentación en cero.

El navegador de DVD funciona en *modo suave* o en *modo de exploración*. En el modo Smooth, envía cada fotograma al descodificador, incluidos los fotogramas B y P. El navegador de DVD utiliza el modo Smooth cuando la velocidad de reproducción es mayor que cero pero menor que la velocidad de datos maxmimum del descodificador. Si la velocidad de reproducción es menor que cero (reproducción inversa) o supera la velocidad de datos máxima del descodificador, el navegador de DVD usa el modo de exploración, donde envía solo los fotogramas I al descodificador. A velocidades muy altas, puede omitir algunos fotogramas I. por ejemplo, puede enviarse todos los demás fotogramas I.

De forma predeterminada, el navegador de DVD silencia la secuencia de audio para velocidades distintas de 1,0. Puede cambiar esto llamando a [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) con la \_ marca AudioDuringFFwdRew de DVD.

### <a name="rate-change-version-11"></a>Versión de cambio de tasa 1,1

La versión 1,1 del conjunto de propiedades Rate Change sigue los mismos principios básicos que la versión 1,0, con las siguientes diferencias:

-   El filtro de origen indica al descodificador que use la versión 1,1 mediante el establecimiento de la propiedad [**\_ \_ UseRateVersion de la tasa AM**](am-rate-userateversion-property.md) . De lo contrario, el descodificador debe usar el comportamiento de la versión 1,0.
-   El filtro de origen no vacía el gráfico entre los cambios de velocidad. Por lo tanto, las marcas de tiempo aumentan de modo monotónica en los límites de cambio de velocidad, en lugar de restablecer a cero.
-   En lugar de poner en cola un cambio de frecuencia para una hora de referencia determinada, el filtro de origen puede especificar que se aplique un cambio de tasa al *ejemplo más avanzado* del descodificador, definido como el ejemplo en el encabezado de la cola de salida del descodificador. Para ello, el filtro de origen usa la [**propiedad \_ \_ SimpleRateChange de la tasa AM**](am-rate-simpleratechange-property.md) , pero establece la hora de inicio igual a-1.
-   El filtro de origen puede consultar el descodificador para la hora de inicio del cambio de frecuencia que se puso en cola más recientemente. Para este fin, usa la propiedad [**\_ \_ QueryLastRateSegPTS de la tasa AM**](am-rate-querylastratesegpts-property.md) .
-   El filtro de origen no quita ejemplos. Si la velocidad supera la velocidad de datos máxima del descodificador, el descodificador debe quitar fotogramas según sea necesario.
-   El filtro de origen no silencia la secuencia de audio, independientemente de la velocidad de datos máxima del descodificador de audio. El descodificador de audio puede quitar muestras si la velocidad de reproducción supera la velocidad máxima del descodificador. Sin embargo, todavía debe mantener la cola de cambios de velocidad programados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 





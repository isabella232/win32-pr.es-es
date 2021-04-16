---
description: Información de parámetros
ms.assetid: 2600b200-f57a-46cd-8740-89b7f7aba540
title: Información de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1a311bbaa7907af0b3578ed88c28e573649f43
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537792"
---
# <a name="parameter-information"></a>Información de parámetros

El método [**IMediaParamInfo:: GetParamInfo**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparaminfo) devuelve una [**estructura \_ PARAMINFO de MP**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_paraminfo) que describe un parámetro. Esta estructura contiene la siguiente información:

-   El miembro **mpType** indica el tipo de datos del valor del parámetro. Por motivos de eficacia, todos los parámetros se implementan como valores de punto flotante de 32 bits. La enumeración de [**\_ tipo de MP**](/previous-versions/windows/desktop/api/Medparam/ne-medparam-mp_type) define si se debe interpretar el valor como un entero, un valor de punto flotante, un valor booleano o una enumeración (serie de enteros).
-   El miembro **mopCaps** indica qué curvas admite este parámetro. Si el tipo de datos es booleano o de enumeración, la única curva que el parámetro puede admitir es "salto".
-   Los miembros **mpdMinValue** y **mpdMaxValue** definen los valores mínimo y máximo para este parámetro. Cualquier curva para este parámetro debe estar dentro de este intervalo.
-   El miembro **mpdNeutralValue** es el valor predeterminado del parámetro.
-   El miembro **szLabel** es el nombre del parámetro y el miembro **szUnitText** es el nombre de la unidad de medida para el parámetro. Entre los ejemplos se incluyen "Volume" y "decibelios" o "Frequency" y "kHz". Ambas cadenas son en inglés y nunca se localizan. DMO puede proporcionar versiones localizadas a través del método [**IMediaParamInfo:: GetParamText**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparamtext) .

La información de cada parámetro permanece fija a lo largo de la vigencia de DMO. Por lo tanto, el cliente puede consultar esta información una vez y almacenarla en caché.

**Formatos de hora**

El cliente debe marcar la marca de tiempo de los datos de entrada para que DMO pueda calcular los valores de parámetro correspondientes. De forma predeterminada, las marcas de tiempo representan unidades de 100 nanosegundos, también denominadas *hora de referencia*. Sin embargo, esta unidad de tiempo no es adecuada para todas las aplicaciones, por lo que un DMO tiene una opción para admitir otros formatos de hora. Los formatos de hora se identifican mediante un GUID.



| **GUID**              | Descripción                   |
|-----------------------|-------------------------------|
| \_referencia de tiempo de GUID \_ | Tiempo de referencia                |
| \_música de tiempo GUID \_     | Elementos por nota de cuarto (PPQN) |
| \_ejemplos de tiempo de GUID \_   | Muestras por segundo            |



 

Se recomienda a los terceros definir sus propios formatos de hora según sea necesario. Sin embargo, todos los DMOs deben admitir el tiempo de referencia. Esto proporciona una línea de base estándar que todos pueden usar. Para determinar cuántos formatos de hora admite DMO, llame al método [**IMediaParamInfo:: GetNumTimeFormats**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getnumtimeformats) . Para enumerar los formatos admitidos, llame al método [**IMediaParamInfo:: GetSupportedTimeFormat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getsupportedtimeformat) .

Para establecer el formato de hora, llame a [**IMediaParams:: SetTimeFormat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-settimeformat). Este método especifica el GUID del formato de hora y los *datos de hora*, que es el número de unidades por TIC de reloj. Por ejemplo, si el formato de hora es muestras por segundo y los datos de hora son 32, un valor de marca de tiempo de 10 corresponde a los ejemplos de 320.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Parámetros multimedia](media-parameters.md)
</dt> </dl>

 

 




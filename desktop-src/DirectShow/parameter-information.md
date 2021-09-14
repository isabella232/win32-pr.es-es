---
description: Información de parámetros
ms.assetid: 2600b200-f57a-46cd-8740-89b7f7aba540
title: Información de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1a311bbaa7907af0b3578ed88c28e573649f43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362337"
---
# <a name="parameter-information"></a>Información de parámetros

El [**método IMediaParamInfo::GetParamInfo**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparaminfo) devuelve una estructura [**MP \_ PARAMINFO**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_paraminfo) que describe un parámetro . Esta estructura contiene la siguiente información:

-   El **miembro mpType** indica el tipo de datos del valor del parámetro. Para mejorar la eficacia, todos los parámetros se implementan como valores de punto flotante de 32 bits. La [**\_ enumeración MP TYPE**](/previous-versions/windows/desktop/api/Medparam/ne-medparam-mp_type) define si se debe interpretar el valor como un entero, un valor de punto flotante, un valor booleano o una enumeración (serie de enteros).
-   El **miembro de la función decaps** indica qué curvas admite este parámetro. Si el tipo de datos es booleano o de enumeración, la única curva que el parámetro puede admitir es "Jump".
-   Los **miembros mpdMinValue** **y mpdMaxValue** definen los valores mínimo y máximo para este parámetro. Las curvas de este parámetro deben estar dentro de este intervalo.
-   El **miembro mpdNeutralValue** es el valor predeterminado del parámetro .
-   El **miembro szLabel** es el nombre del parámetro y el **miembro szUnitText** es el nombre de la unidad de medida del parámetro. Algunos ejemplos pueden ser "Volumen" y "Decibelios", o "Frecuencia" y "kHz". Ambas cadenas están en inglés y nunca se localizan. El DMO puede proporcionar versiones localizadas a través [**del método IMediaParamInfo::GetParamText.**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparamtext)

La información de cada parámetro permanece fija a lo largo de la duración del DMO. Por lo tanto, el cliente puede consultar esta información una vez y, a continuación, almacenarla en caché.

**Formatos de hora**

El cliente debe marcar de tiempo los datos de entrada, para que DMO pueda calcular los valores de parámetro correspondientes. De forma predeterminada, las marcas de tiempo representan unidades de 100 nanosegundos, también denominadas *hora de referencia.* Sin embargo, esta unidad de tiempo no es conveniente para todas las aplicaciones, por lo que DMO tiene una opción para admitir otros formatos de hora. Los formatos de hora se identifican mediante GUID.



| **GUID**              | Descripción                   |
|-----------------------|-------------------------------|
| REFERENCIA DE \_ HORA \_ DE GUID | Tiempo de referencia                |
| GUID \_ TIME \_ MUSIC     | Nota de partes por trimestre (PPQN) |
| EJEMPLOS DE \_ TIEMPO \_ DE GUID   | Ejemplos por segundo            |



 

Se recomienda a terceros que definan sus propios formatos de hora según sea necesario. Sin embargo, todas las DDO deben admitir el tiempo de referencia. Esto proporciona una línea base estándar que todos los usuarios pueden usar. Para determinar cuántos formatos de tiempo admite DMO, llame al [**método IMediaParamInfo::GetNumTimeFormats.**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getnumtimeformats) Para enumerar los formatos admitidos, llame [**al método IMediaParamInfo::GetSupportedTimeFormat.**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getsupportedtimeformat)

Para establecer el formato de hora, llame [**a IMediaParams::SetTimeFormat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-settimeformat). Este método especifica el GUID de formato de hora y los datos *de* hora , que es el número de unidades por tic de reloj. Por ejemplo, si el formato de hora es muestras por segundo y los datos de hora son 32, un valor de marca de tiempo de 10 corresponde a 320 muestras.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Parámetros multimedia](media-parameters.md)
</dt> </dl>

 

 




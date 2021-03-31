---
description: Cada configuración regional tiene un tipo de calendario predeterminado (tipo de datos CALTYPE) asociado. Una configuración regional también puede tener un tipo de calendario alternativo. Para más información sobre los tipos de calendario, vea información de tipo de calendario.
ms.assetid: 32772cba-eb30-4cd3-adaf-57fb8425a6d5
title: Fecha y calendario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a3c21965bfbf8c4215b478e5c3b4adbae579ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912554"
---
# <a name="date-and-calendar"></a>Fecha y calendario

Cada [configuración regional](locales-and-languages.md) tiene un tipo de calendario predeterminado (tipo de datos CALTYPE) asociado. Una configuración regional también puede tener un tipo de calendario alternativo. Para más información sobre los tipos de calendario, vea [información de tipo de calendario](calendar-type-information.md).

> [!Note]  
> Para usar un tipo de calendario alternativo para una configuración regional, la aplicación debe establecer la constante [ \_ IOPTIONALCALENDAR de configuración regional](locale-ioptionalcalendar.md) en el tipo de calendario alternativo para la configuración regional.

 

La mayoría de las configuraciones regionales utilizan el calendario gregoriano estándar y un número establecido de formatos de fecha. Estas opciones predeterminadas para formatos de fecha están disponibles para su presentación mediante la función [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) o [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex) .

Algunas configuraciones regionales requieren consideraciones especiales a la hora de crear una lista completa de opciones de formato. Algunas de estas configuraciones regionales requieren que se inserten cadenas de texto en la cadena de formato de fecha, mientras que otras requieren un método completamente diferente de cálculo de los valores. Una aplicación aborda estos requisitos especiales mediante la adición de determinados tipos de información de configuración regional y tipos de calendario.

Para obtener más información sobre cómo implementar fechas y calendarios en las aplicaciones, vea [recuperar información de fecha y hora](retrieving-time-and-date-information.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la compatibilidad con National Language](about-national-language-support.md)
</dt> <dt>

[Información de tipo de calendario](calendar-type-information.md)
</dt> <dt>

[Recuperar información de fecha y hora](retrieving-time-and-date-information.md)
</dt> <dt>

[**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)
</dt> <dt>

[**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> </dl>

 

 




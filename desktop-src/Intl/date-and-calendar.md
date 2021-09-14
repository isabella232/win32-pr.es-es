---
description: Cada configuración regional tiene un tipo de calendario predeterminado (tipo de datos CALTYPE) asociado. Una configuración regional también puede tener un tipo de calendario alternativo. Para obtener más información sobre los tipos de calendario, vea Información de tipos de calendario.
ms.assetid: 32772cba-eb30-4cd3-adaf-57fb8425a6d5
title: Fecha y calendario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a3c21965bfbf8c4215b478e5c3b4adbae579ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274743"
---
# <a name="date-and-calendar"></a>Fecha y calendario

Cada [configuración regional](locales-and-languages.md) tiene un tipo de calendario predeterminado (tipo de datos CALTYPE) asociado. Una configuración regional también puede tener un tipo de calendario alternativo. Para obtener más información sobre los tipos de calendario, vea [Calendar Type Information](calendar-type-information.md).

> [!Note]  
> Para usar un tipo de calendario alternativo para una configuración regional, la aplicación debe establecer la constante [ \_ LOCALE IOPTIONALCALENDAR en](locale-ioptionalcalendar.md) el tipo de calendario alternativo para la configuración regional.

 

La mayoría de las configuraciones regionales usan el calendario gregoriano estándar y un número establecido de formatos de fecha. Estas opciones predeterminadas para los formatos de fecha están disponibles para mostrarse mediante la función [**EnumDateFormatsEx o**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) [**EnumDateFormatsExEx.**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)

Algunas configuraciones regionales requieren consideraciones especiales al crear una lista completa de opciones de formato. Algunas de estas configuraciones regionales requieren que se inserte cadenas de texto en la cadena de formato de fecha, mientras que otras requieren un método completamente diferente de cálculo de los valores. Una aplicación aborda estos requisitos especiales mediante la adición de determinados tipos de información de configuración regional y tipos de calendario.

Para obtener más información sobre cómo implementar fechas y calendarios en las aplicaciones, vea [Recuperar información de fecha y hora.](retrieving-time-and-date-information.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la compatibilidad con idiomas nacionales](about-national-language-support.md)
</dt> <dt>

[Información de tipo de calendario](calendar-type-information.md)
</dt> <dt>

[Recuperar información de fecha y hora](retrieving-time-and-date-information.md)
</dt> <dt>

[**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)
</dt> <dt>

[**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> </dl>

 

 




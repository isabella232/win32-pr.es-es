---
description: Tratamiento de las eras en el calendario japonés
ms.assetid: a1dabf7c-6521-492e-bdc0-27cfb07cfc20
title: Tratamiento de las eras en el calendario japonés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eba757745bf0d90d119c821772c7fc23f3f8694b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912545"
---
# <a name="era-handling-for-the-japanese-calendar"></a>Tratamiento de las eras en el calendario japonés

Muchos calendarios tienen eras, como AD/BC o CE/BCE. En el calendario japonés, los años se describen mediante Nengō, una combinación del número de año y el nombre de la era. Por ejemplo, 2009 es Heisei 21. En el pasado, los nombres de la era japonesa cambian con frecuencia, pero ahora la posición japonesa cambia solo en una sucesión de Imperial. Windows y Microsoft .NET han admitido históricamente las cuatro eras modernas en esta directiva: Meiji, Taishō, Shōwa y Heisei.

Con Windows 7, Windows Server 2008 R2 y el .NET Framework 4, Microsoft reconoce que se pueden agregar otras eras en el futuro. En estas versiones de Windows, los datos de la era se almacenan en el registro con la clave:<dl> HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control de los \\ \\ calendarios NLS \\ \\ eras  
</dl>

Si es necesario, se pueden agregar otras eras a esa clave a través del proceso de Windows Update normal. Esta clave se puede ver mediante el editor del registro (Regedit.exe). Un ejemplo de la clave y los valores incluidos en Windows 7 es:

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"1868 01 01"="明治_明_Meiji_M"
"1912 07 30"="大正_大_Taisho_T"
"1926 12 25"="昭和_昭_Showa_S"
"1989 01 08"="平成_平_Heisei_H"
```

El nombre de cada valor de era la fecha en que comienza la era en el calendario gregoriano. El valor contiene el nombre de la era en japonés, el nombre abreviado en japonés, el nombre en inglés y un nombre abreviado en Inglés:<dl> "AAAA MM DD" = "JE \_ AJE \_ EE \_ AEE"  
</dl>where

-   ' AAAA MM DD ' es la fecha Gregoriana del inicio de la era en forma de año, mes, día, donde el año es 4 dígitos, el día es 2 dígitos y el mes también es 2 dígitos. Un espacio separa cada parte de la fecha.
-   "JE" es el nombre en japonés de la era y va seguido de un carácter de subrayado.
-   "AJE" es el nombre abreviado de la era, en japonés, y va seguido de un carácter de subrayado.
-   "EE" es el nombre en Inglés de la era japonesa y va seguido de un carácter de subrayado.
-   "AEE" es el nombre abreviado en Inglés de la era japonesa.

Una consideración para los desarrolladores de aplicaciones es la posibilidad de que se agreguen eras adicionales por Windows Update u otros medios. En ese caso, la aplicación puede encontrar más de las cuatro eras esperadas para el calendario japonés. Con fines de prueba, los evaluadores pueden agregar una era adicional al registro; sin embargo, esto se debe restringir únicamente a las máquinas de prueba, ya que afecta el comportamiento de todo el equipo.

A continuación se muestra un ejemplo de este tipo de clave que podría usarse para la prueba. Este cambio se puede realizar con el editor del registro. (Este es un ejemplo solo para uso de pruebas y no pretende predecir ninguna adición futura).

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"2020 09 01"="仮名_仮_Test Era_X"
```

Tenga en cuenta que esto solo afecta a las máquinas que ejecutan Windows 7 y versiones posteriores o .NET Framework 4 y versiones posteriores. Se recomienda a los desarrolladores de aplicaciones probar sus aplicaciones con dichas eras de prueba adicionales para asegurarse de que sus aplicaciones seguirán funcionando si se agregan eras adicionales en una fecha futura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recuperar información de fecha y hora](retrieving-time-and-date-information.md)
</dt> <dt>

[Identificadores de calendario](calendar-identifiers.md)
</dt> </dl>

 

 




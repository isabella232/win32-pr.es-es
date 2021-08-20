---
description: Tratamiento de las eras en el calendario japonés
ms.assetid: a1dabf7c-6521-492e-bdc0-27cfb07cfc20
title: Tratamiento de las eras en el calendario japonés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6ba9c8957bc37a3e200aad546d04629b049dfb3a7962f73d463358d879fb718
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949424"
---
# <a name="era-handling-for-the-japanese-calendar"></a>Tratamiento de las eras en el calendario japonés

Muchos calendarios tienen eras, como AD/BC o CE/UO. En el calendario japonés, los años se describen mediante neng࣏, una combinación del número de año y el nombre de la era. Por ejemplo, 2009 es Heisei 21. En el pasado, los nombres de las eras japonesas cambiaba con frecuencia, pero ahora las eras japonesas solo cambian en la sucesión. Windows y Microsoft .NET han admitido históricamente las cuatro eras modernas de esta directiva: Peroji, Taish Sh y Heisei.

Con Windows 7, Windows Server 2008 R2 y .NET Framework 4, Microsoft reconoce que se pueden agregar eras adicionales en el futuro. En estas versiones de Windows los datos de era se almacenan en el Registro bajo la clave :<dl> HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ Nls \\ Calendars \\ Japanese \\ Eras  
</dl>

Si es necesario, se pueden agregar eras adicionales a esa clave a través del proceso de actualización Windows normal. Esta clave se puede ver mediante el editor del Registro (Regedit.exe). Un ejemplo de la clave y los valores incluidos en Windows 7 es:

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"1868 01 01"="明治_明_Meiji_M"
"1912 07 30"="大正_大_Taisho_T"
"1926 12 25"="昭和_昭_Showa_S"
"1989 01 08"="平成_平_Heisei_H"
```

El nombre de cada valor de era es la fecha en que comienza la era en el calendario gregoriano. El valor contiene el nombre de la era en japonés, el nombre abreviado en japonés, el nombre en inglés y un nombre abreviado en inglés:<dl> "YYYY MM DD"="JE \_ AJE \_ EE \_ AEE"  
</dl>where

-   "YYYY MM DD" es la fecha gregoriana del inicio de la era en forma de año, mes, día donde año es 4 dígitos, día es 2 dígitos y mes también es 2 dígitos. Un espacio separa cada parte de la fecha.
-   "JE" es el nombre japonés de la era y va seguido de un carácter de subrayado.
-   "AJE" es el nombre abreviado de la era, en japonés, y va seguido de un carácter de subrayado.
-   "EE" es el nombre en inglés de la era japonesa y va seguido de un carácter de subrayado.
-   "AEE" es el nombre abreviado en inglés de la era japonesa.

Una consideración para los desarrolladores de aplicaciones es la posibilidad de que se agregarán eras adicionales mediante Windows Update u otros medios. En ese caso, la aplicación puede encontrar más de las cuatro eras esperadas para el calendario japonés. Con fines de prueba, los evaluadores pueden agregar una era adicional al registro. sin embargo, esto solo debe restringirse a las máquinas de prueba, ya que afecta al comportamiento de toda la máquina.

A continuación se muestra un ejemplo de este tipo de clave que podría usarse para la prueba. Este cambio se puede realizar con el editor del Registro. (Este es un ejemplo solo para el uso de pruebas y no está pensado para predecir adiciones futuras).

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"2020 09 01"="仮名_仮_Test Era_X"
```

Tenga en cuenta que esto solo afecta a las máquinas Windows 7 y posteriores o .NET Framework 4 y versiones posteriores. Se recomienda a los desarrolladores de aplicaciones que prueben sus aplicaciones con estas eras de pruebas adicionales para asegurarse de que sus aplicaciones seguirán funcionando si se agregan eras adicionales en alguna fecha futura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recuperar información de fecha y hora](retrieving-time-and-date-information.md)
</dt> <dt>

[Identificadores de calendario](calendar-identifiers.md)
</dt> </dl>

 

 




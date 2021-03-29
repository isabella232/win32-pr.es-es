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
# <a name="era-handling-for-the-japanese-calendar"></a><span data-ttu-id="e09aa-103">Tratamiento de las eras en el calendario japonés</span><span class="sxs-lookup"><span data-stu-id="e09aa-103">Era Handling for the Japanese Calendar</span></span>

<span data-ttu-id="e09aa-104">Muchos calendarios tienen eras, como AD/BC o CE/BCE.</span><span class="sxs-lookup"><span data-stu-id="e09aa-104">Many calendars have eras, such as AD/BC or CE/BCE.</span></span> <span data-ttu-id="e09aa-105">En el calendario japonés, los años se describen mediante Nengō, una combinación del número de año y el nombre de la era.</span><span class="sxs-lookup"><span data-stu-id="e09aa-105">In the Japanese Calendar, years are described by nengō, a combination of the year number and era name.</span></span> <span data-ttu-id="e09aa-106">Por ejemplo, 2009 es Heisei 21.</span><span class="sxs-lookup"><span data-stu-id="e09aa-106">For example, 2009 is Heisei 21.</span></span> <span data-ttu-id="e09aa-107">En el pasado, los nombres de la era japonesa cambian con frecuencia, pero ahora la posición japonesa cambia solo en una sucesión de Imperial.</span><span class="sxs-lookup"><span data-stu-id="e09aa-107">In the past, Japanese era names changed frequently, but now the Japanese eras change only on imperial succession.</span></span> <span data-ttu-id="e09aa-108">Windows y Microsoft .NET han admitido históricamente las cuatro eras modernas en esta directiva: Meiji, Taishō, Shōwa y Heisei.</span><span class="sxs-lookup"><span data-stu-id="e09aa-108">Windows and Microsoft .NET have historically supported the four modern eras under this policy: Meiji, Taishō, Shōwa and Heisei.</span></span>

<span data-ttu-id="e09aa-109">Con Windows 7, Windows Server 2008 R2 y el .NET Framework 4, Microsoft reconoce que se pueden agregar otras eras en el futuro.</span><span class="sxs-lookup"><span data-stu-id="e09aa-109">With Windows 7, Windows Server 2008 R2, and the .NET Framework 4, Microsoft recognizes that additional eras may be added in the future.</span></span> <span data-ttu-id="e09aa-110">En estas versiones de Windows, los datos de la era se almacenan en el registro con la clave:</span><span class="sxs-lookup"><span data-stu-id="e09aa-110">On these versions of Windows the era data is stored in the registry under the key:</span></span><dl> <span data-ttu-id="e09aa-111">HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control de los \\ \\ calendarios NLS \\ \\ eras</span><span class="sxs-lookup"><span data-stu-id="e09aa-111">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Nls\\Calendars\\Japanese\\Eras</span></span>  
</dl>

<span data-ttu-id="e09aa-112">Si es necesario, se pueden agregar otras eras a esa clave a través del proceso de Windows Update normal.</span><span class="sxs-lookup"><span data-stu-id="e09aa-112">If necessary, additional eras can be added to that key through the normal Windows Update process.</span></span> <span data-ttu-id="e09aa-113">Esta clave se puede ver mediante el editor del registro (Regedit.exe).</span><span class="sxs-lookup"><span data-stu-id="e09aa-113">This key can be viewed using the registry editor (Regedit.exe).</span></span> <span data-ttu-id="e09aa-114">Un ejemplo de la clave y los valores incluidos en Windows 7 es:</span><span class="sxs-lookup"><span data-stu-id="e09aa-114">An example of the key and values shipped in Windows 7 is:</span></span>

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"1868 01 01"="明治_明_Meiji_M"
"1912 07 30"="大正_大_Taisho_T"
"1926 12 25"="昭和_昭_Showa_S"
"1989 01 08"="平成_平_Heisei_H"
```

<span data-ttu-id="e09aa-115">El nombre de cada valor de era la fecha en que comienza la era en el calendario gregoriano.</span><span class="sxs-lookup"><span data-stu-id="e09aa-115">The name of each era value is the date the era begins in the Gregorian calendar.</span></span> <span data-ttu-id="e09aa-116">El valor contiene el nombre de la era en japonés, el nombre abreviado en japonés, el nombre en inglés y un nombre abreviado en Inglés:</span><span class="sxs-lookup"><span data-stu-id="e09aa-116">The value contains the era name in Japanese, the abbreviated name in Japanese, the name in English, and an abbreviated name in English:</span></span><dl> <span data-ttu-id="e09aa-117">"AAAA MM DD" = "JE \_ AJE \_ EE \_ AEE"</span><span class="sxs-lookup"><span data-stu-id="e09aa-117">"YYYY MM DD"="JE\_AJE\_EE\_AEE"</span></span>  
</dl>where

-   <span data-ttu-id="e09aa-118">' AAAA MM DD ' es la fecha Gregoriana del inicio de la era en forma de año, mes, día, donde el año es 4 dígitos, el día es 2 dígitos y el mes también es 2 dígitos.</span><span class="sxs-lookup"><span data-stu-id="e09aa-118">"YYYY MM DD" is the Gregorian date of the start of the era in year, month, day form where year is 4 digits, day is 2 digits and month is also 2 digits.</span></span> <span data-ttu-id="e09aa-119">Un espacio separa cada parte de la fecha.</span><span class="sxs-lookup"><span data-stu-id="e09aa-119">A space separates each part of the date.</span></span>
-   <span data-ttu-id="e09aa-120">"JE" es el nombre en japonés de la era y va seguido de un carácter de subrayado.</span><span class="sxs-lookup"><span data-stu-id="e09aa-120">"JE" is the Japanese name of the era, and is followed by an underscore.</span></span>
-   <span data-ttu-id="e09aa-121">"AJE" es el nombre abreviado de la era, en japonés, y va seguido de un carácter de subrayado.</span><span class="sxs-lookup"><span data-stu-id="e09aa-121">"AJE" is the abbreviated name of the era, in Japanese, and is followed by an underscore.</span></span>
-   <span data-ttu-id="e09aa-122">"EE" es el nombre en Inglés de la era japonesa y va seguido de un carácter de subrayado.</span><span class="sxs-lookup"><span data-stu-id="e09aa-122">"EE" is the English name of the Japanese era, and is followed by an underscore.</span></span>
-   <span data-ttu-id="e09aa-123">"AEE" es el nombre abreviado en Inglés de la era japonesa.</span><span class="sxs-lookup"><span data-stu-id="e09aa-123">"AEE" is the abbreviated English name of the Japanese era.</span></span>

<span data-ttu-id="e09aa-124">Una consideración para los desarrolladores de aplicaciones es la posibilidad de que se agreguen eras adicionales por Windows Update u otros medios.</span><span class="sxs-lookup"><span data-stu-id="e09aa-124">One consideration for application developers is the possibility that additional eras will be added by Windows Update or other means.</span></span> <span data-ttu-id="e09aa-125">En ese caso, la aplicación puede encontrar más de las cuatro eras esperadas para el calendario japonés.</span><span class="sxs-lookup"><span data-stu-id="e09aa-125">In that case the application may encounter more than the expected four eras for the Japanese calendar.</span></span> <span data-ttu-id="e09aa-126">Con fines de prueba, los evaluadores pueden agregar una era adicional al registro; sin embargo, esto se debe restringir únicamente a las máquinas de prueba, ya que afecta el comportamiento de todo el equipo.</span><span class="sxs-lookup"><span data-stu-id="e09aa-126">For testing purposes testers may add an additional era to the registry; however, that should be restricted to test machines only, as it impacts the behavior of the entire machine.</span></span>

<span data-ttu-id="e09aa-127">A continuación se muestra un ejemplo de este tipo de clave que podría usarse para la prueba.</span><span class="sxs-lookup"><span data-stu-id="e09aa-127">An example of such a key that could be used for test follows.</span></span> <span data-ttu-id="e09aa-128">Este cambio se puede realizar con el editor del registro.</span><span class="sxs-lookup"><span data-stu-id="e09aa-128">This change can be made with the registry editor.</span></span> <span data-ttu-id="e09aa-129">(Este es un ejemplo solo para uso de pruebas y no pretende predecir ninguna adición futura).</span><span class="sxs-lookup"><span data-stu-id="e09aa-129">(This is an example for test use only, and is not intended to predict any future additions.)</span></span>

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"2020 09 01"="仮名_仮_Test Era_X"
```

<span data-ttu-id="e09aa-130">Tenga en cuenta que esto solo afecta a las máquinas que ejecutan Windows 7 y versiones posteriores o .NET Framework 4 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e09aa-130">Note that this only impacts machines running Windows 7 and later or .NET Framework 4 and later.</span></span> <span data-ttu-id="e09aa-131">Se recomienda a los desarrolladores de aplicaciones probar sus aplicaciones con dichas eras de prueba adicionales para asegurarse de que sus aplicaciones seguirán funcionando si se agregan eras adicionales en una fecha futura.</span><span class="sxs-lookup"><span data-stu-id="e09aa-131">Application developers are encouraged to test their applications with such additional test eras to ensure that their applications will continue to work if additional eras are added at some future date.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e09aa-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e09aa-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e09aa-133">Recuperar información de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="e09aa-133">Retrieving Time and Date Information</span></span>](retrieving-time-and-date-information.md)
</dt> <dt>

[<span data-ttu-id="e09aa-134">Identificadores de calendario</span><span class="sxs-lookup"><span data-stu-id="e09aa-134">Calendar Identifiers</span></span>](calendar-identifiers.md)
</dt> </dl>

 

 




---
title: Archivo de configuración de la aplicación (ACF)
description: Puede haber aspectos de la aplicación distribuida que afecten a un componente, pero no tienen nada que hacer con otro.
ms.assetid: 017d93fd-1701-4713-a786-752a7695b5a6
keywords:
- MIDL DE ACF
- Lenguaje de definición de interfaz de Microsoft MIDL, se describe el archivo de configuración de la aplicación
- archivo de configuración de la aplicación MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9066e5641d6b71e68ba670984765661f1b9f6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105651312"
---
# <a name="application-configuration-file-acf"></a>Archivo de configuración de la aplicación (ACF)

Puede haber aspectos de la aplicación distribuida que afecten a un componente, pero no tienen nada que hacer con otro. Por ejemplo, un objeto puede contener una estructura de datos grande y compleja y pasar el contenido de esta estructura de datos a otro objeto. El diseño exacto de esta estructura de datos puede no tener sentido para la aplicación receptora. Además, la estructura puede contener tipos de datos que el compilador MIDL no reconoce y no puede generar el cálculo de referencias y el código de serialización.

Las aplicaciones cliente pueden compartir la misma interfaz pero se ejecutan en distintas plataformas. cada una de ellas puede necesitar su propio conjunto de rutinas de serialización. Por último, es posible que los clientes individuales no siempre necesiten el mismo conjunto de funciones. No es eficaz generar código auxiliar para las funciones que nunca se implementarán en una aplicación cliente determinada.

Al definir estos aspectos locales de la interfaz en un archivo de configuración de la aplicación (ACF), puede separar las diferencias entre las interfaces de cliente de su representación en la red, lo que permite al servidor enviar y recibir datos en un formato coherente, y hacer que el código auxiliar sea más compacto y eficaz.

La estructura y la sintaxis de una definición de interfaz ACF son idénticas a la definición de IDL:

``` syntax
[ interface-attribute-list] interface interface-name {. . .}
```

De forma predeterminada, el nombre de la interfaz ACF debe coincidir con su nombre en la definición de IDL. Sin embargo, cuando se usa la opción del compilador de MIDL/ [**ACF**](-acf.md) para especificar explícitamente un nombre de archivo ACF, no es necesario que coincidan los nombres de interfaz. Esta característica permite que varias interfaces compartan una especificación ACF única.

 

 





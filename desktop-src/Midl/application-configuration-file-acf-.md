---
title: Archivo de configuración de la aplicación (ACF)
description: Puede haber aspectos de la aplicación distribuida que afecten a un componente, pero que no tengan nada que ver con otro.
ms.assetid: 017d93fd-1701-4713-a786-752a7695b5a6
keywords:
- ACF MIDL
- Lenguaje de definición de interfaz de Microsoft MIDL , descrito, archivo de configuración de la aplicación
- archivo de configuración de la aplicación MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9066e5641d6b71e68ba670984765661f1b9f6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159687"
---
# <a name="application-configuration-file-acf"></a>Archivo de configuración de la aplicación (ACF)

Puede haber aspectos de la aplicación distribuida que afecten a un componente, pero que no tengan nada que ver con otro. Por ejemplo, un objeto puede contener una estructura de datos grande y compleja y pasar el contenido de esta estructura de datos a otro objeto. El diseño exacto de esta estructura de datos puede no tener sentido para la aplicación receptora. Además, la estructura puede contener tipos de datos que el compilador MIDL no reconoce y no puede generar código de serialización y desmarque.

Las aplicaciones cliente pueden compartir la misma interfaz pero ejecutarse en distintas plataformas. es posible que cada uno de ellos necesite su propio conjunto de rutinas de serialización. Por último, es posible que los clientes individuales no necesiten siempre el mismo conjunto de funciones. Es ineficaz generar código auxiliar para funciones que nunca se implementarán en una aplicación cliente determinada.

Al definir estos aspectos locales de la interfaz en un archivo de configuración de aplicaciones (ACF), puede separar las diferencias entre las interfaces de cliente de su representación de red, lo que permite al servidor enviar y recibir datos en un formato coherente y hacer que el código auxiliar sea más compacto y eficaz.

La estructura y la sintaxis de una definición de interfaz de ACF son idénticas a la definición de IDL:

``` syntax
[ interface-attribute-list] interface interface-name {. . .}
```

De forma predeterminada, el nombre de la interfaz ACF debe coincidir con su nombre en la definición de IDL. Sin embargo, cuando se usa la opción del compilador MIDL / [**acf**](-acf.md) para especificar explícitamente un nombre de archivo ACF, los nombres de interfaz no tienen que coincidir. Esta característica permite que varias interfaces compartan una única especificación de ACF.

 

 





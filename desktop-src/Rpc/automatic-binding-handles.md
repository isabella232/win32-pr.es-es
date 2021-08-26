---
title: Identificadores de enlace automáticos
description: Los identificadores de enlace automático son útiles cuando la aplicación no requiere un servidor específico y cuando no necesita mantener información de estado entre el cliente y el servidor.
ms.assetid: ba049369-6c8b-4313-a266-e0364a30056e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b619b17e44e79e623bcffa84f4938d1278a7d146d6de90547cd833e1bf091167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023445"
---
# <a name="automatic-binding-handles"></a>Identificadores de enlace automáticos

Los identificadores de enlace automático son útiles cuando la aplicación no requiere un servidor específico y cuando no necesita mantener información de estado entre el cliente y el servidor. Cuando se usa un identificador de enlace automático, no es necesario escribir ningún código de aplicación cliente para tratar con el enlace y los identificadores, simplemente se especifica el uso del identificador de enlace automático en el archivo de configuración de la aplicación (ACF). A continuación, el código auxiliar define el identificador y administra el enlace.

Por ejemplo, se puede implementar una operación de marca de tiempo mediante un identificador automático. No hace ninguna diferencia con la aplicación cliente a la que el servidor le proporciona la marca de tiempo, ya que puede aceptar la hora de cualquier servidor disponible.

> [!Note]  
> Los identificadores automáticos no se admiten para la plataforma Macintosh.

 

Para especificar el uso de identificadores automáticos, incluya el \[ [**atributo de \_ identificador**](/windows/desktop/Midl/auto-handle) \] automático en el ACF. En el ejemplo de marca de tiempo se usa el ACF siguiente:

``` syntax
/* ACF file */
[
  auto_handle
]
interface autoh
{
}
```

Cuando el ACF no incluye ningún otro atributo de identificador y cuando los procedimientos remotos no usan identificadores explícitos, el compilador midl usa identificadores automáticos de forma predeterminada. También usa identificadores automáticos como valor predeterminado cuando el ACF no está presente.

Los procedimientos remotos se especifican en el archivo IDL. El identificador automático no debe aparecer como argumento para el procedimiento remoto. Por ejemplo:

``` syntax
/* IDL file */
[ 
  uuid (6B29FC40-CA47-1067-B31D-00DD010662DA),
  version(1.0),
  pointer_default(unique)
]
interface autoh
{
  void GetTime([out] long * time);
  void Shutdown(void);
}
```

La ventaja del identificador automático es que el desarrollador no tiene que escribir ningún código para administrar el identificador. los códigos auxiliares administran el enlace automáticamente. Esto es significativamente diferente del ejemplo [Hello, World](tutorial.md), donde el cliente administra el identificador primitivo implícito definido en el ACF y debe llamar a varias funciones en tiempo de ejecución para establecer el identificador de enlace.

 

 
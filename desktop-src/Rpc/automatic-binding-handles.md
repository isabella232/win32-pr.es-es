---
title: Identificadores de enlace automáticos
description: Los identificadores de enlace automáticos son útiles cuando la aplicación no requiere un servidor específico y cuando no necesita mantener ninguna información de estado entre el cliente y el servidor.
ms.assetid: ba049369-6c8b-4313-a266-e0364a30056e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fe83d3f9029e0384c87e5e409583ff70f1e91ac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359300"
---
# <a name="automatic-binding-handles"></a>Identificadores de enlace automáticos

Los identificadores de enlace automáticos son útiles cuando la aplicación no requiere un servidor específico y cuando no necesita mantener ninguna información de estado entre el cliente y el servidor. Cuando se usa un controlador de enlace automático, no es necesario escribir ningún código de aplicación cliente para tratar con enlaces y identificadores; basta con especificar el uso del identificador de enlace automático en el archivo de configuración de la aplicación (ACF). A continuación, el código auxiliar define el identificador y administra el enlace.

Por ejemplo, una operación de marca de tiempo se puede implementar mediante un identificador automático. No hace ninguna diferencia con la aplicación cliente qué servidor la proporciona con la marca de tiempo, ya que puede aceptar el tiempo de cualquier servidor disponible.

> [!Note]  
> Los identificadores automáticos no se admiten para la plataforma Macintosh.

 

Para especificar el uso de identificadores automáticos, incluya el \[ atributo de [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) \] en el ACF. En el ejemplo de marca de tiempo se usa el ACF siguiente:

``` syntax
/* ACF file */
[
  auto_handle
]
interface autoh
{
}
```

Cuando el ACF no incluye ningún otro atributo de identificador y cuando los procedimientos remotos no utilizan identificadores explícitos, el compilador de MIDL usa identificadores automáticos de forma predeterminada. También utiliza identificadores automáticos como valor predeterminado cuando el ACF no está presente.

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

La ventaja del identificador automático es que el desarrollador no tiene que escribir código para administrar el identificador; el código auxiliar administra el enlace automáticamente. Esto es significativamente diferente del [ejemplo Hello, World](tutorial.md), donde el cliente administra el identificador primitivo implícito definido en ACF y debe llamar a varias funciones en tiempo de ejecución para establecer el identificador de enlace.

 

 
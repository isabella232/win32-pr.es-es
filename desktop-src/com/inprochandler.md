---
title: InprocHandler
description: Especifica si una aplicación utiliza un controlador personalizado.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- Clave del registro InprocHandler COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8c19089ece43496465351b44e9faa8793ba893
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418958"
---
# <a name="inprochandler"></a>InprocHandler

Especifica si una aplicación utiliza un controlador personalizado.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **reg \_ SZ** que especifica el controlador personalizado que utiliza la aplicación. Si no se utiliza un controlador personalizado, la entrada debe establecerse en Ole32.dll.

Si un contenedor está buscando en el registro un controlador personalizado, la versión de 16 bits tiene prioridad con un contenedor de 16 bits y la versión de 32 bits tiene prioridad con un contenedor de 32 bits.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**InprocHandler32**](inprochandler32.md)
</dt> </dl>

 

 





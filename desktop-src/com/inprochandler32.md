---
title: InprocHandler32
description: Especifica si una aplicación utiliza un controlador personalizado.
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- Clave del registro InprocHandler32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c918669aa3de1c8cf2622e3caf4acc9ae18f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418476"
---
# <a name="inprochandler32"></a>InprocHandler32

Especifica si una aplicación utiliza un controlador personalizado.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **reg \_ SZ** que especifica el controlador personalizado que utiliza la aplicación. Si no se utiliza un controlador personalizado, la entrada debe establecerse en Ole32.dll.

Si un contenedor está buscando en el registro un controlador personalizado, la versión de 16 bits tiene prioridad con un contenedor de 16 bits y la versión de 32 bits tiene prioridad con un contenedor de 32 bits.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**InprocHandler**](inprochandler.md)
</dt> </dl>

 

 





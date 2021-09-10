---
title: InprocHandler32
description: InprocHandler32 especifica si una aplicación usa un controlador personalizado en HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID clave del Registro.
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- Com de clave del Registro InprocHandler32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be73a8b2577a554b0bb8b5ba5a851e630edbf90a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369460"
---
# <a name="inprochandler32"></a>InprocHandler32

Especifica si una aplicación usa un controlador personalizado.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG SZ** que especifica el controlador personalizado utilizado por la aplicación. Si no se usa un controlador personalizado, la entrada debe establecerse en Ole32.dll.

Si un contenedor busca en el Registro un controlador personalizado, la versión de 16 bits tiene prioridad con un contenedor de 16 bits y la versión de 32 bits tiene prioridad con un contenedor de 32 bits.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**InprocHandler**](inprochandler.md)
</dt> </dl>

 

 





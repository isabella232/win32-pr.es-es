---
title: InprocHandler
description: InprocHandler especifica si una aplicación usa un controlador personalizado en la HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID clave del Registro.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- Com de clave del Registro InprocHandler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aea1ca0d5eb5dec58a36578d268d7020a963a95e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060921"
---
# <a name="inprochandler"></a>InprocHandler

Especifica si una aplicación usa un controlador personalizado.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG SZ** que especifica el controlador personalizado utilizado por la aplicación. Si no se usa un controlador personalizado, la entrada debe establecerse en Ole32.dll.

Si un contenedor busca en el Registro un controlador personalizado, la versión de 16 bits tiene prioridad con un contenedor de 16 bits y la versión de 32 bits tiene prioridad con un contenedor de 32 bits.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**InprocHandler32**](inprochandler32.md)
</dt> </dl>

 

 





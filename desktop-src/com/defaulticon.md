---
title: DefaultIcon
description: Proporciona información de iconos predeterminada para presentaciones iónicas de objetos.
ms.assetid: 45a3289b-d9c4-4857-bf48-1fd664ce4430
keywords:
- DefaultIcon,clave del Registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0079fb02f4429c1939f54d643e0a6b08fbc90eb
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369580"
---
# <a name="defaulticon"></a>DefaultIcon

Proporciona información de iconos predeterminada para presentaciones iónicas de objetos.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DefaultIcon = path, resourceID
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ SZ reg** que especifica la ruta de acceso completa al nombre ejecutable de la aplicación de objeto y el índice de recursos del icono dentro del archivo ejecutable.

**DefaultIcon** identifica el icono que se va a usar cuando, por ejemplo, un control se minimiza en un icono. Esta entrada contiene la ruta de acceso completa al nombre ejecutable de la aplicación de servidor y el índice de recursos del icono dentro del ejecutable. Las aplicaciones pueden usar la información proporcionada por **DefaultIcon para** obtener un identificador de icono [**con ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona).

 

 
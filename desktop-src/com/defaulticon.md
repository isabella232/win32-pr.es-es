---
title: DefaultIcon
description: Proporciona información de iconos predeterminada para presentaciones iónicas de objetos.
ms.assetid: 45a3289b-d9c4-4857-bf48-1fd664ce4430
keywords:
- DefaultIcon registry key COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680994bdd4d4cd6ec6a3d192ca737af27f9190f6179571b3c8aaca5d86b55c5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501265"
---
# <a name="defaulticon"></a>DefaultIcon

Proporciona información de iconos predeterminada para presentaciones iónicas de objetos.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DefaultIcon = path, resourceID
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ SZ reg** que especifica la ruta de acceso completa al nombre ejecutable de la aplicación de objeto y el índice de recursos del icono dentro del ejecutable.

**DefaultIcon** identifica el icono que se va a usar cuando, por ejemplo, un control se minimiza en un icono. Esta entrada contiene la ruta de acceso completa al nombre ejecutable de la aplicación de servidor y el índice de recursos del icono dentro del ejecutable. Las aplicaciones pueden usar la información proporcionada por **DefaultIcon** para obtener un identificador de icono [**con ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona).

 

 
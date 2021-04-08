---
title: DefaultIcon
description: Proporciona información de icono predeterminada para presentaciones con iconos de objetos.
ms.assetid: 45a3289b-d9c4-4857-bf48-1fd664ce4430
keywords:
- Clave del registro DefaultIcon COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0079fb02f4429c1939f54d643e0a6b08fbc90eb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078423"
---
# <a name="defaulticon"></a>DefaultIcon

Proporciona información de icono predeterminada para presentaciones con iconos de objetos.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DefaultIcon = path, resourceID
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **reg \_ SZ** que especifica la ruta de acceso completa al nombre del archivo ejecutable de la aplicación de objeto y el índice de recursos del icono en el ejecutable.

**DefaultIcon** identifica el icono que se va a usar cuando, por ejemplo, un control se minimice a un icono. Esta entrada contiene la ruta de acceso completa al nombre del archivo ejecutable de la aplicación de servidor y el índice de recursos del icono dentro del archivo ejecutable. Las aplicaciones pueden usar la información proporcionada por **DefaultIcon** para obtener un identificador de icono con [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona).

 

 
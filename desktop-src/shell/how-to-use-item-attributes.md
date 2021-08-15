---
description: Los valores de marca SFGAO de los atributos de Shell de un elemento se pueden probar para determinar si el verbo debe habilitarse o deshabilitarse.
ms.assetid: 3A539A9D-DB6B-4E3D-AD26-D5309BECEBB1
title: Cómo usar atributos de elemento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ddcc567a820ba1d9c1394ca38f78fc9ce9ec634596f8dbe41feca9def32e90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859574"
---
# <a name="how-to-use-item-attributes"></a>Cómo usar atributos de elemento

Los [**valores de marca SFGAO**](sfgao.md) de los atributos de Shell de un elemento se pueden probar para determinar si el verbo debe habilitarse o deshabilitarse.

Para usar esta característica de atributo, agregue los siguientes **valores \_ REG DWORD** bajo el verbo :

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Paso 1:

El valor AttributeMask especifica el valor [**SFGAO**](sfgao.md) de los valores de bits de la máscara con la que se probará.

### <a name="step-2"></a>Paso 2:

El valor AttributeValue especifica el valor [**SFGAO**](sfgao.md) de los bits que se prueban.

### <a name="step-3"></a>Paso 3:

ImpliedSelectionModel especifica cero para los verbos de elemento o distinto de cero para los verbos en el menú contextual de fondo.

## <a name="remarks"></a>Comentarios

En la siguiente entrada del Registro de ejemplo, AttributeMask se establece en [**SFGAO \_ READONLY**](sfgao.md) (0x40000).

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

 

 




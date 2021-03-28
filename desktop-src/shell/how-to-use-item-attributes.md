---
description: Los valores de marca SFGAO de los atributos de Shell para un elemento pueden probarse para determinar si el verbo debe estar habilitado o deshabilitado.
ms.assetid: 3A539A9D-DB6B-4E3D-AD26-D5309BECEBB1
title: Cómo usar atributos de elemento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a438c81258677822ca9b940eb9f74366d6226ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909530"
---
# <a name="how-to-use-item-attributes"></a>Cómo usar atributos de elemento

Los valores de marca [**SFGAO**](sfgao.md) de los atributos de Shell para un elemento pueden probarse para determinar si el verbo debe estar habilitado o deshabilitado.

Para usar esta característica de atributo, agregue los siguientes valores de **reg \_ DWORD** en el verbo:

## <a name="instructions"></a>Instrucciones

### <a name="step-1"></a>Paso 1:

El valor AttributeMask especifica el valor de [**SFGAO**](sfgao.md) de los valores de bit de la máscara que se va a probar con.

### <a name="step-2"></a>Paso 2:

El valor AttributeValue especifica el valor de [**SFGAO**](sfgao.md) de los bits que se prueban.

### <a name="step-3"></a>Paso 3:

ImpliedSelectionModel especifica cero para los verbos de elemento o un valor distinto de cero para los verbos en el menú contextual del fondo.

## <a name="remarks"></a>Observaciones

En la siguiente entrada del registro de ejemplo, AttributeMask se establece en [**SFGAO \_ ReadOnly**](sfgao.md) (0x40000).

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

 

 




---
description: Además del registro de modelo de objetos componentes (COM) normal, se deben completar los pasos siguientes para poder registrar controladores de superposición de iconos.
ms.assetid: 73EE5E69-969B-409E-9E8F-5837720EA0B3
title: Cómo registrar controladores de superposición de iconos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb58747adc9b754481f43fec825a4588e1606ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997696"
---
# <a name="how-to-register-icon-overlay-handlers"></a>Cómo registrar controladores de superposición de iconos

Además del registro de modelo de objetos componentes (COM) normal, se deben completar los pasos siguientes para poder registrar controladores de superposición de iconos.

## <a name="instructions"></a>Instrucciones

### <a name="step-1-create-a-subkey-named-for-the-handler-under-this-key"></a>Paso 1: crear una subclave denominada para el controlador en esta clave

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
```

### <a name="step-2-set-the-default-value-of-the-subkey-to-the-string-form-of-the-objects-class-identifier-clsidguid"></a>Paso 2: establecer el valor predeterminado de la subclave en la forma de cadena del GUID del identificador de clase (CLSID) del objeto

En el ejemplo siguiente se muestra cómo registrar un controlador de superposición de iconos denominado superoverlay.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
                     MyOverlay
                        (Default) = {MyOverlay CLSID GUID}
```

 

 




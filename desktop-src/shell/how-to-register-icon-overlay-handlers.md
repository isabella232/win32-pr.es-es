---
description: Además del registro normal del Modelo de objetos componentes (COM), se deben completar los pasos siguientes para registrar controladores de superposición de iconos.
ms.assetid: 73EE5E69-969B-409E-9E8F-5837720EA0B3
title: Cómo registrar controladores de superposición de iconos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a0e62d95b224b131f03c2bd976ddf7c01d7cb3de7ad6995f21568dc7e990d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714915"
---
# <a name="how-to-register-icon-overlay-handlers"></a>Cómo registrar controladores de superposición de iconos

Además del registro normal del Modelo de objetos componentes (COM), se deben completar los pasos siguientes para registrar controladores de superposición de iconos.

## <a name="instructions"></a>Instructions

### <a name="step-1-create-a-subkey-named-for-the-handler-under-this-key"></a>Paso 1: Crear una subclave denominada para el controlador bajo esta clave

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
```

### <a name="step-2-set-the-default-value-of-the-subkey-to-the-string-form-of-the-objects-class-identifier-clsidguid"></a>Paso 2: Establecer el valor predeterminado de la subclave en el formato de cadena del identificador de clase (CLSID)GUID del objeto

En el ejemplo siguiente se muestra cómo registrar un controlador de superposición de iconos denominado MyOverlay.

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

 

 




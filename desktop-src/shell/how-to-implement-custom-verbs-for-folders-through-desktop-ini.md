---
description: En Windows 7 y versiones posteriores, puede Agregar verbos a una carpeta mediante Desktop.ini. Para obtener más información acerca de los archivos de Desktop.ini, consulte Cómo personalizar carpetas con Desktop.ini.
ms.assetid: F03AB35D-FBFE-46C2-A37F-F70C18219B9A
title: Cómo implementar verbos personalizados para carpetas a través de Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133726133abe884863a0b4d2abc0cc76aab1310a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985434"
---
# <a name="how-to-implement-custom-verbs-for-folders-through-desktopini"></a>Cómo implementar verbos personalizados para carpetas a través de Desktop.ini

En Windows 7 y versiones posteriores, puede Agregar verbos a una carpeta mediante Desktop.ini. Para obtener más información acerca de los archivos de Desktop.ini, consulte [Cómo personalizar carpetas con Desktop.ini](how-to-customize-folders-with-desktop-ini.md).

> [!Note]  
> Desktop.ini archivos siempre deben estar marcados como **sistema**  +  **oculto** para que no se muestren a los usuarios.

 

Para agregar verbos personalizados para carpetas a través de un archivo de Desktop.ini, realice los pasos siguientes.

## <a name="instructions"></a>Instrucciones

### <a name="step-1"></a>Paso 1:

Cree una carpeta marcada como **de solo lectura** o **sistema**.

### <a name="step-2"></a>Paso 2:

Cree un archivo de Desktop.ini que incluya un \[ . ShellClassInfo \] DirectoryClass = ProgID.

### <a name="step-3"></a>Paso 3:

En el registro, cree la carpeta **\_ \_ raíz de las clases HKEY** \\  con un valor de CanUseForDirectory. El valor CanUseForDirectory evita el uso incorrecto de los ProgID que se establecen para no participar en la implementación de verbos personalizados para carpetas a través de Desktop.ini.

### <a name="step-4"></a>Paso 4:

Agregue verbos en la subclave ProgID de la **carpeta** , por ejemplo:

```
HKEY_CLASSES_ROOT
   CustomFolderType
      Shell
         MyVerb
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
```

## <a name="remarks"></a>Observaciones

> [!Note]  
> Estos verbos pueden ser los verbos predeterminados, en cuyo caso, al hacer doble clic en la carpeta, se activa el verbo.

 

 

 




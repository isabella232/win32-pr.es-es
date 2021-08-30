---
description: En Windows 7 y versiones posteriores, puede agregar verbos a una carpeta mediante Desktop.ini. Para obtener más información sobre Desktop.ini archivos, vea Personalización de carpetas con Desktop.ini.
ms.assetid: F03AB35D-FBFE-46C2-A37F-F70C18219B9A
title: Cómo implementar verbos personalizados para carpetas mediante Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f49b3f12d51848d08e6480d4180a3768b807703e5655e3fcfcddffcdaf16b734
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111785"
---
# <a name="how-to-implement-custom-verbs-for-folders-through-desktopini"></a>Cómo implementar verbos personalizados para carpetas mediante Desktop.ini

En Windows 7 y versiones posteriores, puede agregar verbos a una carpeta mediante Desktop.ini. Para obtener más información sobre Desktop.ini archivos, [vea How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).

> [!Note]  
> Desktop.ini los archivos deben marcarse siempre **como Sistema** oculto para que no se muestren a los  +   usuarios.

 

Para agregar verbos personalizados para carpetas a través de Desktop.ini archivo, realice los pasos siguientes.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Paso 1:

Cree una carpeta que esté marcada como **De solo lectura** o **Sistema.**

### <a name="step-2"></a>Paso 2:

Cree un Desktop.ini que incluya \[ un . ShellClassInfo \] DirectoryClass=Folder ProgID.

### <a name="step-3"></a>Paso 3:

En el Registro, cree **HKEY \_ CLASSES \_ ROOT** \\ **Folder ProgID** con un valor de CanUseForDirectory. El valor CanUseForDirectory evita el uso incorrecto de progIDs que están establecidos para no participar en la implementación de verbos personalizados para carpetas a través de Desktop.ini.

### <a name="step-4"></a>Paso 4:

Agregue verbos en la **subclave Folder** ProgID, por ejemplo:

```
HKEY_CLASSES_ROOT
   CustomFolderType
      Shell
         MyVerb
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
```

## <a name="remarks"></a>Comentarios

> [!Note]  
> Estos verbos pueden ser los verbos predeterminados, en cuyo caso hacer doble clic en la carpeta activa el verbo.

 

 

 




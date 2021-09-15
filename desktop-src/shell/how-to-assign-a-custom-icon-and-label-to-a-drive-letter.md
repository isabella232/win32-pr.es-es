---
description: Especifique un icono y una etiqueta personalizados para una unidad.
ms.assetid: B6EF7F84-7747-4689-B740-A91CA8E394D7
title: Asignar un icono y una etiqueta personalizados a una letra de unidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848c076db443c502a667d67e0b7b49ce51db4ce6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360376"
---
# <a name="how-to-assign-a-custom-icon-and-label-to-a-drive-letter"></a>Asignación de un icono y una etiqueta personalizados a una letra de unidad

Especifique un icono y una etiqueta personalizados para una unidad.

## <a name="instructions"></a>Instructions

### <a name="step-1-replacing-the-standard-drive-icon-with-a-custom-icon-in-windows-2000"></a>Paso 1: Reemplazar el icono de unidad estándar por un icono personalizado en Windows 2000

Para reemplazar el icono de unidad estándar por un icono personalizado en Windows 2000, agregue una subclave denominada para la letra de unidad a la clave siguiente.

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
```

En el ejemplo siguiente se especifica un icono y una etiqueta personalizados para la unidad E:. El icono está en el archivo deMyDrive.exe C: \\ MyDir \\ con un índice de base cero de tres.

Para Windows 2000:

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
            E
               DefaultIcon
                  (Default) = C:\MyDir\MyDrive.exe,3
               DefaultLabel
                  (Default) = MyDrive
```

### <a name="step-2-replacing-the-standard-drive-icon-with-a-custom-icon-in-all-other-versions-of-windows"></a>Paso 2: Reemplazar el icono de unidad estándar por un icono personalizado en todas las demás versiones de Windows

Para reemplazar el icono de unidad estándar por un icono personalizado en todas las versiones de Windows distintas de Windows 2000, agregue una subclave denominada para la letra de unidad a la clave siguiente.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
```

En el ejemplo siguiente se especifica un icono y una etiqueta personalizados para la unidad E:. El icono está en el archivo deMyDrive.exe C: \\ MyDir \\ con un índice de base cero de tres.

Para todas las demás versiones de Windows:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
                     E
                        DefaultIcon
                           (Default) = C:\MyDir\MyDrive.exe,3
                        DefaultLabel
                           (Default) = MyDrive
```

### <a name="step-3-calling-the-shupdateimage-event"></a>Paso 3: Llamar al evento SHUpdateImage

En todas las versiones de Windows, si cambia un tipo de archivo o un icono de unidad, también debe llamar a SHUpdateImage para notificar al Shell que actualice los iconos que se muestran actualmente.

## <a name="remarks"></a>Observaciones

La letra de unidad no debe ir seguida de dos puntos (:). Agregue una **subclave DefaultIcon** a la subclave de letra de unidad y establezca su valor predeterminado en una cadena que contenga la ubicación del icono. La primera parte de la cadena contiene la ruta de acceso completa del archivo del icono. Si hay más de un icono en el archivo, la ruta de acceso va seguida de una coma y, después, del índice de base cero del icono.

 

 




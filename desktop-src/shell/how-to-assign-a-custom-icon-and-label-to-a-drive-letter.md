---
description: Especifique un icono y una etiqueta personalizados para una unidad.
ms.assetid: B6EF7F84-7747-4689-B740-A91CA8E394D7
title: Asignar un icono y una etiqueta personalizados a una letra de unidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1228ca1d492bd7fdf17d9e95cd6465fc445f798b700b7d1498f972af35583e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049878"
---
# <a name="how-to-assign-a-custom-icon-and-label-to-a-drive-letter"></a>Asignación de un icono y una etiqueta personalizados a una letra de unidad

Especifique un icono y una etiqueta personalizados para una unidad.

## <a name="instructions"></a>Instructions

### <a name="step-1-replacing-the-standard-drive-icon-with-a-custom-icon-in-windows-2000"></a>Paso 1: Reemplazar el icono de unidad estándar por un icono personalizado en Windows 2000

Para reemplazar el icono de unidad estándar por un icono personalizado en Windows 2000, agregue una subclave denominada para la letra de unidad a la siguiente clave.

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
```

En el ejemplo siguiente se especifica un icono personalizado y una etiqueta para la unidad E:. El icono está en el archivo deMyDrive.exe C: \\ MyDir \\ con un índice de base cero de tres.

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

En el ejemplo siguiente se especifica un icono personalizado y una etiqueta para la unidad E:. El icono está en el archivo deMyDrive.exe C: \\ MyDir \\ con un índice de base cero de tres.

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

## <a name="remarks"></a>Comentarios

La letra de unidad no debe ir seguida de dos puntos (:). Agregue una subclave **DefaultIcon** a la subclave de letra de unidad y establezca su valor predeterminado en una cadena que contenga la ubicación del icono. La primera parte de la cadena contiene la ruta de acceso completa del archivo del icono. Si hay más de un icono en el archivo, la ruta de acceso va seguida de una coma y, después, del índice de base cero del icono.

 

 




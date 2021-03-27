---
description: Muestra cómo asegurarse de que la aplicación aparece en el menú y el cuadro de diálogo Abrir con para aplicaciones de escritorio, y que está disponible como una aplicación de la tienda Windows predeterminada para los tipos de archivo especificados.
ms.assetid: DFCC07A6-BED5-41A8-86DC-130082AE665A
title: Cómo incluir una aplicación en el cuadro de diálogo Abrir con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218dcbfe6dc34770208c017f0e13cfda7686430c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909541"
---
# <a name="how-to-include-an-application-in-the-open-with-dialog-box"></a>Cómo incluir una aplicación en el cuadro de diálogo Abrir con

Muestra cómo asegurarse de que la aplicación aparece en el menú y el cuadro de diálogo **abrir con** para aplicaciones de escritorio, y que está disponible como una aplicación de la tienda Windows predeterminada para los tipos de archivo especificados.

## <a name="instructions"></a>Instrucciones

### <a name="for-each-file-type-add-your-application-to-the-openwithprogids-registry-subkey"></a>Para cada tipo de archivo, agregue la aplicación a la subclave del registro OpenWithProgIds.

Agregue el ProgID como un nombre de valor, con el tipo de valor de REG \_ None o REG \_ SZ y una cadena vacía como valor de datos.

Los siguientes ejemplos del registro muestran entradas que asocian InfoPath y Microsoft Visual Studio con el tipo de archivo XML.

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithProgids
         InfoPath.Document.3 REG_SZ
         VisualStudio.xml.10.0 REG_SZ
```

## <a name="remarks"></a>Observaciones

Se prefiere la subclave **OpenWithProgids** a **OpenWithList** para identificar una aplicación. Para obtener más información sobre estas subclaves, vea [configuración de subclaves opcionales y atributos de extensión de tipo de archivo](fa-file-types.md).

**OpenWithList** está pensado únicamente para aplicaciones heredadas (debe ser. exe solamente) en sistemas operativos anteriores a Windows XP.

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithList
         AlternateProgram1.exe
         AlternateProgram2.exe
```

 

 




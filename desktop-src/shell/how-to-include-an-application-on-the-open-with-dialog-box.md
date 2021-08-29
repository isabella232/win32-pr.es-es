---
description: Muestra cómo asegurarse de que la aplicación aparece en el menú Abrir con y en el cuadro de diálogo para las aplicaciones de escritorio, y está disponible como una aplicación predeterminada de Windows Store para los tipos de archivo especificados.
ms.assetid: DFCC07A6-BED5-41A8-86DC-130082AE665A
title: Cómo incluir una aplicación en el cuadro de diálogo Abrir con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ad3d75d0eaf5ed60f2b9b6f4c468225e620c8d0bfbc8e14ed794a28f8f7098f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714985"
---
# <a name="how-to-include-an-application-in-the-open-with-dialog-box"></a>Cómo incluir una aplicación en el cuadro de diálogo Abrir con

Muestra cómo asegurarse de que  la aplicación aparece en el menú Abrir con y en el cuadro de diálogo para las aplicaciones de escritorio, y está disponible como una aplicación predeterminada Windows Store para los tipos de archivo especificados.

## <a name="instructions"></a>Instructions

### <a name="for-each-file-type-add-your-application-to-the-openwithprogids-registry-subkey"></a>Para cada tipo de archivo, agregue la aplicación a la subclave del Registro OpenWithProgIds.

Agregue progID como nombre de valor, con el tipo de valor REG NONE o REG SZ y una cadena vacía \_ \_ como valor de datos.

En los ejemplos del Registro siguientes se muestran las entradas que asocian InfoPath y for Microsoft Visual Studio con el tipo de archivo XML.

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithProgids
         InfoPath.Document.3 REG_SZ
         VisualStudio.xml.10.0 REG_SZ
```

## <a name="remarks"></a>Comentarios

La **subclave OpenWithProgids** es preferible a **OpenWithList** para identificar una aplicación. Para obtener más información sobre estas subclaves, vea [Establecer subclaves opcionales y Atributos de extensión de tipo de archivo](fa-file-types.md).

**OpenWithList** está pensado solo para aplicaciones heredadas (solo .exe) en sistemas operativos anteriores a Windows XP.

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithList
         AlternateProgram1.exe
         AlternateProgram2.exe
```

 

 




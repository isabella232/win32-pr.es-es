---
description: Muestra cómo asegurarse de que la aplicación aparece en el menú Abrir con y en el cuadro de diálogo para las aplicaciones de escritorio, y está disponible como una aplicación predeterminada de Windows Store para los tipos de archivo especificados.
ms.assetid: DFCC07A6-BED5-41A8-86DC-130082AE665A
title: Cómo incluir una aplicación en el cuadro de diálogo Abrir con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218dcbfe6dc34770208c017f0e13cfda7686430c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262543"
---
# <a name="how-to-include-an-application-in-the-open-with-dialog-box"></a>Cómo incluir una aplicación en el cuadro de diálogo Abrir con

Muestra cómo asegurarse de que  la aplicación aparece en el menú Abrir con y en el cuadro de diálogo de las aplicaciones de escritorio, y está disponible como una aplicación predeterminada de la Tienda Windows para los tipos de archivo especificados.

## <a name="instructions"></a>Instructions

### <a name="for-each-file-type-add-your-application-to-the-openwithprogids-registry-subkey"></a>Para cada tipo de archivo, agregue la aplicación a la subclave del Registro OpenWithProgIds.

Agregue el ProgID como nombre de valor, con el tipo de valor REG NONE o REG SZ y una cadena vacía \_ \_ como valor de datos.

En los ejemplos del Registro siguientes se muestran las entradas que asocian InfoPath y Microsoft Visual Studio con el tipo de archivo XML.

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithProgids
         InfoPath.Document.3 REG_SZ
         VisualStudio.xml.10.0 REG_SZ
```

## <a name="remarks"></a>Observaciones

La **subclave OpenWithProgids** es preferible a **OpenWithList** para identificar una aplicación. Para obtener más información sobre estas subclaves, vea [Establecer subclaves opcionales](fa-file-types.md)y Atributos de extensión de tipo de archivo .

**OpenWithList** está pensado solo para aplicaciones heredadas (solo .exe) en sistemas operativos anteriores a Windows XP.

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithList
         AlternateProgram1.exe
         AlternateProgram2.exe
```

 

 




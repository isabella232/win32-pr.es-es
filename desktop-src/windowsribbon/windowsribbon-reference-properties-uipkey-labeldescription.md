---
title: UI_PKEY_LabelDescription
description: Identifica la propiedad \_ PKEY LabelDescription de la \_ interfaz de usuario.
ms.assetid: e7dfbe7e-c9c9-44fe-9e2d-39e20f5f7062
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80a2db487988f66fcc393b3ba449dfda789248dabc3cd9e1d3e48acf9ba3473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438007"
---
# <a name="ui_pkey_labeldescription"></a>UI \_ PKEY \_ LabelDescription

Identifica la propiedad \_ PKEY LabelDescription de la \_ interfaz de usuario.

```
propertyDescription
   name = UI_PKEY_LabelDescription
   shellPKey = UI_PKEY_LabelDescription
   formatID = 00000002-7363-696e-8441798acf5aebb7
   propID = 2
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Comentarios

Una aplicación usa ui PKEY LabelDescription para consultar la \_ descripción asociada a una etiqueta \_ [ \_ PKEY de interfaz de \_ usuario.](windowsribbon-reference-properties-uipkey-label.md)

El valor de propiedad es una cadena restringida a cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.

> [!Note]  
> Use la referencia de caracteres XML de juego de caracteres universales (UCS) `&#xA;` para especificar un salto de línea.

 

La longitud máxima es sin enlazar.

No se admite la alineación derecha.

En la siguiente captura de pantalla se muestra el uso de una etiqueta y una descripción de etiqueta asociada en un menú de la aplicación.

![captura de pantalla que muestra una etiqueta y una descripción de etiqueta asociada en un menú de la aplicación.](images/properties/ui-pkey-labeldescription.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del recurso](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md)
</dt> <dt>

[Etiqueta \_ PKEY de la interfaz de \_ usuario](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 





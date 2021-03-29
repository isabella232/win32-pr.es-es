---
title: UI_PKEY_LabelDescription
description: Identifica la propiedad LabelDescription de PKEY de la interfaz de usuario \_ \_ .
ms.assetid: e7dfbe7e-c9c9-44fe-9e2d-39e20f5f7062
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb81e723d5f55dcfd63f1bb89bff4741b4e088e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903609"
---
# <a name="ui_pkey_labeldescription"></a>UI \_ PKEY \_ LabelDescription

Identifica la propiedad LabelDescription de PKEY de la interfaz de usuario \_ \_ .

```
propertyDescription
   name = UI_PKEY_LabelDescription
   shellPKey = UI_PKEY_LabelDescription
   formatID = 00000002-7363-696e-8441798acf5aebb7
   propID = 2
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Observaciones

\_ \_ Una aplicación usa la interfaz de usuario PKEY LabelDescription para consultar la descripción asociada a [una \_ \_ etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md)de la interfaz de usuario.

El valor de propiedad es una cadena restringida a cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.

> [!Note]  
> Use la referencia de caracteres XML del juego de caracteres universal (UCS) `&#xA;` para especificar un salto de línea.

 

La longitud máxima es sin límite.

No se admite la alineación derecha.

En la captura de pantalla siguiente se muestra el uso de una etiqueta y una descripción de etiqueta asociada en un menú de la aplicación.

![captura de pantalla que muestra una etiqueta y una descripción de etiqueta asociada en un menú de la aplicación.](images/properties/ui-pkey-labeldescription.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de recursos](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Comando. LabelDescription**](windowsribbon-element-command-labeldescription.md)
</dt> <dt>

[\_Etiqueta PKEY de IU \_](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 





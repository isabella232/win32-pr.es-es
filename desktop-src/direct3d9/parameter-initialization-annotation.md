---
description: Use esta anotación para definir el contenido de un archivo externo como el valor de inicialización de un parámetro de efecto.
ms.assetid: 3da1f951-cb8b-49ce-aba2-0badb3178093
title: Anotación de inicialización de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c564b5b5e273b320fdc5de6148ef5ba5dd9f1b78
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274646"
---
# <a name="parameter-initialization-annotation"></a>Anotación de inicialización de parámetros

Use esta anotación para definir el contenido de un archivo externo como el valor de inicialización de un parámetro de efecto. Por ejemplo:


```
string SasResourceAddress = "Value";
```



donde value es una cadena de texto ASCII que puede contener una ruta de acceso absoluta o relativa. Una ruta de acceso relativa es relativa al directorio que contiene el archivo de efecto.

Este es un ejemplo:


```
texture2D DetailTexture
<
    string SasResourceAddress = "noise.dds";
>;
```



El valor predeterminado es una cadena vacía.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de las anotaciones y semánticas estándar de DirectX](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 




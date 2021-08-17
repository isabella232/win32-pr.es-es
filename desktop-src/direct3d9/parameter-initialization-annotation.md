---
description: Use esta anotación para definir el contenido de un archivo externo como el valor de inicialización de un parámetro de efecto.
ms.assetid: 3da1f951-cb8b-49ce-aba2-0badb3178093
title: Anotación de inicialización de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d66d0cc18782d97a5a56c73ab12cd9222d33827930d60023fccf73cd2a8455
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798673"
---
# <a name="parameter-initialization-annotation"></a>Anotación de inicialización de parámetros

Use esta anotación para definir el contenido de un archivo externo como el valor de inicialización de un parámetro de efecto. Por ejemplo:


```
string SasResourceAddress = "Value";
```



donde Value es una cadena de texto ASCII que puede contener una ruta de acceso absoluta o relativa. Una ruta de acceso relativa es relativa al directorio que contiene el archivo de efecto.

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

[Referencia de semántica y anotaciones estándar de DirectX](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 




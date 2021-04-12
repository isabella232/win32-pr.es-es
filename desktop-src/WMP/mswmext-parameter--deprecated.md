---
title: Parámetro MSWMExt (obsoleto)
description: Parámetro MSWMExt (obsoleto)
ms.assetid: cc52da1a-26d1-4321-b421-b0d6f44635cc
keywords:
- Metaarchivos de Windows Media, parámetro MSWMExt
- metaarchivos, parámetro MSWMExt
- Parámetro MSWMExt
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 745ecfb2cf716e973aec3d574247e3e45d8f49ff
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420355"
---
# <a name="mswmext-parameter-deprecated"></a>Parámetro MSWMExt (obsoleto)

El parámetro *MSWMExt* indica a un programa cliente el formato de un archivo al que se hace referencia.

**Sintaxis**


```XML

URL?MSWMExt=.
ext
```



**Código de ejemplo**


```XML
[reference]
Ref01 = https://example.com/GenerateASFFile.aspx?MSWMExt=.asf

```



## <a name="remarks"></a>Observaciones

A veces, los programas cliente usan una extensión de nombre de archivo o un tipo MIME para determinar si se debe representar un archivo multimedia como una secuencia, representar el archivo después de una descarga completa o rechazar el procesamiento del archivo. Si un programa cliente no puede determinar cómo tratar un archivo multimedia en función de la extensión de nombre de archivo o el tipo MIME, puede determinar cómo tratar el archivo mediante la inspección del parámetro *MSWMExt* . Por ejemplo, el cliente podría tratar el archivo como si tuviera una extensión igual al valor del parámetro *MSWMExt* . Para obtener más información sobre los tipos MIME y las extensiones de nombre de archivo, vea [extensiones de nombre de archivo](file-name-extensions.md). Para obtener más información acerca del parámetro *MSWMExt* , consulte el artículo [236895](https://support.microsoft.com/kb/236895) en Microsoft Knowledge base.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Versiones anteriores de los metaarchivos de Windows Media (en desuso)**](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 





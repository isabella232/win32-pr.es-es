---
title: Parámetro MSWMExt (en desuso)
description: Parámetro MSWMExt (en desuso)
ms.assetid: cc52da1a-26d1-4321-b421-b0d6f44635cc
keywords:
- Windows Metarchivos multimedia, parámetro MSWMExt
- metarchivos, parámetro MSWMExt
- Parámetro MSWMExt
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2ec80530f95d4429769758488e5a2b24b0268c57255248c7685a0d00125aa130
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574602"
---
# <a name="mswmext-parameter-deprecated"></a>Parámetro MSWMExt (en desuso)

El *parámetro MSWMExt* indica a un programa cliente el formato de un archivo al que se hace referencia.

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



## <a name="remarks"></a>Comentarios

Los programas cliente a veces usan una extensión de nombre de archivo o un tipo MIME para determinar si se debe representar un archivo multimedia como una secuencia, representar el archivo después de una descarga completa o rechazar la representación del archivo en absoluto. Si un programa cliente no puede determinar cómo tratar un archivo multimedia basado en la extensión de nombre de archivo o el tipo MIME, puede determinar cómo tratar el archivo inspeccionando el parámetro *MSWMExt.* Por ejemplo, el cliente podría tratar el archivo como si tuviera una extensión igual al valor del *parámetro MSWMExt.* Para obtener más información sobre los tipos MIME y las extensiones de nombre de archivo, vea [Extensiones de nombre de archivo](file-name-extensions.md). Para obtener más información sobre *el parámetro MSWMExt,* vea el artículo [236895](https://support.microsoft.com/kb/236895) en el Microsoft Knowledge Base.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Versiones anteriores de Windows metarchivos multimedia (en desuso)**](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 





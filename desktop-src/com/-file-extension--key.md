---
title: file_extension clave
description: Asocia una extensión de nombre de archivo a un ProgID.
ms.assetid: 018998a8-c0da-43ea-bae2-3b184897eb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d7624b63d257e0d0edf168956c862c911ba728da955e8eea3ca54f6ce452878
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071235"
---
# <a name="file_extension-key"></a><extensión \_ de archivo> clave

Asocia una extensión de nombre de archivo a un ProgID.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   .ext = ProgID
```

## <a name="remarks"></a>Comentarios

La información contenida en la clave de extensión de nombre de archivo se usa tanto en el Explorador de Windows como en los monikers de archivos. [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) usa la clave de extensión de nombre de archivo para proporcionar el CLSID asociado.

La **clave HKEY \_ LOCAL MACHINE \_ SOFTWARE \\ \\ Classes** corresponde a la clave RAÍZ **HKEY \_ CLASSES, \_** que se conservaba por compatibilidad con versiones anteriores de COM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**FileType**](filetype-key.md)
</dt> <dt>

[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 





---
title: Clave de file_extension
description: Asocia una extensión de nombre de archivo a un ProgID.
ms.assetid: 018998a8-c0da-43ea-bae2-3b184897eb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e602266f3c851975c2f8e008ced5dfc8e2d40b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903857"
---
# <a name="file_extension-key"></a>Clave de> de extensión de archivo <\_

Asocia una extensión de nombre de archivo a un ProgID.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   .ext = ProgID
```

## <a name="remarks"></a>Observaciones

La información contenida en la clave de extensión de nombre de archivo la usan el explorador de Windows y los monikers de archivo. [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) usa la clave de extensión de nombre de archivo para proporcionar el CLSID asociado.

La clave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde a la clave **\_ \_ raíz de las clases HKEY** , que se conserva por compatibilidad con versiones anteriores de com.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**FileType**](filetype-key.md)
</dt> <dt>

[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 





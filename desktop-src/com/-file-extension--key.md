---
title: file_extension clave
description: Asocia una extensión de nombre de archivo a un ProgID.
ms.assetid: 018998a8-c0da-43ea-bae2-3b184897eb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e602266f3c851975c2f8e008ced5dfc8e2d40b64
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967007"
---
# <a name="file_extension-key"></a><extensión \_ de archivo> clave

Asocia una extensión de nombre de archivo a un ProgID.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   .ext = ProgID
```

## <a name="remarks"></a>Observaciones

Tanto el Explorador de Windows como los monikers de archivos usan la información contenida en la clave de extensión de nombre de archivo. [**GetClassFile usa**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) la clave de extensión de nombre de archivo para proporcionar el CLSID asociado.

La **clave HKEY \_ LOCAL MACHINE \_ SOFTWARE \\ \\ Classes** corresponde a la clave RAÍZ **HKEY \_ CLASSES, \_** que se conservaba por compatibilidad con versiones anteriores de COM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Eltipo**](filetype-key.md)
</dt> <dt>

[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 





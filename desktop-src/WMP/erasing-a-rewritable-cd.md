---
title: Borrado de un CD regrabable
description: Borrado de un CD regrabable
ms.assetid: 272fdd2b-c174-4bde-b05e-839d547532a6
keywords:
- Windows Media Player, grabación de CD
- Modelo de objetos de Windows Media Player, grabación de CD
- modelo de objetos, grabación de CD
- Control ActiveX de Windows Media Player, grabación de CD
- Control ActiveX, grabación de CD
- Control ActiveX móvil de Windows Media Player, grabación de CD
- Windows Media Player Mobile, grabación de CD
- Grabación de CD, borrar CDs regrabables
- grabar CDs, borrar CDs regrabables
- borrado de CDs regrabables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7025b7cd70c86c0b832aa792e50a8a2c64e7f45
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077316"
---
# <a name="erasing-a-rewritable-cd"></a>Borrado de un CD regrabable

La interfaz [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) proporciona un método para borrar los discos CD-RW. Antes de borrar un CD, primero debe asegurarse de que se admite la operación. Para obtener más información, consulte [recuperar el estado de la unidad y del disco](retrieving-the-drive-and-disc-status.md).

Para empezar a borrar el contenido de un CD regrabable, llame a [IWMPCdromBurn:: Erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).


```C++

    HRESULT hr = m_spCdromBurn->erase();
    

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Grabación de un CD**](burning-a-cd.md)
</dt> <dt>

[**Recuperación de la interfaz de grabación de CD**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Iniciar el proceso de grabación**](starting-the-burn-process.md)
</dt> <dt>

[**Recuperación de la unidad y el estado del disco**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Recuperación del estado de la grabación**](retrieving-the-burn-status.md)
</dt> </dl>

 

 





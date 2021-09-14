---
title: Recuperar el estado de la unidad y el disco
description: Recuperar el estado de la unidad y el disco
ms.assetid: 5e3e6107-d2bc-450c-a86e-5d3ef7b3092a
keywords:
- Reproductor de Windows Media, cds
- Reproductor de Windows Media modelo de objetos, cds
- modelo de objetos, grabación de CD
- Reproductor de Windows Media ActiveX control, grabación de CD
- ActiveX control, grabación de CD
- Reproductor de Windows Media Control de ActiveX móvil, grabación de CD
- Reproductor de Windows Media Móvil, cds
- Grabación de CD, recuperación del estado de unidad y disco
- cds, recuperar el estado de la unidad y el disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eab66581c336f642fd53b22f81949847d0a1c89
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070893"
---
# <a name="retrieving-the-drive-and-disc-status"></a>Recuperar el estado de la unidad y el disco

Antes de iniciar una operación de grabación de CD, debe asegurarse de que la unidad de CD-ROM seleccionada admite la operación que desea realizar. Por ejemplo, debe comprobar que un CD es capaz de borrarse antes de llamar a [IWMPCdromCollection::erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase). En el código siguiente se muestra un ejemplo del [uso de IWMPCdromAvailable::isAvailable](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) para determinar si se admite una operación:


```C++
VARIANT_BOOL vbResult;
    
// Check whether this drive can burn CDs.
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("Burn");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->isAvailable(bstrItem, &vbResult);
}
if (SUCCEEDED(hr))
{
    if (VARIANT_TRUE == vbResult)
    {
        // The current drive can burn CDs.
    }
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Grabación de un CD**](burning-a-cd.md)
</dt> <dt>

[**Recuperación de la interfaz de grabación de CD**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Iniciar el proceso de grabación**](starting-the-burn-process.md)
</dt> <dt>

[**Borrado de un CD reescrito**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Recuperación del estado de grabación**](retrieving-the-burn-status.md)
</dt> </dl>

 

 





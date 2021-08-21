---
description: Paso 9.
ms.assetid: 3e476422-ab76-4a2b-af9b-d9d065d79e5b
title: Paso 9. Desconectar la página de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf4bcb670b8a8f29334f7ecd41ebba37a915f724be70e5dbbbfd7abea9730be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526094"
---
# <a name="step-9-disconnect-the-property-page"></a>Paso 9. Desconectar la página de propiedades

Invalide [**el método CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) para liberar las interfaces que obtuvo en el **método OnConnect.** Además, si el usuario descarta la hoja de propiedades sin confirmar los cambios, debe restaurar los valores originales si han cambiado. No hay ningún método "OnCancel" al que se llame cuando el usuario se cancela, por lo que debe realizar un seguimiento de si el usuario ha llamado a **OnApplyChanges.** En este ejemplo se usa la \_ variable m lVal, descrita anteriormente:


```C++
HRESULT CGrayProp::OnDisconnect(void)
{
    if (m_pGray)
    {
        // If the user clicked OK, m_lVal holds the new value.
        // Otherwise, if the user clicked Cancel, m_lVal is the old value.
        m_pGray->SetSaturation(m_lVal);  
        m_pGray->Release();
        m_pGray = NULL;
    }
    return S_OK;
}
```



Siguiente: [Paso 10. Compatibilidad con el registro COM](step-10--support-com-registration.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una página de propiedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 




---
description: Paso 9.
ms.assetid: 3e476422-ab76-4a2b-af9b-d9d065d79e5b
title: Paso 9. Desconectar la página de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59c620179e95afa3f1b949ed40cbfc3a2bca11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688219"
---
# <a name="step-9-disconnect-the-property-page"></a>Paso 9. Desconectar la página de propiedades

Invalide el método [**CBasePropertyPage:: OnDisconnection**](cbasepropertypage-ondisconnect.md) para liberar las interfaces que haya obtenido en el método **alconnect** . Además, si el usuario descarta la hoja de propiedades sin confirmar los cambios, debe restaurar los valores originales si han cambiado. No hay ningún método "OnCancel" al que se llama cuando el usuario cancela, por lo que necesita realizar un seguimiento de si el usuario ha llamado a **OnApplyChanges**. En este ejemplo se utiliza la \_ variable m lVal, descrita anteriormente:


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



Siguiente: [paso 10. Compatibilidad con el registro COM](step-10--support-com-registration.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una página de propiedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 




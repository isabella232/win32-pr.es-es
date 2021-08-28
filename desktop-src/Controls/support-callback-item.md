---
title: Cómo admitir elementos de devolución de llamada
description: En este tema se muestra cómo proporcionar compatibilidad con elementos de devolución de llamada.
ms.assetid: BD32666F-9445-4871-AE21-5DC9F5FC9C1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df078b8be8cd02f56592a74de4242b515974a740df01d3cd4bd36074d5f8e022
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968225"
---
# <a name="how-to-support-callback-items"></a>Cómo admitir elementos de devolución de llamada

En este tema se muestra cómo proporcionar compatibilidad con elementos de devolución de llamada.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


Si la aplicación va a usar elementos de devolución de llamada en un control ComboBoxEx, debe estar preparado para controlar el código de [notificación \_ GETDISPINFO de CBEN.](cben-getdispinfo.md) Un control ComboBoxEx envía esta notificación siempre que necesite que el propietario proporcione información específica del elemento. Para obtener más información sobre los elementos de devolución de llamada, vea [Elementos de devolución de llamada](comboboxex-controls.md).

La siguiente función definida por la aplicación procesa [CBEN \_ GETDISPINFO](cben-getdispinfo.md) proporcionando atributos para un elemento determinado. Tenga en cuenta que establece el **miembro mask** de la estructura [**COMBOBOXEXITEM entrante**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) en CBEIF DI \_ \_ SETITEM. Si **se establece mask** en este valor, el control conserva la información del elemento para que no tenga que volver a solicitar la información.

## <a name="complete-example"></a>Ejemplo completo


```C++
// DoItemCallback - Processes CBEN_GETDISPINFO by providing item
// attributes for a given callback item.

void WINAPI DoItemCallback(PNMCOMBOBOXEX pNMCBex)
{
    DWORD dwMask = pNMCBex->ceItem.mask;

    if(dwMask & CBEIF_TEXT)
    {
            // Insert code to provide item text.
    }

    if(dwMask & CBEIF_IMAGE) 
    {
        // Insert code to provide an item image index.
    }

    // Insert code to provide other callback information as desired.

    // Make the ComboBoxEx control hold onto the item information.
    pNMCBex->ceItem.mask = CBEIF_DI_SETITEM;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los controles ComboBoxEx](comboboxex-controls.md)
</dt> <dt>

[Referencia del control ComboBoxEx](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Usar controles ComboBoxEx](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 
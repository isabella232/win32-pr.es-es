---
title: Constantes y enumeraciones de DWM
description: Esta sección contiene información sobre las constantes y enumeraciones utilizadas en las API de Administrador de ventanas de escritorio (DWM).
ms.assetid: b01f620d-ac87-4e93-88ab-f4297d8cf1d5
keywords:
- Administrador de ventanas de escritorio (DWM), referencia
- DWM (Administrador de ventanas de escritorio), referencia
- Administrador de ventanas de escritorio (DWM), constantes
- DWM (Administrador de ventanas de escritorio), constantes
- Administrador de ventanas de escritorio (DWM), enumeraciones
- DWM (Administrador de ventanas de escritorio), enumeraciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280fff527f95176b47fc99f88d09453dbf579f38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776722"
---
# <a name="dwm-constants-and-enumerations"></a>Constantes y enumeraciones de DWM

Esta sección contiene información sobre las constantes y enumeraciones utilizadas en las API de Administrador de ventanas de escritorio (DWM).

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                     | Descripción                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Desenfoque de DWM detrás de constantes**](dwm-bb-constants.md)<br/>                          | Marcas usadas por la [**estructura \_ BLURBEHIND de DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) para indicar cuál de sus miembros contiene información válida.<br/>                                                                    |
| [**DWM habilitar constantes de composición**](dwm-ec-constants.md)<br/>                   | Marcas usadas por la función [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)  para cambiar el estado de la composición DWM.<br/>                                                                             |
| [**\_muestreo de \_ fotogramas de origen de DWM \_**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwm_source_frame_sampling)<br/>              | Marcas usadas por la función [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) para especificar el tipo de muestreo de fotogramas.<br/>                                                                            |
| [**requisitos de la ventana de pestaña de DWM \_ \_ \_**](/windows/desktop/api/dwmapi/ne-dwmapi-dwm_tab_window_requirements)<br/>          | Devuelto por DwmGetUnmetTabRequirements para indicar los requisitos necesarios para que una ventana Coloque las pestañas en la barra de título de la aplicación.<br/>                                                                    |
| [**\_Constantes TNP de DWM**](dwm-tnp-constants.md)<br/>                                | Marcas usadas por la estructura de [**\_ \_ propiedades de miniatura de DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) para indicar cuál de sus miembros contiene información válida.<br/>                                               |
| [**DWMFLIP3DWINDOWPOLICY**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmflip3dwindowpolicy)<br/>                         | Marcas usadas por la función [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) para especificar la Directiva de la ventana de Flip3D.<br/>                                                                               |
| [**DWMNCRENDERINGPOLICY**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmncrenderingpolicy)<br/>                           | Marcas usadas por la función [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) para especificar la Directiva de representación de área no cliente.<br/>                                                                   |
| [**destino de DWMTRANSITION \_ OWNEDWINDOW \_**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmtransition_ownedwindow_target)<br/> | Identifica el destino.<br/>                                                                                                                                                                               |
| [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute)<br/>                               | Marcas usadas por las funciones [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) y [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) para especificar atributos de ventana para la representación no cliente.<br/> |
| [**tipo de gesto \_**](/windows/desktop/api/Dwmapi/ne-dwmapi-gesture_type)<br/>                                          | Identifica el tipo de gesto especificado en [**DwmRenderGesture**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture).<br/>                                                                                                               |



 

 

 






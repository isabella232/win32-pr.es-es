---
description: Estructuras de la API de impresión de GDI
ms.assetid: 7753a54d-5136-4e46-a5ba-024bcfb961dc
title: Estructuras de la API de impresión de GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5af0087ed47123b29d6712df2c842a7f05c0d77997df7c3049cc42e0677a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971474"
---
# <a name="gdi-print-api-structures"></a>Estructuras de la API de impresión de GDI

## <a name="in-this-section"></a>En esta sección



| Estructura                                                      | Descripción                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)<br/>                          | La [**estructura de datos DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) contiene información sobre la inicialización y el entorno de una impresora o un dispositivo de visualización. <br/>                                                                                                              |
| [**DOCINFO**](/windows/desktop/api/Wingdi/ns-wingdi-docinfoa)<br/>                          | La [**estructura DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) contiene los nombres de archivo de entrada y salida y otra información utilizada por la [**función StartDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)<br/>                                                                                                  |
| [**DRAWPATRECT**](/windows/desktop/api/Wingdi/ns-wingdi-drawpatrect)<br/>                  | La [**estructura DRAWPATRECT**](/windows/desktop/api/wingdi/ns-wingdi-drawpatrect) define un rectángulo que se va a crear.<br/>                                                                                                                                                                         |
| [**PSFEATURE \_ CUSTPAPER**](/windows/desktop/api/Wingdi/ns-wingdi-psfeature_custpaper)<br/> | La [**estructura PSFEATURE \_ CUSTPAPER**](/windows/desktop/api/wingdi/ns-wingdi-psfeature_custpaper) contiene información sobre un tamaño de papel personalizado para un PostScript controlador. Esta estructura se usa con la función de escape de impresora [**GET \_ PS \_ FEATURESETTING.**](/previous-versions/windows/desktop/legacy/dd144954(v=vs.85))<br/> |
| [**SALIDA DE \_ PSFEATURE**](/windows/desktop/api/Wingdi/ns-wingdi-psfeature_output)<br/>       | La [**estructura PSFEATURE \_ OUTPUT**](/windows/desktop/api/wingdi/ns-wingdi-psfeature_output) contiene información sobre las PostScript salida del controlador. Esta estructura se usa con la función de escape de impresora [**GET \_ PS \_ FEATURESETTING.**](/previous-versions/windows/desktop/legacy/dd144954(v=vs.85))<br/>                  |
| [**PSINJECTDATA**](/windows/desktop/api/Wingdi/ns-wingdi-psinjectdata)<br/>                | La [**estructura PSINJECTDATA es**](/windows/desktop/api/wingdi/ns-wingdi-psinjectdata) un encabezado para el búfer de entrada utilizado con la función de escape de impresora [**POSTSCRIPT \_ INJECTION.**](/previous-versions/windows/desktop/legacy/dd162830(v=vs.85))<br/>                                                                            |



 

 


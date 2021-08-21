---
title: Opciones de la prueba de pulsación
description: En esta sección se enumeran los valores de opción que se usan con el parámetro dwOptions de la función HitTestThemeBackground. Para obtener una lista de los valores devueltos al especificar una de estas opciones, vea Valores devueltos de la prueba de acceso.
ms.assetid: a0d5c6c8-bb50-46e1-98ae-2374842344c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e3f9f3c7ba8b5c7a2c4468177befc3083bb2ed613b674cdb02f7fd3ad7f10c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166530"
---
# <a name="hit-test-options"></a>Opciones de la prueba de pulsación

En esta sección se enumeran los valores de opción que se usan con el *parámetro dwOptions* de la [**función HitTestThemeBackground.**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground) Para obtener una lista de los valores devueltos al especificar una de estas opciones, vea [Hit Test Return Values](theme-hit-test-retval.md).

## <a name="option-values"></a>Valores de opción

En la tabla siguiente se enumeran las opciones de la prueba de acceso.



| Opción                       | Valor                                                                                                                    | Descripción                                                                                                                                                                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HTTB \_ BACKGROUNDSEG          | 0x00000000                                                                                                               | Opción de prueba de hit del segmento de fondo del tema.                                                                                                                                           |
| HTTB \_ FIXEDBORDER            | 0x00000002                                                                                                               | Opción de prueba de pulsación de borde fija.                                                                                                                                                       |
| TÍTULO DE \_ HTTB                | 0x00000004                                                                                                               | Opción de prueba de pulsación de título.                                                                                                                                                            |
| HTTB \_ RESIZINGBORDER         | (HTTB \_ RESIZINGBORDER \_ LEFT \| HTTB \_ RESIZINGBORDER \_ TOP \| HTTB \_ RESIZINGBORDER \_ RIGHT \| HTTB \_ RESIZINGBORDER \_ BOTTOM) | Opciones de prueba de impacto de borde de redimensionamiento.                                                                                                                                                   |
| HTTB \_ RESIZINGBORDER \_ LEFT   | 0x00000010                                                                                                               | Opción de prueba de pulsación de borde izquierdo de redimensionamiento.                                                                                                                                               |
| HTTB \_ RESIZINGBORDER \_ TOP    | 0x00000020                                                                                                               | Opción de prueba de selección de borde superior de redimensionamiento.                                                                                                                                                |
| HTTB \_ RESIZINGBORDER \_ RIGHT  | 0x00000040                                                                                                               | Opción de prueba de pulsación de borde derecho de redimensionamiento.                                                                                                                                              |
| HTTB \_ RESIZINGBORDER \_ BOTTOM | 0x00000080                                                                                                               | Opción de prueba de pulsación de borde inferior de redimensionamiento.                                                                                                                                             |
| HTTB \_ SIZINGTEMPLATE         | 0x00000100                                                                                                               | El borde de tamaño se especifica como una plantilla, no solo como bordes de ventana. Esta opción es mutuamente excluyente con HTTB \_ SYSTEMSIZINGMARGINS; HTTB \_ SIZINGTEMPLATE tiene prioridad.         |
| HTTB \_ SYSTEMSIZINGMARGINS    | 0x00000200                                                                                                               | Usa el ancho del borde de cambio de tamaño del sistema en lugar de los márgenes de contenido de estilo visual. Esta opción es mutuamente excluyente con HTTB \_ SIZINGTEMPLATE; HTTB \_ SIZINGTEMPLATE tiene prioridad. |



 

 

 





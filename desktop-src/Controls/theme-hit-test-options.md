---
title: Opciones de la prueba de posicionamiento
description: En esta sección se enumeran los valores de las opciones que se usan con el parámetro dwOptions de la función HitTestThemeBackground. Para obtener una lista de los valores devueltos cuando se especifica una de estas opciones, vea valores devueltos de la prueba de posicionamiento.
ms.assetid: a0d5c6c8-bb50-46e1-98ae-2374842344c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 638a7aaca83c658ad852b195cdb9514210a14c16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486810"
---
# <a name="hit-test-options"></a>Opciones de la prueba de posicionamiento

En esta sección se enumeran los valores de las opciones que se usan con el parámetro *dwOptions* de la función [**HitTestThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground) . Para obtener una lista de los valores devueltos cuando se especifica una de estas opciones, vea [valores devueltos](theme-hit-test-retval.md)de la prueba de posicionamiento.

## <a name="option-values"></a>Valores de opción

En la tabla siguiente se enumeran las opciones de la prueba de posicionamiento.



| Opción                       | Value                                                                                                                    | Descripción                                                                                                                                                                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HTTB \_ BACKGROUNDSEG          | 0x00000000                                                                                                               | Opción de prueba de posicionamiento de segmento de fondo de tema.                                                                                                                                           |
| HTTB \_ FIXEDBORDER            | 0x00000002                                                                                                               | Opción de prueba de posicionamiento de borde fijo.                                                                                                                                                       |
| \_título HTTB                | 0x00000004                                                                                                               | Opción de prueba de posicionamiento de título.                                                                                                                                                            |
| HTTB \_ RESIZINGBORDER         | (HTTB \_ RESIZINGBORDER \_ left \| HTTB \_ RESIZINGBORDER \_ Top \| HTTB \_ RESIZINGBORDER \_ right \| HTTB \_ RESIZINGBORDER \_ bottom) | Cambiar el tamaño de las opciones de la prueba de posicionamiento de borde.                                                                                                                                                   |
| HTTB \_ RESIZINGBORDER \_ izquierda   | 0x00000010                                                                                                               | Cambiar el tamaño de la opción de prueba de posicionamiento de borde izquierdo.                                                                                                                                               |
| HTTB \_ RESIZINGBORDER \_ superior    | 0x00000020                                                                                                               | Cambiar el tamaño de la opción de prueba de posicionamiento de borde superior.                                                                                                                                                |
| HTTB \_ RESIZINGBORDER \_ derecha  | 0x00000040                                                                                                               | Cambiar el tamaño de la opción de prueba de posicionamiento de borde derecho.                                                                                                                                              |
| HTTB \_ RESIZINGBORDER \_ inferior | 0x00000080                                                                                                               | Cambiar el tamaño de la opción de prueba de posicionamiento del borde inferior.                                                                                                                                             |
| HTTB \_ SIZINGTEMPLATE         | 0x00000100                                                                                                               | El borde de cambio de tamaño se especifica como una plantilla, no solo para los bordes de la ventana. Esta opción es mutuamente excluyente con HTTB \_ SYSTEMSIZINGMARGINS; HTTB \_ SIZINGTEMPLATE tiene prioridad.         |
| HTTB \_ SYSTEMSIZINGMARGINS    | 0x00000200                                                                                                               | Usa el ancho del borde de cambio de tamaño del sistema en lugar de los márgenes de contenido de estilo visual. Esta opción es mutuamente excluyente con HTTB \_ SIZINGTEMPLATE; HTTB \_ SIZINGTEMPLATE tiene prioridad. |



 

 

 





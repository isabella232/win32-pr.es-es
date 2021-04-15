---
title: Marcas de inicialización comunes de cuadros de diálogo
description: Las marcas se usan para modificar el comportamiento y la apariencia de un cuadro de diálogo común.
ms.assetid: 072cdcab-00d1-4a09-97fb-a6de2d51392e
keywords:
- Biblioteca de cuadros de diálogo comunes, inicializar
- cuadros de diálogo comunes, inicializar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0c994e743178e3b6a17129275affed099d3004
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/19/2020
ms.locfileid: "104488621"
---
# <a name="common-dialog-box-initialization-flags"></a>Marcas de inicialización comunes de cuadros de diálogo

Las marcas se usan para modificar el comportamiento y la apariencia de un cuadro de diálogo común. Las marcas de inicialización son los valores que se establecen en el miembro **Flags** de la estructura que se usa para crear el cuadro de diálogo. Las marcas se usan para especificar qué controles de un cuadro de diálogo reciben valores iniciales, para deshabilitar los controles seleccionados y para modificar el intervalo de valores que el usuario puede establecer con los controles. También puede usar las marcas para habilitar procedimientos de enlace y plantillas personalizadas para los cuadros de diálogo.

Por ejemplo, puede establecer el valor de los **\_ efectos de CF** en el miembro **Flags** de la estructura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para dirigir el cuadro de diálogo **fuente** para mostrar los controles de efectos. Estos controles permiten al usuario elegir un color de fuente, así como efectos de tachado y subrayado.

Los valores de la marca de inicialización son únicos para cada cuadro de diálogo común y se describen en detalle mediante los miembros de **marcas** de las siguientes estructuras que se corresponden con ellos:

-   [**LAS CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
-   [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
-   [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
-   [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
-   [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
-   [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)
-   [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

 

 





---
title: Marcas comunes de inicialización de cuadros de diálogo
description: Las marcas se usan para modificar el comportamiento y la apariencia de un cuadro de diálogo común.
ms.assetid: 072cdcab-00d1-4a09-97fb-a6de2d51392e
keywords:
- Biblioteca común de cuadros de diálogo, inicialización
- cuadros de diálogo comunes, inicialización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0c994e743178e3b6a17129275affed099d3004
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568349"
---
# <a name="common-dialog-box-initialization-flags"></a>Marcas comunes de inicialización de cuadros de diálogo

Las marcas se usan para modificar el comportamiento y la apariencia de un cuadro de diálogo común. Las marcas de inicialización son los valores que se establecen en el **miembro Flags** de la estructura que se usa para crear el cuadro de diálogo. Las marcas se usan para especificar qué controles de un cuadro de diálogo reciben valores iniciales, para deshabilitar los controles seleccionados y para modificar el intervalo de valores que el usuario puede establecer con los controles. También se usan las marcas para habilitar procedimientos de enlace y plantillas personalizadas para los cuadros de diálogo.

Por ejemplo, puede establecer el valor **CF \_ EFFECTS** en el miembro  **Flags** de la estructura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para dirigir el cuadro de diálogo Fuente para mostrar los controles de efectos. Estos controles permiten al usuario elegir un color de fuente, así como efectos de tachado y subrayado.

Los valores de marca de inicialización son únicos para cada cuadro de diálogo común y se describen en detalle mediante los miembros **Flags** de las estructuras siguientes que se corresponden con ellos:

-   [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
-   [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
-   [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
-   [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
-   [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
-   [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)
-   [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

 

 





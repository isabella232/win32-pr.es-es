---
description: Los temas de esta sección abordan la funcionalidad básica de las fuentes internacionales.
ms.assetid: a47303b5-f49b-4d6c-b061-9d6475530e83
title: Administración internacional de fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ade599577f97c696d3205e32bfaaca106ddaae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274879"
---
# <a name="international-font-management"></a>Administración internacional de fuentes

Los temas de esta sección abordan la funcionalidad básica de las fuentes internacionales. Para obtener instrucciones sobre el uso de la tecnología de fuentes internacionales en las aplicaciones, vea [International Font Enumeration and Selection](using-international-fonts-and-text.md) y Using MS Shell Dlg and MS Shell Dlg 2 ( Enumeración y selección de fuentes internacionales) y Using MS Shell Dlg 2 (Uso de Dlg de Shell de [MS y Dlg 2 de MS Shell).](using-ms-shell-dlg-and-ms-shell-dlg-2.md)

## <a name="font-management-infrastructure"></a>Infraestructura de administración de fuentes

A partir Windows 7, la infraestructura de administración de fuentes admite la ocultación de fuentes que no son adecuadas para las listas de selección de fuentes de un usuario. La configuración predeterminada del sistema elegirá ocultar automáticamente las fuentes que no están diseñadas para los idiomas de entrada (teclados) habilitados en el sistema operativo. Además, los usuarios pueden optar por ocultar manualmente las fuentes en la página Fuentes Panel de control. Esta característica significa que los usuarios ya no necesitan enfrentarse a listas largas de fuentes inapropiadas y es especialmente valiosa para los usuarios internacionales que trabajan en scripts no latinos.

En Windows 7, no hay NINGUNA API para consultar directamente qué fuentes están ocultas o para establecer las fuentes que se ocultarán. Sin embargo, esto no significa que no pueda aprovechar esta característica en la aplicación. Si usa la API Windows [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) (cuadro de diálogo común de fuente) para habilitar la selección de fuentes hoy, se obtiene el nuevo comportamiento de forma gratuita. La nueva cinta Windows Ribbon (Font Controls) introducida en Windows 7 también admite este comportamiento y proporciona otra razón para "ribbonize" las aplicaciones. Para obtener más información sobre el uso de controles de fuente en la cinta de opciones y **ChooseFont** para mostrar fuentes mientras se filtran las fuentes ocultas, consulte Enumeración de fuentes internacionales [y Selección.](using-international-fonts-and-text.md)

Tenga en cuenta que ocultar fuentes solo afecta a la interfaz de usuario de selección de fuentes. No afecta a las API de dibujo. Cuando se selecciona una fuente en un contexto de dispositivo, no hay ningún efecto en el dibujo debido a que la fuente está oculta. La [**función EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) sigue enumerando las fuentes que están establecidas en hidden.

## <a name="gdi-font-embedding-and-subsetting"></a>Inserción y subconjunto de fuentes GDI

La tecnología de fuentes internacionales usa la biblioteca de servicios de inserción de fuentes para permitirle agrupar fuentes TrueType y OpenType en un documento o archivo. Insertar una fuente en un archivo garantiza que la fuente estará presente en el equipo que recibe el archivo. Para obtener más información, vea [Font Embedding Reference](../gdi/font-embedding-reference.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumeración y selección de fuentes internacionales](using-international-fonts-and-text.md)
</dt> <dt>

[Uso de MS Shell Dlg y MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md)
</dt> <dt>

[Referencia de incrustación de fuentes](../gdi/font-embedding-reference.md)
</dt> </dl>

 

 

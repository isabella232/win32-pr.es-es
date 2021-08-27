---
description: Los temas de esta sección abordan la funcionalidad básica de las fuentes internacionales.
ms.assetid: a47303b5-f49b-4d6c-b061-9d6475530e83
title: Administración internacional de fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4c44661b234a95abb4d40f2204382b3d074bf1d7c0bb1c68a241345211695f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083055"
---
# <a name="international-font-management"></a>Administración internacional de fuentes

Los temas de esta sección abordan la funcionalidad básica de las fuentes internacionales. Para obtener instrucciones sobre el uso de la tecnología de fuentes internacionales en las aplicaciones, vea [International Font Enumeration and Selection](using-international-fonts-and-text.md) y Using [MS Shell Dlg and MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md).

## <a name="font-management-infrastructure"></a>Infraestructura de administración de fuentes

A partir Windows 7, la infraestructura de administración de fuentes admite la ocultación de fuentes que no son adecuadas para las listas de selección de fuentes de un usuario. La configuración predeterminada del sistema elegirá ocultar automáticamente las fuentes que no están diseñadas para los idiomas de entrada (teclados) habilitados en el sistema operativo. Además, los usuarios pueden optar por ocultar manualmente las fuentes en la página Fuentes Panel de control. Esta característica significa que los usuarios ya no tienen que enfrentarse a listas largas de fuentes inapropiadas y es especialmente útil para los usuarios internacionales que trabajan en scripts no latinos.

En Windows 7, no hay NINGUNA API para consultar directamente qué fuentes están ocultas o para configurar las fuentes que se van a ocultar. Sin embargo, esto no significa que no pueda aprovechar esta característica en la aplicación. Si usa la API [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) Windows (cuadro de diálogo Común de fuente) para habilitar la selección de fuentes hoy mismo, recibirá el nuevo comportamiento de forma gratuita. La nueva cinta Windows cinta de opciones (controles de fuente) introducida en Windows 7 también admite este comportamiento y proporciona otra razón para "ribbonize" las aplicaciones. Para obtener más información sobre el uso de controles de fuente en la cinta de opciones y **ChooseFont** para mostrar fuentes mientras se filtran las fuentes ocultas, consulte [Enumeración](using-international-fonts-and-text.md)de fuentes internacionales y Selección .

Tenga en cuenta que ocultar fuentes solo afecta a la interfaz de usuario de selección de fuentes. No afecta a las API de dibujo. Cuando se selecciona una fuente en un contexto de dispositivo, no hay ningún efecto en el dibujo debido a que la fuente está oculta. La [**función EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) sigue enumerando las fuentes que están establecidas en hidden.

## <a name="gdi-font-embedding-and-subsetting"></a>Inserción y subconjuntos de fuentes GDI

La tecnología de fuentes internacionales usa la biblioteca de servicios de inserción de fuentes para permitirle agrupar fuentes TrueType y OpenType en un documento o archivo. Insertar una fuente en un archivo garantiza que la fuente estará presente en el equipo que recibe el archivo. Para obtener más información, vea [Font Embedding Reference](../gdi/font-embedding-reference.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumeración y selección de fuentes internacionales](using-international-fonts-and-text.md)
</dt> <dt>

[Uso de Dlg de shell de MS y Dlg 2 de Shell de MS](using-ms-shell-dlg-and-ms-shell-dlg-2.md)
</dt> <dt>

[Referencia de incrustación de fuentes](../gdi/font-embedding-reference.md)
</dt> </dl>

 

 

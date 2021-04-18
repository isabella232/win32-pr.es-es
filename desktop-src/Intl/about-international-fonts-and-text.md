---
description: En los temas de esta sección se aborda la funcionalidad básica de fuentes internacionales.
ms.assetid: a47303b5-f49b-4d6c-b061-9d6475530e83
title: Administración de fuentes internacionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ade599577f97c696d3205e32bfaaca106ddaae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687833"
---
# <a name="international-font-management"></a>Administración de fuentes internacionales

En los temas de esta sección se aborda la funcionalidad básica de fuentes internacionales. Para obtener instrucciones sobre el uso de la tecnología de fuentes internacionales en sus aplicaciones, consulte [enumeración y selección de fuentes internacionales](using-international-fonts-and-text.md) y [uso de MS Shell Dlg y MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md).

## <a name="font-management-infrastructure"></a>Infraestructura de administración de fuentes

A partir de Windows 7, la infraestructura de administración de fuentes admite la ocultación de fuentes que no son adecuadas para las listas de selección de fuentes de un usuario. La configuración predeterminada del sistema elige ocultar automáticamente las fuentes que no están diseñadas para los idiomas de entrada (teclados) habilitados en el sistema operativo. Además, los usuarios pueden optar por ocultar las fuentes manualmente en el panel de control fuentes. Esta característica significa que los usuarios ya no necesitan tener listas largas de fuentes inadecuadas, y es especialmente útil para los usuarios internacionales que trabajan en scripts no latinos.

En Windows 7, no hay ninguna API para consultar directamente las fuentes que están ocultas o para establecer las fuentes que se van a ocultar. Sin embargo, esto no significa que no pueda beneficiarse de esta característica en su aplicación. Si usa la API de Windows [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) (cuadro de diálogo de fuentes comunes) para habilitar la selección de fuentes hoy, obtendrá el nuevo comportamiento de forma gratuita. La nueva cinta Windows Scenic (controles de fuente) introducida en Windows 7 también es compatible con este comportamiento y proporciona otro motivo para "hacer en la cinta" las aplicaciones. Para obtener detalles sobre el uso de controles de fuente en la cinta de opciones y **ChooseFont** para mostrar fuentes mientras se filtran las fuentes ocultas, haga referencia a la [enumeración de fuentes internacionales y seleccione](using-international-fonts-and-text.md).

Tenga en cuenta que ocultar fuentes solo afecta a la interfaz de usuario de selección de fuente. No afecta a las API de dibujo. Cuando se selecciona una fuente en un contexto de dispositivo, no hay ningún efecto en el dibujo debido a que la fuente está oculta. La función [**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) sigue enumerando las fuentes que están establecidas en Hidden.

## <a name="gdi-font-embedding-and-subsetting"></a>Incrustación y subconjunto de fuentes de GDI

La tecnología de fuentes internacionales hace uso de la biblioteca de servicios de incrustación de fuentes para que pueda agrupar las fuentes TrueType y OpenType en un documento o archivo. La incrustación de una fuente en un archivo garantiza que la fuente estará presente en el equipo que recibe el archivo. Para obtener más información, vea [referencia de incrustación de fuentes](../gdi/font-embedding-reference.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumeración y selección de fuentes internacionales](using-international-fonts-and-text.md)
</dt> <dt>

[Usar MS Shell Dlg y MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md)
</dt> <dt>

[Referencia de incrustación de fuentes](../gdi/font-embedding-reference.md)
</dt> </dl>

 

 

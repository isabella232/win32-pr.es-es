---
description: A partir de Windows Vista, el TextInputPanel reemplaza a PenInputPanel para controlar el aspecto de la pantalla y el comportamiento del panel de entrada de Tablet PC. en las secciones siguientes se describe la programación del panel de entrada mediante las interfaces de programación de aplicaciones del panel de entrada de texto. TextInputPanel para los usuarios del panel de entrada de PenInputPanelUsing AutoCompleteEnabling corrección de texto para la entrada de lápiz personalizada CollectorsNote el panel de entrada de texto se implementa en un archivo ejecutable denominado TabTip.exe. La ejecución de TabTip.exe con el parámetro/SeekDesktop intenta ejecutar una versión reducida de la funcionalidad del panel de entrada en un escritorio interactivo no estándar, tal y como se crea con CreateDesktop. En el caso de la mayoría de los escritorios creados, el panel de entrada ya se ejecutará automáticamente en este modo. Este parámetro proporciona los medios para iniciarlo en escenarios de aplicaciones inusuales que, de otro modo, impiden el inicio automático. Si el panel de entrada ya se está ejecutando en el escritorio, este parámetro no tendrá ningún efecto y la instancia de TabTip.exe se cerrará inmediatamente.
ms.assetid: af0a2946-88d0-4f2e-98ca-446398aeb6b8
title: Programar el panel de entrada de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5e6b379a26199e602fc68402d77fa89fb4f8fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720738"
---
# <a name="programming-the-text-input-panel"></a>Programar el panel de entrada de texto

A partir de Windows Vista, el [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) reemplaza a [**PenInputPanel**](peninputpanel-class.md) para controlar el aspecto de la pantalla y el comportamiento del panel de entrada de Tablet PC.

En las secciones siguientes se describe la programación del panel de entrada mediante las interfaces de programación de aplicaciones del panel de entrada de texto.

-   [TextInputPanel para los usuarios de PenInputPanel](textinputpanel-for-users-of-peninputpanel.md)
-   [Uso de autocompletar del panel de entrada](using-input-panel-autocomplete.md)
-   [Habilitar la corrección de texto para los recopiladores de tinta personalizados](enabling-text-correction-for-custom-ink-collectors.md)

> [!Note]  
> El panel de entrada de texto se implementa en un archivo ejecutable denominado TabTip.exe. La ejecución de TabTip.exe con el parámetro */SeekDesktop* intenta ejecutar una versión reducida de la funcionalidad del panel de entrada en un escritorio interactivo no estándar, tal y como se crea con [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa). En el caso de la mayoría de los escritorios creados, el panel de entrada ya se ejecutará automáticamente en este modo. Este parámetro proporciona los medios para iniciarlo en escenarios de aplicaciones inusuales que, de otro modo, impiden el inicio automático. Si el panel de entrada ya se está ejecutando en el escritorio, este parámetro no tendrá ningún efecto y la instancia de TabTip.exe se cerrará inmediatamente.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programar el panel de entrada mediante la clase PenInputPanel](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 

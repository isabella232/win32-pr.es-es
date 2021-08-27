---
description: A partir de Windows Vista, TextInputPanel reemplaza a PenInputPanel para controlar la apariencia y el comportamiento en pantalla del panel de entrada de tableta. En las secciones siguientes se describe la programación del panel de entrada mediante las interfaces de programación de aplicaciones del Panel de entrada de texto. TextInputPanel para usuarios de PenInputPanelUsing Input Panel AutoCompleteEnabling Text Correction for Custom Ink CollectorsNote El panel de entrada de texto se implementa en un archivo ejecutable denominado TabTip.exe. La TabTip.exe con el parámetro /SeekDesktop intenta ejecutar una versión de funcionalidad reducida del Panel de entrada en un escritorio interactivo no estándar, tal como se creó con CreateDesktop. Para la mayoría de los escritorios creados, el Panel de entrada ya se ejecutará automáticamente en este modo. Este parámetro proporciona los medios para iniciarlo en escenarios de aplicación inusuales que, de lo contrario, impiden el inicio automático. Si el Panel de entrada ya se está ejecutando en el escritorio, este parámetro no tendrá ningún efecto y la instancia de TabTip.exe cerrará inmediatamente.
ms.assetid: af0a2946-88d0-4f2e-98ca-446398aeb6b8
title: Programar el panel de entrada de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366eb0a0d1770291ba2251247364fb68e14789d19fa053800ecaeec5ef4652d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716129"
---
# <a name="programming-the-text-input-panel"></a>Programar el panel de entrada de texto

A partir Windows Vista, [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) reemplaza a [**PenInputPanel**](peninputpanel-class.md) para controlar la apariencia en pantalla y el comportamiento del panel de entrada de tableta.

En las secciones siguientes se describe la programación del Panel de entrada mediante las interfaces de programación de aplicaciones del Panel de entrada de texto.

-   [TextInputPanel para usuarios de PenInputPanel](textinputpanel-for-users-of-peninputpanel.md)
-   [Usar autocompletar del panel de entrada](using-input-panel-autocomplete.md)
-   [Habilitación de la corrección de texto para los recopiladores de lápiz personalizados](enabling-text-correction-for-custom-ink-collectors.md)

> [!Note]  
> El Panel de entrada de texto se implementa en un archivo ejecutable denominado TabTip.exe. La TabTip.exe con el parámetro */SeekDesktop* intenta ejecutar una versión de funcionalidad reducida del Panel de entrada en un escritorio interactivo no estándar, tal como se creó [**con CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa). Para la mayoría de los escritorios creados, el Panel de entrada ya se ejecutará automáticamente en este modo. Este parámetro proporciona los medios para iniciarlo en escenarios de aplicación inusuales que, de lo contrario, impiden el inicio automático. Si el Panel de entrada ya se está ejecutando en el escritorio, este parámetro no tendrá ningún efecto y la instancia de TabTip.exe cerrará inmediatamente.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programar el panel de entrada mediante la clase PenInputPanel](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 

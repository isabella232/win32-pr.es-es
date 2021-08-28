---
title: Crear controles comunes
description: En este tema se describe cómo crear una ventana que pertenece a una clase de ventana definida en la biblioteca de controles común, Comctl32.dll.
ms.assetid: BCF25606-5B49-43A5-8107-E7220BE3253C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ddc06def47cef1a34849bbe31bc3871d4c098890bd3ef53830ae6fe7076520
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916345"
---
# <a name="creating-common-controls"></a>Crear controles comunes

En este tema se describe cómo crear una ventana que pertenece a una clase de ventana definida en la biblioteca de controles común, Comctl32.dll.


Los controles más comunes pertenecen a una clase de ventana definida en el archivo DLL de control común. La clase window y el procedimiento de ventana correspondiente definen las propiedades, la apariencia y el comportamiento del control. Para asegurarse de que se carga el archivo DLL de control común, incluya la [**función InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) en la aplicación. Cree un control común especificando el nombre de la clase de ventana al llamar a la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o especificando el nombre de clase adecuado en una plantilla de cuadro de diálogo.


Cada tipo de control común tiene un conjunto de estilos de control que puede usar para variar la apariencia y el comportamiento del control. La biblioteca de controles común también incluye un conjunto de estilos de control que se aplican a dos o más tipos de controles comunes. Los estilos de control comunes se describen en la [sección](common-control-styles.md) Estilos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los controles comunes](common-controls-intro.md)
</dt> </dl>

 

 
---
description: Descripción del uso de controles de cliente para Tablet PC.
ms.assetid: 43d78acd-1f02-417d-97be-1682e90a81a2
title: Usar controles personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c713d2b3912d2bbe4a689c7d8d05d4d977a6eb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907913"
---
# <a name="using-custom-controls"></a>Usar controles personalizados

Puede personalizar los controles estándar mediante el dibujo del propietario para cambiar la apariencia del control y establecer una superclase o una subclase para cambiar el comportamiento del control. En cada caso, el código del sistema subyacente para el tipo de control estándar controla las funciones básicas de control. La mayoría de estos controles puede ser accesible si se usan correctamente.

Un control dibujado por el propietario basado en un control estándar aparece como el control estándar de las ayudas de accesibilidad y es compatible con Microsoft Active Accessibility; sin embargo, tiene una apariencia personalizada. Algunas aplicaciones usan controles personalizados para cambiar la apariencia de un control, pero los controles dibujados por el propietario son una solución más accesible. Para obtener más información sobre cómo definir menús dibujados por el propietario y exponer controles dibujados por el propietario, vea [accesibilidad](../accessibility/accessibility.md).

Establecer una superclase o una subclase es una técnica para personalizar el comportamiento de los controles existentes. Dependiendo del nuevo comportamiento del control, puede ser necesario complementar la información de accesibilidad que expone. Por ejemplo, una aplicación puede usar un control dibujado por el propietario para mostrar una X en una casilla seleccionada, en lugar de una marca de verificación, o etiquetar un botón de comando con una imagen en lugar de una palabra.

Al utilizar controles dibujados por el propietario que son una superclase o una subclase:

-   Proporcione etiquetas para todos los controles, aunque las etiquetas no estén visibles en la pantalla. Si personaliza un control de modo que el título estándar no esté visible (por ejemplo, un botón con una imagen de gráfico) y deje el título como una cadena en blanco, la ayuda de accesibilidad no podrá obtener el título y usarlo para identificar el control.
-   Asegúrese de que se admite el [**\_ GETTEXT de WM**](../winmsg/wm-gettext.md) .
-   Asegúrese de que se admiten todos los mensajes específicos de la clase. Es especialmente importante admitir mensajes de recuperación de texto como [**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md) y [**lb \_ GETTEXT**](../controls/lb-gettext.md). Establezca los bits de estilo adecuados, como **CBS \_ HASSTRINGS** y **lbs \_ HASSTRINGS**, para indicar que el control admite esos mensajes.

 

 

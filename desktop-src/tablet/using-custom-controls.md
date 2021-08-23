---
description: Descripción del uso de controles de cliente para tablet PC.
ms.assetid: 43d78acd-1f02-417d-97be-1682e90a81a2
title: Usar controles personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70699a141f0319f917953e25363db0e0cd38eb21ecc06345c581b55526ad6bbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119551885"
---
# <a name="using-custom-controls"></a>Usar controles personalizados

Puede personalizar los controles estándar mediante el dibujo del propietario para cambiar la apariencia del control y establecer una superclase o subclase para cambiar el comportamiento del control. En cada caso, el código del sistema subyacente para el tipo de control estándar controla las funciones de control básicas. La mayoría de estos controles pueden ser accesibles si los usa correctamente.

Un control dibujado por el propietario que se basa en un control estándar aparece como el control estándar para la accesibilidad ayuda y admite Microsoft Active Accessibility; sin embargo, tiene una apariencia personalizada. Algunas aplicaciones usan controles personalizados para cambiar la apariencia de un control, pero los controles dibujados por el propietario son una solución más accesible. Para obtener más información sobre cómo definir menús dibujados por el propietario y exponer controles dibujados por el propietario, vea [Accesibilidad.](../accessibility/accessibility.md)

El establecimiento de una superclase o subclase es una técnica para personalizar el comportamiento de los controles existentes. Según el nuevo comportamiento del control, puede ser necesario complementar la información de accesibilidad que expone. Por ejemplo, una aplicación puede usar un control dibujado por el propietario para mostrar una X en una casilla seleccionada, en lugar de una marca de verificación, o etiquetar un botón de comando con una imagen en lugar de una palabra.

Cuando se usan controles dibujados por el propietario que son una superclase o una subclase:

-   Proporcione etiquetas para todos los controles, incluso cuando las etiquetas no estén visibles en la pantalla. Si personaliza un control para que el título estándar no esté visible (por ejemplo, un botón con una cara gráfica) y deja el título como una cadena en blanco, la ayuda de accesibilidad no puede obtener el título y usarlo para identificar el control.
-   Asegúrese de [**que se admite WM \_ GETTEXT.**](../winmsg/wm-gettext.md)
-   Asegúrese de que se admiten todos los mensajes específicos de clase. Es especialmente importante admitir mensajes de recuperación de texto como [**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md) [**y LB \_ GETTEXT**](../controls/lb-gettext.md). Establezca los bits de estilo adecuados, como **CBS \_ HASSTRINGS** y **LBS \_ HASSTRINGS,** para indicar que el control admite esos mensajes.

 

 

---
title: Control de errores en COM (COM)
description: Control de errores en COM
ms.assetid: 15f3ae3e-1794-4948-a7aa-6309a703364b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19af496eabf50833c99d462ff074254bc39bb7a0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488902"
---
# <a name="error-handling-in-com-com"></a>Control de errores en COM (COM)

Casi todas las funciones COM y los métodos de interfaz devuelven un valor de tipo **HRESULT**. El **HRESULT** (para el *identificador del resultado*) es una forma de devolver valores correctos, de advertencia y de error. Los **Valores HRESULT** no son realmente controles de nada; solo son valores con varios campos codificados en el valor. Según la especificación COM, un resultado de cero indica que se ha realizado correctamente y un resultado distinto de cero indica un error.

En el nivel de código fuente, todos los valores de error constan de tres partes, separadas por un carácter de subrayado. La primera parte es el prefijo que identifica la instalación asociada al error, la segunda parte es E para el error y la tercera parte es una cadena que describe la condición real. Por ejemplo, se devuelve **STG \_ E \_ MEDIUMFULL** cuando no queda espacio en el disco duro. El prefijo **STG** indica la instalación del almacenamiento, **e** indica que el código de estado representa un error y **MEDIUMFULL** proporciona información específica sobre el error. Muchos de los valores que puede querer devolver desde un método de interfaz o función se definen en Winerror. h.

Para obtener más información sobre el control de errores, vea las siguientes secciones:

-   [Estructura de los códigos de error COM](structure-of-com-error-codes.md)
-   [Códigos en facil \_ ITF](codes-in-facility-itf.md)
-   [Usar macros para el control de errores](using-macros-for-error-handling.md)
-   [Control de errores COM en Java y Visual Basic](com-error-handling-in-java-and-visual-basic.md)
-   [Estrategias de control de errores](error-handling-strategies.md)
-   [Control de errores desconocidos](handling-unknown-errors.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códigos de error COM](com-error-codes.md)
</dt> </dl>

 

 





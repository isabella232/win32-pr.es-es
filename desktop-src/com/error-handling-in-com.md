---
title: Control de errores en COM (COM)
description: Control de errores en COM
ms.assetid: 15f3ae3e-1794-4948-a7aa-6309a703364b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19af496eabf50833c99d462ff074254bc39bb7a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973671"
---
# <a name="error-handling-in-com-com"></a>Control de errores en COM (COM)

Casi todas las funciones COM y los métodos de interfaz devuelven un valor del tipo **HRESULT**. HRESULT **(para** el *identificador de resultados)* es una manera de devolver valores correctos, de advertencia y de error. **Los HRESULT** no son realmente identificadores de nada; solo son valores con varios campos codificados en el valor. Según la especificación COM, un resultado de cero indica correcto y un resultado distinto de cero indica un error.

En el nivel de código fuente, todos los valores de error constan de tres partes, separadas por caracteres de subrayado. La primera parte es el prefijo que identifica la instalación asociada al error, la segunda parte es E para error y la tercera parte es una cadena que describe la condición real. Por ejemplo, **STG \_ E \_ MEDIUMFULL** se devuelve cuando no queda espacio en un disco duro. El **prefijo STG** indica la instalación de almacenamiento, **E** indica que el código de estado representa un error y **MEDIUMFULL** proporciona información específica sobre el error. Muchos de los valores que puede devolver de un método o función de interfaz se definen en Winerror.h.

Para obtener más información sobre el control de errores, vea las secciones siguientes:

-   [Estructura de códigos de error COM](structure-of-com-error-codes.md)
-   [Códigos en FACILITY \_ ITF](codes-in-facility-itf.md)
-   [Usar macros para el control de errores](using-macros-for-error-handling.md)
-   [Control de errores COM en Java y Visual Basic](com-error-handling-in-java-and-visual-basic.md)
-   [Estrategias de control de errores](error-handling-strategies.md)
-   [Control de errores desconocidos](handling-unknown-errors.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códigos de error COM](com-error-codes.md)
</dt> </dl>

 

 





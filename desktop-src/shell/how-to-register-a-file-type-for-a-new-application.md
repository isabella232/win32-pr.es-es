---
description: Si tiene previsto asociar uno o varios tipos de archivo a una nueva aplicación, debe definir un ProgID para cada tipo de archivo que quiera asociar a la aplicación.
ms.assetid: 997600C9-5264-44EC-BAEC-CB5CEEA0BD14
title: Cómo registrar un tipo de archivo para una nueva aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728cc48075ab1c2631f0a950059da65ae326ae79
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267887"
---
# <a name="how-to-register-a-file-type-for-a-new-application"></a>Cómo registrar un tipo de archivo para una nueva aplicación

Si tiene previsto asociar uno o varios tipos de archivo a una nueva aplicación, debe definir un ProgID para cada tipo de archivo que quiera asociar a la aplicación.

Para crear un ProgID para cada tipo de archivo único que controla la aplicación, siga estos pasos.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Paso 1:

Tenga en cuenta que algunos tipos de archivo tienen varias extensiones que apuntan al mismo ProgID; por ejemplo:

-   **HKEY \_ CLASSES \_ ROOT** \\ **App.jpeg** (su ProgID)
-   **HKEY \_ CLASSES \_ ROOT** \\ **.jpg** = App.jpeg (las asignaciones de tipos de archivo)
-   **HKEY \_ CLASSES \_ ROOT** \\ **.jpeg** = App.jpeg

### <a name="step-2"></a>Paso 2:

Quite los valores de ProgID al instalar y desinstalar el programa.

### <a name="step-3"></a>Paso 3:

Deje las asignaciones de tipos de archivo sin cambios en el momento de la desinstalación. Esto funciona porque las asignaciones de tipos de archivo se almacenan por usuario en HKEY CLASSES ROOT .ext y el sistema identifica el caso en el que falta el valor de ProgID y lo \_ \_ \\ omite. Dejar las asignaciones de tipos de archivo sin cambios evita la necesidad de tener código condicional que solo quite la asignación de tipos de archivo si el valor sigue apuntando al ProgID. Es importante evitar hacerlo en casos en los que otra aplicación podría haber cambiado y, por tanto, no se puede quitar fácilmente el valor.

### <a name="step-4"></a>Paso 4:

Especifique un valor único para la descripción del tipo de archivo de cada tipo de archivo ProgID mediante una de las siguientes acciones:

-   Deje vacío el valor predeterminado del ProgID, en cuyo caso el sistema usa el archivo .ext.
-   Proporcione un valor localizado a través de FriendlyTypeName y, para compatibilidad con aplicaciones antiguas que leen directamente el Registro, asegúrese de proporcionar el valor predeterminado de ProgID como la descripción del tipo de archivo (es decir, use el mismo valor al que hace referencia FriendlyTypeName en el recurso inglés).

## <a name="remarks"></a>Observaciones

Si tiene previsto asociar el archivo a una aplicación existente, busque un ProgID de aplicación en el Registro. Para obtener más información, vea [Tipos de archivo](fa-file-types.md).

 

 




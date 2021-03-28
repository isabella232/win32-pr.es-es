---
description: Si tiene previsto asociar uno o varios tipos de archivo a una nueva aplicación, debe definir un ProgID para cada tipo de archivo que desee asociar a la aplicación.
ms.assetid: 997600C9-5264-44EC-BAEC-CB5CEEA0BD14
title: Cómo registrar un tipo de archivo para una nueva aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728cc48075ab1c2631f0a950059da65ae326ae79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985423"
---
# <a name="how-to-register-a-file-type-for-a-new-application"></a>Cómo registrar un tipo de archivo para una nueva aplicación

Si tiene previsto asociar uno o varios tipos de archivo a una nueva aplicación, debe definir un ProgID para cada tipo de archivo que desee asociar a la aplicación.

Para crear un ProgID para cada tipo de archivo único que controla la aplicación, siga estos pasos.

## <a name="instructions"></a>Instrucciones

### <a name="step-1"></a>Paso 1:

Tenga en cuenta que algunos tipos de archivo tienen varias extensiones que señalan al mismo ProgID; por ejemplo:

-   **HKEY \_ Clases \_ raíz** \\ **app. JPEG** (su ProgID)
-   **HKEY \_ Clases \_ root** \\ **. jpg** = app. JPEG (asignaciones de tipo de archivo)
-   **HKEY \_ Clases \_ root** \\ **. JPEG** = app. JPEG

### <a name="step-2"></a>Paso 2:

Quite los valores de ProgID al instalar y desinstalar el programa.

### <a name="step-3"></a>Paso 3:

Dejar las asignaciones de tipos de archivo sin modificar en el momento de la desinstalación. Esto funciona porque las asignaciones de tipo de archivo se almacenan por usuario en \_ las clases HKEY \_ root \\ . ext y el sistema identifica el caso en el que falta el valor ProgID y lo omite. Dejar las asignaciones de tipos de archivo sin cambios evita la necesidad de tener código condicional que solo Quite la asignación de tipo de archivo si el valor sigue señalando al ProgID. Es importante evitar hacerlo en los casos en los que otra aplicación podría haber cambiado y, por tanto, no se puede quitar fácilmente el valor.

### <a name="step-4"></a>Paso 4:

Especifique un valor único para la descripción del tipo de archivo de cada ProgID del tipo de archivo mediante una de las siguientes acciones:

-   Deje el valor predeterminado de ProgID vacío, en cuyo caso el sistema utiliza el archivo. ext.
-   Proporcione un valor localizado a través de FriendlyTypeName y, para la compatibilidad con las aplicaciones antiguas que leen el registro directamente, asegúrese de proporcionar el valor predeterminado del ProgID como la descripción del tipo de archivo (es decir, use el mismo valor al que hace referencia el FriendlyTypeName en el recurso en inglés).

## <a name="remarks"></a>Observaciones

Si tiene previsto asociar el archivo a una aplicación existente, busque un ProgID de aplicación en el registro. Para obtener más información, vea [tipos de archivo](fa-file-types.md).

 

 




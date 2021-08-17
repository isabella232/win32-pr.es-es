---
description: Básicamente, no hay ninguna restricción sobre cómo escribir una aplicación de inicio AutoRun.
ms.assetid: 6D95E5F0-8D93-47A8-9D8C-49CBDCA150A7
title: Cómo implementar aplicaciones de inicio de ejecución automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5c31f57c8a972ee6b138b55c09c432d9cf8fc1a9f33644c92c95229c344893
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350775"
---
# <a name="how-to-implement-autorun-startup-applications"></a>Cómo implementar aplicaciones de inicio de ejecución automática

Básicamente, no hay ninguna restricción sobre cómo escribir una aplicación de inicio AutoRun. Puede implementar la aplicación de inicio para hacer lo que sea necesario para instalar, desinstalar, configurar o ejecutar la aplicación. Sin embargo, las sugerencias siguientes proporcionan algunas directrices para implementar una aplicación de inicio de AutoRun eficaz.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Paso 1:

Asegúrese de que los usuarios reciben comentarios lo antes posible después de insertar un disco AutoRun en la unidad. Las aplicaciones de inicio deben ser programas pequeños que se carguen rápidamente. Deben identificar claramente la aplicación y proporcionar una manera sencilla de cancelar la operación.

### <a name="step-2"></a>Paso 2:

Compruebe si el programa ya está instalado. Si no es así, el siguiente paso probablemente será el procedimiento de instalación. La aplicación de inicio puede aprovechar el tiempo que el usuario dedica a leer el cuadro de diálogo iniciando otro subproceso para empezar a cargar el código de instalación. Cuando el usuario haga clic en **Aceptar,** el programa de instalación ya estará parcialmente si no está totalmente cargado. Este enfoque reduce significativamente la percepción del usuario de la cantidad de tiempo que se tarda en cargar la aplicación.

> [!Note]  
> Normalmente, la parte inicial de la aplicación de inicio presenta a los usuarios una interfaz de usuario, como un cuadro de diálogo, que les pregunta cómo les gustaría continuar.

 

### <a name="step-3"></a>Paso 3:

Inicie otro subproceso para empezar a cargar el código de la aplicación para acortar el tiempo de espera del usuario. Si la aplicación ya se ha instalado, es probable que el usuario inserte el disco para ejecutar la aplicación.

### <a name="step-4"></a>Paso 4:

Use las sugerencias siguientes para minimizar el uso del disco duro:

-   Mantenga el número mínimo de archivos que deben estar en el disco duro. Deben limitarse a los archivos que son esenciales para ejecutar el programa o que tardarían una cantidad inaceptablemente grande de tiempo en leerse desde los medios.
-   En muchos casos, no es necesario instalar archivos no esenciales en el disco duro, pero podría proporcionar ventajas como un mayor rendimiento. Dé al usuario la opción de decidir cómo realizar el equilibrio entre los costos y las ventajas del almacenamiento en disco duro.
-   Proporcione una manera de desinstalar los componentes que se colocaron en el disco duro.
-   Si la aplicación almacena en caché los datos, dé al usuario control sobre los datos. Incluya opciones en la aplicación de inicio, como establecer un límite en la cantidad máxima de datos almacenados en caché que se almacenarán en el disco duro o hacer que la aplicación descarte los datos almacenados en caché cuando finalice.

### <a name="step-5"></a>Paso 5:

Deshabilite La ejecución automática si es necesario. AutoRun se puede suprimir mediante programación o deshabilitarse completamente con el Registro, incluso cuando un medio tiene un archivo Autorun.inf. Consulte [Habilitación y deshabilitación de la ejecución automática](autoplay-reg.md) para obtener más información.

 

 




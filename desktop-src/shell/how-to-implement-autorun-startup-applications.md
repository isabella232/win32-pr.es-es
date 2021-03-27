---
description: En esencia, no hay restricciones en cuanto a cómo escribir una aplicación de inicio de ejecución automática.
ms.assetid: 6D95E5F0-8D93-47A8-9D8C-49CBDCA150A7
title: Cómo implementar aplicaciones de inicio de ejecución automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b553e102f574835103898b17558541000633412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001907"
---
# <a name="how-to-implement-autorun-startup-applications"></a>Cómo implementar aplicaciones de inicio de ejecución automática

En esencia, no hay restricciones en cuanto a cómo escribir una aplicación de inicio de ejecución automática. Puede implementar la aplicación de inicio para hacer todo lo que encuentre necesario para instalar, desinstalar, configurar o ejecutar la aplicación. Sin embargo, las siguientes sugerencias proporcionan algunas instrucciones para implementar una aplicación de inicio de ejecución automática en vigor.

## <a name="instructions"></a>Instrucciones

### <a name="step-1"></a>Paso 1:

Asegúrese de que los usuarios reciben los comentarios lo antes posible después de insertar un disco de ejecución automática en la unidad. Las aplicaciones de inicio deben ser programas pequeños que se cargan rápidamente. Deben identificar claramente la aplicación y proporcionar una manera sencilla de cancelar la operación.

### <a name="step-2"></a>Paso 2:

Compruebe si el programa ya está instalado. Si no es así, el paso siguiente será probablemente el procedimiento de instalación. La aplicación de inicio puede aprovechar las ventajas del tiempo que el usuario emplea en leer el cuadro de diálogo al iniciar otro subproceso para empezar a cargar el código de instalación. En el momento en que el usuario hace clic en **Aceptar**, el programa de instalación ya estará en parte si no se ha cargado por completo. Este enfoque reduce significativamente la percepción del usuario de la cantidad de tiempo que se tarda en cargar la aplicación.

> [!Note]  
> Normalmente, la parte inicial de la aplicación de inicio presenta a los usuarios una interfaz de usuario, como un cuadro de diálogo, preguntándoles cómo desea continuar.

 

### <a name="step-3"></a>Paso 3:

Inicie otro subproceso para empezar a cargar código de aplicación para acortar el tiempo de espera del usuario. Si ya se ha instalado la aplicación, es probable que el usuario haya insertado el disco para ejecutar la aplicación.

### <a name="step-4"></a>Paso 4:

Use las siguientes sugerencias para minimizar el uso del disco duro:

-   Mantenga el número mínimo de archivos que deben estar en el disco duro. Deben estar restringidos a los archivos que son esenciales para ejecutar el programa o que tardarán una cantidad de tiempo inaceptablemente grande en leerse desde el medio.
-   En muchos casos, no es necesario instalar archivos no esenciales en el disco duro, pero puede proporcionar ventajas como el aumento del rendimiento. Ofrezca al usuario la opción de decidir cómo sacar el equilibrio entre los costos y las ventajas del almacenamiento en disco duro.
-   Proporcionan una manera de desinstalar los componentes que se colocaron en el disco duro.
-   Si la aplicación almacena en caché los datos, conceda al usuario algún control sobre él. Incluir opciones en la aplicación de inicio, como establecer un límite en la cantidad máxima de datos almacenados en caché que se almacenarán en el disco duro, o hacer que la aplicación descarte los datos almacenados en caché cuando finalice.

### <a name="step-5"></a>Paso 5:

Deshabilite la ejecución automática si es necesario. La ejecución automática se puede suprimir mediante programación o deshabilitar completamente con el registro, incluso cuando un medio tiene un archivo Autorun. inf. Vea [habilitar y deshabilitar la ejecución automática](autoplay-reg.md) para obtener más información.

 

 




---
title: Evitar la ocultación de información
description: En ocasiones, los programas ocultan información del motor de cálculo de referencias de RPC deliberadamente o accidentalmente.
ms.assetid: 016b9221-092d-4c25-a396-4f41dcdfb3cf
keywords:
- compatibilidad con versiones anteriores de 64 bits programación de Windows
- problemas de compatibilidad con la programación de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4b9e4ba7ed5165378beb93005243af03f9e469
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420976"
---
# <a name="avoiding-information-hiding"></a>Evitar la ocultación de información

En ocasiones, los programas ocultan información del motor de cálculo de referencias de RPC deliberadamente o accidentalmente. Algunos ejemplos son los siguientes:

-   Enviar una estructura de datos como un bloque de bytes no diferenciado
-   Aprovechar el rendimiento mediante el uso de un efecto secundario de un método para canalizar datos adicionales a través de la conexión
-   Intentando disfrazar un controlador pasándolo como **DWORD** o **ULong**

Se garantiza que estas técnicas presentan problemas de compatibilidad incluso antes de migrar la aplicación a Windows de 64 bits.

En lugar de enviar un contexto de servidor como **DWORD** en una llamada a procedimiento remoto estándar, use un identificador de contexto para proporcionar un identificador opaco a un contexto de servidor que se mantiene en nombre de un cliente. Los contextos se identifican mediante GUID definidos por el tiempo de ejecución de RPC cuando un servidor crea un identificador de contexto para un cliente. No se usa ningún puntero a través de la conexión y la operación es completamente transparente en los límites de 32 o 64 bits. Para obtener más información sobre el uso de identificadores de contexto, vea [identificadores de contexto](/windows/desktop/Rpc/context-handles).

Las interfaces DCOM no pueden usar identificadores de contexto porque COM proporciona su propia administración de contexto. En lugar de crear un identificador de contexto, puede pasar un puntero de interfaz al objeto COM. Después, puede llamar a los métodos directamente a través del puntero de interfaz o colocar el puntero dentro de otras llamadas. Para liberar el objeto de servidor, el cliente llama al método de **liberación** de la interfaz a través del puntero de interfaz.

De nuevo, puede haber ocasiones en las que no se pueda cambiar el diseño original del código que se está trasladando. Si no hay ninguna manera de evitar el envío de un puntero a través de la conexión como **DWORD**, tendrá que implementar algún tipo de asignación del lado servidor entre los valores **DWORD** y los punteros. Una manera de hacerlo es cambiar los punteros en la aplicación del lado cliente a tipos de precisión de puntero, como **ULong \_ ptr** o **DWORD \_ ptr**. A continuación, use la llamada de MIDL \[ [**\_ como**](/windows/desktop/Midl/call-as) \] atributo para colocar los punteros en la conexión como valores **DWORD** . El contenedor del lado cliente solo necesita pasar los argumentos. El contenedor del servidor controla la asignación entre ambos tipos. De forma similar, puede usar el atributo de \[ [**transmisión \_ como**](/windows/desktop/Midl/transmit-as) \] o el atributo de \[ [**representación \_ como**](/windows/desktop/Midl/represent-as) \] para convertir los datos a un formato compatible con versiones anteriores para la representación de la conexión.

Si la compatibilidad con el cable de retroceso no es un problema o si el identificador no se utiliza para las llamadas remotas y está seguro de que nunca se producirán llamadas remotas entre los procesos de 32 y 64 bits, puede volver a definir un argumento como **ULONG64**. Si es necesario, puede modificar la aplicación de 32 bits para pasar un **valor DWORD** al usuario. Como alternativa, puede crear códigos auxiliares independientes a partir de archivos IDL independientes para cada plataforma mediante un **valor DWORD** en windows de 32 bits y un **ULONG64** en Windows de 64 bits.

 

 
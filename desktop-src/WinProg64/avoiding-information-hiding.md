---
title: Evitar la ocultación de información
description: En ocasiones, los programas ocultan deliberada u involuntariamente información del motor de serialización RPC.
ms.assetid: 016b9221-092d-4c25-a396-4f41dcdfb3cf
keywords:
- compatibilidad con versiones anteriores de 64 bits Windows programación
- problemas de compatibilidad de programación de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4b9e4ba7ed5165378beb93005243af03f9e469
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068305"
---
# <a name="avoiding-information-hiding"></a>Evitar la ocultación de información

En ocasiones, los programas ocultan deliberada u involuntariamente información del motor de serialización RPC. Algunos ejemplos son los siguientes:

-   Envío de una estructura de datos como un bloque de bytes sin diferenciar
-   Aprovechamiento del rendimiento mediante el uso de un efecto secundario de un método para canalizar datos adicionales a través de la conexión
-   Intentar manipular un identificador pasándoselo como **DWORD** o **ULONG**

Casi se garantiza que estas técnicas introducen problemas de compatibilidad incluso antes de portabilidad de la aplicación a archivos de 64 Windows.

En lugar de enviar un contexto de servidor como **DWORD** en una llamada a procedimiento remoto estándar, use un identificador de contexto para proporcionar un identificador opaco a un contexto de servidor que se mantiene en nombre de un cliente. Los contextos se identifican mediante GUID definidos por el tiempo de ejecución de RPC cuando un servidor crea un identificador de contexto para un cliente. No se usa ningún puntero sobre la conexión y la operación es completamente transparente en los límites de 32 o 64 bits. Para obtener más información sobre el uso de identificadores de contexto, vea [Identificadores de contexto.](/windows/desktop/Rpc/context-handles)

Las interfaces DCOM no pueden usar identificadores de contexto porque COM proporciona su propia administración de contexto. En lugar de crear un identificador de contexto, puede pasar un puntero de interfaz al objeto COM. A continuación, puede llamar a los métodos directamente a través del puntero de interfaz o colocar el puntero dentro de otras llamadas. Para liberar el objeto de servidor, el cliente llama al método **Release** de la interfaz a través del puntero de interfaz.

De nuevo, puede haber ocasiones en las que no se pueda cambiar el diseño original del código que se va a portear. Si no hay ninguna manera de evitar el envío de un puntero a través de la conexión como **DWORD,** tendrá que implementar algún tipo de asignación del lado servidor entre los valores **DWORD** y los punteros. Una manera de hacerlo es cambiar los punteros de la aplicación del lado cliente a tipos de precisión de puntero, como **ULONG \_ PTR** o **DWORD \_ PTR.** A continuación, use la llamada MIDL como atributo para colocar los \[ [**\_**](/windows/desktop/Midl/call-as) \] punteros en la conexión como **valores DWORD.** El contenedor del lado cliente solo necesita pasar los argumentos. El contenedor del lado servidor controla la asignación entre ambos tipos. De forma similar, puede usar la transmisión como atributo o el atributo representar como para convertir los datos a un formato compatible con versiones anteriores para la representación \[ [**\_**](/windows/desktop/Midl/transmit-as) de \] la \[ [**\_**](/windows/desktop/Midl/represent-as) \] conexión.

Si la compatibilidad con la conexión con versiones anteriores no es un problema o si el identificador no se usa para las llamadas remotas y está seguro de que nunca se realizarán llamadas remotas entre procesos de 32 y 64 bits, puede volver a definir un argumento como **ULONG64**. Si es necesario, puede modificar la aplicación de 32 bits para pasar un **DWORD** al usuario. Como alternativa, puede crear código auxiliar independiente a partir de archivos IDL independientes para cada plataforma mediante **un DWORD** en un archivo Windows de 32 bits y un **ULONG64** en archivos de 64 Windows.

 

 
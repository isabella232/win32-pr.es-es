---
title: El archivo IDL
description: El archivo IDL está formado por una o varias definiciones de interfaz, cada una de las cuales tiene un encabezado y un cuerpo.
ms.assetid: 64a30a12-a53e-4c53-b8cf-7af85ffd0a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862adfad2a43f10dac3598279554fd6e1f00a302
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487810"
---
# <a name="the-idl-file"></a>El archivo IDL

El archivo IDL está formado por una o varias definiciones de interfaz, cada una de las cuales tiene un encabezado y un cuerpo. El encabezado contiene información que se aplica a toda la interfaz, como el UUID. Esta información se incluye entre corchetes y va seguida de la **interfaz** de palabra clave y el nombre de la interfaz. El cuerpo contiene definiciones de tipos de datos y prototipos de función de estilo C, ampliados con atributos que describen cómo se transmiten los datos a través de la red.

En este ejemplo, el encabezado de interfaz contiene solo el UUID y el número de versión. El número de versión garantiza que cuando hay varias versiones de una interfaz RPC, solo se conectarán las versiones compatibles del cliente y el servidor.

El cuerpo de la interfaz contiene el prototipo de función para **HelloProc**. En este prototipo, el parámetro de función pszString tiene los atributos **\[** [**in**](/windows/desktop/Midl/in) **\]** y **\[** [**String**](/windows/desktop/Midl/string) **\]** . El atributo in indica a la biblioteca **\[ en \]** tiempo de ejecución que el parámetro solo se pasa desde el cliente al servidor. El atributo de **\[ cadena \]** especifica que el código auxiliar debe tratar el parámetro como una cadena de caracteres de estilo C.

La aplicación cliente debe poder cerrar la aplicación de servidor, por lo que la interfaz contiene un prototipo para otra función remota,**Shutdown** , que se implementará más adelante en este tutorial.

``` syntax
//file hello.idl
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface hello
{
    void HelloProc([in, string] unsigned char * pszString);
    void Shutdown(void);
}
```

 

 
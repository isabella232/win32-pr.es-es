---
title: Requisitos del servidor DLL
description: Aunque la mayoría de los archivos DLL se pueden ejecutar en un suplente, algunos archivos dll no.
ms.assetid: f89dabe6-f65f-4d90-ad0e-c680d4b08ba5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae82aa44771d398d80169c56976df7b0e209ea6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076376"
---
# <a name="dll-server-requirements"></a>Requisitos del servidor DLL

Aunque la mayoría de los archivos DLL se pueden ejecutar en un suplente, algunos archivos dll no.

Si desea utilizar el suplente proporcionado por el sistema, el archivo DLL debe estar bien comportado. Por ejemplo, un archivo DLL que llama a métodos que registran devoluciones de llamada del cliente intentaría invocar esas devoluciones de llamada como si los punteros de función recibidos fueran instrucciones en su espacio de direcciones, que no es el caso. Del mismo modo, un archivo DLL que utiliza una variable global a la que espera que el cliente tenga acceso no funciona. En general, los parámetros que no se pueden serializar correctamente impedirán que el servidor DLL se ejecute fuera del proceso del cliente. En muchos casos, puede escribir un suplente personalizado diseñado específicamente para compensar el comportamiento "incorrecto". (Para obtener más información, consulte [Writing a Custom suplente](writing-a-custom-surrogate.md)).

Si el servidor DLL usa interfaces personalizadas, tendría que asegurarse de que el código de serialización esté disponible para esas interfaces. Por ejemplo, puede generar y registrar un archivo DLL de proxy, o proporcionar y registrar una biblioteca de tipos que permita que el servidor funcione correctamente mientras se ejecuta en un suplente.

Los servidores DLL se cargarán solo en un proceso suplente que se ejecute en el contexto de seguridad adecuado. El contexto de seguridad para el suplente del servidor DLL se determina de la misma manera que para los servidores EXE. El suplente del servidor DLL se ejecuta en el mismo contexto de seguridad que el cliente, a menos que se establezca un valor **runas** , que determina el contexto de seguridad, en la sección del registro [AppID](appid-clsid.md) del servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suplentes DLL](dll-surrogates.md)
</dt> </dl>

 

 





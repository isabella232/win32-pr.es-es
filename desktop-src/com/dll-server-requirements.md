---
title: Requisitos del servidor DLL
description: Aunque la mayoría de los archivos DLL se pueden ejecutar en un suplente, algunos archivos DLL no.
ms.assetid: f89dabe6-f65f-4d90-ad0e-c680d4b08ba5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae82aa44771d398d80169c56976df7b0e209ea6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359388"
---
# <a name="dll-server-requirements"></a>Requisitos del servidor DLL

Aunque la mayoría de los archivos DLL se pueden ejecutar en un suplente, algunos archivos DLL no.

El archivo DLL debe tener un comportamiento correcto si desea usar el suplente proporcionado por el sistema. Por ejemplo, un archivo DLL que llama a métodos que registran devoluciones de llamada desde el cliente intentaría invocar esas devoluciones de llamada como si los punteros de función que recibió fueran para obtener instrucciones en su espacio de direcciones, lo que no es el caso. De forma similar, un archivo DLL que usa una variable global a la que espera que el cliente acceda no funcionaría. En general, los parámetros que no se pueden serializar correctamente impedirán que el servidor DLL se ejecute fuera del proceso de cliente. En muchos casos, puede escribir un suplente personalizado diseñado específicamente para compensar el comportamiento "malo". (Para obtener más información, vea [Escribir un suplente personalizado).](writing-a-custom-surrogate.md)

Si el servidor DLL usa interfaces personalizadas, tendría que asegurarse de que el código de serialización está disponible para esas interfaces. Por ejemplo, puede compilar y registrar un archivo DLL de proxy o proporcionar y registrar una biblioteca de tipos que permita que el servidor funcione correctamente mientras se ejecuta en un suplente.

Los servidores DLL solo se cargarán en un proceso suplente que se ejecute en el contexto de seguridad adecuado. El contexto de seguridad del suplente del servidor DLL se determina de la misma manera que para los servidores EXE. El suplente del servidor DLL se ejecuta en el mismo contexto de seguridad que el cliente, a menos que se establezca un valor **RunAs,** que determina el contexto de seguridad, en la sección [Registro de AppID](appid-clsid.md) del servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suplentes de DLL](dll-surrogates.md)
</dt> </dl>

 

 





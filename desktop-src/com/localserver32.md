---
title: LocalServer32
description: Especifica la ruta de acceso completa a una aplicación de servidor local de 32 bits.
ms.assetid: 5d922230-f53d-4bf9-be50-c8c00f45b7a8
keywords:
- Clave del registro LocalServer32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd068f51f33b6c283384198c0206bc9c3b6357f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104533550"
---
# <a name="localserver32"></a>LocalServer32

Especifica la ruta de acceso completa a una aplicación de servidor local de 32 bits.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer32
         (Default) = path
         ServerExecutable = path
```

## <a name="remarks"></a>Observaciones

El valor **ServerExecutable** , que es de tipo **reg \_ SZ** y se admite a partir de Windows Server 2003, funciona junto con la subclave **LocalServer32** para evitar ambigüedades al utilizar la función [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) . **LocalServer32** especifica la ubicación de la aplicación de servidor com que se va a iniciar y esta información se pasa como el primer parámetro *lpApplicationName* para **CreateProcess**. Dependiendo de la implementación de **CreateProcess**, esta información puede ser ambigua. Por esta razón, si se especifica **ServerExecutable** , com pasa el valor con nombre **ServerExecutable** al parámetro *lpApplicationName* de **CreateProcess**. Si no se especifica **ServerExecutable** , com pasa **null** como el valor para el primer parámetro de **CreateProcess**.

Para ayudar a proporcionar seguridad del sistema, utilice cadenas entre comillas en la ruta de acceso para indicar dónde finaliza el nombre del archivo ejecutable y los argumentos comienzan. Por ejemplo, en lugar de especificar la siguiente ruta de acceso como la entrada de **LocalServer32** :

"C: archivos de la \\ compañía de archivos de programa \\ \\Application.exe parám1 param2"

Especifique la ruta de acceso con la siguiente sintaxis:

" \\ C: archivos de la \\ compañía de archivos de programa \\ \\Application.exe\\ " parám1 parám2 "

COM anexa la marca "-Embedding" a la cadena, por lo que la aplicación que usa marcas debe analizar toda la cadena y comprobar la marca-Embedding.

Cuando COM inicia un servidor local de 32 bits, el servidor debe registrar un objeto de clase dentro de un tiempo transcurrido establecido por el usuario. De forma predeterminada, el valor de tiempo transcurrido debe ser de al menos 5 minutos, en milisegundos, pero no puede superar el número de milisegundos en 30 días. Normalmente, las aplicaciones no deben establecer este valor, que se encuentra en la entrada **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ COM2 \\ ServerStartElapsedTime** .

Las entradas necesarias para los servidores locales de 32 bits son [**InprocHandler32**](inprochandler32.md), [**LocalServer**](localserver.md), **LocalServer32** e [**inserciones**](insertable.md).

Si un contenedor está buscando en el registro un servidor local, un servidor local de 32 bits tiene prioridad sobre un servidor local de 16 bits.

Si va a implementar clases como servicios, debe tener en cuenta que se usa el valor con nombre [**LocalService**](localservice.md) en preferencia a la clave **LocalServer32** para la activación local y remota Requestsâ € "Si **LocalService** existe y hace referencia a un servicio válido, se omite la clave **LocalServer32** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**LocalServer**](localserver.md)
</dt> <dt>

[**LocalService (Servicio local)**](localservice.md)
</dt> </dl>

 

 
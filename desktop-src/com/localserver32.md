---
title: LocalServer32
description: Especifica la ruta de acceso completa a una aplicación de servidor local de 32 bits.
ms.assetid: 5d922230-f53d-4bf9-be50-c8c00f45b7a8
keywords:
- Com de clave del Registro LocalServer32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105cb352ffa3833c59e5ee8d042689e82e77b29dbcea7e49608d0047876bdd37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859405"
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

## <a name="remarks"></a>Comentarios

El valor **ServerExecutable,** que es de tipo **REG \_ SZ** y se admite a partir de Windows Server 2003, funciona junto con la subclave **LocalServer32** para evitar cualquier ambigüedad al usar la [**función CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) **LocalServer32 especifica** la ubicación de la aplicación de servidor COM que se va a iniciar y esta información se pasa como el primer parámetro *lpApplicationName* para **CreateProcess.** En función de la implementación **de CreateProcess,** esta información puede ser ambigua. Por este motivo, si se especifica **ServerExecutable,** COM pasa el valor con nombre **ServerExecutable** al parámetro *lpApplicationName* **de CreateProcess**. Si **no se especifica ServerExecutable,** COM pasa **NULL** como valor para el primer parámetro **de CreateProcess.**

Para ayudar a proporcionar seguridad del sistema, use cadenas entre comillas en la ruta de acceso para indicar dónde finaliza el nombre de archivo ejecutable y comienzan los argumentos. Por ejemplo, en lugar de especificar la ruta de acceso siguiente como entrada **LocalServer32:**

"C: \\ Archivos de programa archivos de empresaApplication.exe \\ \\ param1 param2"

especifique la ruta de acceso con la sintaxis siguiente:

" \\ "C: \\ Archivos de programa archivos de empresaApplication.exe" \\ \\ \\ param1 param2"

COM anexa la marca "-Embedding" a la cadena, por lo que la aplicación que usa marcas debe analizar toda la cadena y buscar la marca -Embedding.

Cuando COM inicia un servidor local de 32 bits, el servidor debe registrar un objeto de clase dentro de un tiempo transcurrido establecido por el usuario. De forma predeterminada, el valor de tiempo transcurrido debe ser de al menos 5 minutos, en milisegundos, pero no puede superar el número de milisegundos en 30 días. Normalmente, las aplicaciones no deben establecer este valor, que se encuentra en la entrada **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft \_ \\ \\ \\ COM2 \\ ServerStartElapsedTime.**

Las entradas necesarias para los servidores locales de 32 bits son [**InprocHandler32,**](inprochandler32.md) [**LocalServer,**](localserver.md) **LocalServer32** e [**Insertable.**](insertable.md)

Si un contenedor busca en el Registro un servidor local, un servidor local de 32 bits tiene prioridad sobre un servidor local de 16 bits.

Si va a implementar clases como servicios, debe tener en cuenta que el valor con nombre [**LocalService**](localservice.md) se usa en lugar de la clave **LocalServer32** para las solicitudes de activación locales y remotas; si **LocalService** existe y hace referencia a un servicio válido, se omite la clave **LocalServer32.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**LocalServer**](localserver.md)
</dt> <dt>

[**LocalService (Servicio local)**](localservice.md)
</dt> </dl>

 

 
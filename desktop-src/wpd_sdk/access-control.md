---
description: Control de acceso
ms.assetid: d17137f9-b206-4ced-82e5-96a7d927c89b
title: Access Control (API de WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7820f38a41cbf9ff0199e5fde8de8ed3609063
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912890"
---
# <a name="access-control-wpd-api"></a>Access Control (API de WPD)

El Modelo de controlador de Windows (WDM) permite restringir el acceso a los dispositivos a través de listas de Access Control (ACL) en los nodos de dispositivo Plug and Play (PnP). Esto significa que los proveedores y administradores de red pueden restringir el acceso a cualquier tipo de dispositivo. Cuando una aplicación abre un identificador a un controlador mediante una llamada a [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), el administrador de e/s del controlador comprueba si el usuario especificado tiene el acceso necesario y, de igual modo, realiza comprobaciones de acceso cuando se envía IOCTL al controlador desde ese controlador.

Por ejemplo, un administrador de red puede restringir a los usuarios invitados a acceso de solo lectura para dispositivos portátiles, mientras que pueden conceder a usuarios autenticados acceso de lectura y escritura. En este caso, implica que si un invitado ha emitido un comando de WPD que requiere acceso de lectura y escritura (por ejemplo, eliminar objeto); se produciría un error de acceso denegado, mientras que si un usuario autenticado hubiera emitido el mismo comando, se realizaría correctamente.

Las entradas directiva de grupos para controlar el acceso al almacenamiento extraíble y a los dispositivos portátiles no es realmente nada más que una manera sencilla para que los administradores apliquen las ACL de nodo del dispositivo PnP a una clase completa de dispositivos a la vez (por ejemplo, al aplicar el directiva de grupo "denegar el acceso de escritura a dispositivos portátiles" ajustaría las ACL de todos los dispositivos WPD para denegar el acceso

## <a name="io-control-codes-in-wpd"></a>Códigos de control de e/s en WPD

Las aplicaciones de WPD se comunican con los controladores abriendo los controladores de dispositivos y enviando códigos de control de e/s (ioctl). Estos ioctl se componen de cuatro secciones:

1.  Tipo de dispositivo
2.  Código de función
3.  Buffer (método)
4.  Tipo de acceso

La cuarta sección, el tipo de acceso, especifica el requisito de acceso específico para el comando especificado. El administrador de e/s del controlador usa estos datos para realizar la comprobación de la lista de Access Control (ACL).

Por tanto, si se definió un IOCTL como:


```C++
    #define MY_READ_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Y, METHOD_BUFFERED, FILE_READ_ACCESS)
```



El administrador de e/s del controlador comprobará que el propietario del controlador del dispositivo tiene acceso de lectura al dispositivo cuando se envía este mensaje.

Y, si se definió un IOCTL como:


```C++
    #define MY_READWRITE_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Z, METHOD_BUFFERED, (FILE_READ_ACCESS | FILE_WRITE_ACCESS))
```



El administrador de e/s del controlador comprobaría que el propietario del identificador del dispositivo tiene acceso de lectura y escritura al dispositivo cuando se envía este mensaje.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información general de la aplicación**](application-overview.md)
</dt> <dt>

[**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)
</dt> <dt>

[**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)
</dt> </dl>

 

 




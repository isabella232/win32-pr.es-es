---
description: Control de acceso
ms.assetid: d17137f9-b206-4ced-82e5-96a7d927c89b
title: Access Control (API de WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7820f38a41cbf9ff0199e5fde8de8ed3609063
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266919"
---
# <a name="access-control-wpd-api"></a>Access Control (API de WPD)

El Windows Driver Model (WDM) admite la restricción del acceso de dispositivos a través de listas de Access Control (ACL) en los nodos de dispositivo Plug and Play (PnP). Esto significa que los proveedores y administradores de red pueden restringir el acceso a cualquier tipo de dispositivo. Cuando una aplicación abre un identificador para un controlador mediante una llamada a [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), el Administrador de E/S del controlador comprueba si el usuario determinado tiene el acceso necesario y, de forma similar, realiza comprobaciones de acceso cuando se envían ICTL al controlador desde ese identificador.

Por ejemplo, un administrador de red podría restringir a los usuarios invitados el acceso de solo lectura para dispositivos portátiles, mientras que podría conceder a los usuarios autenticados acceso de lectura y escritura. En este caso, implica que si un invitado emitió un comando WPD que requería acceso de lectura y escritura (como Eliminar objeto); se produciría un error con acceso denegado, mientras que si un usuario autenticado emitiese el mismo comando, se realizaría correctamente.

Las entradas directiva de grupo para controlar el acceso a dispositivos portátiles y de almacenamiento extraíbles no son más que una manera sencilla para que los administradores apliquen las ACL de nodo de dispositivo PnP a toda una clase de dispositivos a la vez (por ejemplo, aplicar el directiva de grupo "Denegar el acceso de escritura a dispositivos portátiles" ajustaría las ACL de todos los dispositivos WPD para denegar el acceso de escritura).

## <a name="io-control-codes-in-wpd"></a>Códigos de control de E/S en WPD

Las aplicaciones WPD se comunican con los controladores abriendo identificadores de dispositivo y enviando códigos de control de E/S (IOCTL). Estas ICTL constan de cuatro secciones:

1.  Tipo de dispositivo
2.  Código de función
3.  Buffer (método)
4.  Tipo de acceso

La cuarta sección, tipo de acceso, especifica el requisito de acceso específico para el comando especificado. El administrador de E/S del controlador usa estos datos para realizar la comprobación Access Control lista de direcciones (ACL).

Por lo tanto, si una IOCTL se definió como:


```C++
    #define MY_READ_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Y, METHOD_BUFFERED, FILE_READ_ACCESS)
```



El administrador de E/S del controlador comprobaría que el propietario del identificador del dispositivo tiene acceso de lectura al dispositivo cuando se envía este mensaje.

Y, si una IOCTL se definió como:


```C++
    #define MY_READWRITE_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Z, METHOD_BUFFERED, (FILE_READ_ACCESS | FILE_WRITE_ACCESS))
```



El administrador de E/S del controlador comprobaría que el propietario del identificador de dispositivo tiene acceso de lectura y escritura al dispositivo cuando se envía este mensaje.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción a la aplicación**](application-overview.md)
</dt> <dt>

[**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)
</dt> <dt>

[**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)
</dt> </dl>

 

 




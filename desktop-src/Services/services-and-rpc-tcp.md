---
description: A partir de Windows Vista, el administrador de control de servicios (SCM) admite llamadas a procedimientos remotos en el protocolo de control de transmisión (RPC/TCP) y canalizaciones con nombre (RPC/NP).
ms.assetid: c51732f6-c22f-4726-afaa-13a8948ac44f
title: Servicios y RPC/TCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fdb2ef3b21f280ba4e5078d302813de41a5a43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668459"
---
# <a name="services-and-rpctcp"></a>Servicios y RPC/TCP

A partir de Windows Vista, el administrador de control de servicios (SCM) admite llamadas a procedimientos remotos en el protocolo de control de transmisión (RPC/TCP) y canalizaciones con nombre (RPC/NP). De forma predeterminada, las funciones SCM del lado cliente usan RPC/TCP.

RPC/TCP es adecuado para la mayoría de las aplicaciones que usan funciones SCM de forma remota, como herramientas de supervisión o administración remota. Sin embargo, para ofrecer compatibilidad y rendimiento, es posible que algunas aplicaciones necesiten deshabilitar RPC/TCP mediante la configuración de los valores del registro descritos en este tema.

Cuando un servicio llama a una función SCM remota, el SCM del cliente primero intenta usar RPC/TCP para comunicarse con el SCM del servidor. Si el servidor ejecuta una versión de Windows que admite RPC/TCP y permite el tráfico RPC/TCP, la conexión RPC/TCPP se realizará correctamente. Si el servidor ejecuta una versión de Windows que no es compatible con RPC/TCP, o es compatible con RPC/TCP, pero funciona detrás de un firewall que solo permite el tráfico de canalización con nombre, se agota el tiempo de espera de la conexión RPC/TCP y el SCM vuelve a intentar la conexión con RPC/NP. Esto se realizará correctamente, pero puede tardar algún tiempo (normalmente más de 20 segundos), lo que hace que la función de [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) parezca bloqueada.

TCP no contiene las credenciales de usuario especificadas con un comando **net use** . Por lo tanto, si RPC/TCP está habilitado y se usa **sc.exe** para intentar tener acceso al servicio especificado, se podría producir un error de acceso denegado en el comando. Deshabilitar RPC/TCP en el lado cliente hace que el comando **sc.exe** use una canalización con nombre que contenga las credenciales de usuario, por lo que el comando se ejecutará correctamente. Para obtener información sobre sc.exe, consulte [controlar un servicio mediante SC](controlling-a-service-using-sc.md).

> [!Note]  
> Un servicio no debe proporcionar credenciales explícitas a un comando de **uso de red** , ya que esas credenciales podrían compartirse sin darse cuenta fuera de los límites del servicio. En su lugar, el servicio debe utilizar la [suplantación de cliente](/windows/desktop/SecAuthZ/client-impersonation) para suplantar al usuario.

 

### <a name="rpctcp-registry-values"></a>Valores del registro de RPC/TCP

RPC/TCP se controla mediante los valores del registro **SCMApiConnectionParam**, **DisableRPCOverTCP** y **DisableRemoteScmEndpoints** , que se encuentran bajo la clave de control CurrentControlSet del sistema **\_ \_ Machine local** \\  \\  \\  . Todos estos valores tienen un tipo de \_ datos REG DWORD. Los procedimientos siguientes muestran cómo usar estos valores del registro para controlar RPC/TCP.

En el procedimiento siguiente se describe cómo deshabilitar RPC/TCP en el lado cliente.

**Para deshabilitar RPC/TCP en el lado cliente**

1.  Combine el valor del registro **SCMApiConnectionParam** con el valor de Mask 0x80000000.
2.  Reinicie la aplicación que llama a la función [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) .

En el procedimiento siguiente se describe cómo deshabilitar TCP en el servidor.

**Para deshabilitar TCP en el lado servidor**

1.  Establezca el valor del registro **DisableRPCOverTCP** en 1.
2.  Reinicie el servidor.

En el procedimiento siguiente se describe cómo deshabilitar RPC/TCP y RPC/NP en el servidor (por ejemplo, para reducir la superficie expuesta a ataques).

**Para deshabilitar RPC/TCP y RPC/NP en el servidor**

1.  Establezca el valor del registro **DisableRemoteScmEndpoints** en 1.
2.  Reinicie el servidor.

El valor del registro **SCMApiConnectionParam** también se puede usar para especificar el intervalo de tiempo de espera de RPC/TCP, en milisegundos. Por ejemplo, un valor de 30.000 especifica un intervalo de tiempo de espera de 30 segundos. El valor predeterminado es 21.000 (21 segundos).

 

 

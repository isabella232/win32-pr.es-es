---
description: A partir de Windows Vista, el administrador de control de servicios (SCM) admite llamadas a procedimiento remoto a través del Protocolo de control de transmisión (RPC/TCP) y las canalizaciones con nombre (RPC/NP).
ms.assetid: c51732f6-c22f-4726-afaa-13a8948ac44f
title: Servicios y RPC/TCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d4ddfe95e114a972c600c9bef44864aa99fbe4ec412312d03e08fa7d7fe15b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888562"
---
# <a name="services-and-rpctcp"></a>Servicios y RPC/TCP

A partir de Windows Vista, el administrador de control de servicios (SCM) admite llamadas a procedimiento remoto a través del Protocolo de control de transmisión (RPC/TCP) y las canalizaciones con nombre (RPC/NP). Las funciones de SCM del lado cliente usan RPC/TCP de forma predeterminada.

RPC/TCP es adecuado para la mayoría de las aplicaciones que usan funciones de SCM de forma remota, como herramientas de administración remota o supervisión. Sin embargo, para la compatibilidad y el rendimiento, es posible que algunas aplicaciones deba deshabilitar RPC/TCP estableciendo los valores del Registro descritos en este tema.

Cuando un servicio llama a una función remota de SCM, el SCM del lado cliente primero intenta usar RPC/TCP para comunicarse con el SCM del lado servidor. Si el servidor ejecuta una versión de Windows admite RPC/TCP y permite el tráfico RPC/TCP, la conexión RPC/TCPP se realizará correctamente. Si el servidor ejecuta una versión de Windows que no admite RPC/TCP o que admite RPC/TCP, pero que funciona detrás de un firewall que solo permite el tráfico de canalización con nombre, se agota el tiempo de espera de la conexión RPC/TCP y el SCM vuelve a insondizar la conexión con RPC/NP. Esto se realizará correctamente, pero puede tardar algún tiempo (normalmente más de 20 segundos), lo que hace que la [**función OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) parezca bloqueada.

TCP no lleva las credenciales de usuario especificadas con un **comando net use.** Por lo tanto, si RPC/TCP está habilitado **ysc.exe** se usa para intentar acceder al servicio especificado, el comando podría producir un error con acceso denegado. Al deshabilitar RPC/TCP en el lado cliente, el comando **sc.exe** usa una canalización con nombre que lleva credenciales de usuario, por lo que el comando se realizará correctamente. Para obtener información sobre sc.exe, vea [Controlar un servicio mediante SC.](controlling-a-service-using-sc.md)

> [!Note]  
> Un servicio no debe proporcionar credenciales explícitas a un comando **net use,** ya que esas credenciales podrían compartirse accidentalmente fuera de los límites del servicio. En su lugar, el servicio debe [usar la suplantación de cliente](/windows/desktop/SecAuthZ/client-impersonation) para suplantar al usuario.

 

### <a name="rpctcp-registry-values"></a>Valores del Registro RPC/TCP

RPC/TCP se controla mediante los valores del Registro **SCMApiConnectionParam**, **DisableRPCOverTCP** y **DisableRemoteScmEndpoints,** que están todos en la clave de control **\_ \_** \\  \\ **CurrentControlSet** de HKEY LOCAL MACHINE \\  SYSTEM. Todos estos valores tienen un tipo de \_ datos REG DWORD. Los procedimientos siguientes muestran cómo usar estos valores del Registro para controlar RPC/TCP.

En el procedimiento siguiente se describe cómo deshabilitar RPC/TCP en el lado cliente.

**Para deshabilitar RPC/TCP en el lado cliente**

1.  Combine el valor del Registro **SCMApiConnectionParam** con el valor de máscara 0x80000000.
2.  Reinicie la aplicación que llama a la [**función OpenSCManager.**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)

En el procedimiento siguiente se describe cómo deshabilitar TCP en el lado servidor.

**Para deshabilitar TCP en el lado servidor**

1.  Establezca el **valor del Registro DisableRPCOverTCP** en 1.
2.  Reinicie el servidor.

En el procedimiento siguiente se describe cómo deshabilitar RPC/TCP y RPC/NP en el servidor (por ejemplo, para reducir la superficie de ataque).

**Para deshabilitar RPC/TCP y RPC/NP en el servidor**

1.  Establezca el **valor del Registro DisableRemoteScmEndpoints** en 1.
2.  Reinicie el servidor.

El valor del Registro **SCMApiConnectionParam** también se puede usar para especificar el intervalo de tiempo de espera de RPC/TCP, en milisegundos. Por ejemplo, un valor de 30 000 especifica un intervalo de tiempo de espera de 30 segundos. El valor predeterminado es 21 000 (21 segundos).

 

 

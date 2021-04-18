---
description: El número máximo de sockets admitidos por un proveedor de servicios de Windows Sockets determinado es específico de la implementación.
ms.assetid: acf5ab29-3848-4dbc-afa7-a0f19045ddec
title: Número máximo de sockets admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207893836a411a2465ffcefe10e838c2e8b59011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715118"
---
# <a name="maximum-number-of-sockets-supported"></a>Número máximo de sockets admitidos

El número máximo de sockets admitidos por un proveedor de servicios de Windows Sockets determinado es específico de la implementación. El proveedor de Microsoft Winsock limita el número máximo de sockets admitidos solo por la memoria disponible en el equipo local. Sin embargo, los proveedores de Winsock de terceros pueden tener limitaciones en cuanto a los números de sockets compatibles. Una aplicación no debe hacer suposiciones sobre la disponibilidad de un determinado número de Sockets. Para obtener más información sobre este tema, vea [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).

## <a name="fd_set-and-select"></a>FD \_ set y SELECT

\_En el archivo de encabezado *WinSock2. h* se definen varias macros de FD XXX para su uso en la migración de aplicaciones a Windows desde el entorno de Unix. Estas macros se utilizan con las funciones [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) y [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) para la migración de aplicaciones a Windows. El número máximo de sockets que puede usar una aplicación de Windows Sockets no se ve afectado por la constante del manifiesto FD \_ setSize. Este valor definido en el archivo de encabezado *WinSock2. h* se usa para construir las [**estructuras \_ set FD**](/windows/desktop/api/winsock/nf-winsock-fd_set) utilizadas con la función **Select** . El valor predeterminado en WinSock2. h es 64. Si una aplicación está diseñada para ser capaz de trabajar con más de 64 Sockets mediante las funciones **Select** y **WSAPoll** , el implementador debe definir el manifiesto FD \_ en cada archivo de código fuente antes de incluir el archivo de encabezado *WinSock2. h* . Una forma de hacerlo puede ser incluir la definición dentro de las opciones del compilador en el archivo make. Por ejemplo, puede Agregar "-DFD \_ setSize = 128" como una opción a la línea de comandos del compilador de Microsoft C++. Se debe resaltar que \_ la definición de FD setSize como un valor determinado no tiene ningún efecto en el número real de sockets que proporciona un proveedor de servicios de Windows Sockets. Este valor solo afecta a las \_ macros FD XXX usadas por las funciones **Select** y **WSAPoll** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**FD ( \_ conjunto)**](/windows/desktop/api/winsock/nf-winsock-fd_set)
</dt> <dt>

[Trasladar aplicaciones de socket a Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**no**](/windows/desktop/api/Winsock2/nf-winsock2-select)
</dt> <dt>

[Consideraciones sobre la programación de Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup)
</dt> <dt>

[**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)
</dt> </dl>

 

 

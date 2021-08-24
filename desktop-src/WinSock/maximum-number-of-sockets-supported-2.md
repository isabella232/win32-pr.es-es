---
description: El número máximo de sockets admitidos por un proveedor de servicios Windows Sockets es específico de la implementación.
ms.assetid: acf5ab29-3848-4dbc-afa7-a0f19045ddec
title: Número máximo de sockets admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b567b9733dfb869c901ac499ca8dac66904c84bbe77d750780504acee076385f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569764"
---
# <a name="maximum-number-of-sockets-supported"></a>Número máximo de sockets admitidos

El número máximo de sockets admitidos por un proveedor de servicios Windows Sockets es específico de la implementación. El proveedor de Microsoft Winsock limita el número máximo de sockets admitidos solo por la memoria disponible en el equipo local. Sin embargo, los proveedores de Winsock de terceros pueden tener limitaciones en el número de sockets admitidos. Una aplicación no debe realizar suposiciones sobre la disponibilidad de un número determinado de sockets. Para obtener más información sobre este tema, [**vea WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).

## <a name="fd_set-and-select"></a>FD \_ SET y selección

Se definen varias macros XXX de FD en el archivo de encabezado \_ *Winsock2.h* para su uso en la porción de aplicaciones para Windows desde el UNIX de ejecución. Estas macros se usan con las [**funciones select**](/windows/desktop/api/Winsock2/nf-winsock2-select) y [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) para portear aplicaciones a Windows. El número máximo de sockets que una aplicación Windows Sockets puede usar no se ve afectado por la constante de manifiesto FD \_ SETSIZE. Este valor definido en el archivo de encabezado *Winsock2.h* se usa para construir las estructuras [**FD \_ SET**](/windows/desktop/api/winsock/nf-winsock-fd_set) usadas con **la función select.** El valor predeterminado de Winsock2.h es 64. Si una aplicación está diseñada para ser capaz de trabajar con más de 64 sockets mediante las funciones **select** y **WSAPoll,** el implementador debe definir el manifiesto FD SETSIZE en cada archivo de origen antes de incluir el archivo de encabezado \_ *Winsock2.h.* Una manera de hacerlo puede ser incluir la definición dentro de las opciones del compilador en el archivo make. Por ejemplo, podría agregar "-DFD SETSIZE=128" como opción a la línea de comandos del \_ compilador para Microsoft C++. Debe destacarse que definir FD SETSIZE como un valor determinado no tiene ningún efecto en el número real de sockets proporcionado por un proveedor de servicios \_ Windows Sockets. Este valor solo afecta a las \_ macros XXX de FD usadas por las funciones **select** y **WSAPoll.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**FD \_ SET**](/windows/desktop/api/winsock/nf-winsock-fd_set)
</dt> <dt>

[Porte de aplicaciones de socket a Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**Seleccione**](/windows/desktop/api/Winsock2/nf-winsock2-select)
</dt> <dt>

[Consideraciones de programación de Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup)
</dt> <dt>

[**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)
</dt> </dl>

 

 

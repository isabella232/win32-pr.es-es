---
description: Cómo crear una aplicación auxiliar de IP básica.
ms.assetid: b53f1cf5-3659-407e-8279-5c94333f3017
title: Creación de una aplicación auxiliar de IP básica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baae961f8ffb6aa899e96fd05f0cb9f0c41469ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361652"
---
# <a name="creating-a-basic-ip-helper-application"></a>Creación de una aplicación auxiliar de IP básica

**Para crear una aplicación auxiliar de IP básica**

1.  Cree un nuevo proyecto vacío.
2.  Agregue un archivo de código fuente de C++ vacío al proyecto.
3.  Asegúrese de que el entorno de compilación hace referencia a los directorios include, lib y src del kit de desarrollo de software (SDK) de la plataforma.
4.  Asegúrese de que el entorno de compilación se vincula con el archivo de biblioteca auxiliar de IP iphlpapi. lib y el archivo de biblioteca Winsock WS2 \_ 32. lib.
    > [!Note]  
    > Algunas funciones básicas de Winsock se utilizan para devolver valores de dirección IP y otra información.

     

5.  Empiece a programar la aplicación auxiliar de IP. Use la API auxiliar de IP incluyendo el archivo de encabezado de la aplicación auxiliar de IP.

    ```C++
    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > El archivo de encabezado *iphlpapi. h* es necesario para las aplicaciones que usan las funciones auxiliares de IP. El archivo de encabezado *iphlpapi. h* incluye automáticamente otros archivos de encabezados con estructuras y enumeraciones usadas por las funciones auxiliares de IP.
    >
    > Las nuevas funciones auxiliares de IP introducidas en Windows Vista y versiones posteriores se definen en el archivo de encabezado *Netioapi. h* que se incluye automáticamente en el archivo de encabezado *iphlpapi. h* . El archivo de encabezado *Netioapi. h* nunca debe usarse directamente.
    >
    > Muchas de las estructuras y enumeraciones usadas por las funciones auxiliares de IP se definen en los archivos de encabezado *Iprtrmib. h*, *Ipexport. h* y *Iptypes. h* . Estos archivos de encabezado se incluyen automáticamente en el archivo de encabezado *iphlpapi. h* y nunca deben usarse directamente.
    >
    > En el kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado. Algunas de las estructuras se definen ahora en los archivos de encabezado *Ipmib. h*, *Tcpmib. h* y *Udpmib. h* , no en el archivo de encabezado *Iprtrmib. h* . El archivo de encabezado *Ipmib. h* incluye automáticamente el archivo de encabezado *Ifmib. h* . Tenga en cuenta que estos archivos de encabezado se incluyen automáticamente en *Iprtrmib. h*, que se incluye automáticamente en el archivo de encabezado *iphlpapi. h* .
    >
    > La mayoría de las aplicaciones que usan las API auxiliares de IP requieren el archivo de encabezado *WinSock2. h* para Windows sockets 2,0. Cuando se requiere el archivo de encabezado *WinSock2. h* , la \# línea de inclusión de este archivo debe colocarse antes que la \# línea de inclusión del archivo de encabezado *iphlpapi. h* .
    >
    > El archivo de encabezado *WinSock2. h* incluye internamente los elementos básicos del archivo de encabezado *Windows. h* , por lo que no suele haber una \# línea de inclusión para el archivo de encabezado *Windows. h* en aplicaciones auxiliares de IP. Si \# se necesita una línea de inclusión para el archivo de encabezado de *Windows. h* , debe ir precedida de la \# macro definir Win32 \_ lean \_ y \_ Mean. Por motivos históricos, el encabezado *Windows. h* tiene como valor predeterminado el archivo de encabezado *Winsock. h* para Windows Sockets 1,1. Las declaraciones del archivo de encabezado *Winsock. h* para Windows sockets 1,1 entrarán en conflicto con las declaraciones del archivo de encabezado *WinSock2. h* requerido por Windows Sockets 2,0. La \_ macro lean y Mean de Win32 impide que el archivo \_ de encabezado \_ de *Windows. h* incluya el archivo de encabezado *Winsock. h* . A continuación se muestra un ejemplo que ilustra esto.

     

    ```C++
    #ifndef WIN32_LEAN_AND_MEAN
    #define WIN32_LEAN_AND_MEAN
    #endif

    #include <windows.h>

    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > Esta aplicación auxiliar de IP básica solo usa algunas estructuras de datos de direcciones IP y direcciones IP para las funciones de conversión de cadenas de Windows Sockets 2,0. Estas funciones de Windows Sockets se pueden usar sin llamar a [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para inicializar los recursos de Windows Sockets y [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) cuando se realizan con estos recursos.
    >
    > En las aplicaciones auxiliares de IP que usan otras funciones de Winsock que no son de esta dirección IP a las funciones de cadena, se debe llamar a la función [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para inicializar los recursos de Windows Sockets antes de llamar a cualquier función de Windows Sockets y se debe llamar a [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) cuando la aplicación se realiza mediante recursos de Windows Sockets.

     

    > [!Note]
    >
    > El archivo de encabezado *stdio. h* es necesario para el uso de varias funciones estándar de C en esta aplicación auxiliar de IP básica.

     

    Siguiente paso: [recuperar información mediante GetNetworkParams](retrieving-information-using-getnetworkparams.md)

 

 

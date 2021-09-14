---
description: Cómo crear una aplicación auxiliar de IP básica.
ms.assetid: b53f1cf5-3659-407e-8279-5c94333f3017
title: Creación de una aplicación auxiliar de IP básica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baae961f8ffb6aa899e96fd05f0cb9f0c41469ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069793"
---
# <a name="creating-a-basic-ip-helper-application"></a>Creación de una aplicación auxiliar de IP básica

**Para crear una aplicación auxiliar de IP básica**

1.  Cree un nuevo proyecto vacío.
2.  Agregue un archivo de código fuente de C++ vacío al proyecto.
3.  Asegúrese de que el entorno de compilación hace referencia a los directorios Include, Lib y Src del Kit de desarrollo de software (SDK) de plataforma.
4.  Asegúrese de que el entorno de compilación se vincula al archivo iphlpapi.lib de la biblioteca auxiliar de IP y al archivo WS2 32.lib de la biblioteca \_ Winsock.
    > [!Note]  
    > Algunas funciones básicas de Winsock se usan para devolver valores de dirección IP y otra información.

     

5.  Comience a programar la aplicación del asistente de IP. Use la API del asistente de IP mediante la inclusión del archivo de encabezado del asistente de IP.

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
    > El *archivo de encabezado Iphlpapi.h* es necesario para las aplicaciones que usan las funciones auxiliares de IP. El *archivo de encabezado Iphlpapi.h* incluye automáticamente otros archivos de encabezado con estructuras y enumeraciones usadas por las funciones auxiliares de IP.
    >
    > Las nuevas funciones del asistente de IP introducidas en Windows Vista y versiones posteriores se definen en el archivo de encabezado *Netioapi.h* que se incluye automáticamente en el archivo de encabezado *Iphlpapi.h.* El *archivo de encabezado Netioapi.h* nunca debe usarse directamente.
    >
    > Muchas de las estructuras y enumeraciones usadas por las funciones auxiliares de IP se definen en los archivos de encabezado *Iprtmidb.h*, *Ipexport.h* e *Iptypes.h.* Estos archivos de encabezado se incluyen automáticamente en el archivo de encabezado *Iphlpapi.h* y nunca se deben usar directamente.
    >
    > En microsoft Windows Software Development Kit (SDK) publicado para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado. Algunas de las estructuras se definen ahora en los archivos de encabezado *Ipmib.h,* *Tcpmib.h* y *Udpmib.h,* no en el archivo de encabezado *Iprtmidb.h.* El *archivo de encabezado Ipmib.h* incluye automáticamente el archivo de encabezado *Ifmib.h.* Tenga en cuenta que estos archivos de encabezado se incluyen automáticamente en *Iprtmidb.h,* que se incluye automáticamente en el archivo de encabezado *Iphlpapi.h.*
    >
    > La mayoría de las aplicaciones que usan las API auxiliares de IP requieren el archivo de encabezado *Winsock2.h* para Windows Sockets 2.0. Cuando se requiere el archivo de encabezado *Winsock2.h,* la línea include de este archivo debe colocarse antes de la línea include del archivo de encabezado \# \# *Iphlpapi.h.*
    >
    > El archivo de encabezado *Winsock2.h* incluye internamente elementos principales del archivo de encabezado *Windows.h,* por lo que no suele haber una línea de include para el archivo de encabezado \# *Windows.h* en las aplicaciones auxiliares de IP. Si se necesita una línea de include para el archivo de encabezado Windows.h, debe ir precedida de la \# macro DEFINE  \# WIN32 LEAN AND \_ \_ \_ MEAN. Por motivos históricos, *el encabezado Windows.h* incluye de forma predeterminada el archivo de encabezado *Winsock.h* para Windows Sockets 1.1. Las declaraciones del archivo de encabezado *Winsock.h* para Windows Sockets 1.1 estarán en conflicto con las declaraciones del archivo de encabezado *Winsock2.h* requerido por Windows Sockets 2.0. La macro WIN32 LEAN AND MEAN impide que el archivo de encabezado Winsock.h se incluya en \_ el archivo de encabezado \_ \_ *Windows.h.*  A continuación se muestra un ejemplo que ilustra esto.

     

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
    > Esta aplicación básica del asistente de IP solo usa algunas estructuras de datos de direcciones IP y funciones de conversión de direcciones IP a cadenas Windows Sockets 2.0. Estas Windows sockets se pueden usar sin llamar a [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para inicializar los recursos de Windows Sockets y [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) cuando termine de usar estos recursos.
    >
    > En las aplicaciones auxiliares de IP que usan otras funciones de Winsock que no sean estas funciones de dirección IP a funciones de cadena, se debe llamar a la función [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) para inicializar los recursos de sockets de Windows antes de llamar a cualquier función de sockets de Windows y se debe llamar a [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) cuando la aplicación se realiza mediante recursos de sockets de Windows.

     

    > [!Note]
    >
    > El *archivo de encabezado Stdio.h* es necesario para el uso de varias funciones estándar de C en esta aplicación del asistente de IP básica.

     

    Paso siguiente: [Recuperar información mediante GetNetworkParams](retrieving-information-using-getnetworkparams.md)

 

 

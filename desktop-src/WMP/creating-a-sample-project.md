---
title: Crear un proyecto de ejemplo
description: Crear un proyecto de ejemplo
ms.assetid: 9cbbd1a7-88e7-4947-8dca-e06e364102f7
keywords:
- Windows Media Player tiendas en línea, crear proyectos de ejemplo
- tiendas en línea, crear proyectos de ejemplo
- tipo 2 tiendas en línea, crear proyectos de ejemplo
- Windows Media Player tiendas en línea, proyectos de ejemplo
- tiendas en línea, proyectos de ejemplo
- tipo 2 tiendas en línea, proyectos de ejemplo
- Windows Media Player tiendas en línea, Asistente para proyectos
- tiendas en línea, Asistente para proyectos
- tipo 2 tiendas en línea, Asistente para proyectos
- complementos, Asistente para proyectos
- Complementos de Windows Media Player, Asistente para proyectos
- crear proyectos de ejemplo
- ejemplos, tipo 2 tiendas en línea
- Asistente para proyectos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4756cc7ae8d27c2a790a7ac96af638eea72d861
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "104149116"
---
# <a name="creating-a-sample-project"></a>Crear un proyecto de ejemplo

Para crear un nuevo proyecto mediante el Asistente para proyectos, siga estos pasos:

1.  Abra Microsoft Visual Studio.
2.  Desde el menú **Archivo**, pulse **Nuevo** y, después, haga clic en **Proyecto**.
3.  En el cuadro de lista **tipos de proyecto** , elija **proyectos de Visual C++**.
4.  En el cuadro de lista **plantillas** , elija **Windows Media Player Asistente para tiendas en línea**.
5.  Escriba un nombre y una ubicación para el proyecto.
6.  Haga clic en **Aceptar** para iniciar el Asistente para proyectos.
7.  Seleccione **tipo 2 (integración básica)** y haga clic en **siguiente**.
8.  Escriba el nombre descriptivo y el ID. de distribuidor de contenido para el servicio. Escriba la dirección URL de la página web que quita el servicio del equipo del usuario.
    > [!Note]  
    > El valor que se proporciona para el identificador del distribuidor de contenido no debe contener espacios. El asistente quita los espacios de la cadena proporcionada.

     

9.  Haga clic en **Finish** (Finalizar) para crear el proyecto.

El asistente genera automáticamente un nuevo proyecto de C++ que crea un complemento de la tienda en línea de tipo 2 que implementa las interfaces **IWMPSubscriptionService** y **IWMPSubscriptionService2** . Cada vez que se ejecuta el asistente, se crea el mismo proyecto, pero el componente que se crea al compilar el proyecto tiene un identificador de clase único. El nombre del proyecto, el nombre descriptivo y el identificador del distribuidor de contenido también pueden ser diferentes en función de los valores proporcionados al ejecutar el asistente. El proyecto de ejemplo registra el componente mediante el uso de un nombre de clave que coincida con el valor proporcionado para el nombre descriptivo.

En el ejemplo se utiliza el código de Active Template Library (ATL) para proporcionar implementaciones COM.

El asistente crea los siguientes archivos:

-   *Projectname* dll. cpp. Implementa las exportaciones de la biblioteca de vínculos dinámicos (DLL), como la función de punto de entrada DLL principal. También contiene la declaración de módulo y el mapa de objetos ATL.
-   *Projectname*. cpp. Contiene implementaciones predeterminadas para los métodos de las interfaces IWMPSubscriptionService y IWMPSubscriptionService2. También contiene código para definir los cuadros de diálogo que se abre en el ejemplo cuando Windows Media Player llama a los métodos.
-   *Projectname*. def. Declara las exportaciones de DLL.
-   StdAfx. cpp. Incluye encabezados estándar.
-   WMP. h. El archivo de encabezado de Media Player de Windows.
-   wmpplug. h. El archivo de encabezado del complemento de Windows Media Player.
-   subscriptionservices. h. El archivo de encabezado de Windows Media Player online Stores.
-   Resource. h. Contiene definiciones de recursos.
-   **Projectname**. h. Contiene definiciones de clase para el objeto de tienda en línea y los cuadros de diálogo. Define el identificador de clase del objeto y la constante de identificador del distribuidor de contenido.
-   StdAfx. h. Contiene inclusiones del sistema estándar.
-   *NombreDeProyecto*. rc. Archivo de script de recursos. Contiene definiciones de los recursos y controles del cuadro de diálogo. Aquí también es donde se almacena la tabla de cadenas. La tabla de cadenas contiene las constantes de cadena de nombre de proyecto y nombre descriptivo. Normalmente se trabaja con este archivo en el editor de recursos de Visual Studio, no como texto sin formato.
-   *Projectname*. RGS. Archivo de script del registro. Este archivo contiene la información que se usa para agregar la clase de componente al registro para que Windows Media Player pueda encontrarla. Puede cambiar el nombre de la clave del servicio en este archivo.

> [!Note]  
> Debe establecer la dirección base del archivo DLL en 0x0F100000 para evitar conflictos con Windows Media Player.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Compilar el complemento para una tienda en línea de tipo 2**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> <dt>

[**Interfaz IWMPSubscriptionService**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[**Interfaz IWMPSubscriptionService2**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> </dl>

 

 





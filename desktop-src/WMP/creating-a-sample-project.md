---
title: Creación de un ejemplo Project
description: Creación de un ejemplo Project
ms.assetid: 9cbbd1a7-88e7-4947-8dca-e06e364102f7
keywords:
- Reproductor de Windows Media en línea, crear proyectos de ejemplo
- tiendas en línea, creación de proyectos de ejemplo
- tiendas en línea de tipo 2, creación de proyectos de ejemplo
- Reproductor de Windows Media en línea, proyectos de ejemplo
- tiendas en línea, proyectos de ejemplo
- tiendas en línea de tipo 2, proyectos de ejemplo
- Reproductor de Windows Media en línea, asistente para proyectos
- tiendas en línea, asistente para proyectos
- tiendas en línea de tipo 2, asistente para proyectos
- complementos, asistente para proyectos
- Reproductor de Windows Media complementos, asistente para proyectos
- crear proyectos de ejemplo
- samples,type 2 online stores
- Asistente para proyectos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4756cc7ae8d27c2a790a7ac96af638eea72d861
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967660"
---
# <a name="creating-a-sample-project"></a>Creación de un ejemplo Project

Para crear un nuevo proyecto mediante el Asistente para proyectos, siga estos pasos:

1.  Abra Microsoft Visual Studio.
2.  Desde el menú **Archivo**, pulse **Nuevo** y, después, haga clic en **Proyecto**.
3.  En el **cuadro Project de lista Tipos,** elija Visual C++ **Projects**.
4.  En el **cuadro de** lista Plantillas, elija Reproductor de Windows Media Online Stores Wizard ( Asistente para tiendas **en línea).**
5.  Escriba un nombre y una ubicación para el proyecto.
6.  Haga **clic en** Aceptar para iniciar el Asistente para proyectos.
7.  Seleccione **Tipo 2 (integración básica)** y haga clic **en Siguiente.**
8.  Escriba el nombre descriptivo y el identificador del distribuidor de contenido para el servicio. Escriba la dirección URL de la página web que quita el servicio del equipo del usuario.
    > [!Note]  
    > El valor que proporcione para el identificador del distribuidor de contenido no debe contener espacios. El asistente quita los espacios de la cadena que proporcione.

     

9.  Haga clic en **Finish** (Finalizar) para crear el proyecto.

El asistente genera automáticamente un nuevo proyecto de C++ que crea un complemento de tienda en línea de tipo 2 que implementa las interfaces **IWMPSubscriptionService** e **IWMPSubscriptionService2.** Cada vez que ejecuta el asistente, crea el mismo proyecto, pero el componente que se crea al compilar el proyecto tiene un identificador de clase único. El nombre del proyecto, el nombre descriptivo y el identificador del distribuidor de contenido también pueden ser diferentes en función de los valores que proporcionó al realizar la ejecución del asistente. El proyecto de ejemplo registra el componente mediante un nombre de clave que coincide con el valor proporcionado para el nombre descriptivo.

El ejemplo usa Active Template Library (ATL) para proporcionar implementaciones COM.

El asistente crea automáticamente los siguientes archivos:

-   *ProjectName* dll.cpp. Implementa las exportaciones de la biblioteca de vínculos dinámicos (DLL), como la función de punto de entrada dll principal. También contiene el mapa de objetos ATL y la declaración del módulo.
-   *ProjectName*.cpp. Contiene implementaciones predeterminadas para los métodos de las interfaces IWMPSubscriptionService e IWMPSubscriptionService2. También contiene código para definir los cuadros de diálogo que se abren en el ejemplo cuando se llama a los métodos Reproductor de Windows Media.
-   *ProjectName*.def. Declara las exportaciones dll.
-   StdAfx.cpp. Incluye encabezados estándar.
-   wmp.h. Archivo Reproductor de Windows Media encabezado.
-   wmpplug.h. El Reproductor de Windows Media de encabezado del complemento.
-   subscriptionservices.h. El Reproductor de Windows Media en línea almacena el archivo de encabezado.
-   resource.h. Contiene definiciones de recursos.
-   **ProjectName**.h. Contiene definiciones de clase para el objeto de almacén en línea y los cuadros de diálogo. Define el identificador de clase del objeto y la constante de identificador del distribuidor de contenido.
-   StdAfx.h. Contiene las funciones estándar del sistema.
-   *ProjectName*.rc. Archivo de script de recursos. Contiene definiciones de los recursos y controles del cuadro de diálogo. Aquí también se almacena la tabla de cadenas. La tabla de cadenas contiene el nombre del proyecto y las constantes de cadena de nombre descriptivo. Normalmente se trabaja con este archivo en el editor Visual Studio recursos, no como texto sin formato.
-   *ProjectName*.rgs. Archivo de script del Registro. Este archivo contiene la información que se usa para agregar la clase de componente al registro para Reproductor de Windows Media pueda encontrarlo. Puede cambiar el nombre de clave del servicio en este archivo.

> [!Note]  
> Debe establecer la dirección base del archivo DLL en 0x0F100000 evitar conflictos con Reproductor de Windows Media.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación del complemento para una tienda en línea de tipo 2**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> <dt>

[**IWMPSubscriptionService (interfaz)**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[**Interfaz IWMPSubscriptionService2**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> </dl>

 

 





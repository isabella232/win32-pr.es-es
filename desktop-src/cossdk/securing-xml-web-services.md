---
description: El acceso a las aplicaciones COM+ que se exponen como servicios Web XML se controla mediante el servidor Web de IIS, que procesa las solicitudes entrantes.
ms.assetid: 440b0636-8afc-4fb3-a179-140958948b94
title: Proteger los servicios Web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94953ce0769c44ddaeda27cacdac99ab4ff252d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705369"
---
# <a name="securing-xml-web-services"></a>Proteger los servicios Web XML

El acceso a las aplicaciones COM+ que se exponen como servicios Web XML se controla mediante el servidor Web de IIS, que procesa las solicitudes entrantes. También puede configurar IIS para que requiera que las comunicaciones con el autor de la llamada tengan lugar a través de un canal seguro establecido mediante el protocolo Capa de sockets seguros (SSL).

> [!Note]  
> Un servicio Web XML protegido no admite el acceso de WKO a través de WSDL. En su lugar, los clientes que han instalado el .NET Framework versión 1,1 pueden llamarlo en el modo CAO. Si los clientes de terceros necesitan tener acceso al servicio Web XML a través de WSDL, debe permitir el acceso anónimo.

 

> [!Note]  
> Para usar el protocolo SSL para establecer un canal de comunicación seguro, debe obtener e instalar un certificado SSL.

 

## <a name="component-services-administrative-tool"></a>Herramienta administrativa Servicios de componentes

Para seleccionar el mecanismo de autenticación para un servicio Web XML, siga estos pasos:

1.  Haga clic con el botón secundario en el icono de **mi PC** en el escritorio y haga clic en **administrar**.

2.  En **servicios y aplicaciones** e **Internet Information** Services, busque el icono correspondiente al directorio raíz virtual del servicio Web XML. Haga clic con el botón derecho en el icono del directorio y elija **propiedades**.

3.  En la pestaña **seguridad de directorios** del cuadro de diálogo Propiedades, busque **autenticación y control de acceso** y haga clic en el botón **Editar** correspondiente.

4.  En el cuadro de diálogo **métodos de autenticación** , en **acceso autenticado**, use las casillas de verificación para seleccionar los mecanismos de autenticación que desea permitir. Haga clic en **OK**.

    > [!Note]  
    > Puede configurar IIS para autenticar a los autores de llamadas mediante cualquiera de las siguientes opciones en el cuadro de diálogo **métodos de autenticación** de IIS: **autenticación integrada de Windows**, **autenticación implícita para servidores de dominio de Windows**, **autenticación básica (la contraseña se envía en texto no cifrado)** o **autenticación de .NET Passport**. También puede permitir el acceso anónimo.

     

5.  En el cuadro de diálogo Propiedades, haga clic en **Aceptar**.

Para permitir el acceso anónimo y no seguro a un servicio Web XML, siga estos pasos:

1.  Haga clic con el botón secundario en el icono de **mi PC** en el escritorio y haga clic en **administrar**.

2.  En **servicios y aplicaciones** e **Internet Information** Services, busque el icono correspondiente al directorio raíz virtual del servicio Web XML. Haga clic con el botón derecho en el icono del directorio y elija **propiedades**.

3.  En la pestaña **seguridad de directorios** del cuadro de diálogo Propiedades, busque **autenticación y control de acceso** y haga clic en el botón **Editar** correspondiente. Active la casilla **Habilitar acceso anónimo** . Haga clic en **OK**.

4.  En la pestaña **seguridad de directorios** del cuadro de diálogo Propiedades, busque **comunicaciones seguras** y haga clic en el botón **Editar** correspondiente. Desactive la casilla **requerir canal seguro (SSL)** . Haga clic en **OK**.

5.  En el cuadro de diálogo Propiedades, haga clic en **Aceptar**.

## <a name="visual-basic"></a>Visual Basic

No corresponde.

## <a name="cc"></a>C/C++

No corresponde.

## <a name="additional-security-considerations"></a>Consideraciones de seguridad adicionales

Al exigir un canal seguro, es más fácil proteger la confidencialidad de los datos intercambiados mediante el cifrado de las comunicaciones entre el cliente y el servicio Web XML. Si permite la autenticación mediante contraseñas de texto no cifrado, debe requerir un canal seguro para evitar la exposición de contraseñas en la red.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener acceso a los servicios Web XML en el modo de CAO](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Obtener acceso a los servicios Web XML en modo WKO](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Consideraciones de seguridad del servicio SOAP de COM+](com--soap-service-security-considerations.md)
</dt> <dt>

[Crear servicios Web XML](creating-xml-web-services.md)
</dt> </dl>

 

 




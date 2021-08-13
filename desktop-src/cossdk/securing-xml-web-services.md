---
description: El acceso a las aplicaciones COM+ expuestas como servicios web XML se controla mediante el servidor web IIS, que procesa las solicitudes entrantes.
ms.assetid: 440b0636-8afc-4fb3-a179-140958948b94
title: Protección de servicios Web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccc49a096def7fdca3f508ca590cd23df0fbf2e92fd816ba55300931122361e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546968"
---
# <a name="securing-xml-web-services"></a>Protección de servicios Web XML

El acceso a las aplicaciones COM+ expuestas como servicios web XML se controla mediante el servidor web IIS, que procesa las solicitudes entrantes. También puede configurar IIS para requerir que las comunicaciones con el autor de la llamada se lleve a cabo a través de un canal seguro establecido mediante el protocolo Capa de sockets seguros (SSL).

> [!Note]  
> Un servicio web XML protegido no admite el acceso WKO a través de WSDL. En su lugar, los clientes que han instalado el .NET Framework versión 1.1 pueden llamarlo en modo DESEDI. Si los clientes de terceros necesitan acceder al servicio web XML a través de WSDL, debe permitir el acceso anónimo.

 

> [!Note]  
> Para usar el protocolo SSL para establecer un canal de comunicación seguro, debe obtener e instalar un certificado SSL.

 

## <a name="component-services-administrative-tool"></a>Herramienta administrativa de servicios de componentes

Para seleccionar el mecanismo de autenticación de un servicio web XML, siga estos pasos:

1.  Haga clic con el botón **derecho en Mi PC** en el escritorio y haga clic en **Administrar.**

2.  En **Servicios y aplicaciones e** Internet Information **Service,** busque el icono correspondiente al directorio raíz virtual del servicio web XML. Haga clic con el botón derecho en el icono de directorio y elija **Propiedades.**

3.  En la pestaña **Seguridad del directorio** del cuadro de diálogo de propiedades, busque **Autenticación y control de acceso** y haga clic en el botón **Editar** correspondiente.

4.  En el **cuadro de diálogo Métodos** de autenticación, en **Acceso** autenticado , use las casillas para seleccionar los mecanismos de autenticación que desea permitir. Haga clic en **Aceptar**.

    > [!Note]  
    > Puede configurar IIS para autenticar a los llamadores mediante cualquiera de las siguientes opciones en el cuadro de diálogo Métodos de autenticación de **IIS:** Autenticación integrada de **Windows**, Autenticación implícita para servidores de dominio **Windows,** Autenticación básica (la contraseña se envía en texto no **enviado)** o autenticación **de .NET Passport**. También puede permitir el acceso anónimo.

     

5.  En el cuadro de diálogo de propiedades, haga clic **en Aceptar.**

Para permitir el acceso anónimo no seguro a un servicio web XML, siga estos pasos:

1.  Haga clic con el botón **derecho en Mi PC** en el escritorio y haga clic en **Administrar.**

2.  En **Servicios y aplicaciones e** Internet Information **Service,** busque el icono correspondiente al directorio raíz virtual del servicio web XML. Haga clic con el botón derecho en el icono de directorio y elija **Propiedades.**

3.  En la pestaña **Seguridad del directorio** del cuadro de diálogo de propiedades, busque **Autenticación y control de acceso** y haga clic en el botón **Editar** correspondiente. Active la casilla **Habilitar acceso** anónimo. Haga clic en **Aceptar**.

4.  En la **pestaña Seguridad de directorio** del cuadro de diálogo de propiedades, busque **Comunicaciones seguras** y haga clic en el **botón Editar** correspondiente. Desactive la **casilla Requerir canal seguro (SSL).** Haga clic en **Aceptar**.

5.  En el cuadro de diálogo de propiedades, haga clic **en Aceptar.**

## <a name="visual-basic"></a>Visual Basic

No corresponde.

## <a name="cc"></a>C/C++

No corresponde.

## <a name="additional-security-considerations"></a>Consideraciones de seguridad adicionales

Al requerir un canal seguro, se ayuda a proteger la confidencialidad de los datos intercambiados mediante el cifrado de las comunicaciones entre el cliente y el servicio web XML. Si permite la autenticación mediante contraseñas de texto no cifrada, debe requerir un canal seguro para evitar exponer contraseñas en la red.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso a servicios web XML en modo DESA](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Acceso a servicios web XML en modo WKO](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Consideraciones de seguridad del servicio SOAP de COM+](com--soap-service-security-considerations.md)
</dt> <dt>

[Creación de servicios web XML](creating-xml-web-services.md)
</dt> </dl>

 

 




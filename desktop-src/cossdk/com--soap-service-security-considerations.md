---
description: Consideraciones de seguridad del servicio SOAP de COM+
ms.assetid: c4f7744c-ff57-4d9d-8632-7e5bbb73449a
title: Consideraciones de seguridad del servicio SOAP de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a238860e154e9928672a64ef44f9db37e9c8ad2c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907483"
---
# <a name="com-soap-service-security-considerations"></a>Consideraciones de seguridad del servicio SOAP de COM+

El servicio SOAP de COM+ depende del servidor Web de IIS para la seguridad. Incluso en el [modo de objeto activado](accessing-xml-web-services-in-cao-mode.md)en el cliente, una RPC de com+ no transmite la identidad del cliente y, por lo tanto, no puede usar la seguridad basada en roles o cualquier otra característica de seguridad proporcionada por DCOM. Si desea ayudar a proteger la privacidad de los datos transmitidos hacia y desde el servicio Web XML, o para ayudar a proteger el servicio Web XML frente al acceso no autorizado, puede configurar IIS para limitar el acceso a un servicio Web XML basado en una dirección IP de clientes o requerir a un cliente que presente un certificado digital para comprobar su identidad. Si no limita el acceso, cualquier cliente que pueda comunicarse con el servidor web puede tener acceso al servicio Web XML.

Puede configurar IIS para cifrar las comunicaciones del servicio Web XML con los clientes mediante los protocolos SSL o TLS de cifrado de clave pública. Si no cifra las comunicaciones SOAP, los datos intercambiados entre un cliente y un servidor podrían ser observados por terceros con acceso a cualquier red a través de la cual viaja la comunicación SOAP; dependiendo de la topología de red, podría tratarse de una pequeña LAN o podría ser Internet.

De forma predeterminada, las comunicaciones SOAP sin cifrar se reciben en el puerto HTTP (80) y las comunicaciones SOAP cifradas se reciben en el Puerto HTTPS (443). Para que un cliente tenga acceso correctamente a un servicio Web XML, todos los firewalls entre el cliente y el servidor deben estar configurados para permitir que los paquetes SYN de TCP alcancen el puerto del servidor adecuado. Por el contrario, para limitar el acceso a los servicios Web XML, un administrador de Firewall puede optar por cerrar estos puertos.

La configuración de seguridad predeterminada para un componente COM expuesto como servicio Web XML varía en función de la versión de Microsoft .NET Framework que esté instalada. Si está instalada la versión 1,0, los servicios Web XML no son seguros de forma predeterminada; todas las llamadas se aceptan y no se utiliza ningún cifrado. Si está instalada la versión 1,1 o posterior, los servicios Web XML son seguros de forma predeterminada. los llamadores deben autenticarse y se requiere cifrado.

Un servicio Web XML protegido no admite el acceso de WKO a través de WSDL. En su lugar, los clientes que han instalado el .NET Framework versión 1,1 pueden llamarlo en el modo CAO. Si los clientes de terceros necesitan tener acceso al servicio Web XML a través de WSDL, debe permitir el acceso anónimo.

Un componente COM expuesto como servicio Web XML se ejecuta de forma predeterminada con los permisos del usuario anónimo (no con los permisos de su llamador). Puede configurar IIS para ejecutar el servicio Web XML como un usuario diferente; en ocasiones, esto puede ser necesario porque el componente utiliza archivos u otros recursos a los que el usuario anónimo no tiene acceso. No obstante, siempre debe intentar ejecutar el componente con los mínimos privilegios posibles, para limitar el daño que podría provocar un llamador malintencionado.

> [!Note]  
> Dado que un método expuesto a través de un servicio Web XML podría estar expuesto a llamadores malintencionados, siempre debe asegurarse de validar los parámetros de entrada de los que depende.

 

Para obtener instrucciones detalladas sobre cómo configurar los valores específicos de seguridad del servicio Web XML, vea [proteger servicios Web XML](securing-xml-web-services.md).

**Para convertir una aplicación SOAP segura en una aplicación SOAP no segura**

1.  Abra la herramienta de administración de Internet Information Services (IIS).
2.  Busque el directorio virtual de la aplicación y abra el cuadro de diálogo **propiedades** .
3.  Active la **Página habilitar contenido predeterminado** en la pestaña **documentos** .
4.  En la pestaña **seguridad de directorios** , haga clic en **Editar** en **control de autenticación y acceso anónimo**.
5.  Active el **acceso anónimo** para habilitar el acceso anónimo y haga clic en **Aceptar**.
6.  Haga clic en **Editar** en **comunicaciones seguras**.
7.  Desactive la casilla **requerir canal seguro (SSL)** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción al servicio SOAP de COM+](com--soap-service-overview.md)
</dt> </dl>

 

 




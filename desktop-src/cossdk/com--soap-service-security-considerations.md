---
description: Consideraciones de seguridad del servicio SOAP de COM+
ms.assetid: c4f7744c-ff57-4d9d-8632-7e5bbb73449a
title: Consideraciones de seguridad del servicio SOAP de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c67e034dfeaa4ec7f8688420aafcaec434653c942665ec3e3cbaa1535b51980d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548555"
---
# <a name="com-soap-service-security-considerations"></a>Consideraciones de seguridad del servicio SOAP de COM+

El servicio SOAP de COM+ depende del servidor web IIS para la seguridad. Incluso en [el modo](accessing-xml-web-services-in-cao-mode.md)de objeto activado por el cliente, una RPC de COM+ no transmite la identidad del cliente y, por tanto, no puede usar la seguridad basada en roles ni ninguna otra característica de seguridad proporcionada por DCOM. Si desea ayudar a proteger la privacidad de los datos transmitidos hacia y desde el servicio web XML, o para ayudar a proteger el servicio web XML frente a accesos no autorizados, puede configurar IIS para limitar el acceso a un servicio web XML basado en una dirección IP de clientes o para requerir que un cliente presente un certificado digital para comprobar su identidad. Si no limita el acceso, cualquier cliente que pueda comunicarse con el servidor web puede acceder al servicio web XML.

Puede configurar IIS para cifrar las comunicaciones del servicio web XML con los clientes mediante los protocolos SSL o TLS de cifrado de claves públicas. Si no cifra las comunicaciones SOAP, los datos intercambiados entre un cliente y un servidor podrían ser observados por un tercero con acceso a cualquier red a través de la que viaja la comunicación SOAP. dependiendo de la topología de red, podría ser una LAN pequeña o podría ser Internet.

De forma predeterminada, las comunicaciones SOAP sin cifrar se reciben en el puerto HTTP (80) y las comunicaciones SOAP cifradas se reciben en el puerto HTTPS (443). Para que un cliente acceda correctamente a un servicio web XML, se deben configurar los firewalls entre el cliente y el servidor para permitir que los paquetes TCP SYN lleguen al puerto de servidor adecuado. Por el contrario, para limitar el acceso a los servicios web XML, un administrador de firewall puede optar por cerrar estos puertos.

La configuración de seguridad predeterminada para un componente COM expuesto como un servicio web XML varía en función de la versión de Microsoft .NET Framework está instalada. Si está instalada la versión 1.0, los servicios web XML no son seguros de forma predeterminada; se aceptan todas las llamadas y no se usa ningún cifrado. Si está instalada la versión 1.1 o posterior, los servicios web XML son seguros de forma predeterminada; los llamadores deben autenticarse y se requiere cifrado.

Un servicio web XML protegido no admite el acceso WKO a través de WSDL. En su lugar, los clientes que han instalado el .NET Framework versión 1.1 pueden llamarlo en el modo DHCP. Si los clientes de terceros necesitan acceder al servicio web XML a través de WSDL, debe permitir el acceso anónimo.

Un componente COM expuesto como un servicio web XML se ejecuta de forma predeterminada con los permisos del usuario anónimo (no con los permisos de su autor de la llamada). Puede configurar IIS para ejecutar el servicio web XML como un usuario diferente; Esto puede ser necesario a veces porque el componente usa archivos u otros recursos a los que el usuario anónimo no tiene acceso. No obstante, siempre debe intentar ejecutar el componente con el menor número de privilegios posible para limitar los daños que podría causar un autor de llamada malintencionado.

> [!Note]  
> Dado que un método expuesto a través de un servicio web XML podría exponerse a llamadores malintencionados, siempre debe asegurarse de validar los parámetros de entrada de los que depende.

 

Para obtener instrucciones detalladas sobre cómo configurar opciones de seguridad de servicios web XML específicas, vea [Securing XML Web Services](securing-xml-web-services.md).

**Para convertir una aplicación SOAP segura en una aplicación SOAP no segura**

1.  Abra la herramienta Internet Information Services administración de iis (iis).
2.  Busque el directorio virtual de la aplicación y abra el **cuadro de diálogo** Propiedades .
3.  Active **la página Habilitar contenido predeterminado** en la **pestaña** Documentos.
4.  En la pestaña **Seguridad del directorio,** haga clic **en Editar** en Control **de autenticación y acceso anónimo.**
5.  Active **Acceso anónimo para** habilitar el acceso anónimo y haga clic en **Aceptar.**
6.  Haga clic **en Editar** en **Comunicaciones seguras.**
7.  Desactive la **casilla Requerir canal seguro (SSL).**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre el servicio SOAP de COM+](com--soap-service-overview.md)
</dt> </dl>

 

 




---
description: Un motor de datos adjuntos es un archivo DLL que controla las solicitudes de configuración y análisis específicas del servicio.
ms.assetid: bbca486a-9eec-4510-b5fd-435972182a69
title: Motores de datos adjuntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af0711caa5ceada7c16ae11b6470568a76d16ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911581"
---
# <a name="attachment-engines"></a>Motores de datos adjuntos

Un motor de datos adjuntos es un archivo DLL que controla las solicitudes de configuración y análisis específicas del servicio.

El usuario realiza una solicitud de análisis y configuración específica del servicio mediante la extensión del complemento de datos adjuntos. Esta solicitud se pasa a través de los complementos de configuración de seguridad al motor de configuración de seguridad general, que a su vez pasa el procesamiento específico del servicio al motor de datos adjuntos adecuado. A continuación, el motor de datos adjuntos se conecta al servicio y cambia su configuración. En otras palabras, el motor de datos adjuntos proporciona el procesamiento de back-end que admite la extensión del complemento de datos adjuntos.

Un motor de datos adjuntos debe implementar las tres funciones siguientes:

-   [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), que calcula la diferencia entre la configuración del servicio y la configuración almacenada en la base de datos de seguridad. Las diferencias se escriben en la base de datos de seguridad.
-   [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), que configura el servicio como se especifica en la interfaz de usuario del complemento.
-   [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), que actualiza la configuración base y el análisis de configuración para el servicio en la base de datos de seguridad.

Para simplificar la implementación de las funciones anteriores, el conjunto de herramientas de configuración de seguridad proporciona funciones y estructuras de compatibilidad que su aplicación puede usar para consultar y establecer información en la base de datos de seguridad. Para obtener más información, vea [funciones de devolución de llamada de datos adjuntos](management-functions.md).

Al crear una DLL del motor de datos adjuntos, debe instalarla y registrarla en el motor de configuración de seguridad. Para registrar el archivo DLL, agregue una clave específica al registro. Cuando se inicia el motor de configuración de seguridad, comprueba el registro y carga todos los archivos dll registrados del motor de datos adjuntos. Después, pasa las solicitudes de configuración y análisis específicas del servicio al motor de datos adjuntos adecuado. El motor de configuración de seguridad controla las solicitudes de configuración y análisis estándar, las que no son específicas del servicio.

 

 




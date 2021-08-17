---
description: Un motor de datos adjuntos es un archivo DLL que controla las solicitudes de análisis y configuración específicas del servicio.
ms.assetid: bbca486a-9eec-4510-b5fd-435972182a69
title: Motores de datos adjuntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62e09996bfb58e0447ec8e25bb627af6a4c93751a86f9f73f3499cf7f8b0fdb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895058"
---
# <a name="attachment-engines"></a>Motores de datos adjuntos

Un motor de datos adjuntos es un archivo DLL que controla las solicitudes de análisis y configuración específicas del servicio.

El usuario realiza una solicitud de configuración y análisis específica del servicio mediante la extensión de complemento de datos adjuntos. A continuación, esta solicitud se pasa a través de los complementos de configuración de seguridad al motor de configuración de seguridad general, que a su vez pasa el procesamiento específico del servicio al motor de datos adjuntos adecuado. A continuación, el motor de datos adjuntos se conecta al servicio y cambia su configuración. En otras palabras, el motor de datos adjuntos proporciona el procesamiento de back-end que admite la extensión de complemento de datos adjuntos.

Un motor de datos adjuntos debe implementar las tres funciones siguientes:

-   [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), que calcula la diferencia entre la configuración del servicio y la configuración almacenada en la base de datos de seguridad. Las diferencias se escriben en la base de datos de seguridad.
-   [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), que configura el servicio como se especifica en la interfaz de usuario del complemento.
-   [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), que actualiza la configuración base y el análisis de configuración del servicio en la base de datos de seguridad.

Para simplificar la implementación de las funciones anteriores, el conjunto de herramientas configuración de seguridad proporciona funciones de compatibilidad y estructuras que la aplicación puede usar para consultar y establecer información en la base de datos de seguridad. Para obtener más información, vea [Funciones de devolución de llamada de datos adjuntos](management-functions.md).

Al crear un archivo DLL del motor de datos adjuntos, debe instalarlo y registrarlo con el motor de configuración de seguridad. Para registrar el archivo DLL, agregue una clave específica al registro. Cuando se inicia el motor de configuración de seguridad, comprueba el registro y carga todos los archivos DLL del motor de datos adjuntos registrados. A continuación, pasa solicitudes de análisis y configuración específicas del servicio al motor de datos adjuntos adecuado. Las solicitudes de configuración y análisis estándar, las que no son específicas del servicio, se controlan mediante el motor de configuración de seguridad.

 

 




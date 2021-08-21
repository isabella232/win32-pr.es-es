---
description: Un motor de datos adjuntos es un archivo DLL que procesa solicitudes de análisis y configuración específicas del servicio. En otras palabras, controla el procesamiento que no puede controlar el conjunto de herramientas de configuración de seguridad estándar.
ms.assetid: c04779f4-f1e9-40b0-9f00-0176afb1b839
title: Crear un motor de datos adjuntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4705de9babaa7316d339cccadb6e7b39f44dd6f68957659b069759550e2b537
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969528"
---
# <a name="creating-an-attachment-engine"></a>Crear un motor de datos adjuntos

Un motor de datos adjuntos es un archivo DLL que procesa solicitudes de análisis y configuración específicas del servicio. En otras palabras, controla el procesamiento que no puede controlar el conjunto de herramientas de configuración de seguridad estándar.

Para crear un motor de datos adjuntos, debe implementar las tres funciones siguientes:

-   [**SceSvcAttachmentAnalyze ,**](scesvcattachmentanalyze.md)que calcula la diferencia entre la configuración del servicio y la configuración almacenada en la base de datos de seguridad. Estas diferencias se escriben en la base de datos de seguridad. Para obtener más información, [vea Implementing SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).
-   [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), que configura el servicio como se especifica en la interfaz de usuario del complemento. Para obtener más información, [vea Implementing SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md).
-   [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), que actualiza la configuración base y el análisis de configuración del servicio en la base de datos de seguridad. Para obtener más información, [vea Implementing SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md).

El conjunto de herramientas configuración de seguridad implementa un conjunto de funciones de soporte técnico a las que la aplicación puede llamar para consultar y establecer información en la base de datos de seguridad. Para obtener más información, vea [Funciones de devolución de llamada de datos adjuntos](management-functions.md).

Después de crear un archivo DLL del motor de datos adjuntos, debe registrarlo con el conjunto de herramientas configuración de seguridad. Este proceso se describe en [Registro de un motor de datos adjuntos.](registering-an-attachment-engine.md)

Además de crear un motor de datos adjuntos, también debe crear una extensión de complemento de datos adjuntos. La extensión de complemento proporciona una interfaz de usuario para tareas específicas del servicio. Cuando el usuario especifica una nueva configuración mediante una extensión de complemento, la solicitud se pasa al motor de datos adjuntos adecuado. A continuación, el motor se conecta al servicio y cambia su configuración. Si no implementa una extensión de complemento, los usuarios no tendrán ninguna manera de cambiar la configuración o el análisis del servicio. Para obtener más información sobre cómo crear una extensión de complemento de datos adjuntos, vea [Crear una extensión de complemento de datos adjuntos](creating-an-attachment-snap-in-extension.md).

 

 




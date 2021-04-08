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
# <a name="attachment-engines"></a><span data-ttu-id="2b218-103">Motores de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="2b218-103">Attachment Engines</span></span>

<span data-ttu-id="2b218-104">Un motor de datos adjuntos es un archivo DLL que controla las solicitudes de configuración y análisis específicas del servicio.</span><span class="sxs-lookup"><span data-stu-id="2b218-104">An attachment engine is a DLL that handles service-specific configuration and analysis requests.</span></span>

<span data-ttu-id="2b218-105">El usuario realiza una solicitud de análisis y configuración específica del servicio mediante la extensión del complemento de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="2b218-105">The user makes a service-specific configuration and analysis request using the attachment snap-in extension.</span></span> <span data-ttu-id="2b218-106">Esta solicitud se pasa a través de los complementos de configuración de seguridad al motor de configuración de seguridad general, que a su vez pasa el procesamiento específico del servicio al motor de datos adjuntos adecuado.</span><span class="sxs-lookup"><span data-stu-id="2b218-106">This request is then passed through the Security Configuration snap-ins to the general Security Configuration Engine, which in turn passes the service-specific processing to the appropriate attachment engine.</span></span> <span data-ttu-id="2b218-107">A continuación, el motor de datos adjuntos se conecta al servicio y cambia su configuración.</span><span class="sxs-lookup"><span data-stu-id="2b218-107">The attachment engine then connects to the service and changes its configuration.</span></span> <span data-ttu-id="2b218-108">En otras palabras, el motor de datos adjuntos proporciona el procesamiento de back-end que admite la extensión del complemento de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="2b218-108">In other words, the attachment engine provides the back-end processing that supports the attachment snap-in extension.</span></span>

<span data-ttu-id="2b218-109">Un motor de datos adjuntos debe implementar las tres funciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="2b218-109">An attachment engine must implement the following three functions:</span></span>

-   <span data-ttu-id="2b218-110">[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), que calcula la diferencia entre la configuración del servicio y la configuración almacenada en la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2b218-110">[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), which computes the difference between the service's configuration and the configuration stored in the security database.</span></span> <span data-ttu-id="2b218-111">Las diferencias se escriben en la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2b218-111">The differences are written to the security database.</span></span>
-   <span data-ttu-id="2b218-112">[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), que configura el servicio como se especifica en la interfaz de usuario del complemento.</span><span class="sxs-lookup"><span data-stu-id="2b218-112">[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), which configures the service as specified in the snap-in user interface.</span></span>
-   <span data-ttu-id="2b218-113">[**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), que actualiza la configuración base y el análisis de configuración para el servicio en la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2b218-113">[**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), which updates the base configuration and configuration analysis for the service in the security database.</span></span>

<span data-ttu-id="2b218-114">Para simplificar la implementación de las funciones anteriores, el conjunto de herramientas de configuración de seguridad proporciona funciones y estructuras de compatibilidad que su aplicación puede usar para consultar y establecer información en la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2b218-114">To simplify implementation of the preceding functions, the Security Configuration tool set provides support functions and structures that your application can use to query and set information in the security database.</span></span> <span data-ttu-id="2b218-115">Para obtener más información, vea [funciones de devolución de llamada de datos adjuntos](management-functions.md).</span><span class="sxs-lookup"><span data-stu-id="2b218-115">For more information, see [Attachment Callback Functions](management-functions.md).</span></span>

<span data-ttu-id="2b218-116">Al crear una DLL del motor de datos adjuntos, debe instalarla y registrarla en el motor de configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2b218-116">When you create an attachment engine DLL, you must install it and then register it with the Security Configuration Engine.</span></span> <span data-ttu-id="2b218-117">Para registrar el archivo DLL, agregue una clave específica al registro.</span><span class="sxs-lookup"><span data-stu-id="2b218-117">To register the DLL, you add a specific key to the registry.</span></span> <span data-ttu-id="2b218-118">Cuando se inicia el motor de configuración de seguridad, comprueba el registro y carga todos los archivos dll registrados del motor de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="2b218-118">When the Security Configuration Engine starts, it checks the registry and loads all registered attachment engine DLLs.</span></span> <span data-ttu-id="2b218-119">Después, pasa las solicitudes de configuración y análisis específicas del servicio al motor de datos adjuntos adecuado.</span><span class="sxs-lookup"><span data-stu-id="2b218-119">It then passes service-specific configuration and analysis requests to the appropriate attachment engine.</span></span> <span data-ttu-id="2b218-120">El motor de configuración de seguridad controla las solicitudes de configuración y análisis estándar, las que no son específicas del servicio.</span><span class="sxs-lookup"><span data-stu-id="2b218-120">Standard configuration and analysis requests, those that are not service-specific, are handled by the Security Configuration Engine.</span></span>

 

 




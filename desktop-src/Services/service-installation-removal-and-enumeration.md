---
description: Un programa de configuración utiliza la función CreateService para instalar un nuevo servicio en la base de datos SCM.
ms.assetid: 554b9983-4e49-4b11-b420-a4754123d854
title: Instalación, eliminación y enumeración del servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1069bba094205efd3257063a89c74326b2806455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809445"
---
# <a name="service-installation-removal-and-enumeration"></a><span data-ttu-id="a039c-103">Instalación, eliminación y enumeración del servicio</span><span class="sxs-lookup"><span data-stu-id="a039c-103">Service Installation, Removal, and Enumeration</span></span>

<span data-ttu-id="a039c-104">Un programa de configuración utiliza la función [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) para instalar un nuevo servicio en la base de datos SCM.</span><span class="sxs-lookup"><span data-stu-id="a039c-104">A configuration program uses the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to install a new service in the SCM database.</span></span> <span data-ttu-id="a039c-105">Esta función especifica el nombre del servicio y proporciona información de configuración que se almacena en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="a039c-105">This function specifies the name of the service and provides configuration information that is stored in the database.</span></span> <span data-ttu-id="a039c-106">Para obtener una descripción de la información almacenada en la base de datos para cada servicio, vea [base de datos de servicios instalados](database-of-installed-services.md).</span><span class="sxs-lookup"><span data-stu-id="a039c-106">For a description of the information stored in the database for each service, see [Database of Installed Services](database-of-installed-services.md).</span></span> <span data-ttu-id="a039c-107">Para ver el código de ejemplo, consulte [instalación de un servicio](installing-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="a039c-107">For sample code, see [Installing a Service](installing-a-service.md).</span></span>

<span data-ttu-id="a039c-108">Un programa de configuración utiliza la función [**actividades**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) para quitar un servicio instalado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="a039c-108">A configuration program uses the [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) function to remove an installed service from the database.</span></span> <span data-ttu-id="a039c-109">Para obtener más información, consulte [eliminación de un servicio](deleting-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="a039c-109">For more information, see [Deleting a Service](deleting-a-service.md).</span></span>

<span data-ttu-id="a039c-110">Para obtener el nombre del servicio, llame a la función [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) .</span><span class="sxs-lookup"><span data-stu-id="a039c-110">To obtain the service name, call the [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) function.</span></span> <span data-ttu-id="a039c-111">El nombre para mostrar del servicio, que se usa en el applet servicios del panel de control, se puede obtener llamando a la función [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea) .</span><span class="sxs-lookup"><span data-stu-id="a039c-111">The service display name, used in the Services control panel applet, can be obtained by calling the [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea) function.</span></span>

<span data-ttu-id="a039c-112">Un programa de configuración de servicio puede utilizar la función [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) para enumerar todos los servicios y sus Estados.</span><span class="sxs-lookup"><span data-stu-id="a039c-112">A service configuration program can use the [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) function to enumerate all services and their statuses.</span></span> <span data-ttu-id="a039c-113">También puede utilizar la función [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) para enumerar los servicios que dependen de un objeto de servicio especificado.</span><span class="sxs-lookup"><span data-stu-id="a039c-113">It can also use the [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) function to enumerate which services are dependent on a specified service object.</span></span>

 

 




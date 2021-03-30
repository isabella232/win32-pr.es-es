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
# <a name="service-installation-removal-and-enumeration"></a>Instalación, eliminación y enumeración del servicio

Un programa de configuración utiliza la función [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) para instalar un nuevo servicio en la base de datos SCM. Esta función especifica el nombre del servicio y proporciona información de configuración que se almacena en la base de datos. Para obtener una descripción de la información almacenada en la base de datos para cada servicio, vea [base de datos de servicios instalados](database-of-installed-services.md). Para ver el código de ejemplo, consulte [instalación de un servicio](installing-a-service.md).

Un programa de configuración utiliza la función [**actividades**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) para quitar un servicio instalado de la base de datos. Para obtener más información, consulte [eliminación de un servicio](deleting-a-service.md).

Para obtener el nombre del servicio, llame a la función [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) . El nombre para mostrar del servicio, que se usa en el applet servicios del panel de control, se puede obtener llamando a la función [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea) .

Un programa de configuración de servicio puede utilizar la función [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) para enumerar todos los servicios y sus Estados. También puede utilizar la función [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) para enumerar los servicios que dependen de un objeto de servicio especificado.

 

 




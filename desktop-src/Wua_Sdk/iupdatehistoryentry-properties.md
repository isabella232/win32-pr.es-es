---
description: La interfaz IUpdateHistoryEntry define las siguientes propiedades.
ms.assetid: ea4e698c-4a4c-4266-96e0-870dc5709a72
title: Propiedades de IUpdateHistoryEntry
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5c6951857f72f4a9ee4f86cd29d42e024e05b87d58d589043f5a40e951d4c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738274"
---
# <a name="iupdatehistoryentry-properties"></a>Propiedades de IUpdateHistoryEntry

La [**interfaz IUpdateHistoryEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry) define las siguientes propiedades.



| Propiedad                                                               | Descripción                                                                                                              |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_clientapplicationid) | Obtiene el identificador de la aplicación cliente que procesó una actualización.                                                  |
| [**Fecha**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_date)                               | Obtiene la fecha y la hora en que se aplicó una actualización.                                                                        |
| [**Descripción**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_description)                 | Obtiene la descripción de una actualización.                                                                                       |
| [**Hresult**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_hresult)                         | Obtiene el **valor HRESULT** que se devuelve de la operación en una actualización.                                             |
| [**Operación**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_operation)                     | Obtiene un [**valor UpdateOperation**](/windows/win32/api/wuapi/ne-wuapi-updateoperation) que especifica la operación en una actualización.                      |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_resultcode)                   | Obtiene un [**valor OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) que especifica el resultado de una operación en una actualización. |
| [**ServerSelection**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_serverselection)         | Obtiene el [**valor ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) que indica qué servidor proporcionó una actualización.                |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_serviceid)                     | Obtiene el identificador de servicio de un servicio de actualización que no es una Windows actualización.                                           |
| [**SupportUrl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_supporturl)                   | Obtiene un hipervínculo a la información de soporte técnico específica del lenguaje para una actualización.                                             |
| [**Título**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_title)                             | Obtiene el título de una actualización.                                                                                             |
| [**UninstallationNotes**](/windows/win32/api/wuapi/nf-wuapi-iupdatehistoryentry-get_uninstallationnotes) | Obtiene las notas de desinstalación de una actualización.                                                                              |
| [**UninstallationSteps**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_uninstallationsteps) | Obtiene la [**interfaz IStringCollection**](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection) que contiene los pasos de desinstalación de una actualización.  |
| [**UnmappedResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_unmappedresultcode)   | Obtiene el código de resultado no administrado que se devuelve de una operación en una actualización.                                           |
| [**UpdateIdentity**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_updateidentity)           | Obtiene una cadena. La cadena contiene el identificador único de una actualización.                                                   |



 

 

 

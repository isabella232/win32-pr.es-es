---
description: Enumera los tipos de datos utilizados por los archivos DLL de datos adjuntos de configuración de seguridad y sus funciones de apoyo.
ms.assetid: 1d3bdf0d-320c-4b25-9e9b-fda134876979
title: Tipos de datos de administración de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23c22ef996f54a9664dfa128a90fdb0c2825d60b68b7deafe7534d2b3b05737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969022"
---
# <a name="security-management-data-types"></a>Tipos de datos de administración de seguridad

Los tipos de datos de administración de seguridad incluyen los siguientes:

-   [Tipos de datos adjuntos](#attachment-data-types)
-   [Tipos de datos de directiva LSA](#lsa-policy-data-types)

## <a name="attachment-data-types"></a>Tipos de datos adjuntos

Los siguientes tipos de datos los usan los archivos DLL de datos adjuntos de configuración de seguridad y sus funciones de soporte.



| Tipo de datos                                                    | Descripción                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CONTEXTO DE \_ ENUMERACIÓN SCE \_**](sce-enumeration-context.md) | Usado por la función [**PFSCE \_ QUERY \_ INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) para navegar por la base de datos de seguridad.                                                                                                                                              |
| [**Identificador \_ de SCE**](sce-handle.md)                            | Se usa en [**PFSCE \_ QUERY \_ INFO y**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) [**PFSCE \_ SET \_ INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) para pasar información entre los datos adjuntos y la base de datos de seguridad.                                                                                 |
| [**SCESTATUS**](scestatus.md)                               | La API del conjunto de herramientas de configuración de seguridad usa el tipo de datos para devolver información sobre los resultados de una llamada de función.                                                                                                                                    |
| [**IDENTIFICADOR \_ SCESVC**](scesvc-handle.md)                      | Usado por los métodos de las interfaces [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) e [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) para pasar información entre el complemento Configuración de seguridad y la extensión del complemento. |
| [**TIPO DE INFORMACIÓN \_ DE SCESVC \_**](/windows/desktop/api/Scesvc/ne-scesvc-scesvc_info_type)               | PfSCE [**\_ QUERY \_ INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) y [**PFSCE \_ SET \_ INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) usan la enumeración para indicar el tipo de información solicitada o pasada a la base de datos de seguridad.                                                 |



 

## <a name="lsa-policy-data-types"></a>Tipos de datos de directiva LSA

Las funciones de administración de directivas LSA usan los siguientes tipos de datos.



| Tipo de datos                                                  | Descripción                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------|
| [**IDENTIFICADOR DE ENUMERACIÓN LSA \_ \_**](lsa-enumeration-handle.md) | Se usa para realizar un seguimiento de las enumeraciones en las que se requieren varias llamadas de función. |
| [**CONTROLADOR \_ LSA**](lsa-handle.md)                          | Identificador de un [**objeto Policy.**](policy-object.md)                       |



 

 

 

---
description: Enumera los tipos de datos utilizados por los archivos dll de datos adjuntos de configuración de seguridad y sus funciones auxiliares.
ms.assetid: 1d3bdf0d-320c-4b25-9e9b-fda134876979
title: Tipos de datos de administración de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae7efedb32ab545b903c61819042e32b7d83dbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667526"
---
# <a name="security-management-data-types"></a>Tipos de datos de administración de seguridad

Entre los tipos de datos de administración de seguridad se incluyen los siguientes:

-   [Tipos de datos adjuntos](#attachment-data-types)
-   [Tipos de datos de directiva de LSA](#lsa-policy-data-types)

## <a name="attachment-data-types"></a>Tipos de datos adjuntos

Los archivos dll de datos adjuntos de configuración de seguridad usan los siguientes tipos de datos y sus funciones auxiliares.



| Tipo de datos                                                    | Descripción                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_contexto de enumeración de SCE \_**](sce-enumeration-context.md) | Lo utiliza la función de [**\_ \_ información de consulta PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) para navegar por la base de datos de seguridad.                                                                                                                                              |
| [**identificador de SCE \_**](sce-handle.md)                            | Usado por [**PFSCE \_ query \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) y [**PFSCE \_ set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) para pasar información entre los datos adjuntos y la base de datos de seguridad.                                                                                 |
| [**SCESTATUS**](scestatus.md)                               | El tipo de datos lo usa la API del conjunto de herramientas de configuración de seguridad para devolver información sobre los resultados de una llamada de función.                                                                                                                                    |
| [**identificador de SCESVC \_**](scesvc-handle.md)                      | Lo usan los métodos de las interfaces [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) y [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) para pasar información entre el complemento configuración de seguridad y la extensión del complemento. |
| [**\_tipo de información de SCESVC \_**](/windows/desktop/api/Scesvc/ne-scesvc-scesvc_info_type)               | La información de [**consulta de \_ PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) y la información de conjunto de PFSCE utilizan la enumeración para indicar el tipo de información que se solicita o se pasa a la base de datos de seguridad. [**\_ \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)                                                 |



 

## <a name="lsa-policy-data-types"></a>Tipos de datos de directiva de LSA

Las funciones de administración de directivas de LSA usan los siguientes tipos de datos.



| Tipo de datos                                                  | Descripción                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------|
| [**\_identificador de enumeración de LSA \_**](lsa-enumeration-handle.md) | Se utiliza para realizar el seguimiento de las enumeraciones en las que se requieren varias llamadas a funciones. |
| [**identificador de LSA \_**](lsa-handle.md)                          | Identificador de un objeto de [**Directiva**](policy-object.md) .                       |



 

 

 

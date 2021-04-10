---
description: KTM define las siguientes máscaras de acceso de inscripción que se usarán al abrir un administrador de recursos.
ms.assetid: 6b901b73-516d-4f27-b258-3b93a8f9675f
title: Administrador de recursos máscaras de acceso (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0f579a96ed80de100a5cb41cb9c4e9b847a060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156364"
---
# <a name="resource-manager-access-masks"></a>Máscaras de acceso Administrador de recursos

KTM define las siguientes máscaras de acceso de inscripción que se usarán al abrir un administrador de recursos.

<dl> <dt>

<span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**\_información de consulta de RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



El autor de la llamada puede consultar la información de Resource Manager (RM).


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**\_información del conjunto de RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



El autor de la llamada puede establecer la información de RM.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**recuperación de RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



El autor de la llamada puede recuperar el RM especificado.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**\_dar de alta RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



El autor de la llamada puede dar de alta un RM en una transacción.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**\_notificación get de RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



El autor de la llamada puede recibir una notificación de un RM.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**\_lectura genérica de RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



El autor de la llamada tiene los siguientes privilegios: \_ derechos estándar \_ leídos, información de consulta de ResourceManager \_ \_ y recuperación de ResourceManager \_ .


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**\_escritura genérica de RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



El autor de la llamada tiene los siguientes privilegios: estándar de \_ \_ escritura de derechos, información de conjunto de ResourceManager, error de inscripción de ResourceManager \_ \_ \_ y notificación de obtención de ResourceManager \_ \_ .


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**\_ejecución genérica de RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



El autor de la llamada tiene los siguientes privilegios: estándar \_ \_ Execute, ResourceManager \_ dar de alta y ResourceManager \_ Get \_ Notification.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**\_ \_ acceso a RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



El autor de la llamada tiene el siguiente privilegio: \_ derechos estándar \_ requeridos.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



 

 





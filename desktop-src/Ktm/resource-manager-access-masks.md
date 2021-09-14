---
description: KTM define las siguientes máscaras de acceso de registro que se usarán al abrir un administrador de recursos.
ms.assetid: 6b901b73-516d-4f27-b258-3b93a8f9675f
title: Resource Manager máscaras de acceso (WinNT.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0f579a96ed80de100a5cb41cb9c4e9b847a060
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160023"
---
# <a name="resource-manager-access-masks"></a>Resource Manager máscaras de acceso

KTM define las siguientes máscaras de acceso de registro que se usarán al abrir un administrador de recursos.

<dl> <dt>

<span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**INFORMACIÓN DE \_ CONSULTA DE \_ RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



El autor de la llamada puede consultar la información del Administrador de recursos (RM).


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**INFORMACIÓN DEL \_ CONJUNTO DE \_ RESOURCEMANAGER**
</dt> <dd> <dl> <dt>



El autor de la llamada puede establecer la información de RM.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**RECUPERACIÓN DE RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>



El autor de la llamada puede recuperar el RM especificado.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**RESOURCEMANAGER \_ ENLIST**
</dt> <dd> <dl> <dt>



El autor de la llamada puede hacer una lista de un rm en una transacción.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**NOTIFICACIÓN GET DE RESOURCEMANAGER \_ \_**
</dt> <dd> <dl> <dt>



El autor de la llamada puede recibir una notificación para un rm.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**LECTURA GENÉRICA DE RESOURCEMANAGER \_ \_**
</dt> <dd> <dl> <dt>



El autor de la llamada tiene los siguientes privilegios: STANDARD \_ RIGHTS \_ READ, RESOURCEMANAGER \_ QUERY INFORMATION y \_ RESOURCEMANAGER \_ RECOVER.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**ESCRITURA GENÉRICA DE RESOURCEMANAGER \_ \_**
</dt> <dd> <dl> <dt>



El autor de la llamada tiene los siguientes privilegios: STANDARD \_ RIGHTS \_ WRITE, RESOURCEMANAGER \_ SET \_ INFORMATION, RESOURCEMANAGER ENLIST y \_ RESOURCEMANAGER GET \_ \_ NOTIFICATION.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**RESOURCEMANAGER \_ GENERIC \_ EXECUTE**
</dt> <dd> <dl> <dt>



El autor de la llamada tiene los siguientes privilegios: STANDARD \_ RIGHTS \_ EXECUTE, RESOURCEMANAGER \_ ENLIST y RESOURCEMANAGER \_ GET \_ NOTIFICATION.


</dt> </dl> </dd> <dt>

<span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**ACCESO A RESOURCEMANAGER \_ \_ ALL**
</dt> <dd> <dl> <dt>



El autor de la llamada tiene el siguiente privilegio: STANDARD \_ RIGHTS \_ REQUIRED.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>WinNT.h</dt> </dl> |



 

 





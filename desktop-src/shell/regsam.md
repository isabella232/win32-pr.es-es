---
description: Tipo de datos utilizado para especificar los atributos de acceso de seguridad en el Registro.
title: REGSAM (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 003f6be9-e4ba-4d23-b486-a167063c630e
api_name:
- KEY_ALL_ACCESS
- KEY_CREATE_LINK
- KEY_CREATE_SUB_KEY
- KEY_ENUMERATE_SUB_KEYS
- KEY_EXECUTE
- KEY_NOTIFY
- KEY_QUERY_VALUE
- KEY_READ
- KEY_SET_VALUE
- KEY_WRITE
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2700e278f86db046d532b91b64bf5a2d00582e14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267836"
---
# <a name="regsam"></a>REGSAM

Tipo de datos utilizado para especificar los atributos de acceso de seguridad en el Registro.



| Constante                                                                                                                                                                                   | Descripción                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KEY_ALL_ACCESS"></span><span id="key_all_access"></span><dl> <dt>**KEY \_ ALL \_ ACCESS**</dt> </dl>                          | Combinación de acceso de **KEY \_ QUERY \_ VALUE*,**KEY \_ ENUMERATE \_ SUB \_ KEYS*,***KEY \_ NOTIFY*,**KEY \_ CREATE SUB \_ \_ KEY**,**KEY \_ CREATE \_ LINK*%, y *).KEY \_ SET \_ VALUE*!.<br/> |
| <span id="KEY_CREATE_LINK"></span><span id="key_create_link"></span><dl> <dt>**VÍNCULO \_ DE CREACIÓN DE \_ CLAVE**</dt> </dl>                       | Permiso para crear un vínculo simbólico.<br/>                                                                                                                                                           |
| <span id="KEY_CREATE_SUB_KEY"></span><span id="key_create_sub_key"></span><dl> <dt>**KEY \_ CREATE \_ SUB \_ KEY**</dt> </dl>             | Permiso para crear subclaves.<br/>                                                                                                                                                                   |
| <span id="KEY_ENUMERATE_SUB_KEYS"></span><span id="key_enumerate_sub_keys"></span><dl> <dt>**\_SUBCLAVE ENUMERACIÓN \_ DE \_ CLAVES**</dt> </dl> | Permiso para enumerar subclaves.<br/>                                                                                                                                                                |
| <span id="KEY_EXECUTE"></span><span id="key_execute"></span><dl> <dt>**KEY \_ EXECUTE**</dt> </dl>                                    | Permiso para el acceso de lectura.<br/>                                                                                                                                                                     |
| <span id="KEY_NOTIFY"></span><span id="key_notify"></span><dl> <dt>**NOTIFICACIÓN \_ DE CLAVE**</dt> </dl>                                       | Permiso para la notificación de cambios.<br/>                                                                                                                                                             |
| <span id="KEY_QUERY_VALUE"></span><span id="key_query_value"></span><dl> <dt>**VALOR DE \_ CONSULTA \_ DE CLAVE**</dt> </dl>                       | Permiso para consultar datos de subclave.<br/>                                                                                                                                                                |
| <span id="KEY_READ"></span><span id="key_read"></span><dl> <dt>**KEY \_ READ**</dt> </dl>                                             | Combinación de los accesos **KEY \_ QUERY \_ VALUE*,**KEY \_ ENUMERATE \_ SUB \_ KEYS*%, y **KEY \_ NOTIFY*!.<br/>                                                                                    |
| <span id="KEY_SET_VALUE"></span><span id="key_set_value"></span><dl> <dt>**VALOR \_ DEL CONJUNTO DE \_ CLAVES**</dt> </dl>                             | Permiso para establecer datos de subclave.<br/>                                                                                                                                                                  |
| <span id="KEY_WRITE"></span><span id="key_write"></span><dl> <dt>**ESCRITURA \_ DE CLAVE**</dt> </dl>                                          | Combinación del acceso *:KEY \_ SET \_ VALUE*" y ***KEY \_ CREATE SUB \_ \_ KEY*".<br/>                                                                                                                |



## <a name="remarks"></a>Observaciones

Un **valor REGSAM** puede ser uno o varios de los valores enumerados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winnt.h</dt> </dl> |



 

 





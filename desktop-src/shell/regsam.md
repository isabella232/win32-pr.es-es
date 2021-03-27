---
description: Un tipo de datos que se usa para especificar los atributos de acceso de seguridad en el registro.
title: REGSAM (Winnt. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987606"
---
# <a name="regsam"></a>REGSAM

Un tipo de datos que se usa para especificar los atributos de acceso de seguridad en el registro.



| Constante                                                                                                                                                                                   | Descripción                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KEY_ALL_ACCESS"></span><span id="key_all_access"></span><dl> <dt>**acceso de clave \_ \_ a todo**</dt> </dl>                          | Combinación de * * * * valor de consulta de clave * * * *, * * * * subclaves de \_ \_ \_ enumeración de clave \_ * * * * \_ , * * * * notificación de clave \_ * * * *, * * * * clave de \_ creación \_ \_ \_ \_ \_ \_ de clave * * * * * * * * * * * * *<br/> |
| <span id="KEY_CREATE_LINK"></span><span id="key_create_link"></span><dl> <dt>**\_vínculo de creación de clave \_**</dt> </dl>                       | Permiso para crear un vínculo simbólico.<br/>                                                                                                                                                           |
| <span id="KEY_CREATE_SUB_KEY"></span><span id="key_create_sub_key"></span><dl> <dt>**subclave de creación de clave \_ \_ \_**</dt> </dl>             | Permiso para crear subclaves.<br/>                                                                                                                                                                   |
| <span id="KEY_ENUMERATE_SUB_KEYS"></span><span id="key_enumerate_sub_keys"></span><dl> <dt>**subclaves de \_ enumeración de clave \_ \_**</dt> </dl> | Permiso para enumerar las subclaves.<br/>                                                                                                                                                                |
| <span id="KEY_EXECUTE"></span><span id="key_execute"></span><dl> <dt>**ejecución de clave \_**</dt> </dl>                                    | Permiso de acceso de lectura.<br/>                                                                                                                                                                     |
| <span id="KEY_NOTIFY"></span><span id="key_notify"></span><dl> <dt>**notificación de clave \_**</dt> </dl>                                       | Permiso para la notificación de cambios.<br/>                                                                                                                                                             |
| <span id="KEY_QUERY_VALUE"></span><span id="key_query_value"></span><dl> <dt>**\_valor de consulta de clave \_**</dt> </dl>                       | Permiso para consultar los datos de subclaves.<br/>                                                                                                                                                                |
| <span id="KEY_READ"></span><span id="key_read"></span><dl> <dt>**lectura de clave \_**</dt> </dl>                                             | Combinación de * * * * valor de consulta de clave * * * *, * * * * subclaves de \_ \_ enumeración de claves * * * * y * * * * el \_ \_ \_ \_ acceso a la clave.<br/>                                                                                    |
| <span id="KEY_SET_VALUE"></span><span id="key_set_value"></span><dl> <dt>**\_valor del conjunto de claves \_**</dt> </dl>                             | Permiso para establecer los datos de la subclave.<br/>                                                                                                                                                                  |
| <span id="KEY_WRITE"></span><span id="key_write"></span><dl> <dt>**escritura de claves \_**</dt> </dl>                                          | Combinación de * * * * valor del conjunto de claves * * * * * \_ \_ y * * * * acceso de clave de \_ creación de \_ clave \_<br/>                                                                                                                |



## <a name="remarks"></a>Observaciones

Un valor de **REGSAM** puede ser uno o varios de los valores enumerados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winnt. h</dt> </dl> |



 

 





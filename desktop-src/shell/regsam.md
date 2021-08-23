---
description: Tipo de datos que se usa para especificar los atributos de acceso de seguridad en el Registro.
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
ms.openlocfilehash: e202e615561ce0c51f44fc39726d8ab864afc2b5e1bcbbe5612edbb74c476c29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820425"
---
# <a name="regsam"></a>REGSAM

Tipo de datos que se usa para especificar los atributos de acceso de seguridad en el Registro.



| Constante                                                                                                                                                                                   | Descripción                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KEY_ALL_ACCESS"></span><span id="key_all_access"></span><dl> <dt>**ACCESO \_ A KEY \_ ALL**</dt> </dl>                          | Combinación de **KEY \_ QUERY \_ VALUE**,*KEY \_ ENUMERATE \_ SUB \_ KEYS*,*,*KEY \_ NOTIFY**,**KEY \_ CREATE SUB \_ \_ KEY**,**KEY \_ CREATE \_ LINK** y *).KEY \_ SET \_ VALUE** acceso.<br/> |
| <span id="KEY_CREATE_LINK"></span><span id="key_create_link"></span><dl> <dt>**VÍNCULO \_ DE CREACIÓN DE \_ CLAVE**</dt> </dl>                       | Permiso para crear un vínculo simbólico.<br/>                                                                                                                                                           |
| <span id="KEY_CREATE_SUB_KEY"></span><span id="key_create_sub_key"></span><dl> <dt>**KEY \_ CREATE \_ SUB \_ KEY**</dt> </dl>             | Permiso para crear subclaves.<br/>                                                                                                                                                                   |
| <span id="KEY_ENUMERATE_SUB_KEYS"></span><span id="key_enumerate_sub_keys"></span><dl> <dt>**CLAVES \_ ENUMERAR \_ \_ SUBCLAVE**</dt> </dl> | Permiso para enumerar subclaves.<br/>                                                                                                                                                                |
| <span id="KEY_EXECUTE"></span><span id="key_execute"></span><dl> <dt>**KEY \_ EXECUTE**</dt> </dl>                                    | Permiso para el acceso de lectura.<br/>                                                                                                                                                                     |
| <span id="KEY_NOTIFY"></span><span id="key_notify"></span><dl> <dt>**NOTIFICACIÓN \_ DE CLAVE**</dt> </dl>                                       | Permiso para la notificación de cambios.<br/>                                                                                                                                                             |
| <span id="KEY_QUERY_VALUE"></span><span id="key_query_value"></span><dl> <dt>**VALOR \_ DE CONSULTA DE \_ CLAVE**</dt> </dl>                       | Permiso para consultar datos de subclave.<br/>                                                                                                                                                                |
| <span id="KEY_READ"></span><span id="key_read"></span><dl> <dt>**KEY \_ READ**</dt> </dl>                                             | Combinación del acceso **KEY \_ QUERY \_ VALUE**,**KEY \_ ENUMERATE \_ SUB \_ KEYS*%, y *"KEY \_ NOTIFY*".<br/>                                                                                    |
| <span id="KEY_SET_VALUE"></span><span id="key_set_value"></span><dl> <dt>**VALOR \_ DE CONJUNTO DE \_ CLAVES**</dt> </dl>                             | Permiso para establecer datos de subclave.<br/>                                                                                                                                                                  |
| <span id="KEY_WRITE"></span><span id="key_write"></span><dl> <dt>**KEY \_ WRITE**</dt> </dl>                                          | Combinación del acceso de *"KEY \_ SET \_ VALUE*" y "*KEY \_ CREATE SUB \_ \_ KEY*".<br/>                                                                                                                |



## <a name="remarks"></a>Comentarios

Un **valor REGSAM** puede ser uno o varios de los valores enumerados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winnt.h</dt> </dl> |



 

 





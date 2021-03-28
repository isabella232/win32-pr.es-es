---
description: Estos tipos de datos se pueden utilizar para especificar el tipo de un valor del registro.
title: Tipos de datos del registro (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4185e7af-e1f0-40af-91c7-0ff7e27896ae
api_name:
- REG_BINARY
- REG_DWORD
- REG_QWORD
- REG_DWORD_LITTLE_ENDIAN
- REG_QWORD_LITTLE_ENDIAN
- REG_DWORD_BIG_ENDIAN
- REG_EXPAND_SZ
- REG_LINK
- REG_MULTI_SZ
- REG_NONE
- REG_RESOURCE_LIST
- REG_SZ
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4de4595b55716d58df04a598dd6ba298f22829d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104998983"
---
# <a name="registry-data-types"></a>Tipos de datos del registro

Estos tipos de datos se pueden utilizar para especificar el tipo de un valor del registro.



| Constante                                                                                                                                                                                      | Descripción                                                                                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_BINARY"></span><span id="reg_binary"></span><dl> <dt>**\_binario de reg**</dt> </dl>                                          | Datos binarios en cualquier formato.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="REG_DWORD"></span><span id="reg_dword"></span><dl> <dt>**\_valor DWORD reg**</dt> </dl>                                             | número de bits 32.<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_QWORD"></span><span id="reg_qword"></span><dl> <dt>**QWord de REG \_**</dt> </dl>                                             | número de bits 64.<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_DWORD_LITTLE_ENDIAN"></span><span id="reg_dword_little_endian"></span><dl> <dt>**REG \_ DWORD \_ Little \_ endian**</dt> </dl> | 32: número de bits en formato Little-Endian. Es equivalente a **reg \_ DWORD**.<br/> En el formato Little-endian, se almacena un valor multibyte en la memoria desde el byte más bajo (el "pequeño extremo") hasta el byte más alto. Por ejemplo, el valor 0x12345678 se almacena como (0x78 0x56 0x34 0X12) en formato Little-Endian.<br/> |
| <span id="REG_QWORD_LITTLE_ENDIAN"></span><span id="reg_qword_little_endian"></span><dl> <dt>**REG \_ QWord \_ Little \_ endian**</dt> </dl> | Número de 64 bits en formato Little-Endian. Esto es equivalente a **reg \_ QWord**. <br/>                                                                                                                                                                                                                                   |
| <span id="REG_DWORD_BIG_ENDIAN"></span><span id="reg_dword_big_endian"></span><dl> <dt>**REG \_ DWORD \_ Big \_ endian**</dt> </dl>          | 32: número de bits en formato Big-Endian.<br/> En el formato Big-endian, se almacena un valor multibyte en la memoria desde el byte más alto (el "Big end") hasta el byte más bajo. Por ejemplo, el valor 0x12345678 se almacena como (0X12 0x34 0x56 0x78) en formato Big-Endian.<br/>                                                   |
| <span id="REG_EXPAND_SZ"></span><span id="reg_expand_sz"></span><dl> <dt>**REG \_ expandir \_ SZ**</dt> </dl>                                | Cadena terminada en null que contiene referencias no expandidas a variables de entorno (por ejemplo, "% PATH%"). Será una cadena ANSI o Unicode, en función de si se utilizan las funciones Unicode o ANSI.<br/>                                                                                                     |
| <span id="REG_LINK"></span><span id="reg_link"></span><dl> <dt>**\_vínculo reg**</dt> </dl>                                                | Vínculo simbólico Unicode.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dl> <dt>**REG \_ multi \_ SZ**</dt> </dl>                                   | Matriz de cadenas terminadas en null que finalizan con dos caracteres null.<br/>                                                                                                                                                                                                                                      |
| <span id="REG_NONE"></span><span id="reg_none"></span><dl> <dt>**REG \_ ninguno**</dt> </dl>                                                | No hay ningún tipo de valor definido.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_RESOURCE_LIST"></span><span id="reg_resource_list"></span><dl> <dt>**\_lista de recursos del registro \_**</dt> </dl>                    | Lista de recursos de controlador de dispositivo.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="REG_SZ"></span><span id="reg_sz"></span><dl> <dt>**Registro \_ SZ**</dt> </dl>                                                      | Cadena terminada en un valor nulo. Será una cadena ANSI o Unicode, en función de si se utilizan las funciones Unicode o ANSI.<br/>                                                                                                                                                                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winnt. h</dt> </dl> |



 

 





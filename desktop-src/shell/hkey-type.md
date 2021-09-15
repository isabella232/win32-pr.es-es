---
description: Estos tipos de datos se pueden usar para especificar el tipo de un valor del Registro.
title: Tipos de datos del Registro (Winnt.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572525"
---
# <a name="registry-data-types"></a>Tipos de datos del Registro

Estos tipos de datos se pueden usar para especificar el tipo de un valor del Registro.



| Constante                                                                                                                                                                                      | Descripción                                                                                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_BINARY"></span><span id="reg_binary"></span><dl> <dt>**REG \_ BINARY**</dt> </dl>                                          | Datos binarios en cualquier formato.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="REG_DWORD"></span><span id="reg_dword"></span><dl> <dt>**REG \_ DWORD**</dt> </dl>                                             | Número de 32 bits.<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_QWORD"></span><span id="reg_qword"></span><dl> <dt>**REG \_ QWORD**</dt> </dl>                                             | Número de 64 bits.<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_DWORD_LITTLE_ENDIAN"></span><span id="reg_dword_little_endian"></span><dl> <dt>**REG \_ DWORD \_ LITTLE \_ ENDIAN**</dt> </dl> | Número de 32 bits en formato little-endian. Esto equivale a **REG \_ DWORD.**<br/> En formato little-endian, un valor multibyte se almacena en memoria desde el byte más bajo (el "pequeño extremo") hasta el byte más alto. Por ejemplo, el valor 0x12345678 se almacena como (0x78 0x56 0x34 0x12) en formato little-endian.<br/> |
| <span id="REG_QWORD_LITTLE_ENDIAN"></span><span id="reg_qword_little_endian"></span><dl> <dt>**REG \_ QWORD \_ LITTLE \_ ENDIAN**</dt> </dl> | Número de 64 bits en formato little-endian. Esto equivale a **REG \_ QWORD.** <br/>                                                                                                                                                                                                                                   |
| <span id="REG_DWORD_BIG_ENDIAN"></span><span id="reg_dword_big_endian"></span><dl> <dt>**REG \_ DWORD \_ BIG \_ ENDIAN**</dt> </dl>          | Número de 32 bits en formato big-endian.<br/> En formato big-endian, un valor multibyte se almacena en memoria desde el byte más alto (el "big end") hasta el byte más bajo. Por ejemplo, el valor 0x12345678 se almacena como (0x12 0x34 0x56 0x78) en formato big-endian.<br/>                                                   |
| <span id="REG_EXPAND_SZ"></span><span id="reg_expand_sz"></span><dl> <dt>**REG \_ EXPAND \_ SZ**</dt> </dl>                                | Cadena terminada en NULL que contiene referencias no exploradas a variables de entorno (por ejemplo, "%PATH%"). Será una cadena Unicode o ANSI, en función de si se usan las funciones Unicode o ANSI.<br/>                                                                                                     |
| <span id="REG_LINK"></span><span id="reg_link"></span><dl> <dt>**REG \_ LINK**</dt> </dl>                                                | Vínculo simbólico Unicode.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dl> <dt>**REG \_ MULTI \_ SZ**</dt> </dl>                                   | Matriz de cadenas terminadas en NULL terminadas por dos caracteres NULL.<br/>                                                                                                                                                                                                                                      |
| <span id="REG_NONE"></span><span id="reg_none"></span><dl> <dt>**REG \_ NONE**</dt> </dl>                                                | No hay ningún tipo de valor definido.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_RESOURCE_LIST"></span><span id="reg_resource_list"></span><dl> <dt>**REG \_ RESOURCE \_ LIST**</dt> </dl>                    | Lista de recursos del controlador de dispositivo.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="REG_SZ"></span><span id="reg_sz"></span><dl> <dt>**REG \_ SZ**</dt> </dl>                                                      | Cadena terminada en un valor nulo. Será una cadena Unicode o ANSI, en función de si se usan las funciones Unicode o ANSI.<br/>                                                                                                                                                                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Winnt.h</dt> </dl> |



 

 





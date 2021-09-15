---
description: La API de protección de datos de CNG usa las siguientes constantes.
ms.assetid: 4E43FAA9-7D6F-43DB-A998-189411E0AB4C
title: Constantes DPAPI de CNG (NCryptprotect.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece376a0b7282f26ef933b249a1356b2d012d438
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271244"
---
# <a name="cng-dpapi-constants"></a>Constantes DPAPI de CNG

La API de protección de datos de CNG usa las siguientes constantes.

<dl> <dt>

<span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**DELIMITADOR \_ DE NCRYPT \_ DESCR \_ Y**
</dt> <dd> <dl> <dt>

L" Y "
</dt> <dt>



Se puede usar para probar una cadena de descriptor de protección para un delimitador AND.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**NCRYPT \_ DESCR \_ EQUAL**
</dt> <dd> <dl> <dt>

L"="
</dt> <dt>



Se puede usar para probar una cadena de descriptor de protección para un signo igual.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**DELIMITADOR \_ DE NCRYPT DESCR \_ \_ O**
</dt> <dd> <dl> <dt>

L" O "
</dt> <dt>



Se puede usar para probar una cadena de descriptor de protección para un delimitador OR.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**ALGORITMO DE PROTECCIÓN DE CLAVES NCRYPT \_ \_ \_ \_ LOCAL**
</dt> <dd> <dl> <dt>

"LOCAL"
</dt> <dt>



El descriptor de protección LOCAL protege el contenido de la sesión de inicio de sesión, el usuario actual o el equipo local, tal como se identifica en las constantes siguientes:

-   **INICIO DE SESIÓN LOCAL DE NCRYPT \_ KEY \_ PROTECTION \_ \_**
-   **USUARIO LOCAL DE NCRYPT \_ KEY \_ PROTECTION \_ \_**
-   **EQUIPO \_ LOCAL DE PROTECCIÓN \_ DE CLAVES \_ NCRYPT \_**


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**SDDL \_ DEL ALGORITMO DE PROTECCIÓN DE CLAVES \_ \_ \_ NCRYPT**
</dt> <dd> <dl> <dt>

"SDDL"
</dt> <dt>



Protege el contenido de una cadena SDDL (lenguaje de definición de descriptor de seguridad) que contiene información del descriptor de seguridad.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**SID DEL \_ ALGORITMO DE PROTECCIÓN DE CLAVES \_ \_ \_ NCRYPT**
</dt> <dd> <dl> <dt>

"SID"
</dt> <dt>



El descriptor de protección de SID contiene una identidad de grupo o entidad de seguridad.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**CREDENCIALES WEB DEL \_ ALGORITMO DE PROTECCIÓN DE CLAVES \_ \_ \_ NCRYPT**
</dt> <dd> <dl> <dt>

"WEBCREDENTIALS"
</dt> <dt>



Protege las credenciales de la cuenta web de un usuario.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**INICIO DE SESIÓN LOCAL DE NCRYPT \_ KEY \_ PROTECTION \_ \_**
</dt> <dd> <dl> <dt>

"logon"
</dt> <dt>



Protege el contenido de la sesión de inicio de sesión actual. Los usuarios no podrán descifrar el contenido protegido después de cerrar o reiniciar.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**EQUIPO \_ LOCAL DE PROTECCIÓN \_ DE CLAVES \_ NCRYPT \_**
</dt> <dd> <dl> <dt>

"machine"
</dt> <dt>



Protege el contenido en el equipo local. Todos los usuarios del equipo local pueden descifrar el contenido protegido.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**USUARIO LOCAL DE NCRYPT \_ KEY \_ PROTECTION \_ \_**
</dt> <dd> <dl> <dt>

"user"
</dt> <dt>



Protege el contenido de la sesión de usuario actual. Solo este usuario del equipo local podrá descifrar el contenido protegido.


</dt> </dl> </dd> <dt>

<span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**PROVEEDOR DE \_ PROTECCIÓN \_ DE CLAVES DE MS \_**
</dt> <dd> <dl> <dt>

"Proveedor de Protección de claves de Microsoft"
</dt> <dt>



Representa el proveedor de protección de claves de Microsoft que admite formatos representados por las constantes siguientes:

-   **SID DEL \_ ALGORITMO DE PROTECCIÓN DE CLAVES \_ \_ \_ NCRYPT**
-   **ALGORITMO DE PROTECCIÓN DE CLAVES NCRYPT \_ \_ \_ \_ LOCAL**
-   **SDDL \_ DEL ALGORITMO DE PROTECCIÓN DE CLAVES \_ \_ \_ NCRYPT**


</dt> </dl> </dd> <dt>

<span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**PROVEEDOR \_ DE PROTECCIÓN DE CLAVES DE CLIENTE \_ \_ \_ DE WINDOWS**
</dt> <dd> <dl> <dt>

"Windows client Key Protection Provider"
</dt> <dt>



Representa el proveedor de protección de claves de Microsoft que solo está disponible en el cliente y que admite formatos representados por las constantes siguientes:

-   **CREDENCIALES WEB DEL \_ ALGORITMO DE PROTECCIÓN DE CLAVES \_ \_ \_ NCRYPT**


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>NCryptprotect.h</dt> </dl> |



 

 





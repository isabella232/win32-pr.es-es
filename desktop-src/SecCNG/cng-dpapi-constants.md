---
description: La API de protección de datos de CNG usa las siguientes constantes.
ms.assetid: 4E43FAA9-7D6F-43DB-A998-189411E0AB4C
title: Constantes DPAPI de CNG (NCryptprotect. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece376a0b7282f26ef933b249a1356b2d012d438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496972"
---
# <a name="cng-dpapi-constants"></a>Constantes DPAPI de CNG

La API de protección de datos de CNG usa las siguientes constantes.

<dl> <dt>

<span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**\_ \_ delimitador \_ de descripción de NCRYPT y**
</dt> <dd> <dl> <dt>

L "Y"
</dt> <dt>



Se puede usar para probar una cadena de descriptor de protección para un delimitador y.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**valor de descripción de NCRYPT \_ \_ igual**
</dt> <dd> <dl> <dt>

L "="
</dt> <dt>



Se puede usar para probar una cadena de descriptor de protección para un signo igual.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**\_ \_ delimitador \_ de descripción de NCRYPT o**
</dt> <dd> <dl> <dt>

L "O"
</dt> <dt>



Se puede usar para probar una cadena de descriptor de protección para un delimitador o.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**\_algoritmo de protección de claves NCRYPT \_ \_ \_ local**
</dt> <dd> <dl> <dt>

"LOCAL"
</dt> <dt>



El descriptor de protección LOCAL protege el contenido en la sesión de inicio de sesión, el usuario actual o el equipo local, tal y como se identifica en las siguientes constantes:

-   **\_configuración de \_ Inicio \_ de \_ sesión local de la protección de claves NCRYPT**
-   **\_ \_ usuario local de protección de claves NCRYPT \_ \_**
-   **\_ \_ máquina local de protección de claves NCRYPT \_ \_**


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**algoritmo de protección de claves de NCRYPT \_ \_ \_ \_ SDDL**
</dt> <dd> <dl> <dt>

SDDL
</dt> <dt>



Protege el contenido en una cadena SDDL (lenguaje de definición de descriptores de seguridad) que contiene información del descriptor de seguridad.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**\_SID del \_ algoritmo de protección de claves NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

Junction
</dt> <dt>



El descriptor de protección de SID contiene un grupo o una identidad de entidad de seguridad.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**\_claves de \_ algoritmo de protección de claves NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

"CREDENCIALes"
</dt> <dt>



Protege a las credenciales de la cuenta Web de un usuario.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**\_configuración de \_ Inicio \_ de \_ sesión local de la protección de claves NCRYPT**
</dt> <dd> <dl> <dt>

expire
</dt> <dt>



Protege el contenido de la sesión de inicio de sesión actual. Los usuarios no podrán descifrar el contenido protegido después de cerrar la sesión o reiniciar.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**\_ \_ máquina local de protección de claves NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

sistema
</dt> <dt>



Protege el contenido en el equipo local. Todos los usuarios del equipo local pueden descifrar el contenido protegido.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**\_ \_ usuario local de protección de claves NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

usuario
</dt> <dt>



Protege el contenido de la sesión de usuario actual. Solo este usuario en el equipo local podrá descifrar el contenido protegido.


</dt> </dl> </dd> <dt>

<span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**\_proveedor de \_ protección de claves de MS \_**
</dt> <dd> <dl> <dt>

"Proveedor de protección de claves de Microsoft"
</dt> <dt>



Representa el proveedor de protección de claves de Microsoft, que admite formatos representados por las constantes siguientes:

-   **\_SID del \_ algoritmo de protección de claves NCRYPT \_ \_**
-   **\_algoritmo de protección de claves NCRYPT \_ \_ \_ local**
-   **algoritmo de protección de claves de NCRYPT \_ \_ \_ \_ SDDL**


</dt> </dl> </dd> <dt>

<span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**\_proveedor de \_ protección de claves de cliente de Windows \_ \_**
</dt> <dd> <dl> <dt>

"Proveedor de protección de claves de cliente de Windows"
</dt> <dt>



Representa el proveedor de protección de claves de Microsoft que solo está disponible en el cliente y que admite formatos representados por las constantes siguientes:

-   **\_claves de \_ algoritmo de protección de claves NCRYPT \_ \_**


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>NCryptprotect. h</dt> </dl> |



 

 





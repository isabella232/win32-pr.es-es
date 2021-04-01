---
description: Se usa para representar entradas del registro que controlan el almacenamiento en caché de la clave privada por parte de los CSP basados en software de Microsoft.
ms.assetid: 67909072-72fe-4777-ae52-a7b9047c9dd5
title: Constantes de almacenamiento en caché de claves privadas (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6afa1394b33f4e36e31934e813b7c9fc41814e28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913625"
---
# <a name="private-key-caching-constants"></a>Constantes de almacenamiento en caché de claves privadas

Las constantes siguientes se usan para representar entradas del registro que controlan el almacenamiento en caché de la [*clave privada*](../secgloss/p-gly.md) por parte de CSP basados en software de Microsoft.



| Constante o valor                                                                                                                                                                                                                                                                                                                                                                                    | Descripción                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| <span id="szKEY_CRYPTOAPI_PRIVATE_KEY_OPTIONS"></span><span id="szkey_cryptoapi_private_key_options"></span><span id="SZKEY_CRYPTOAPI_PRIVATE_KEY_OPTIONS"></span><dl> <dt>**szKEY \_ \_Opciones de \_ clave \_ privada de CryptoAPI**</dt> <dt>"criptografía de \\ \\ \\ \\ Microsoft \\ \\ " de directivas de software</dt> </dl> | La ruta de acceso, en la raíz de la **\_ \_ máquina local HKEY** , de las entradas del registro de la clave privada de almacenamiento en caché.<br/> |



Las constantes siguientes se usan para identificar los valores del registro que controlan globalmente el almacenamiento en caché de la clave privada para un proceso específico de los CSP basados en software de Microsoft.



| Constante o valor                                                                                                                                                                                                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="szPRIV_KEY_CACHE_MAX_ITEMS"></span><span id="szpriv_key_cache_max_items"></span><span id="SZPRIV_KEY_CACHE_MAX_ITEMS"></span><dl> <dt>**szPRIV \_ \_ \_ Número máximo de \_ elementos**</dt> de la caché de claves <dt>"PrivKeyCacheMaxItems"</dt> </dl>                                                                  | Un valor de **reg \_ DWORD** en la clave del registro **szKEY \_ CryptoAPI \_ Private \_ key \_ Options** que especifica el número máximo de claves privadas que se pueden almacenar en caché al mismo tiempo para un único proceso. Esta comprobación se realiza siempre que se lee una clave privada almacenada. Si se supera el número máximo, la clave usada menos recientemente se quita de la memoria caché.<br/> Si este valor es cero, no se almacena ninguna clave en la memoria caché. Si este valor no está presente, el **valor \_ \_ predeterminado de \_ número máximo de \_ elementos \_** de la caché de claves de cPRIV se usa como valor predeterminado.<br/> Si actualmente se hace referencia a una clave privada que se elimina de la memoria caché en un contexto abierto, la clave se lee desde el almacenamiento la próxima vez que se realiza un intento de usar la clave.<br/> **Windows Server 2003 y Windows XP con SP1 y versiones anteriores:** No se admite este valor del registro.<br/>                                  |
| <span id="cPRIV_KEY_CACHE_MAX_ITEMS_DEFAULT"></span><span id="cpriv_key_cache_max_items_default"></span><span id="CPRIV_KEY_CACHE_MAX_ITEMS_DEFAULT"></span><dl> <dt>**cPRIV \_ \_ \_ Número máximo \_ \_ predeterminado de elementos de caché de claves**</dt> <dt>20</dt> </dl>                                                         | El valor predeterminado de la entrada del registro **\_ \_ Max key cache \_ Max \_ Items** si no se especifica ningún valor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="szPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS"></span><span id="szpriv_key_cache_purge_interval_seconds"></span><span id="SZPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS"></span><dl> <dt>**szPRIV \_ Intervalo de purga de caché de claves \_ en \_ \_ \_ segundos**</dt> <dt>"PrivKeyCachePurgeIntervalSeconds"</dt> </dl> | Un valor de **reg \_ DWORD** en la clave del registro **szKEY \_ CryptoAPI \_ Private \_ key \_ Options** que especifica la antigüedad máxima, en segundos, de cualquier clave privada almacenada en caché. Esta comprobación se realiza siempre que se usa o se lee una clave privada almacenada. Si esta cantidad de tiempo ha transcurrido desde la última vez que se produjo el desbloqueo, se quitarán de la memoria caché todas las claves almacenadas en caché a las que no se haya hecho referencia desde el último borrado.<br/> Si este valor no está presente, el **valor \_ \_ predeterminado del \_ \_ intervalo \_ \_ de purga de cPRIV** de la caché de claves de clave se utiliza como valor predeterminado.<br/> Si actualmente se hace referencia a una clave privada que se ha borrado de la memoria caché en un contexto abierto, la clave se leerá desde el almacenamiento la próxima vez que se intente usar la clave.<br/> **Windows Server 2003 y Windows XP con SP1 y versiones anteriores:** No se admite este valor del registro.<br/> |
| <span id="cPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS_DEFAULT"></span><span id="cpriv_key_cache_purge_interval_seconds_default"></span><span id="CPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS_DEFAULT"></span><dl> <dt>**cPRIV \_ Intervalo de purga de caché de clave \_ \_ \_ \_ \_ predeterminado**</dt> <dt>86400</dt> </dl> | El valor predeterminado de la entrada del registro de intervalo de purga de la caché de claves de SzPRIV si no se especifica ningún valor. **\_ \_ \_ \_ \_** Este valor equivale a un día.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



Las constantes siguientes se usan para identificar los valores del registro que controlan el almacenamiento en caché de la clave privada para una única instancia de [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) basada en software de Microsoft.



| Constante o valor                                                                                                                                                                                                                                                                                          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>"AllowCachePW"</dt> </dl>                                                                                                                                                         | Un valor de **reg \_ DWORD** en la clave del registro **HKEY \_ local \_ Machine \\ software \\ Policies \\ \\ \\ protección** de contraseñas de Microsoft, que especifica si el almacenamiento en caché de contraseñas está habilitado para las claves protegidas con contraseña en los CSP basados en software de Microsoft. Si este valor es 0, el almacenamiento en caché de contraseñas se desprotege y se solicita al usuario la contraseña cada vez que se usa una clave protegida por contraseña. Cualquier otro valor, o la ausencia de este valor, indica que la contraseña se almacenará en caché. En este escenario, el usuario solo se le solicita una vez por cada proceso por cada clave. <br/> |
| <span id="szKEY_CACHE_ENABLED"></span><span id="szkey_cache_enabled"></span><span id="SZKEY_CACHE_ENABLED"></span><dl> <dt>**szKEY \_ CACHÉ \_ habilitada**</dt> <dt>"CachePrivateKeys"</dt> </dl>          | Un valor de **reg \_ DWORD** en la clave del registro **szKEY \_ CryptoAPI \_ Private \_ key \_ Options** que especifica si está habilitado el almacenamiento en caché de clave privada. Si este valor es 1, se habilita el almacenamiento en caché de la clave privada. Cualquier otro valor, o la ausencia de este valor, indica que el almacenamiento en caché de la clave privada está deshabilitado.<br/> **Windows Vista con SP1, Windows Vista y Windows XP:** No se admite este valor del registro.<br/>                                                                                                                                                        |
| <span id="szKEY_CACHE_SECONDS"></span><span id="szkey_cache_seconds"></span><span id="SZKEY_CACHE_SECONDS"></span><dl> <dt>**szKEY \_ \_Segundos de caché**</dt> <dt>"PrivateKeyLifetimeSeconds"</dt> </dl> | Un valor de **reg \_ DWORD** en la clave del registro **szKEY \_ CryptoAPI \_ Private \_ key \_ Options** que especifica la antigüedad máxima, en segundos, de cualquier clave privada almacenada en caché.<br/> **Windows XP:** No se admite este valor del registro.<br/>                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Observaciones

Las diferencias entre los **\_ \_ segundos de caché de szKEY** y los valores de **\_ \_ \_ \_ \_ segundos del intervalo de purga** de la caché de claves de szPRIV son las siguientes:

 **\_segundos de caché de szKEY \_**  

-   Este valor solo se aplica a un CSP específico. Una vez publicado el CSP, también se libera la memoria caché del CSP.  
-   Este valor solo se aplica cuando se realiza un intento de usar una clave privada específica con un identificador de contexto específico.  

**intervalo de purga de caché de clave de szPRIV \_ \_ \_ \_ \_ segundos**  

-   Este valor se aplica a todos los CSP de un proceso. Aunque se lance el CSP, esta memoria caché no se libera.  
-   Este valor se aplica siempre que se use una clave privada almacenada o se lea desde el almacenamiento en un único proceso.  



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 

---
description: Se usa para representar entradas del Registro que controlan el almacenamiento en caché de claves privadas por parte de LOSPS basados en software de Microsoft.
ms.assetid: 67909072-72fe-4777-ae52-a7b9047c9dd5
title: Constantes de almacenamiento en caché de clave privada (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87d4caf6a3973a5113e03cbe24882241609ff83b8be65a20492f8f967abb734f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978566"
---
# <a name="private-key-caching-constants"></a>Constantes de almacenamiento en caché de clave privada

Las siguientes constantes se usan para representar las entradas del Registro que [*controlan*](../secgloss/p-gly.md) el almacenamiento en caché de claves privadas por parte de LOSPS basados en software de Microsoft.



| Constante o valor                                                                                                                                                                                                                                                                                                                                                                                    | Descripción                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| <span id="szKEY_CRYPTOAPI_PRIVATE_KEY_OPTIONS"></span><span id="szkey_cryptoapi_private_key_options"></span><span id="SZKEY_CRYPTOAPI_PRIVATE_KEY_OPTIONS"></span><dl> <dt>**szKEY \_ OPCIONES DE \_ CLAVE \_ PRIVADA \_ DE CRYPTOAPI**</dt> <dt>"Directivas de software \\ \\ \\ \\ \\ \\ Criptografía de Microsoft"</dt> </dl> | Ruta de acceso, bajo la raíz **HKEY \_ LOCAL \_ MACHINE,** de las entradas del Registro de almacenamiento en caché de claves privadas.<br/> |



Las siguientes constantes se usan para identificar los valores del Registro que controlan el almacenamiento en caché de claves privadas globalmente para un proceso específico por parte de LOSPS basados en software de Microsoft.



| Constante o valor                                                                                                                                                                                                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="szPRIV_KEY_CACHE_MAX_ITEMS"></span><span id="szpriv_key_cache_max_items"></span><span id="SZPRIV_KEY_CACHE_MAX_ITEMS"></span><dl> <dt>**szPRIV \_ KEY \_ CACHE \_ MAX \_ ITEMS**</dt> <dt>"PrivKeyCacheMaxItems"</dt> </dl>                                                                  | Valor **REG \_ DWORD** bajo la clave del Registro **szKEY \_ CRYPTOAPI PRIVATE KEY \_ \_ \_ OPTIONS** que especifica el número máximo de claves privadas que se pueden almacenar en caché al mismo tiempo para un único proceso. Esta comprobación se realiza siempre que se lee una clave privada almacenada. Si se supera el número máximo, la clave usada menos recientemente se quita de la memoria caché.<br/> Si este valor es cero, no se almacena en caché ninguna clave. Si este valor no está presente, el valor predeterminado **cPRIV \_ KEY CACHE MAX ITEMS \_ \_ \_ \_ DEFAULT** se usa como valor predeterminado.<br/> Si actualmente se hace referencia a una clave privada que se elimina de la caché en un contexto abierto, la clave se lee del almacenamiento la próxima vez que se intente usar la clave.<br/> **Windows Server 2003 y Windows XP con SP1 y versiones anteriores:** No se admite este valor del Registro.<br/>                                  |
| <span id="cPRIV_KEY_CACHE_MAX_ITEMS_DEFAULT"></span><span id="cpriv_key_cache_max_items_default"></span><span id="CPRIV_KEY_CACHE_MAX_ITEMS_DEFAULT"></span><dl> <dt>**cPRIV \_ NÚMERO \_ MÁXIMO DE ELEMENTOS DE CACHÉ DE CLAVES \_ \_ \_ PREDETERMINADO**</dt> <dt>20</dt> </dl>                                                         | Valor predeterminado de la entrada del Registro **szPRIV \_ KEY CACHE MAX \_ \_ \_ ITEMS** si no se especifica ningún valor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="szPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS"></span><span id="szpriv_key_cache_purge_interval_seconds"></span><span id="SZPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS"></span><dl> <dt>**szPRIV \_ KEY \_ CACHE PURGE INTERVAL \_ \_ \_ SECONDS**</dt> <dt>"PrivKeyCachePurgeIntervalSeconds"</dt> </dl> | Valor **REG \_ DWORD bajo** la clave del Registro **szKEY \_ CRYPTOAPI PRIVATE KEY \_ \_ \_ OPTIONS** que especifica la antigüedad máxima, en segundos, de cualquier clave privada almacenada en caché. Esta comprobación se realiza siempre que se usa o lee una clave privada almacenada. Si esta cantidad de tiempo ha transcurrido desde que se produjo la última eliminación, todas las claves almacenadas en caché a las que no se ha hecho referencia desde la última eliminación se quitarán de la memoria caché.<br/> Si este valor no está presente, el valor predeterminado **cPRIV \_ KEY CACHE PURGE INTERVAL SECONDS \_ \_ \_ \_ \_ DEFAULT** se usa como valor predeterminado.<br/> Si actualmente se hace referencia a una clave privada que se borra de la caché en un contexto abierto, la clave se leerá del almacenamiento la próxima vez que se intente usar la clave.<br/> **Windows Server 2003 y Windows XP con SP1 y versiones anteriores:** No se admite este valor del Registro.<br/> |
| <span id="cPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS_DEFAULT"></span><span id="cpriv_key_cache_purge_interval_seconds_default"></span><span id="CPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS_DEFAULT"></span><dl> <dt>**cPRIV \_ INTERVALO DE \_ PURGA DE CACHÉ DE CLAVES SEGUNDOS \_ \_ \_ \_ PREDETERMINADO**</dt> <dt>86400</dt> </dl> | Valor predeterminado de la entrada del Registro **szPRIV \_ KEY CACHE PURGE INTERVAL \_ \_ \_ \_ SECONDS** si no se especifica ningún valor. Este valor es equivalente a un día.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



Las siguientes constantes se usan para identificar los valores del Registro que [](../secgloss/c-gly.md) controlan el almacenamiento en caché de claves privadas para una única instancia del proveedor de servicios criptográficos (CSP) basado en software de Microsoft.



| Constante o valor                                                                                                                                                                                                                                                                                          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>"AllowCachePW"</dt> </dl>                                                                                                                                                         | Valor **REG \_ DWORD** en la clave del Registro **HKEY LOCAL MACHINE SOFTWARE \_ Policies Microsoft \_ \\ \\ \\ \\ Cryptography \\ Protect** que especifica si el almacenamiento en caché de contraseñas está habilitado para las claves protegidas con contraseña en los CSP basados en software de Microsoft. Si este valor es 0, el almacenamiento en caché de contraseñas no se puede almacenar en caché y se solicita al usuario la contraseña cada vez que se usa una clave protegida con contraseña. Cualquier otro valor, o la ausencia de este valor, indica que la contraseña se almacenará en caché. En este escenario, solo se solicita al usuario una vez por proceso para cada una de estas claves. <br/> |
| <span id="szKEY_CACHE_ENABLED"></span><span id="szkey_cache_enabled"></span><span id="SZKEY_CACHE_ENABLED"></span><dl> <dt>**szKEY \_ CACHE \_ ENABLED**</dt> <dt>"CachePrivateKeys"</dt> </dl>          | Valor **REG \_ DWORD bajo** la clave del Registro **szKEY \_ CRYPTOAPI PRIVATE KEY \_ \_ \_ OPTIONS** que especifica si está habilitado el almacenamiento en caché de claves privadas. Si este valor es 1, el almacenamiento en caché de claves privadas está habilitado. Cualquier otro valor, o la ausencia de este valor, indica que el almacenamiento en caché de claves privadas está deshabilitado.<br/> **Windows Vista con SP1, Windows Vista y Windows XP:** No se admite este valor del Registro.<br/>                                                                                                                                                        |
| <span id="szKEY_CACHE_SECONDS"></span><span id="szkey_cache_seconds"></span><span id="SZKEY_CACHE_SECONDS"></span><dl> <dt>**szKEY \_ SEGUNDOS \_ DE CACHÉ**</dt> <dt>"PrivateKeyLifetimeSeconds"</dt> </dl> | Valor **REG \_ DWORD bajo** la clave del Registro **szKEY \_ CRYPTOAPI PRIVATE KEY \_ \_ \_ OPTIONS** que especifica la antigüedad máxima, en segundos, de cualquier clave privada almacenada en caché.<br/> **Windows XP:** No se admite este valor del Registro.<br/>                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Comentarios

Las diferencias entre los **valores szKEY \_ CACHE \_ SECONDS** y **szPRIV KEY CACHE PURGE \_ INTERVAL \_ \_ \_ \_ SECONDS** son las siguientes:

 **szKEY \_ CACHE \_ SECONDS**  

-   Este valor solo se aplica a un CSP específico. Una vez publicado el CSP, también se libera la memoria caché del CSP.  
-   Este valor solo se aplica cuando se intenta usar una clave privada específica con un identificador de contexto específico.  

**szPRIV \_ KEY CACHE PURGE INTERVAL \_ \_ \_ \_ SECONDS**  

-   Este valor se aplica a todos los CSP de un proceso. Incluso si se libera el CSP, esta caché no se libera.  
-   Este valor se aplica siempre que se usa o lee cualquier clave privada almacenada desde el almacenamiento en un único proceso.  



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 

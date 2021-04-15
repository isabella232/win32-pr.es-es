---
description: Se usa para identificar una propiedad de almacenamiento de claves.
ms.assetid: 407f0e42-07c8-4ec6-81c6-f8bde005adb0
title: Identificadores de propiedad de almacenamiento de claves (ncrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 813a15ba106989cb558eba181bc893d75c6d1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669911"
---
# <a name="key-storage-property-identifiers"></a>Identificadores de propiedad de almacenamiento de claves

Los valores siguientes se usan para identificar una propiedad de almacenamiento de claves.

<dl> <dt>

<span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**\_propiedad de \_ grupo de algoritmo NCRYPT \_**
</dt> <dd> <dl> <dt>

L "grupo de algoritmos"
</dt> <dt>



Una cadena Unicode terminada en null que contiene el nombre del grupo de algoritmos del objeto. Esta propiedad solo se aplica a las claves. El proveedor de almacenamiento de claves de Microsoft devuelve los siguientes identificadores.



| Identificador                                     | Value              | Descripción                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------|
| **\_grupo de \_ algoritmos RSA de NCRYPT \_**<br/>   | RSA<br/>   | El grupo de algoritmos RSA.<br/>                           |
| **\_grupo de \_ algoritmos DH NCRYPT \_**<br/>    | DH<br/>    | El grupo de algoritmos Diffie-Hellman.<br/>                |
| **\_grupo de \_ algoritmo \_ DSA de NCRYPT**<br/>   | ALGORITMO<br/>   | El grupo de algoritmos DSA.<br/>                           |
| **\_grupo de \_ algoritmos ECDSA de NCRYPT \_**<br/> | ECDSA<br/> | El grupo de algoritmo DSA de curva elíptica.<br/>            |
| **\_grupo de \_ algoritmos ECDH NCRYPT \_**<br/>  | ECDH<br/>  | Curva elíptica Diffie-Hellman grupo de algoritmos.<br/> |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**\_propiedad del algoritmo NCRYPT \_**
</dt> <dd> <dl> <dt>

L "nombre del algoritmo"
</dt> <dt>



Una cadena Unicode terminada en null que contiene el nombre del algoritmo del objeto. Puede ser uno de los [**identificadores de algoritmo CNG**](cng-algorithm-identifiers.md) predefinidos u otro identificador de algoritmo registrado. Esta propiedad solo se aplica a las claves.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**\_ \_ clave ECDH asociada de NCRYPT \_**
</dt> <dd> <dl> <dt>

L "SmartCardAssociatedECDHKey"
</dt> <dt>



Valor **LPWStr** que indica el nombre del contenedor de la clave de curva elíptica Diffie-Hellman (ECDH) que se va a usar durante el inicio de sesión para un identificador determinado de una clave de algoritmo de firma digital de curva elíptica (ECDSA). Si no hay ninguna clave ECDH en la tarjeta, el [*proveedor de almacenamiento de claves*](/windows/desktop/SecGloss/k-gly) (KSP) devuelve **NTE \_ no \_ encontrado**. Esta propiedad se aplica a las claves ECDSA para el inicio de sesión con tarjetas inteligentes. La propiedad es compatible con el proveedor de almacenamiento de claves de tarjeta inteligente de Microsoft y no con el proveedor de almacenamiento de claves de software de Microsoft.

**Windows Server 2008 y Windows Vista:** Este valor no se admite.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**\_ \_ propiedad longitud de bloque NCRYPT \_**
</dt> <dd> <dl> <dt>

L "longitud de bloque"
</dt> <dt>



**DWORD** que contiene la longitud, en bytes, del bloque de cifrado. Esta propiedad solo se aplica a las claves que admiten el cifrado.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**\_propiedad de certificado NCRYPT \_**
</dt> <dd> <dl> <dt>

L "SmartCardKeyCertificate"
</dt> <dt>



Un [*BLOB*](/windows/desktop/SecGloss/b-gly) que contiene un certificado X. 509 que está asociado a la clave.

**Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Un [*BLOB*](/windows/desktop/SecGloss/b-gly) que contiene el [*certificado*](/windows/desktop/SecGloss/c-gly)de clave de [*tarjeta inteligente*](/windows/desktop/SecGloss/s-gly) . Esta propiedad no es compatible con el proveedor de almacenamiento de claves de software de Microsoft.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**\_propiedad de \_ parámetros \_ DH de NCRYPT**
</dt> <dd> <dl> <dt>

L "DHParameters"
</dt> <dt>



Especifica los parámetros que se van a usar con una clave de Diffie-Hellman. Este tipo de datos es un puntero a una estructura de [**\_ encabezado de \_ parámetro \_ de BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) . Esta propiedad solo se puede establecer y debe establecerse para la clave antes de que se complete la clave.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**\_propiedad de \_ Directiva de exportación de NCRYPT \_**
</dt> <dd> <dl> <dt>

L "exportar Directiva"
</dt> <dt>



**DWORD** que contiene un conjunto de marcas que especifican la Directiva de exportación para una clave conservada. Esta propiedad solo se aplica a las claves. Puede contener cero o una combinación de uno o varios de los valores siguientes.



| Identificador                                    | Value      | Descripción                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_marca permitir \_ exportación de NCRYPT \_**               | 0x00000001 | Se puede exportar la clave privada.                                                                                                                                                                                                                                                                                 |
| **NCRYPT \_ permitir \_ la \_ marca de exportación de texto sin formato \_**    | 0x00000002 | La clave privada se puede exportar en formato de texto simple.                                                                                                                                                                                                                                                               |
| **\_marca permitir \_ archivado \_ de NCRYPT**            | 0x00000004 | La clave privada se puede exportar una vez para fines de archivado. Esta marca solo se aplica al identificador de clave original en el que se establece. Esta directiva solo se puede aplicar al identificador de clave original. Una vez que se ha cerrado el identificador de clave, ya no se puede exportar la clave para fines de archivado.                   |
| **NCRYPT \_ permitir \_ el \_ marcado de archivo sin formato \_** | 0x00000008 | La clave privada se puede exportar una vez en formato de texto no cifrado. Esta marca solo se aplica al identificador de clave original en el que se establece. Esta directiva solo se puede aplicar al identificador de clave original. Una vez que se ha cerrado el identificador de clave, ya no se puede exportar la clave para fines de archivado. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**\_propiedad del \_ tipo impl impl \_**
</dt> <dd> <dl> <dt>

L "tipo impl"
</dt> <dt>



**DWORD** que contiene un conjunto de marcadores que definen los detalles de implementación del proveedor. Esta propiedad solo se aplica a los proveedores de almacenamiento de claves. Puede contener cero o una combinación de uno o varios de los valores siguientes.



| Identificador                            | Value      | Descripción                                               |
|---------------------------------------|------------|-----------------------------------------------------------|
| **\_marca de \_ hardware NCRYPT impl \_**      | 0x00000001 | El proveedor está basado en hardware.                           |
| **\_marca de \_ software NCRYPT impl \_**      | 0x00000002 | El proveedor está basado en software.                           |
| **\_ \_ marca extraíble de NCRYPT impl \_**     | 0x00000008 | El proveedor es extraíble.                                |
| **\_ \_ \_ marca RNG de hardware \_ de NCRYPT impl** | 0x00000010 | El proveedor es un generador de números aleatorios basado en hardware. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**\_ \_ propiedad tipo de clave NCRYPT \_**
</dt> <dd> <dl> <dt>

L "tipo de clave"
</dt> <dt>



**DWORD** que contiene un conjunto de marcas que definen el tipo de clave. Esta propiedad solo se aplica a las claves. Puede contener cero o el valor siguiente.



| Identificador                     | Value      | Descripción                                                                                              |
|--------------------------------|------------|----------------------------------------------------------------------------------------------------------|
| **\_marca de \_ clave de equipo NCRYPT \_** | 0x00000001 | La clave se aplica al equipo local. Si este marcador no está presente, la clave se aplica al usuario actual. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**\_ \_ propiedad uso de clave NCRYPT \_**
</dt> <dd> <dl> <dt>

L "uso de la clave"
</dt> <dt>



**DWORD** que contiene un conjunto de marcas que definen los detalles de uso de una clave. Esta propiedad solo se aplica a las claves. Puede contener cero o una combinación de uno o varios de los valores siguientes.



| Identificador                              | Value      | Descripción                                          |
|-----------------------------------------|------------|------------------------------------------------------|
| **NCRYPT \_ permitir \_ marca de descifrado \_**        | 0x00000001 | La clave se puede utilizar para el descifrado.                  |
| **NCRYPT \_ permitir \_ la \_ marca de firma**        | 0x00000002 | La clave se puede utilizar para firmar.                     |
| **\_marca de \_ acuerdo de clave de permitir NCRYPT \_ \_** | 0x00000004 | La clave se puede usar para el cifrado del acuerdo secreto. |
| **NCRYPT \_ permite \_ todos los \_ usos**          | 0x00FFFFFF | La clave se puede utilizar para cualquier propósito.                 |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**\_propiedad última \_ modificación de NCRYPT \_**
</dt> <dd> <dl> <dt>

L "modificado"
</dt> <dt>



Indica cuándo se modificó por última vez la clave. Este tipo de datos es un puntero a una estructura de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) . Esta propiedad solo se aplica a las claves persistentes.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**\_propiedad longitud de NCRYPT \_**
</dt> <dd> <dl> <dt>

L "longitud"
</dt> <dt>



**DWORD** que contiene la longitud, en bits, de la clave. Esta propiedad solo se aplica a las claves.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**\_propiedad de longitudes NCRYPT \_**
</dt> <dd> <dl> <dt>

L "longitudes"
</dt> <dt>



Indica los tamaños de clave admitidos por la clave. Este tipo de datos es un puntero a una estructura de [**\_ \_ longitudes admitidas de NCRYPT**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) que contiene esta información. Esta propiedad solo se aplica a las claves.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**\_ \_ \_ propiedad longitud máxima del nombre NCRYPT \_**
</dt> <dd> <dl> <dt>

L "longitud máxima del nombre"
</dt> <dt>



**DWORD** que contiene la longitud máxima, en caracteres, del nombre de una clave persistente. Esta propiedad solo se aplica a un proveedor.

Esta propiedad está pensada principalmente para ser utilizada por proveedores de almacenamiento de claves que almacenan sus claves en un dispositivo con una cantidad limitada de memoria disponible, como una tarjeta inteligente.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**\_propiedad de nombre NCRYPT \_**
</dt> <dd> <dl> <dt>

L "nombre"
</dt> <dt>



Puntero a una cadena Unicode terminada en null que contiene el nombre del objeto.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**\_ \_ propiedad del símbolo del PIN de NCRYPT \_**
</dt> <dd> <dl> <dt>

L "SmartCardPinPrompt"
</dt> <dt>



Este valor no se admite.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**\_propiedad PIN de NCRYPT \_**
</dt> <dd> <dl> <dt>

L "SmartCardPin"
</dt> <dt>



Puntero a una cadena Unicode terminada en null que contiene el código PIN. El PIN se usa para una clave de tarjeta inteligente o la contraseña de una clave protegida por contraseña almacenada en un KSP basado en software. Esta propiedad solo se puede establecer. Microsoft KSP almacenará en caché este valor para que el usuario solo se le solicite una vez por cada proceso.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**\_propiedad de \_ identificador del proveedor NCRYPT \_**
</dt> <dd> <dl> <dt>

L "identificador de proveedor"
</dt> <dt>



**\_ \_ Identificador Prov de NCRYPT** que contiene el identificador del proveedor de almacenamiento de claves CNG. Cuando haya terminado de usar el identificador, debe llamar a [**NCryptFreeObject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) para liberarlo.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**\_propiedad del lector NCRYPT \_**
</dt> <dd> <dl> <dt>

L "SmartCardReader"
</dt> <dt>



Puntero a una cadena Unicode terminada en null que contiene el nombre del lector de tarjeta inteligente. Esta propiedad solo se puede establecer.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**\_ \_ propiedad CERTSTORE raíz \_ NCRYPT**
</dt> <dd> <dl> <dt>

L "SmartcardRootCertStore"
</dt> <dt>



**HCERTSTORE** que representa el almacén de certificados raíz de la tarjeta inteligente.


</dt> </dl> </dd> <dt>

<span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span>**NCRYPT \_ identificador de \_ PIN \_ PPAC**
</dt> <dd> <dl> <dt>

L "SmartCardPinId"
</dt> <dt>



Un puntero al valor **de \_ identificador de PIN** asociado a una [*clave criptográfica*](/windows/desktop/SecGloss/c-gly) determinada en una [*tarjeta inteligente*](/windows/desktop/SecGloss/s-gly). Se trata de una propiedad de solo lectura. El tipo de datos del **\_ identificador de PIN** se define en Cardmod. h.

**Windows Server 2008 y Windows Vista:** Este valor no se admite.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**\_ \_ información del PIN PPAC (NCRYPT) \_**
</dt> <dd> <dl> <dt>

L "SmartCardPinInfo"
</dt> <dt>



Un puntero a la estructura de [**\_ información**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) del PIN asociado a una clave criptográfica determinada en la tarjeta inteligente. El autor de la llamada proporciona el identificador de clave. Esta propiedad es de solo lectura. La estructura de **\_ información del PIN** se define en Cardmod. h.

**Windows Server 2008 y Windows Vista:** Este valor no se admite.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**\_propiedad de \_ PIN \_ seguro de NCRYPT**
</dt> <dd> <dl> <dt>

L "SmartCardSecurePin"
</dt> <dt>



Puntero a una cadena Unicode terminada en null que contiene el PIN de la sesión de tarjeta inteligente. Esta propiedad solo se puede establecer.

**Windows Vista:** Esta propiedad no se admite.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**\_propiedad de \_ Descripción de seguridad NCRYPT \_**
</dt> <dd> <dl> <dt>

L "Descripción de seguridad"
</dt> <dt>



Puntero a una estructura [**de \_ descriptores de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que contiene información de control de acceso para la clave. Esta propiedad solo se aplica a las claves persistentes. El parámetro *dwFlags* de la función [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) o [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) identifica la parte del descriptor de seguridad que se va a obtener o establecer.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**\_propiedad de \_ compatibilidad del Descr de seguridad NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L "compatibilidad con el Descr de seguridad"
</dt> <dt>



Indica si el proveedor admite descriptores de seguridad para las claves. Esta propiedad es un **valor DWORD** que contiene 1 si el proveedor admite descriptores de seguridad para las claves. Si esta propiedad contiene cualquier otro valor, o si la función [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) devuelve **NTE \_ not \_** Supported, el proveedor no admite descriptores de seguridad para las claves. Esta propiedad solo se aplica a los proveedores.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**\_propiedad GUID de tarjeta inteligente NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L "SmartCardGuid"
</dt> <dt>



Un BLOB que contiene el identificador de la tarjeta inteligente.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**propiedad de directiva de interfaz de \_ usuario NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L "Directiva de la interfaz de usuario"
</dt> <dt>



Si se usa con la función [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) o [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) , se trata de un puntero a una estructura de [**Directiva de \_ \_ interfaz**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) de usuario de NCRYPT que contiene la Directiva de interfaz de usuario de clave segura para la clave. Esta propiedad solo se aplica a las claves persistentes. Esta propiedad solo se puede establecer cuando se genera la clave. Una vez que se ha llamado a la función [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) para esta clave, esta propiedad es de solo lectura.

Un proveedor de almacenamiento de claves puede recibir este parámetro a través de una función de devolución de llamada [**NCryptSetPropertyFn**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) . El valor del parámetro es una \_ estructura de BLOB de directiva de interfaz de usuario NCRYPT \_ \_ que contiene la misma información. Del mismo modo, cuando una aplicación realiza una solicitud a través de NCryptSetPropertyFn al proveedor para devolver esta propiedad, se espera que el proveedor devuelva una \_ estructura de BLOB de directiva de interfaz de usuario NCRYPT \_ \_ .


</dt> </dl> </dd> <dt>

<span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**\_ \_ propiedad nombre único de NCRYPT \_**
</dt> <dd> <dl> <dt>

L "nombre único"
</dt> <dt>



Puntero a una cadena Unicode terminada en null que contiene el nombre único del objeto. Se trata de un nombre alternativo que se puede usar al obtener acceso a la clave. Esta propiedad se usa cuando se considera que el nombre de clave que se pasó originalmente a [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) no es suficiente para identificar de forma confiable la clave persistente. El proveedor de almacenamiento de claves de Microsoft devolverá el nombre de archivo de la clave como esta propiedad.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**\_propiedad de \_ contexto \_ use NCRYPT**
</dt> <dd> <dl> <dt>

L "usar contexto"
</dt> <dt>



Puntero a una cadena Unicode terminada en null que describe el contexto de la operación. Esta propiedad no es persistente y se puede establecer en un proveedor o una clave. Una clave no tiene acceso a la propiedad **de \_ \_ \_ propiedad de contexto usar** el valor de NCRYPT del proveedor porque la propiedad solo es específica del identificador para el que se establece.

Un ejemplo en el que esta propiedad se utilizaría en el contexto de un proveedor es un proveedor de almacenamiento de claves que necesita preguntar al usuario durante una llamada a [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) (por ejemplo, "insertar la tarjeta inteligente en el lector"). Dado que el identificador de clave no está disponible hasta que **NCryptOpenKey** devuelve, la aplicación debe establecer esta propiedad en el identificador del proveedor antes de llamar a **NCryptOpenKey**.

Un ejemplo en el que esta propiedad se usaría en el contexto de un identificador de clave es un proveedor de almacenamiento de claves que necesita preguntar al usuario durante una operación con la clave (por ejemplo, "esta aplicación necesita usar esta clave para firmar un documento"). Después, el proveedor puede retransmitir esta información de contexto al usuario en cualquier interfaz de usuario que se muestra durante la operación.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**\_propiedad de recuento de uso de NCRYPT \_ \_ habilitado \_**
</dt> <dd> <dl> <dt>

L "recuento de uso habilitado"
</dt> <dt>



Indica si el proveedor admite el recuento de uso de claves. Esta propiedad es un **valor DWORD** que contiene 1 si el proveedor admite el recuento de uso de claves. Si esta propiedad contiene cualquier otro valor, o si la función [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) devuelve **NTE \_ not \_** Supported, el proveedor no admite el recuento de uso de las claves. Esta propiedad solo se aplica a los proveedores.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**\_propiedad de \_ recuento de uso de NCRYPT \_**
</dt> <dd> <dl> <dt>

L "recuento de uso"
</dt> <dt>



Una variable de [**\_ entero ULARGE**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) que contiene el número de operaciones que ha realizado la [*clave privada*](/windows/desktop/SecGloss/p-gly) especificada. Esta propiedad es opcional y es posible que no sea compatible con todos los proveedores. Los proveedores que admiten esta propiedad en las claves deben admitir también la propiedad de **\_ propiedad de recuento de uso de NCRYPT \_ \_ habilitada \_** en el identificador del proveedor. El proveedor de almacenamiento de claves de Microsoft no admite esta propiedad. Esta propiedad solo se aplica a las claves persistentes.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**\_ \_ propiedad CERTSTORE de usuario de NCRYPT \_**
</dt> <dd> <dl> <dt>

L "SmartCardUserCertStore"
</dt> <dt>



Un **HCERTSTORE** que representa el almacén de certificados de usuario de tarjeta inteligente.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**\_propiedad versión de NCRYPT \_**
</dt> <dd> <dl> <dt>

L "versión"
</dt> <dt>



**DWORD** que contiene la versión de software del proveedor. La palabra alta contiene la versión principal y la palabra baja contiene la versión secundaria. Por ejemplo, 0x00030033 = 3,51. Esta propiedad solo se aplica a los proveedores.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**\_propiedad de \_ identificador de ventana NCRYPT \_**
</dt> <dd> <dl> <dt>

L "identificador de HWND"
</dt> <dt>



Puntero al identificador de ventana (**hWnd**) que se va a usar como elemento primario de cualquier interfaz de usuario que se muestre.

Dado que el comportamiento no deseado puede producirse cuando se muestra una interfaz de usuario mediante un identificador de ventana **nulo** para el elemento primario, se recomienda encarecidamente que un proveedor de almacenamiento de claves no muestre una interfaz de usuario a menos que se establezca esta propiedad.


</dt> </dl> </dd> </dl>

Los valores siguientes se usan para definir los límites de los datos de propiedad.



| Constante o valor                                                                                                                                                                                                                                                 | Descripción                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="NCRYPT_MAX_PROPERTY_DATA"></span><span id="ncrypt_max_property_data"></span><dl> <dt>**NCRYPT \_ Longitud máxima de \_ \_ datos de propiedad**</dt> <dt>0x100000</dt> </dl> | Especifica el tamaño máximo de un valor de propiedad, en bytes.<br/>     |
| <span id="NCRYPT_MAX_PROPERTY_NAME"></span><span id="ncrypt_max_property_name"></span><dl> <dt>**NCRYPT \_ \_ \_ Nombre de propiedad Max**</dt> <dt>64</dt> </dl>       | Especifica el tamaño máximo de un nombre de propiedad, en caracteres.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Ncrypt. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty)
</dt> <dt>

[**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)
</dt> </dl>

 


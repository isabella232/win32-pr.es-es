---
description: Se usa para identificar una propiedad de almacenamiento de claves.
ms.assetid: 407f0e42-07c8-4ec6-81c6-f8bde005adb0
title: Identificadores Storage propiedad clave (Ncrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b8fca27591837a555e4f75040ba16056c42e16ce488c0bb99f2d8f7de70bd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907631"
---
# <a name="key-storage-property-identifiers"></a>Identificadores de Storage clave

Los valores siguientes se usan para identificar una propiedad de almacenamiento de claves.

<dl> <dt>

<span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**NCRYPT \_ ALGORITHM \_ GROUP \_ PROPERTY**
</dt> <dd> <dl> <dt>

L"Algorithm Group"
</dt> <dt>



Cadena Unicode terminada en NULL que contiene el nombre del grupo de algoritmos del objeto. Esta propiedad solo se aplica a las claves. El proveedor de almacenamiento de claves de Microsoft devuelve los identificadores siguientes.



| Identificador                                     | Value              | Descripción                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------|
| **NCRYPT \_ RSA \_ ALGORITHM \_ GROUP**<br/>   | "RSA"<br/>   | El grupo de algoritmos RSA.<br/>                           |
| **NCRYPT \_ DH \_ ALGORITHM \_ GROUP**<br/>    | "DH"<br/>    | El Diffie-Hellman de algoritmos.<br/>                |
| **NCRYPT \_ DSA \_ ALGORITHM \_ GROUP**<br/>   | "DSA"<br/>   | El grupo de algoritmos DSA.<br/>                           |
| **NCRYPT \_ ECDSA \_ ALGORITHM \_ GROUP**<br/> | "ECDSA"<br/> | Grupo de algoritmos DSA de curva elíptica.<br/>            |
| **NCRYPT \_ ECDH \_ ALGORITHM \_ GROUP**<br/>  | "ECDH"<br/>  | La curva elíptica Diffie-Hellman grupo de algoritmos.<br/> |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**PROPIEDAD NCRYPT \_ ALGORITHM \_**
</dt> <dd> <dl> <dt>

L"Nombre del algoritmo"
</dt> <dt>



Cadena Unicode terminada en NULL que contiene el nombre del algoritmo del objeto. Puede ser uno de los identificadores de algoritmo [**CNG predefinidos**](cng-algorithm-identifiers.md) u otro identificador de algoritmo registrado. Esta propiedad solo se aplica a las claves.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**NCRYPT \_ ASSOCIATED \_ ECDH \_ KEY**
</dt> <dd> <dl> <dt>

L"SmartCardAssociatedECDHKey"
</dt> <dt>



Valor **LPWSTR** que indica el nombre del contenedor de la clave elíptica curve Diffie-Hellman (ECDH) que se usará durante el inicio de sesión para un identificador determinado en una clave del algoritmo de firma digital de curva elíptica (ECDSA). Si no hay claves ECDH en la tarjeta, el proveedor [*de*](/windows/desktop/SecGloss/k-gly) almacenamiento de claves (KSP) devuelve **NTE \_ NOT \_ FOUND**. Esta propiedad se aplica a las claves ECDSA para el inicio de sesión con tarjetas inteligentes. La propiedad es compatible con el proveedor de almacenamiento de claves de tarjeta inteligente de Microsoft y no con el proveedor de almacenamiento de claves de software de Microsoft.

**Windows Server 2008 y Windows Vista:** Este valor no se admite.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**PROPIEDAD NCRYPT \_ BLOCK \_ \_ LENGTH**
</dt> <dd> <dl> <dt>

L"Block Length"
</dt> <dt>



DWORD **que** contiene la longitud, en bytes, del bloque de cifrado. Esta propiedad solo se aplica a las claves que admiten el cifrado.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**PROPIEDAD DE \_ CERTIFICADO NCRYPT \_**
</dt> <dd> <dl> <dt>

L"SmartCardKeyCertificate"
</dt> <dt>



Blob [*que*](/windows/desktop/SecGloss/b-gly) contiene un certificado X.509 asociado a la clave.

**Windows Server 2008 R2, Windows 7, Windows Server 2008 y Windows Vista:** Blob [*que*](/windows/desktop/SecGloss/b-gly) contiene el certificado [*de clave de*](/windows/desktop/SecGloss/s-gly) tarjeta [*inteligente*](/windows/desktop/SecGloss/c-gly). Esta propiedad no es compatible con el proveedor de claves de software Storage Microsoft.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**NCRYPT \_ DH \_ PARAMETERS \_ PROPERTY**
</dt> <dd> <dl> <dt>

L"DHParameters"
</dt> <dt>



Especifica los parámetros que se usarán con una Diffie-Hellman clave. Este tipo de datos es un puntero a una estructura [**\_ BCRYPT DH \_ PARAMETER \_ HEADER.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) Esta propiedad solo se puede establecer y debe establecerse para la clave antes de que se complete la clave.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**PROPIEDAD DE DIRECTIVA \_ DE \_ EXPORTACIÓN DE \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"Directiva de exportación"
</dt> <dt>



DWORD **que** contiene un conjunto de marcas que especifican la directiva de exportación para una clave persistente. Esta propiedad solo se aplica a las claves. Puede contener cero o una combinación de uno o varios de los valores siguientes.



| Identificador                                    | Value      | Descripción                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NCRYPT \_ ALLOW \_ EXPORT \_ FLAG**               | 0x00000001 | La clave privada se puede exportar.                                                                                                                                                                                                                                                                                 |
| **NCRYPT \_ ALLOW \_ PLAINTEXT \_ EXPORT \_ FLAG**    | 0x00000002 | La clave privada se puede exportar en formato de texto no cifrado.                                                                                                                                                                                                                                                               |
| **NCRYPT \_ ALLOW \_ ARCHIVING \_ FLAG**            | 0x00000004 | La clave privada se puede exportar una vez con fines de archivado. Esta marca solo se aplica al identificador de clave original en el que se establece. Esta directiva solo se puede aplicar al identificador de clave original. Una vez cerrado el identificador de clave, la clave ya no se puede exportar con fines de archivado.                   |
| **NCRYPT \_ ALLOW \_ PLAINTEXT \_ ARCHIVING \_ FLAG** | 0x00000008 | La clave privada se puede exportar una vez en formato de texto no cifrado con fines de archivado. Esta marca solo se aplica al identificador de clave original en el que se establece. Esta directiva solo se puede aplicar al identificador de clave original. Una vez cerrado el identificador de clave, la clave ya no se puede exportar con fines de archivado. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**NCRYPT \_ IMPL \_ TYPE \_ PROPERTY**
</dt> <dd> <dl> <dt>

L"Impl Type"
</dt> <dt>



DWORD **que** contiene un conjunto de marcas que definen los detalles de implementación del proveedor. Esta propiedad solo se aplica a los proveedores de almacenamiento de claves. Puede contener cero o una combinación de uno o varios de los valores siguientes.



| Identificador                            | Value      | Descripción                                               |
|---------------------------------------|------------|-----------------------------------------------------------|
| **NCRYPT \_ IMPL \_ HARDWARE \_ FLAG**      | 0x00000001 | El proveedor está basado en hardware.                           |
| **MARCA DE \_ SOFTWARE NCRYPT \_ \_ IMPL**      | 0x00000002 | El proveedor está basado en software.                           |
| **MARCA \_ EXTRAÍBLE NCRYPT IMPL \_ \_**     | 0x00000008 | El proveedor es extraíble.                                |
| **NCRYPT \_ IMPL \_ HARDWARE \_ RNG \_ FLAG** | 0x00000010 | El proveedor es un generador de números aleatorios basado en hardware. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**PROPIEDAD DE TIPO \_ DE \_ CLAVE NCRYPT \_**
</dt> <dd> <dl> <dt>

L"Tipo de clave"
</dt> <dt>



DWORD **que** contiene un conjunto de marcas que definen el tipo de clave. Esta propiedad solo se aplica a las claves. Puede contener cero o el siguiente valor.



| Identificador                     | Value      | Descripción                                                                                              |
|--------------------------------|------------|----------------------------------------------------------------------------------------------------------|
| **MARCA DE \_ CLAVE DE \_ MÁQUINA NCRYPT \_** | 0x00000001 | La clave se aplica al equipo local. Si esta marca no está presente, la clave se aplica al usuario actual. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**PROPIEDAD NCRYPT \_ KEY \_ USAGE \_**
</dt> <dd> <dl> <dt>

L"Uso de clave"
</dt> <dt>



DWORD **que** contiene un conjunto de marcas que definen los detalles de uso de una clave. Esta propiedad solo se aplica a las claves. Puede contener cero o una combinación de uno o varios de los valores siguientes.



| Identificador                              | Value      | Descripción                                          |
|-----------------------------------------|------------|------------------------------------------------------|
| **NCRYPT \_ ALLOW \_ DECRYPT \_ FLAG**        | 0x00000001 | La clave se puede usar para el descifrado.                  |
| **NCRYPT \_ ALLOW \_ SIGNING \_ FLAG**        | 0x00000002 | La clave se puede usar para firmar.                     |
| **NCRYPT \_ ALLOW \_ KEY \_ AGREEMENT \_ FLAG** | 0x00000004 | La clave se puede usar para el cifrado del contrato secreto. |
| **NCRYPT \_ PERMITE TODOS LOS \_ \_ USOS**          | 0x00ffffff | La clave se puede usar para cualquier propósito.                 |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**PROPIEDAD NCRYPT \_ LAST \_ MODIFIED \_**
</dt> <dd> <dl> <dt>

L"Modified"
</dt> <dt>



Indica cuándo se modificó la clave por última vez. Este tipo de datos es un puntero a una [**estructura FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) Esta propiedad solo se aplica a las claves persistentes.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**PROPIEDAD NCRYPT \_ \_ LENGTH**
</dt> <dd> <dl> <dt>

L"Length"
</dt> <dt>



DWORD **que** contiene la longitud, en bits, de la clave. Esta propiedad solo se aplica a las claves.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**PROPIEDAD NCRYPT \_ LENGTHS \_**
</dt> <dd> <dl> <dt>

L"Lengths"
</dt> <dt>



Indica los tamaños de clave admitidos por la clave. Este tipo de datos es un puntero a una estructura [**NCRYPT \_ SUPPORTED \_ LENGTHS**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) que contiene esta información. Esta propiedad solo se aplica a las claves.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**PROPIEDAD NCRYPT \_ MAX \_ NAME \_ \_ LENGTH**
</dt> <dd> <dl> <dt>

L"Longitud máxima del nombre"
</dt> <dt>



DWORD **que** contiene la longitud máxima, en caracteres, del nombre de una clave persistente. Esta propiedad solo se aplica a un proveedor.

Esta propiedad está diseñada principalmente para que la usen los proveedores de almacenamiento de claves que almacenan sus claves en un dispositivo que tiene una cantidad limitada de memoria disponible, como una tarjeta inteligente.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**NCRYPT \_ NAME \_ PROPERTY**
</dt> <dd> <dl> <dt>

L"Name"
</dt> <dt>



Puntero a una cadena Unicode terminada en NULL que contiene el nombre del objeto.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**PROPIEDAD DEL \_ SÍMBOLO DEL SISTEMA DE PIN \_ DE NCRYPT \_**
</dt> <dd> <dl> <dt>

L"SmartCardPinPrompt"
</dt> <dt>



Este valor no se admite.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**PROPIEDAD DE PIN de NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"SmartCardPin"
</dt> <dt>



Puntero a una cadena Unicode terminada en NULL que contiene el PIN. El PIN se usa para una clave de tarjeta inteligente o la contraseña de una clave protegida con contraseña almacenada en un KSP basado en software. Esta propiedad solo se puede establecer. Los KSP de Microsoft almacenarán en caché este valor para que solo se solicite al usuario una vez por proceso.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**PROPIEDAD DE \_ IDENTIFICADOR DEL \_ PROVEEDOR NCRYPT \_**
</dt> <dd> <dl> <dt>

L"Provider Handle"
</dt> <dt>



Identificador **de \_ prov de NCRYPT \_** que contiene el identificador del proveedor de almacenamiento de claves CNG. Cuando haya terminado de usar el identificador, debe llamar a [**NCryptFreeObject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) para liberarlo.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**PROPIEDAD LECTOR \_ NCRYPT \_**
</dt> <dd> <dl> <dt>

L"SmartCardReader"
</dt> <dt>



Puntero a una cadena Unicode terminada en NULL que contiene el nombre del lector de tarjetas inteligentes. Esta propiedad solo se puede establecer.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**PROPIEDAD \_ CERTSTORE RAÍZ \_ DE NCRYPT \_**
</dt> <dd> <dl> <dt>

L"SmartcardRootCertStore"
</dt> <dt>



**HCERTSTORE que representa** el almacén de certificados raíz de tarjeta inteligente.


</dt> </dl> </dd> <dt>

<span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span>**NCRYPT \_ Id. de \_ PIN de SCARD \_**
</dt> <dd> <dl> <dt>

L"SmartCardPinId"
</dt> <dt>



Puntero al valor de **identificador \_ de PIN** asociado a una clave [*criptográfica determinada*](/windows/desktop/SecGloss/c-gly) en una tarjeta [*inteligente.*](/windows/desktop/SecGloss/s-gly) Se trata de una propiedad de solo lectura. El **tipo de datos pin \_ ID** se define en Cardmod.h.

**Windows Server 2008 y Windows Vista:** Este valor no se admite.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**NCRYPT \_ SCARD \_ PIN \_ INFO**
</dt> <dd> <dl> <dt>

L"SmartCardPinInfo"
</dt> <dt>



Puntero a la [**estructura DE \_ INFORMACIÓN**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) de PIN del PIN asociado a una clave criptográfica determinada en la tarjeta inteligente. El autor de la llamada proporciona el identificador de clave. Esta propiedad es de solo lectura. La **estructura \_ DE INFORMACIÓN** de PIN se define en Cardmod.h.

**Windows Server 2008 y Windows Vista:** Este valor no se admite.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**NCRYPT \_ SECURE \_ PIN \_ PROPERTY**
</dt> <dd> <dl> <dt>

L"SmartCardSecurePin"
</dt> <dt>



Puntero a una cadena Unicode terminada en NULL que contiene el PIN de sesión de tarjeta inteligente. Esta propiedad solo se puede establecer.

**Windows Vista:** Esta propiedad no se admite.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**NCRYPT \_ SECURITY \_ DESCR \_ PROPERTY**
</dt> <dd> <dl> <dt>

L"Security Descr"
</dt> <dt>



Puntero a una estructura [**\_ DE DESCRIPTOR DE SEGURIDAD**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que contiene información de control de acceso para la clave. Esta propiedad solo se aplica a las claves persistentes. El *parámetro dwFlags* de la función [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) o [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) identifica la parte del descriptor de seguridad que se va a obtener o establecer.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**NCRYPT \_ SECURITY \_ DESCR \_ SUPPORT \_ PROPERTY**
</dt> <dd> <dl> <dt>

L"Security Descr Support"
</dt> <dt>



Indica si el proveedor admite descriptores de seguridad para las claves. Esta propiedad es un **DWORD** que contiene 1 si el proveedor admite descriptores de seguridad para las claves. Si esta propiedad contiene cualquier otro valor o si la función [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) devuelve **NTE \_ NOT \_ SUPPORTED**, el proveedor no admite descriptores de seguridad para las claves. Esta propiedad solo se aplica a los proveedores.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**PROPIEDAD GUID \_ DE TARJETA INTELIGENTE \_ NCRYPT \_**
</dt> <dd> <dl> <dt>

L"SmartCardGuid"
</dt> <dt>



Blob que contiene el identificador de la tarjeta inteligente.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**PROPIEDAD DE DIRECTIVA \_ DE INTERFAZ DE USUARIO \_ NCRYPT \_**
</dt> <dd> <dl> <dt>

L"Directiva de interfaz de usuario"
</dt> <dt>



Si se usa con la función [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) o [**NCryptGetProperty,**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) se trata de un puntero a una estructura directiva de interfaz de usuario [**de NCRYPT \_ \_**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) que contiene la directiva de interfaz de usuario de clave segura para la clave. Esta propiedad solo se aplica a las claves persistentes. Esta propiedad solo se puede establecer cuando se genera la clave. Una vez que se ha llamado a la función [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) para esta clave, esta propiedad pasa a ser de solo lectura.

Un proveedor de almacenamiento de claves puede recibir este parámetro a través de una función de devolución de llamada [**NCryptSetPropertyFn.**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) El valor del parámetro es una estructura blob de directiva de interfaz de usuario de NCRYPT \_ que contiene la misma \_ \_ información. De forma similar, cuando una aplicación realiza una solicitud a través de NCryptSetPropertyFn al proveedor para devolver esta propiedad, se espera que el proveedor devuelva una estructura BLOB de directiva de interfaz de usuario de \_ \_ \_ NCRYPT.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**NCRYPT \_ UNIQUE \_ NAME \_ PROPERTY**
</dt> <dd> <dl> <dt>

L"Nombre único"
</dt> <dt>



Puntero a una cadena Unicode terminada en NULL que contiene el nombre único del objeto. Se trata de un nombre alternativo que se puede usar al acceder a la clave. Esta propiedad se usa cuando se piensa que el nombre de clave que se pasó originalmente a [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) no es lo suficientemente único como para identificar de forma confiable la clave persistente. El proveedor de almacenamiento de claves de Microsoft devolverá el nombre de archivo de la clave como esta propiedad.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**NCRYPT \_ USE \_ CONTEXT \_ PROPERTY**
</dt> <dd> <dl> <dt>

L"Use Context"
</dt> <dt>



Puntero a una cadena Unicode terminada en NULL que describe el contexto de la operación. Esta propiedad no es persistente y se puede establecer en un proveedor o una clave. Una clave no tiene acceso a la propiedad **\_ USE CONTEXT \_ \_ PROPERTY** de NCRYPT del proveedor porque la propiedad solo es específica del identificador para el que se establece.

Un ejemplo en el que esta propiedad se usaría en el contexto de un proveedor es un proveedor de almacenamiento de claves que necesita preguntar al usuario durante una llamada a [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) (por ejemplo, "Insertar la tarjeta inteligente en el lector"). Dado que el identificador de clave no está disponible hasta después de que se devuelva **NCryptOpenKey,** la aplicación debe establecer esta propiedad en el identificador del proveedor antes de llamar a **NCryptOpenKey**.

Un ejemplo en el que esta propiedad se usaría en el contexto de un identificador de clave es un proveedor de almacenamiento de claves que necesita preguntar al usuario durante una operación mediante la clave (por ejemplo, "Esta aplicación necesita usar esta clave para firmar un documento"). A continuación, el proveedor podría retransmitir esta información de contexto al usuario en cualquier interfaz de usuario que se muestra durante la operación.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**PROPIEDAD NCRYPT \_ USE \_ COUNT \_ ENABLED \_**
</dt> <dd> <dl> <dt>

L"Recuento de uso habilitado"
</dt> <dt>



Indica si el proveedor admite el recuento de uso para las claves. Esta propiedad es un **DWORD** que contiene 1 si el proveedor admite el recuento de uso para las claves. Si esta propiedad contiene cualquier otro valor, o si la función [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) devuelve **NTE \_ NOT \_ SUPPORTED**, el proveedor no admite el recuento de uso para las claves. Esta propiedad solo se aplica a los proveedores.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**NCRYPT \_ USE \_ \_ COUNT,PROPIEDAD**
</dt> <dd> <dl> <dt>

L"Use Count"
</dt> <dt>



Variable [**INTEGER \_ de ULARGE**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) que contiene el número de operaciones que ha realizado la [*clave privada*](/windows/desktop/SecGloss/p-gly) especificada. Esta propiedad es opcional y es posible que no sea compatible con todos los proveedores. Los proveedores que admiten esta propiedad en las claves también deben admitir la propiedad **\_ USE COUNT ENABLED \_ \_ \_ PROPERTY** de NCRYPT en el identificador del proveedor. El proveedor de almacenamiento de claves de Microsoft no admite esta propiedad. Esta propiedad solo se aplica a las claves persistentes.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**PROPIEDAD \_ \_ CERTSTORE DE USUARIO NCRYPT \_**
</dt> <dd> <dl> <dt>

L"SmartCardUserCertStore"
</dt> <dt>



**HCERTSTORE que representa** el almacén de certificados de usuario de tarjeta inteligente.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**PROPIEDAD DE VERSIÓN DE NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"Version"
</dt> <dt>



DWORD **que** contiene la versión de software del proveedor. La palabra alta contiene la versión principal y la palabra baja contiene la versión secundaria. Por ejemplo, 0x00030033 = 3,51. Esta propiedad solo se aplica a los proveedores.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**PROPIEDAD DE IDENTIFICADOR \_ DE VENTANA \_ NCRYPT \_**
</dt> <dd> <dl> <dt>

L"HWND Handle"
</dt> <dt>



Puntero al identificador de ventana **(HWND)** que se usará como elemento primario de cualquier interfaz de usuario que se muestre.

Dado que puede producirse un comportamiento no deseado cuando se muestra una interfaz de usuario mediante un identificador de ventana **NULL** para el elemento primario, se recomienda encarecidamente que un proveedor de almacenamiento de claves no muestre una interfaz de usuario a menos que se establezca esta propiedad.


</dt> </dl> </dd> </dl>

Los siguientes valores se usan para definir límites de datos de propiedad.



| Constante o valor                                                                                                                                                                                                                                                 | Descripción                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="NCRYPT_MAX_PROPERTY_DATA"></span><span id="ncrypt_max_property_data"></span><dl> <dt>**NCRYPT \_ MAX \_ PROPERTY \_ DATA**</dt> <dt>0x100000</dt> </dl> | Especifica el tamaño máximo de un valor de propiedad, en bytes.<br/>     |
| <span id="NCRYPT_MAX_PROPERTY_NAME"></span><span id="ncrypt_max_property_name"></span><dl> <dt>**NCRYPT \_ NOMBRE \_ MÁXIMO \_ DE PROPIEDAD**</dt> <dt>64</dt> </dl>       | Especifica el tamaño máximo de un nombre de propiedad, en caracteres.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Ncrypt.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty)
</dt> <dt>

[**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)
</dt> </dl>

 


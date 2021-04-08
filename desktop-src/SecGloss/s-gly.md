---
description: Contiene definiciones de términos de seguridad que comienzan por la letra S.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3e9d7672-2314-45c8-8178-5a0afcfd0c50
title: S (Glosario de seguridad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975df9e3638f12ba7f3766d6119685fba1fa599b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002339"
---
# <a name="s-security-glossary"></a>S (Glosario de seguridad)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [o](o-gly.md) [p](p-gly.md) Q [R](r-gly.md) s [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_s_mime_gly"></span><span id="_SECURITY_S_MIME_GLY"></span>**S/MIME**
</dt> <dd>

Consulte *extensiones seguras multipropósito de correo de Internet*.

</dd> <dt>

<span id="_security_sacl_gly"></span><span id="_SECURITY_SACL_GLY"></span>**SACL**
</dt> <dd>

Vea *lista de control de acceso del sistema*.

</dd> <dt>

<span id="_security_salt_value_gly"></span><span id="_SECURITY_SALT_VALUE_GLY"></span>**valor Salt**
</dt> <dd>

Datos aleatorios que a veces se incluyen como parte de una clave de sesión. Cuando se agregan a una clave de sesión, los datos de sal de texto sin formato se colocan delante de los datos de clave cifrada. Los valores Salt se agregan para aumentar el trabajo necesario para montar un ataque por fuerza bruta (diccionario) en los datos cifrados con un cifrado de clave simétrica. Los valores Salt se generan mediante una llamada a **CryptGenRandom**.

</dd> <dt>

<span id="_security_sam_gly"></span><span id="_SECURITY_SAM_GLY"></span>**Juan**
</dt> <dd>

Consulte *Administrador de cuentas de seguridad*.

</dd> <dt>

<span id="_security_sanitized_name_gly"></span><span id="_SECURITY_SANITIZED_NAME_GLY"></span>**nombre saneado**
</dt> <dd>

Forma de un nombre de entidad de certificación (CA) que se usa en los nombres de archivo (por ejemplo, para una [*lista de revocación de certificados*](c-gly.md)) y en las claves del registro. El proceso de sanear el nombre de la entidad de certificación es necesario para quitar los caracteres que no son válidos para los nombres de archivo, los nombres de clave del registro o los valores de nombre distintivo, o que no son válidos para razones específicas de la tecnología. En servicios de Certificate Server, el proceso de limpieza convierte cualquier carácter no válido en el nombre común de la CA en una representación de 5 caracteres en el formato **.** _xxxx_, donde **.** se utiliza como carácter de escape y *xxxx* representa cuatro enteros hexadecimales que identifican de forma única el carácter que se va a convertir.

</dd> <dt>

<span id="security.s_1_gly"></span><span id="SECURITY.S_1_GLY"></span>**ASOCIACIONES**
</dt> <dd>

Consulte *secuencia de atención de seguridad*.

</dd> <dt>

<span id="_security_scard_defaultreaders_gly"></span><span id="_SECURITY_SCARD_DEFAULTREADERS_GLY"></span>**PPAC $ DefaultReaders**
</dt> <dd>

Sin embargo, un grupo de lectores de Terminal Server que contenga todos los lectores asignados a ese terminal no está reservado para este uso específico.

</dd> <dt>

<span id="_security_scard_allreaders_gly"></span><span id="_SECURITY_SCARD_ALLREADERS_GLY"></span>**PPAC $ AllReaders**
</dt> <dd>

Un grupo de lectores del sistema de tarjetas inteligentes que incluye todos los lectores introducidos en el administrador de recursos de tarjeta inteligente. Los lectores se agregan automáticamente al grupo cuando se introducen en el sistema.

</dd> <dt>

<span id="_security_scard_autoallocate_gly"></span><span id="_SECURITY_SCARD_AUTOALLOCATE_GLY"></span>**\_asignación AUTOasignada**
</dt> <dd>

Constante del sistema de tarjeta inteligente que indica al administrador de recursos de tarjeta inteligente que asigne suficiente memoria, devolviendo un puntero al búfer asignado en lugar de rellenar un búfer proporcionado por el usuario. El búfer devuelto se debe liberar finalmente llamando a **SCardFreeMemory**.

</dd> <dt>

<span id="_security_scep_gly"></span><span id="_SECURITY_SCEP_GLY"></span>**SCEP**
</dt> <dd>

Consulte *Protocolo de inscripción de certificados simple*

</dd> <dt>

<span id="_security_schannel_gly"></span><span id="_SECURITY_SCHANNEL_GLY"></span>**Schannel**
</dt> <dd>

Paquete de seguridad que proporciona autenticación entre clientes y servidores.

</dd> <dt>

<span id="_security_secure_attention_sequence_gly"></span><span id="_SECURITY_SECURE_ATTENTION_SEQUENCE_GLY"></span>**secuencia de atención segura**
</dt> <dd>

ASOCIACIONES Una secuencia de teclas que inicia el proceso de inicio o apagado de sesión. La secuencia predeterminada es CTRL + ALT + SUPR.

</dd> <dt>

<span id="_security_secure_electronic_transaction_gly"></span><span id="_SECURITY_SECURE_ELECTRONIC_TRANSACTION_GLY"></span>**Transacción electrónica segura**
</dt> <dd>

CONJUNTO Un protocolo para proteger las transacciones electrónicas a través de Internet.

</dd> <dt>

<span id="_security_secure_hash_algorithm_gly"></span><span id="_SECURITY_SECURE_HASH_ALGORITHM_GLY"></span>**Algoritmo hash seguro**
</dt> <dd>

Sha Algoritmo hash que genera una síntesis del mensaje. SHA se utiliza con el Algoritmo de firma digital (DSA) en el Estándar de firmas digitales (DSS), entre otros. CryptoAPI hace referencia a este algoritmo mediante el identificador del algoritmo (CALG \_ SHA), el nombre (SHA) y la clase ( \_ hash de clase alg \_ ). Hay cuatro variedades de SHA: SHA-1, SHA-256, SHA-384 y SHA-512. SHA-1 genera una síntesis del mensaje de 160 bits. SHA-256, SHA-384 y SHA-512 generan síntesis de mensajes de 256, 384 y 512 bits, respectivamente. SHA fue desarrollado por el National Institute of Standards and Technology (NIST, Instituto nacional de estándares y tecnología) y la National Security Agency (NSA, Agencia de seguridad nacional).

</dd> <dt>

<span id="_security_secure_hash_standard_gly"></span><span id="_SECURITY_SECURE_HASH_STANDARD_GLY"></span>**Estándar de hash seguro**
</dt> <dd>

Estándar diseñado por NIST y NSA. Este estándar define el algoritmo hash seguro (SHA-1) para su uso con el estándar de firma digital (DSS).

Vea también *algoritmo hash seguro*.

</dd> <dt>

<span id="_security_secure_sockets_layer_protocol_gly"></span><span id="_SECURITY_SECURE_SOCKETS_LAYER_PROTOCOL_GLY"></span>**Protocolo Capa de sockets seguros**
</dt> <dd>

SSL Un protocolo para proteger las comunicaciones de red mediante una combinación de tecnología de clave pública y secreta.

</dd> <dt>

<span id="_security_secure_multipurpose_internet_mail_extensions_gly"></span><span id="_SECURITY_SECURE_MULTIPURPOSE_INTERNET_MAIL_EXTENSIONS_GLY"></span>**Extensiones seguras multipropósito de correo Internet**
</dt> <dd>

(S/MIME) Estándar de seguridad de correo electrónico que usa el cifrado de clave pública.

</dd> <dt>

<span id="_security_security_accounts_manager_gly"></span><span id="_SECURITY_SECURITY_ACCOUNTS_MANAGER_GLY"></span>**Administrador de cuentas de seguridad**
</dt> <dd>

Juan Un servicio de Windows que se usa durante el proceso de inicio de sesión. SAM mantiene la información de cuenta de usuario, incluidos los grupos a los que un usuario pertenece.

</dd> <dt>

<span id="_security_security_context_gly"></span><span id="_SECURITY_SECURITY_CONTEXT_GLY"></span>**contexto de seguridad**
</dt> <dd>

Las reglas o atributos de seguridad que están en vigor actualmente. Por ejemplo, el usuario actual con sesión iniciada en el equipo o el número de identificación personal escrito por el usuario de tarjeta inteligente. Para SSPI, un contexto de seguridad es una estructura de datos opaca que contiene datos de seguridad pertinentes a una conexión, como una clave de sesión o una indicación de la duración de la sesión.

</dd> <dt>

<span id="_security_security_descriptor_gly"></span><span id="_SECURITY_SECURITY_DESCRIPTOR_GLY"></span>**descriptor de seguridad**
</dt> <dd>

Estructura y datos asociados que contienen la información de seguridad para un objeto protegible. Un descriptor de seguridad identifica el propietario y el grupo primario del objeto. También puede contener una DACL que controla el acceso al objeto y una SACL que controla el registro de intentos de acceso al objeto.

Vea también [*descriptor de seguridad absoluto*](a-gly.md), [*lista de control de acceso discrecional*](d-gly.md), *descriptor de seguridad autorelativo*, *lista de control de acceso del sistema*.

</dd> <dt>

<span id="_security_security_identifier_gly"></span><span id="_SECURITY_SECURITY_IDENTIFIER_GLY"></span>**identificador de seguridad**
</dt> <dd>

Junction Estructura de datos de longitud variable que identifica las cuentas de usuario, de grupo y de equipo. A cada cuenta de la red se le asigna un SID único cuando se crea por primera vez. Los procesos internos de Windows hacen referencia al SID de una cuenta en lugar del nombre de usuario o grupo de la cuenta.

</dd> <dt>

<span id="_security_security_package_gly"></span><span id="_SECURITY_SECURITY_PACKAGE_GLY"></span>**paquete de seguridad**
</dt> <dd>

La implementación de software de un protocolo de seguridad. Los paquetes de seguridad están incluidos en los archivos DLL del proveedor de compatibilidad para seguridad o en el proveedor de compatibilidad de seguridad o el paquete de autenticación.

</dd> <dt>

<span id="_security_security_protocol_gly"></span><span id="_SECURITY_SECURITY_PROTOCOL_GLY"></span>**Protocolo de seguridad**
</dt> <dd>

Especificación que define los objetos de datos relacionados con la seguridad y las reglas sobre cómo se utilizan los objetos para mantener la seguridad en un sistema informático.

</dd> <dt>

<span id="_security_security_principal_gly"></span><span id="_SECURITY_SECURITY_PRINCIPAL_GLY"></span>**entidad de seguridad**
</dt> <dd>

Una entidad reconocida por el sistema de seguridad. Las entidades de seguridad pueden incluir usuarios humanos así como procesos autónomos.

</dd> <dt>

<span id="_security_security_support_provider_gly"></span><span id="_SECURITY_SECURITY_SUPPORT_PROVIDER_GLY"></span>**proveedor de compatibilidad para seguridad**
</dt> <dd>

Marcos Biblioteca de vínculos dinámicos (DLL) que implementa la SSPI haciendo que uno o varios paquetes de seguridad estén disponibles para las aplicaciones. Cada paquete de seguridad proporciona asignaciones entre las llamadas de funciones de SSPI de una aplicación y las funciones de un modelo de seguridad real. Los paquetes de seguridad admiten protocolos de seguridad como la autenticación Kerberos y el administrador de LAN de Microsoft.

</dd> <dt>

<span id="_security_security_support_provider_interface_gly"></span><span id="_SECURITY_SECURITY_SUPPORT_PROVIDER_INTERFACE_GLY"></span>**Interfaz del proveedor de compatibilidad con seguridad**
</dt> <dd>

SSPI Interfaz común entre las aplicaciones de nivel de transporte, como la llamada a procedimiento remoto (RPC) de Microsoft, y los proveedores de seguridad, como la seguridad distribuida de Windows. SSPI permite a una aplicación de transporte llamar a uno de varios proveedores de seguridad para obtener una conexión autenticada. Estas llamadas no requieren un conocimiento extenso de los detalles del protocolo de seguridad.

</dd> <dt>

<span id="_security_self_relative_security_descriptor_gly"></span><span id="_SECURITY_SELF_RELATIVE_SECURITY_DESCRIPTOR_GLY"></span>**descriptor de seguridad autorelativo**
</dt> <dd>

Descriptor de seguridad que almacena toda su información de seguridad en un bloque de memoria contiguo.

Vea también *descriptor de seguridad*.

</dd> <dt>

<span id="_security_serialize_gly"></span><span id="_SECURITY_SERIALIZE_GLY"></span>**serializar**
</dt> <dd>

Proceso de conversión de datos en una cadena de unos y ceros para que se pueda transmitir en serie. La codificación forma parte de este proceso.

</dd> <dt>

<span id="_security_serialized_certificate_store_format_gly"></span><span id="_SECURITY_SERIALIZED_CERTIFICATE_STORE_FORMAT_GLY"></span>**Formato del almacén de certificados serializado**
</dt> <dd>

SST El formato del almacén de certificados serializado es el único formato que conserva todas las propiedades del almacén de certificados. Resulta útil en casos como cuando las raíces se han configurado con propiedades EKU personalizadas y desea moverlas a otro equipo.

</dd> <dt>

<span id="_security_server_gly"></span><span id="_SECURITY_SERVER_GLY"></span>**servidor**
</dt> <dd>

Equipo que responde a los comandos de un equipo cliente. El cliente y el servidor trabajan juntos para realizar la funcionalidad de la aplicación distributivo.

Vea también [*cliente*](c-gly.md).

</dd> <dt>

<span id="_security_server_certificate_gly"></span><span id="_SECURITY_SERVER_CERTIFICATE_GLY"></span>**certificado de servidor**
</dt> <dd>

Hace referencia a un certificado utilizado para la autenticación de servidor, como la autenticación de un servidor Web en un explorador Web. Cuando un cliente del explorador Web intenta obtener acceso a un servidor Web seguro, el servidor envía su certificado al explorador para permitirle comprobar la identidad del servidor.

</dd> <dt>

<span id="_security_server_gated_cryptography_gly"></span><span id="_SECURITY_SERVER_GATED_CRYPTOGRAPHY_GLY"></span>**Criptografía controlada por servidor**
</dt> <dd>

SGC Extensión de *capa de sockets seguros* (SSL) que permite a las organizaciones, como las instituciones financieras, que tienen versiones de exportación de Internet Information Services (IIS) usar cifrado seguro (por ejemplo, cifrado de 128 bits).

</dd> <dt>

<span id="_security_service_principal_name_gly"></span><span id="_SECURITY_SERVICE_PRINCIPAL_NAME_GLY"></span>**nombre de entidad de seguridad de servicio**
</dt> <dd>

SPN Nombre por el que un cliente identifica de forma única una instancia de un servicio. Si instala varias instancias de un servicio en equipos a lo largo de un bosque, cada instancia debe tener su propio SPN. Una instancia de servicio determinada puede tener varios SPN si hay varios nombres que los clientes pueden usar para la autenticación.

</dd> <dt>

<span id="_security_service_provider_smart_card__gly"></span><span id="_SECURITY_SERVICE_PROVIDER_SMART_CARD__GLY"></span>**proveedor de servicios (tarjeta inteligente)**
</dt> <dd>

Componente de subsistema de tarjeta inteligente que proporciona acceso a servicios de tarjeta inteligente específicos mediante interfaces COM.

Vea también [*proveedor de servicios principal*](p-gly.md).

</dd> <dt>

<span id="_security_session_gly"></span><span id="_SECURITY_SESSION_GLY"></span>**sesión**
</dt> <dd>

Un intercambio de mensajes bajo la protección de una única parte de material para claves. Por ejemplo, las sesiones SSL utilizan una clave única para devolver varios mensajes hacia delante y hacia detrás bajo esa clave.

</dd> <dt>

<span id="_security_session_key_gly"></span><span id="_SECURITY_SESSION_KEY_GLY"></span>**clave de sesión**
</dt> <dd>

Una clave criptográfica relativamente corta, a menudo negociada por un cliente y un servidor basados en un secreto compartido. La duración de una clave de sesión está limitada por la sesión a la que está asociada. Una clave de sesión debe ser lo suficientemente segura como para resistir Cryptanalysis para la duración de la sesión. Cuando se transmiten las claves de sesión, generalmente están protegidas con claves de intercambio de claves (que suelen ser claves asimétricas) para que solo el destinatario previsto pueda acceder a ellas. Las claves de sesión se pueden derivar de valores hash mediante una llamada a la función **CryptDeriveKey** .

</dd> <dt>

<span id="_security_session_key_derivation_scheme_gly"></span><span id="_SECURITY_SESSION_KEY_DERIVATION_SCHEME_GLY"></span>**esquema de derivación de claves de sesión**
</dt> <dd>

Especifica cuándo se deriva una clave de un hash. Los métodos que se usan dependen del tipo de CSP.

</dd> <dt>

<span id="_security_set_gly"></span><span id="_SECURITY_SET_GLY"></span>**CONJUNTO**
</dt> <dd>

Consulte *transacción electrónica segura*.

</dd> <dt>

<span id="_security_sha_gly"></span><span id="_SECURITY_SHA_GLY"></span>**SHA**
</dt> <dd>

El nombre de CryptoAPI para el algoritmo hash seguro, SHA-1. Otros algoritmos hash incluyen [*MD2*](m-gly.md), [*MD4*](m-gly.md)y [*MD5*](m-gly.md).

Vea también *algoritmo hash seguro*.

</dd> <dt>

<span id="_security_shs_gly"></span><span id="_SECURITY_SHS_GLY"></span>**SHS**
</dt> <dd>

Consulte *Secure hash Standard*.

</dd> <dt>

<span id="_security_sid_gly"></span><span id="_SECURITY_SID_GLY"></span>**Junction**
</dt> <dd>

Consulte *identificador de seguridad*.

</dd> <dt>

<span id="_security_signature_and_data_verification_functions_gly"></span><span id="_SECURITY_SIGNATURE_AND_DATA_VERIFICATION_FUNCTIONS_GLY"></span>**funciones de firma y comprobación de datos**
</dt> <dd>

Funciones de mensaje simplificadas utilizadas para firmar los mensajes salientes y comprobar la autenticidad de las firmas aplicadas en los mensajes recibidos y los datos relacionados.

Consulte *funciones de mensaje simplificadas*.

</dd> <dt>

<span id="_security_signature_certificate_gly"></span><span id="_SECURITY_SIGNATURE_CERTIFICATE_GLY"></span>**certificado de firma**
</dt> <dd>

Un certificado que contiene una clave pública que se utiliza para comprobar las firmas digitales.

</dd> <dt>

<span id="_security_signature_file_gly"></span><span id="_SECURITY_SIGNATURE_FILE_GLY"></span>**archivo de Signatura**
</dt> <dd>

Archivo que contiene la firma de un proveedor de [*servicios criptográficos*](c-gly.md) (CSP) determinado. El archivo de signatura es necesario para asegurarse de que CryptoAPI reconoce el CSP. CryptoAPI valida esta firma periódicamente para asegurarse de que el CSP no se ha manipulado.

</dd> <dt>

<span id="_security_signature_functions_gly"></span><span id="_SECURITY_SIGNATURE_FUNCTIONS_GLY"></span>**funciones de firma**
</dt> <dd>

Funciones utilizadas para crear y comprobar firmas digitales.

Vea también *funciones de mensaje simplificadas*.

</dd> <dt>

<span id="_security_signature_key_pair_gly"></span><span id="_SECURITY_SIGNATURE_KEY_PAIR_GLY"></span>**par de claves de firma**
</dt> <dd>

Par de claves pública y privada que se usa para autenticar mensajes (firma digital). Los pares de claves de firma se crean mediante una llamada a **CryptGenKey**.

Vea también [*par de claves de Exchange*](e-gly.md).

</dd> <dt>

<span id="_security_signature_private_key_gly"></span><span id="_SECURITY_SIGNATURE_PRIVATE_KEY_GLY"></span>**clave privada de firma**
</dt> <dd>

La clave privada de un par de claves de firma.

Vea *par de claves de firma*.

</dd> <dt>

<span id="_security_signed_and_enveloped_data_gly"></span><span id="_SECURITY_SIGNED_AND_ENVELOPED_DATA_GLY"></span>**datos con signo y con doble cifrado**
</dt> <dd>

Un tipo de contenido de datos definido por PKCS \# 7. Este tipo de datos consta de contenido cifrado de cualquier tipo, claves cifradas de cifrado de contenido para uno o más destinatarios y hashes de mensaje de doble cifrado para uno o más firmantes. El cifrado doble consta de un cifrado con la clave privada de un firmante seguido de un cifrado con la clave de cifrado de contenido.

</dd> <dt>

<span id="_security_signed_data_gly"></span><span id="_SECURITY_SIGNED_DATA_GLY"></span>**datos firmados**
</dt> <dd>

Un tipo de contenido de datos definido por PKCS \# 7. Este tipo de datos consta de cualquier tipo de contenido y hashes de mensajes cifrados (resúmenes) del contenido para cero o más firmantes. Los valores hash resultantes se pueden usar para confirmar quién firmó el mensaje. Estos valores hash también confirman que el mensaje original no se ha modificado desde que se firmó el mensaje.

</dd> <dt>

<span id="_security_simple_certificate_enrollment_protocol_gly"></span><span id="_SECURITY_SIMPLE_CERTIFICATE_ENROLLMENT_PROTOCOL_GLY"></span>**Protocolo de inscripción de certificados simple**
</dt> <dd>

SCEP Acrónimo que representa Protocolo de inscripción de certificados simple. El protocolo es actualmente un borrador estándar de Internet que define la comunicación entre los dispositivos de red y una autoridad de registro (RA) para la inscripción de certificados. Para obtener más información, consulte las notas [del producto de implementación de Microsoft SCEP](https://www.scribd.com/document/31941679/Microsoft-SCEP-Implementation-Whitepaper).

</dd> <dt>

<span id="_security_simple_key_blob_gly"></span><span id="_SECURITY_SIMPLE_KEY_BLOB_GLY"></span>**BLOB de clave simple**
</dt> <dd>

Una clave de sesión cifrada con la clave pública de intercambio de claves del usuario de destino. Este tipo de BLOB de clave se usa al almacenar una clave de sesión o al transmitir una clave de sesión a otro usuario. Un BLOB de clave se crea llamando a **CryptExportKey**.

</dd> <dt>

<span id="_security_simplified_message_functions_gly"></span><span id="_SECURITY_SIMPLIFIED_MESSAGE_FUNCTIONS_GLY"></span>**funciones de mensaje simplificadas**
</dt> <dd>

Funciones de administración de mensajes, como el cifrado de mensajes, el descifrado, la firma y las funciones de comprobación de firmas. Las funciones de mensaje simplificado funcionan en un nivel superior al de las funciones criptográficas base o las funciones de mensaje de bajo nivel. Las funciones de mensaje simplificadas incluyen varias de las funciones criptográficas de nivel de datos y de cifrado base, y las funciones de certificado en una sola función que realiza una tarea específica de una forma específica, como el cifrado de un \# mensaje PKCS 7 o la firma de un mensaje.

Vea también [*funciones de mensaje de bajo nivel*](l-gly.md).

</dd> <dt>

<span id="_security_single_sign_on_gly"></span><span id="_SECURITY_SINGLE_SIGN_ON_GLY"></span>**Inicio de sesión único**
</dt> <dd>

SSO La capacidad de vincular un cuenta Microsoft (como una cuenta de Microsoft Outlook.com) con una cuenta local para que un inicio de sesión permita al usuario usar otras aplicaciones que admiten el inicio de sesión con sus cuenta Microsoft.

</dd> <dt>

<span id="_security_sip_gly"></span><span id="_SECURITY_SIP_GLY"></span>**SIP**
</dt> <dd>

Vea *paquete* de la interfaz de asunto.

</dd> <dt>

<span id="_security_site_certificate_gly"></span><span id="_SECURITY_SITE_CERTIFICATE_GLY"></span>**certificado de sitio**
</dt> <dd>

Los certificados de servidor y los certificados de [*entidad de certificación*](c-gly.md) (CA) a veces se denominan certificados de sitio. Al hacer referencia a un certificado de servidor, el certificado identifica el servidor Web que presenta el certificado. Cuando se hace referencia a un certificado de CA, el certificado identifica la CA que emite certificados de autenticación de cliente y servidor a los servidores y clientes que solicitan estos certificados.

</dd> <dt>

<span id="_security_skipjack_gly"></span><span id="_SECURITY_SKIPJACK_GLY"></span>**Skipjack**
</dt> <dd>

Algoritmo de cifrado especificado como parte del conjunto de cifrado Fortezza. Skipjack es un cifrado simétrico con una longitud de clave fija de 80 bits. Skipjack es un algoritmo clasificado creado por el Estados Unidos Agencia de seguridad nacional (NSA). Los detalles técnicos del algoritmo Skipjack son secretos.

</dd> <dt>

<span id="_security_smart_card_gly"></span><span id="_SECURITY_SMART_CARD_GLY"></span>**tarjeta inteligente**
</dt> <dd>

Tarjeta de circuito integrado (ICC) propiedad de una persona o un grupo cuya información debe estar protegida según las asignaciones de propiedad específicas. Proporciona su propio control de acceso físico. sin el subsistema de tarjeta inteligente que coloca el control de acceso adicional en la tarjeta inteligente. Una tarjeta inteligente es una tarjeta plástica que contiene un circuito integrado compatible con ISO 7816.

</dd> <dt>

<span id="_security_smart_card_common_dialog_gly"></span><span id="_SECURITY_SMART_CARD_COMMON_DIALOG_GLY"></span>**cuadro de diálogo común de tarjeta inteligente**
</dt> <dd>

Cuadro de diálogo común que ayuda al usuario a seleccionar y ubicar una tarjeta inteligente. Funciona con los servicios de lectura y los servicios de administración de bases de datos de tarjeta inteligente para ayudar a la aplicación y, si es necesario, al usuario, para identificar la tarjeta inteligente que se va a usar para un fin determinado.

</dd> <dt>

<span id="_security_smart_card_database_gly"></span><span id="_SECURITY_SMART_CARD_DATABASE_GLY"></span>**base de datos de tarjeta inteligente**
</dt> <dd>

La base de datos utilizada por el administrador de recursos para administrar los recursos. Contiene una lista de tarjetas inteligentes conocidas, las interfaces y el proveedor de servicios principal de cada tarjeta, y lectores de tarjetas inteligentes conocidos y grupos de lector.

</dd> <dt>

<span id="_security_smart_card_subsystem_gly"></span><span id="_SECURITY_SMART_CARD_SUBSYSTEM_GLY"></span>**subsistema de tarjeta inteligente**
</dt> <dd>

El subsistema utilizado para proporcionar un vínculo entre los lectores de tarjetas inteligentes y las aplicaciones basadas en tarjetas inteligentes.

</dd> <dt>

<span id="_security_software_publisher_certificate_gly"></span><span id="_SECURITY_SOFTWARE_PUBLISHER_CERTIFICATE_GLY"></span>**Certificado de editor de software**
</dt> <dd>

SPC Un \# objeto de datos con signo PKCS 7 que contiene los certificados X. 509.

</dd> <dt>

<span id="_security_spc_gly"></span><span id="_SECURITY_SPC_GLY"></span>**SPC**
</dt> <dd>

Consulte *certificado de editor de software*.

</dd> <dt>

<span id="_security_spn_gly"></span><span id="_SECURITY_SPN_GLY"></span>**SPN**
</dt> <dd>

Consulte *nombre de entidad* de seguridad de servicio.

</dd> <dt>

<span id="_security_ssl_gly"></span><span id="_SECURITY_SSL_GLY"></span>**SSL**
</dt> <dd>

Consulte *Protocolo de capa de sockets seguros*.

</dd> <dt>

<span id="_security_ssl3_client_authentication_algorithm_gly"></span><span id="_SECURITY_SSL3_CLIENT_AUTHENTICATION_ALGORITHM_GLY"></span>**Algoritmo de autenticación del cliente de SSL3**
</dt> <dd>

Algoritmo usado para la autenticación de cliente en Capa de sockets seguros (SSL) versión 3. En el protocolo SSL3, una concatenación de un hash MD5 y un hash SHA-1 se firman con una clave privada RSA. CryptoAPI y los proveedores de servicios criptográficos mejorados y base de Microsoft admiten SSL3 con el tipo de hash CALG \_ SSL3 \_ SHAMD5.

</dd> <dt>

<span id="_security_ssl3_protocol_gly"></span><span id="_SECURITY_SSL3_PROTOCOL_GLY"></span>**Protocolo SSL3**
</dt> <dd>

Versión 3 del protocolo Capa de sockets seguros (SSL).

</dd> <dt>

<span id="_security_sso_gly"></span><span id="_SECURITY_SSO_GLY"></span>**SSO**
</dt> <dd>

Consulte *Inicio de sesión único*.

</dd> <dt>

<span id="_security_ssp_gly"></span><span id="_SECURITY_SSP_GLY"></span>**Marcos**
</dt> <dd>

Consulte *proveedor de compatibilidad con seguridad*.

</dd> <dt>

<span id="_security_sspi_gly"></span><span id="_SECURITY_SSPI_GLY"></span>**SSPI**
</dt> <dd>

Vea *interfaz del proveedor de compatibilidad con seguridad*.

</dd> <dt>

<span id="_security_sst_gly"></span><span id="_SECURITY_SST_GLY"></span>**SST**
</dt> <dd>

Consulte *formato de almacén de certificados serializado*.

</dd> <dt>

<span id="_security_state_gly"></span><span id="_SECURITY_STATE_GLY"></span>**State**
</dt> <dd>

Conjunto de todos los valores persistentes asociados a una entidad criptográfica como una clave o un valor hash. Este conjunto puede incluir elementos como el [*Vector de inicialización*](i-gly.md) (IV) que se está usando, el algoritmo que se está usando o el valor de la entidad ya calculado.

</dd> <dt>

<span id="_security_stream_cipher_gly"></span><span id="_SECURITY_STREAM_CIPHER_GLY"></span>**cifrado de secuencias**
</dt> <dd>

Cifrado que cifra los datos en serie, de un bit a la vez.

Vea también [*cifrado de bloques*](b-gly.md).

</dd> <dt>

<span id="_security_subauthentication_package_gly"></span><span id="_SECURITY_SUBAUTHENTICATION_PACKAGE_GLY"></span>**paquete de subautenticación**
</dt> <dd>

DLL opcional que proporciona funcionalidad de autenticación adicional, normalmente mediante la extensión del algoritmo de autenticación. Si se instala un paquete de subautenticación, el paquete de autenticación llamará al paquete de subautenticación antes de devolver su resultado de autenticación a la autoridad de seguridad local (LSA).

Consulte también [*autoridad de seguridad local*](l-gly.md).

</dd> <dt>

<span id="_security_subject_interface_package_gly"></span><span id="_SECURITY_SUBJECT_INTERFACE_PACKAGE_GLY"></span>**paquete de interfaz de asunto**
</dt> <dd>

SIP Una especificación de propiedad de Microsoft para una capa de software que permite a las aplicaciones crear, almacenar, recuperar y comprobar una firma de asunto. Los temas incluyen, entre otros, imágenes ejecutables portables (. exe), imágenes de contenedor (. cab), archivos planos y archivos de catálogo. Cada tipo de asunto usa un subconjunto diferente de sus datos para el cálculo de hash y requiere un procedimiento diferente para el almacenamiento y la recuperación. Por lo tanto, cada tipo de asunto tiene una especificación de paquete de interfaz de asunto única.

</dd> <dt>

<span id="_security_suite_b_gly"></span><span id="_SECURITY_SUITE_B_GLY"></span>**Suite B**
</dt> <dd>

Un conjunto de algoritmos criptográficos que ha declarado la Agencia de seguridad nacional de EE. UU. como parte de su programa de modernización criptográfica.

</dd> <dt>

<span id="_security_supplemental_credentials_gly"></span><span id="_SECURITY_SUPPLEMENTAL_CREDENTIALS_GLY"></span>**credenciales adicionales**
</dt> <dd>

Credenciales que se usan para autenticar una *entidad de seguridad* en dominios de seguridad externos.

Vea también [*credenciales principales*](p-gly.md).

</dd> <dt>

<span id="_security_symmetric_algorithm_gly"></span><span id="_SECURITY_SYMMETRIC_ALGORITHM_GLY"></span>**algoritmo simétrico**
</dt> <dd>

Un algoritmo criptográfico que normalmente usa una clave única, a la que se suele hacer referencia como clave de sesión, para el cifrado y el descifrado. Los algoritmos simétricos se pueden dividir en dos categorías, algoritmos de secuencia y algoritmos de bloque (también denominados [*cifrados*](b-gly.md)de *flujo* y de bloque).

</dd> <dt>

<span id="_security_symmetric_encryption_gly"></span><span id="_SECURITY_SYMMETRIC_ENCRYPTION_GLY"></span>**cifrado simétrico**
</dt> <dd>

Cifrado que utiliza una clave única tanto para el cifrado como para el descifrado. Se prefiere el cifrado simétrico si se van a cifrar cantidades grandes de datos. Algunos de los algoritmos de cifrado simétrico más comunes son [*RC2*](r-gly.md), [*RC4*](r-gly.md)y [*estándar de cifrado de datos*](d-gly.md) (des).

Vea también [*cifrado de clave pública*](p-gly.md).

</dd> <dt>

<span id="_security_symmetric_key_gly"></span><span id="_SECURITY_SYMMETRIC_KEY_GLY"></span>**clave simétrica**
</dt> <dd>

Clave secreta que se usa con un algoritmo criptográfico simétrico (es decir, un algoritmo que utiliza la misma clave para el cifrado y el descifrado). Este tipo de clave debe ser conocido para todas las partes que se comunican.

</dd> <dt>

<span id="_security_system_access_control_list_gly"></span><span id="_SECURITY_SYSTEM_ACCESS_CONTROL_LIST_GLY"></span>**lista de control de acceso del sistema**
</dt> <dd>

SACL ACL que controla la generación de mensajes de auditoría para los intentos de acceso a un objeto protegible. La capacidad de obtener o establecer la SACL de un objeto se controla mediante un privilegio que normalmente solo mantienen los administradores del sistema.

Vea también [*lista de control de acceso*](a-gly.md), [*lista de control de acceso discrecional*](d-gly.md), [*privilegio*](p-gly.md).

</dd> <dt>

<span id="_security_system_program_interface_gly"></span><span id="_SECURITY_SYSTEM_PROGRAM_INTERFACE_GLY"></span>**interfaz del programa del sistema**
</dt> <dd>

Conjunto de funciones proporcionadas por un [*proveedor de servicios criptográficos*](c-gly.md) (CSP) que implementa las funciones de una aplicación.

</dd> </dl>

 

 




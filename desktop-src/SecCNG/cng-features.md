---
description: CNG tiene las siguientes características.
ms.assetid: 400a2b6e-6bbe-4ba4-abde-a2f625007517
title: Características de CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df40606a255adc90bd36540571979c1c34579611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666261"
---
# <a name="cng-features"></a>Características de CNG

CNG tiene las siguientes características.

-   [Agilidad criptográfica](#cryptographic-agility)
-   [Certificación y cumplimiento](#certification-and-compliance)
-   [Compatibilidad con Suite B](#suite-b-support)
-   [Compatibilidad heredada](#legacy-support)
-   [Compatibilidad con el modo kernel](#kernel-mode-support)
-   [Auditoría](#auditing)
-   [Generadores de números aleatorios reemplazables](#replaceable-random-number-generators)
-   [Seguridad para subprocesos](#thread-safety)
-   [Modo de operación](#mode-of-operation)

## <a name="cryptographic-agility"></a>Agilidad criptográfica

Una de las propuestas de valor clave de CNG es la agilidad criptográfica, que a veces se denomina "independiente criptográfica". Sin embargo, para convertir la implementación de protocolos, como [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL) o seguridad de la [*capa de transporte*](/windows/desktop/SecGloss/t-gly) (TLS), CMS (S/MIME), IPSec, Kerberos, etc., en CNG, era necesario. En el nivel de CNG, era necesario proporcionar sustitución y detección para todos los tipos de algoritmo (funciones simétricas, asimétricas y hash), la generación de números aleatorios y otras funciones de utilidad. Los cambios de nivel de protocolo son más importantes porque, en muchos casos, las API de protocolo necesarias para agregar la selección del algoritmo y otras opciones de flexibilidad que no existían previamente.

CNG está disponible en primer lugar en Windows Vista y está posicionado para reemplazar los usos existentes de [*CryptoAPI*](/windows/desktop/SecGloss/c-gly) en la pila de software de Microsoft. Los desarrolladores de terceros encontrarán muchas características nuevas en CNG, entre las que se incluyen:

-   Un nuevo sistema de configuración de cifrado, que admite una mejor agilidad criptográfica.
-   Abstracción más específica para el almacenamiento de claves (y separación del almacenamiento de las operaciones de algoritmo).
-   Aislamiento del proceso para las operaciones con claves a largo plazo.
-   Generadores de números aleatorios reemplazables.
-   Desahogo de las restricciones de la firma de exportación.
-   Seguridad para subprocesos en toda la pila.
-   API criptográfica de modo kernel.

Además, CNG incluye compatibilidad con todos los algoritmos de Suite B necesarios, como la [*criptografía de curva elíptica*](/windows/desktop/SecGloss/e-gly) (ECC). Las aplicaciones CryptoAPI existentes seguirán funcionando a medida que CNG esté disponible.

## <a name="certification-and-compliance"></a>Certificación y cumplimiento

CNG se valida con los estándares federales de procesamiento de información (FIPS) 140-2 y forma parte del objetivo de evaluación de la certificación de criterios comunes de Windows. CNG se diseñó para ser utilizable como componente en un sistema validado de nivel 2 de FIPS.

CNG cumple los requisitos de criterios comunes mediante el almacenamiento y el uso de claves de larga duración en un proceso seguro.

## <a name="suite-b-support"></a>Compatibilidad con Suite B

Una característica importante de CNG es su compatibilidad con los algoritmos de Suite B. En febrero de 2005, la Agencia de seguridad nacional (NSA) de la Estados Unidos anunció un conjunto coordinado de cifrado simétrico, el acuerdo secreto asimétrico (también conocido como intercambio de claves), las funciones de firma digital y hash para el uso futuro de la administración pública de EE. UU. denominada *Suite B*. La NSA ha anunciado que las implementaciones de Suite B certificadas se pueden usar para la protección de la información designada como secreto, secreto e información privada que, en el pasado, se describía como sensible, pero sin clasificar. Por este motivo, la compatibilidad con Suite B es muy importante para los proveedores de software de aplicaciones e integradores de sistemas, así como para Microsoft.

Todos los algoritmos de Suite B se conocen públicamente. Se han desarrollado fuera del ámbito del secreto gubernamental históricamente asociado al desarrollo de algoritmos criptográficos. En este mismo período de tiempo, algunos países y regiones europeos también han propuesto los mismos requisitos Suite B para proteger su información.

Suite B criptografía recomienda el uso de Diffie-Hellman de curva elíptica (ECDH) en muchos protocolos existentes como el Intercambio de claves por red (IKE, principalmente usado en IPsec), la seguridad de la [*capa de transporte*](/windows/desktop/SecGloss/t-gly) (TLS) y MIME seguro (S/MIME).

CNG incluye compatibilidad con Suite B que se extiende a todos los algoritmos necesarios: AES (todos los tamaños de clave), la familia SHA-2 (SHA-256, SHA-384 y SHA-512) de algoritmos hash, ECDH y el DSA de curva elíptica (ECDSA) sobre las curvas primos estándar de NIST P-256, P-384 y P-521. Los proveedores de algoritmos de Microsoft que se incluyen con Windows Vista no admiten curvas binarias, curvas de Koblitz, curvas principales personalizadas y curvas elípticas Menezes-qu-Vanstone (ECMQV).

## <a name="legacy-support"></a>Compatibilidad heredada

CNG proporciona compatibilidad con el conjunto actual de algoritmos en [*CryptoAPI*](/windows/desktop/SecGloss/c-gly) 1,0. Todos los algoritmos que se admiten actualmente en *CryptoAPI* 1,0 seguirán siendo compatibles con CNG.

## <a name="kernel-mode-support"></a>Compatibilidad con el modo kernel

CNG admite la criptografía en modo kernel. Se usan las mismas API en el modo de kernel y usuario para admitir todas las características de criptografía. SSL/TLS e IPsec funcionan en modo kernel, además de los procesos de arranque que utilizarán CNG. No todas las funciones de CNG pueden llamarse desde el modo kernel. El tema de referencia de las funciones a las que no se puede llamar desde el modo kernel indica explícitamente que no se puede llamar a la función desde el modo kernel. De lo contrario, se puede llamar a todas las funciones de CNG desde el modo kernel si el autor de la llamada se ejecuta en el [*IRQL*](/windows/desktop/SecGloss/i-gly)de **\_ nivel pasivo** . Además, algunas funciones CNG de modo kernel pueden ser Invocables en el **\_ IRQL de nivel de envío**, dependiendo de las capacidades del proveedor.

La interfaz del proveedor de compatibilidad para seguridad (Ksecdd.sys) del kernel de Microsoft es un módulo criptográfico basado en software y de uso general que reside en el nivel de modo kernel de Windows. Ksecdd.sys se ejecuta como un controlador de exportación del modo kernel y proporciona servicios de cifrado a través de las interfaces documentadas a los componentes de kernel. El único algoritmo de proveedor de Microsoft integrado que no es compatible con Ksecdd.sys es DSA.

**Windows Server 2008 y Windows Vista:** CNG no es compatible con los algoritmos y los proveedores conectables en modo kernel. Los únicos algoritmos criptográficos admitidos disponibles en modo kernel son las implementaciones proporcionadas por Microsoft a través de las API de CNG en modo kernel.

## <a name="auditing"></a>Auditoría

Para cumplir algunos de los requisitos de criterios comunes además de proporcionar una seguridad completa, muchas de las acciones que se producen en el nivel de CNG se auditan en el proveedor de almacenamiento de claves (KSP) de software de Microsoft. El KSP de Microsoft cumple las siguientes directrices para crear registros de auditoría en el registro de seguridad:

-   Los errores de generación de claves y pares de claves, incluidos los errores de prueba automática, se deben auditar.
-   Se debe auditar la importación y exportación de claves.
-   Los errores de destrucción de claves se deben auditar.
-   Las claves persistentes se deben auditar cuando se escriben y se leen de los archivos.
-   Los errores de comprobación de coherencia en pares se deben auditar.
-   Los errores de validación de clave secreta, si los hay, se deben auditar, por ejemplo, comprobaciones de paridad en claves 3DES.
-   Se deben auditar los errores de cifrado, descifrado, hash, firma, comprobación, intercambio de claves y generación de números aleatorios.
-   Las pruebas automáticas criptográficas se deben auditar.

En general, si una clave no tiene un nombre, es una clave efímera. No se conserva una clave efímera y el KSP de Microsoft no genera registros de auditoría para claves efímeras. El KSP de Microsoft genera registros de auditoría en modo de usuario solo en el proceso LSA. CNG de modo kernel no genera ningún registro de auditoría. Los administradores tienen que configurar la Directiva de auditoría para obtener todos los registros de auditoría de KSP del registro de seguridad. Un administrador debe ejecutar la siguiente línea de comandos para configurar las auditorías adicionales generadas por KSP:

**AuditPol/Set/subcategory: "otros eventos del sistema"/Success: enable/Failure: enable**

## <a name="replaceable-random-number-generators"></a>Generadores de números aleatorios reemplazables

Otra mejora que CNG proporciona es la posibilidad de reemplazar el generador de números aleatorios (RNG) predeterminado. En CryptoAPI, es posible proporcionar una RNG alternativa como parte de un proveedor de servicios criptográficos (CSP), pero no es posible redirigir a los CSP de base de Microsoft para que usen otra RNG. CNG permite especificar explícitamente una RNG determinada para usarla en llamadas particulares.

## <a name="thread-safety"></a>Seguridad para subprocesos

Las funciones que modifican la misma área de memoria al mismo tiempo (secciones críticas) cuando se llaman desde subprocesos independientes no son seguras para subprocesos.

## <a name="mode-of-operation"></a>Modo de operación

CNG admite cinco modos de operaciones que se pueden usar con cifrados de bloques simétricos a través de las API de cifrado. Estos modos y su compatibilidad se muestran en la tabla siguiente. El modo de operación se puede cambiar estableciendo la propiedad [**de \_ \_ modo de encadenamiento BCRYPT**](cng-property-identifiers.md) para el proveedor de algoritmos mediante la función [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) .



| Modo de operación           | \_Valor del modo de encadenamiento BCRYPT \_ | Algoritmos              | Estándar  |
|-----------------------------|------------------------------|-------------------------|-----------|
| ECB (Electronic Codebook)   | **\_ECB del \_ modo de cadena BCRYPT \_** | Cifrado de bloques simétricos | SP800-38A |
| CBC (encadenamiento de bloques de cifrado) | **\_modo de cadena BCRYPT \_ \_ CBC** | Cifrado de bloques simétricos | SP800-38A |
| CFB (comentarios de cifrado)       | **\_modo de cadena BCRYPT \_ \_ CFB** | Cifrado de bloques simétricos | SP800-38A |
| CCM (contador con CBC)      | **\_CCM del \_ modo de cadena BCRYPT \_** | AES                     | SP800-38C |
| GCM (modo Galois/Counter)   | **\_modo de cadena BCRYPT \_ \_ GCM** | AES                     | SP800-38D |



 

> [!Note]  
> Solo los modos de operación ECB, CBC y CFB se definen en Windows Vista. GCM y CCM requieren Windows Vista con Service Pack 1 (SP1) o Windows Server 2008.

 

 

 

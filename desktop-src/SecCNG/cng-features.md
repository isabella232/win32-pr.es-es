---
description: CNG tiene las siguientes características.
ms.assetid: 400a2b6e-6bbe-4ba4-abde-a2f625007517
title: Características de CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434c72075c04b0c280c85831ca78d930c0fcc047de19609d11764bcf63ddad56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908452"
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

Una de las propuestas de valor clave de CNG es la agilidad criptográfica, a veces denominada agnóstico criptográfico. La conversión de la implementación de protocolos como el protocolo Capa de sockets seguros (SSL) o la seguridad de la capa de transporte [*(TLS),*](/windows/desktop/SecGloss/t-gly) CMS (S/MIME), IPsec, Kerberos, y así sucesivamente, [*a*](/windows/desktop/SecGloss/s-gly) CNG, era necesaria para que esta capacidad fuera valiosa. En el nivel de CNG, era necesario proporcionar sustitución y detectabilidad para todos los tipos de algoritmo (funciones simétricas, asimétricas, hash), generación de números aleatorios y otras funciones de utilidad. Los cambios de nivel de protocolo son más significativos porque, en muchos casos, las API de protocolo necesitaban agregar la selección de algoritmos y otras opciones de flexibilidad que no existían anteriormente.

CNG está disponible primero en Windows Vista y se coloca para reemplazar los usos existentes de [*CryptoAPI*](/windows/desktop/SecGloss/c-gly) en toda la pila de software de Microsoft. Los desarrolladores de terceros encontrarán muchas características nuevas en CNG, entre las que se incluyen:

-   Un nuevo sistema de configuración de criptografía, que admite una mejor agilidad criptográfica.
-   Abstracción más detallada para el almacenamiento de claves (y separación del almacenamiento de las operaciones de algoritmo).
-   Aislamiento de procesos para operaciones con claves a largo plazo.
-   Generadores de números aleatorios reemplazables.
-   El resalte de las restricciones de firma de exportación.
-   Seguridad de subprocesos en toda la pila.
-   API criptográfica en modo kernel.

Además, CNG incluye compatibilidad con todos los algoritmos de Suite B, incluida la [*criptografía de curva elíptica*](/windows/desktop/SecGloss/e-gly) (ECC). Las aplicaciones CryptoAPI existentes seguirán funcionando a medida que CNG esté disponible.

## <a name="certification-and-compliance"></a>Certificación y cumplimiento

CNG se valida con el estándar federal de procesamiento de información (FIPS) 140-2 y forma parte del objetivo de evaluación para la certificación Windows common criteria. CNG se diseñó para poder usarse como componente en un sistema validado de nivel 2 de FIPS.

CNG cumple los requisitos de Common Criteria mediante el almacenamiento y el uso de claves de larga duración en un proceso seguro.

## <a name="suite-b-support"></a>Compatibilidad con Suite B

Una característica importante de CNG es su compatibilidad con los algoritmos Suite B estándar. En febrero de 2005, la Agencia de Seguridad Nacional (NSA) de la Estados Unidos anunció un conjunto coordinado de cifrado simétrico, acuerdo de secreto asimétrico (también conocido como intercambio de claves), firma digital y funciones hash para el uso futuro del gobierno de EE. UU. *denominado Suite B*. La NSA ha anunciado que las implementaciones de Suite B certificadas pueden y se usarán para la protección de la información designada como secreto superior, secreto e información privada que, en el pasado, se describía como confidencial pero sin clasificar. Por este problema, Suite B soporte técnico es muy importante para los proveedores de software de aplicaciones y los integradores de sistemas, así como para Microsoft.

Todos Suite B algoritmos se conocen públicamente. Se han desarrollado fuera del ámbito de la confidencialidad gubernamental asociada históricamente al desarrollo de algoritmos criptográficos. En este mismo período de tiempo, algunos países y regiones europeos también han propuesto los mismos Suite B para proteger su información.

Suite B criptografía recomienda el uso de la curva elíptica Diffie-Hellman (ECDH) en muchos protocolos existentes, como Internet Key Exchange [](/windows/desktop/SecGloss/t-gly) (IKE, que se usa principalmente en IPsec), seguridad de la capa de transporte (TLS) y MIME seguro (S/MIME).

CNG incluye compatibilidad con Suite B que se extiende a todos los algoritmos necesarios: AES (todos los tamaños de clave), la familia SHA-2 (SHA-256, SHA-384 y SHA-512) de algoritmos hash, ECDH y DSA de curva elíptica (ECDSA) sobre las curvas prime estándar de NIST P-256, P-384 y P-521. Las curvas binarias, las curvas Koblitz, las curvas prime personalizadas y las curvas elípticas Menezes-Qu-Vanstone (ECMQV) no son compatibles con los proveedores de algoritmos de Microsoft incluidos con Windows Vista.

## <a name="legacy-support"></a>Compatibilidad heredada

CNG proporciona compatibilidad con el conjunto actual de algoritmos en [*CryptoAPI*](/windows/desktop/SecGloss/c-gly) 1.0. Todos los algoritmos que se admiten actualmente *en CryptoAPI* 1.0 seguirán siendo compatibles con CNG.

## <a name="kernel-mode-support"></a>Compatibilidad con el modo kernel

CNG admite criptografía en modo kernel. Las mismas API se usan en modo kernel y usuario para admitir completamente las características de criptografía. Tanto SSL/TLS como IPsec funcionan en modo kernel, además de los procesos de arranque que usarán CNG. No se puede llamar a todas las funciones CNG desde el modo kernel. El tema de referencia de las funciones a las que no se puede llamar desde el modo kernel mostrará explícitamente que no se puede llamar a la función desde el modo kernel. De lo contrario, se puede llamar a todas las funciones CNG desde el modo kernel si el autor de la llamada se ejecuta en **\_ EL** [*IRQL DE NIVEL PASIVO.*](/windows/desktop/SecGloss/i-gly) Además, algunas funciones CNG del modo kernel pueden ser a las que se puede llamar en **DISPATCH \_ LEVEL IRQL,** en función de las funcionalidades del proveedor.

La interfaz del proveedor de compatibilidad con la seguridad del kernel de Microsoft (Ksecdd.sys) es un módulo criptográfico basado en software de uso general que reside en el nivel de modo kernel de Windows. Ksecdd.sys ejecuta como controlador de exportación en modo kernel y proporciona servicios criptográficos a través de sus interfaces documentadas a los componentes del kernel. El único algoritmo de proveedor de Microsoft integrado que no es compatible con Ksecdd.sys es DSA.

**Windows Server 2008 y Windows Vista:** CNG no admite algoritmos y proveedores conectables en modo kernel. Los únicos algoritmos criptográficos admitidos disponibles en modo kernel son las implementaciones proporcionadas por Microsoft a través de las API de CNG en modo kernel.

## <a name="auditing"></a>Auditoría

Para cumplir algunos de los requisitos de Common Criteria además de proporcionar una seguridad completa, muchas acciones que se suceden en la capa de CNG se auditan en el proveedor de almacenamiento de claves de software (KSP) de Microsoft. Microsoft KSP se adhiere a las siguientes directrices para crear registros de auditoría en el registro de seguridad:

-   Se deben auditar los errores de generación de pares clave y par de claves, incluidos los errores de prueba automática.
-   Se debe auditar la importación y exportación de claves.
-   Se deben auditar los errores de destrucción de claves.
-   Las claves persistentes deben auditarse cuando se escriben en archivos y se leen desde ellos.
-   Se deben auditar los errores de comprobación de coherencia por pares.
-   Los errores de validación de claves secretas, si los hay, deben auditarse, por ejemplo, las comprobaciones de paridad en claves 3DES.
-   Se deben auditar los errores de cifrado, descifrado, hash, firma, comprobación, intercambio de claves y generación de números aleatorios.
-   Se deben auditar las autoprobaciones criptográficas.

En general, si una clave no tiene un nombre, es una clave efímera. Una clave efímera no persiste y Microsoft KSP no genera registros de auditoría para las claves efímeras. Microsoft KSP genera registros de auditoría en modo de usuario solo en el proceso LSA. El CNG del modo kernel no genera ningún registro de auditoría. Los administradores deben configurar la directiva de auditoría para obtener todos los registros de auditoría de KSP del registro de seguridad. Un administrador debe ejecutar la siguiente línea de comandos para configurar auditorías adicionales generadas por los KSP:

**auditpol /set /subcategory:"otros eventos del sistema" /success:enable /failure:enable**

## <a name="replaceable-random-number-generators"></a>Generadores de números aleatorios reemplazables

Otra mejora que proporciona CNG es la capacidad de reemplazar el generador de números aleatorios (RNG) predeterminado. En CryptoAPI, es posible proporcionar un RNG alternativo como parte de un proveedor de servicios criptográficos (CSP), pero no es posible redirigir los CSP base de Microsoft para que usen otro RNG. CNG permite especificar explícitamente un RNG determinado para usarlo en determinadas llamadas.

## <a name="thread-safety"></a>Seguridad para subprocesos

Las funciones que modifican el mismo área de memoria al mismo tiempo (secciones críticas) cuando se llama desde subprocesos independientes no son seguras para subprocesos.

## <a name="mode-of-operation"></a>Modo de operación

CNG admite cinco modos de operaciones que se pueden usar con cifrados de bloques simétricos a través de las API de cifrado. Estos modos y su compatibilidad se enumeran en la tabla siguiente. El modo de operación se puede cambiar estableciendo la propiedad [**\_ BCRYPT CHAINING \_ MODE**](cng-property-identifiers.md) para el proveedor de algoritmos mediante la [**función BCryptSetProperty.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty)



| Modo de operación           | Valor de \_ BCRYPT CHAINING \_ MODE | Algoritmos              | Estándar  |
|-----------------------------|------------------------------|-------------------------|-----------|
| ECB (Electronic Codebook)   | **BCRYPT \_ CHAIN \_ MODE \_ ECB** | Cifrados de bloques simétricos | SP800-38A |
| CBC (encadenamiento de bloques de cifrado) | **BCRYPT \_ CHAIN \_ MODE \_ CBC** | Cifrados de bloques simétricos | SP800-38A |
| CFB (comentarios de cifrado)       | **BCRYPT \_ CHAIN \_ MODE \_ CFB** | Cifrados de bloques simétricos | SP800-38A |
| CCM (contador con CBC)      | **CCM EN MODO \_ DE \_ CADENA \_ BCRYPT** | AES                     | SP800-38C |
| GCM (modo Galois/Counter)   | **BCRYPT \_ CHAIN \_ MODE \_ GCM** | AES                     | SP800-38D |



 

> [!Note]  
> En vista, solo se definen los modos de funcionamiento DE LAN, CBC y CFB Windows Vista. GCM y CCM requieren Windows Vista con Service Pack 1 (SP1) o Windows Server 2008.

 

 

 

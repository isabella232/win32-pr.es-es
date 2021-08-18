---
description: CNG proporciona un modelo para el almacenamiento de claves privadas que permite adaptarse a las demandas actuales y futuras de creación de aplicaciones que usan características de criptografía como el cifrado de claves pública o privada, así como las demandas del almacenamiento del material de clave.
ms.assetid: 95e5750f-fdc5-41f3-a4ce-9593a7081e95
title: Clave Storage recuperación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81b2100f005f0ff293e34a3f4c0a7460b7a4d4e9c2b15fbe0b3577b5e52394a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907695"
---
# <a name="key-storage-and-retrieval"></a>Clave Storage recuperación

-   [Arquitectura de Storage clave](#key-storage-architecture)
-   [Tipos de clave](#key-types)
-   [Algoritmos admitidos](#supported-algorithms)
-   [Directorios y archivos clave](#key-directories-and-files)

## <a name="key-storage-architecture"></a>Arquitectura de Storage clave

CNG proporciona un modelo para el almacenamiento de claves privadas que permite adaptarse a las demandas actuales y futuras de creación de aplicaciones que usan características de criptografía como el cifrado de claves pública o privada, así como las demandas del almacenamiento del material de clave. El enrutador de almacenamiento de claves es la rutina central de este modelo y se implementa en Ncrypt.dll. Una aplicación accede a los proveedores de almacenamiento de claves (KSP) del sistema a través del enrutador de almacenamiento de claves, que oculta los detalles, como el aislamiento de claves, tanto de la aplicación como del propio proveedor de almacenamiento. En la ilustración siguiente se muestra el diseño y la función de la arquitectura de aislamiento de claves CNG.

![Proveedor de almacenamiento de claves cng](images/cng-key-storage-provider.png)

Para cumplir los requisitos de criterios comunes (CC), las claves de larga duración deben aislarse para que nunca estén presentes en el proceso de aplicación. Actualmente, CNG admite el almacenamiento de claves privadas asimétricas mediante el software KSP de Microsoft que se incluye con Windows Server 2008 y Windows Vista y se instala de forma predeterminada.

El aislamiento de claves está habilitado de forma predeterminada en Windows Server 2008 y Windows Vista. La característica de aislamiento de claves no está disponible en plataformas anteriores a estas. Además, los KSP de terceros no se cargan en el servicio de aislamiento de claves (proceso LSA). Solo el KSP de Microsoft se carga en el servicio de aislamiento de claves.

El proceso LSA se usa como proceso de aislamiento de claves para maximizar el rendimiento. Todo el acceso a las claves privadas pasa por el enrutador de almacenamiento de claves, que expone un conjunto completo de funciones para administrar y usar claves privadas.

CNG almacena la parte pública de la clave almacenada por separado de la parte privada. La parte pública de un par de claves también se mantiene en el servicio de aislamiento de claves y se accede a esta mediante la llamada a procedimiento remoto local (LRPC). El enrutador de almacenamiento de claves usa LRPC al llamar al proceso de aislamiento de claves. Todo el acceso a las claves privadas pasa a través del enrutador de clave privada y el CNG lo audita.

Como se describió anteriormente, se puede usar una amplia gama de dispositivos de almacenamiento de hardware. En cada caso, la interfaz a todos estos dispositivos de almacenamiento es idéntica. Incluye funciones para realizar varias operaciones de clave privada, así como funciones que pertenecen al almacenamiento y la administración de claves.

CNG proporciona un conjunto de API que se usan para crear, almacenar y recuperar claves criptográficas. Para obtener una lista de estas API, vea [CNG Key Storage Functions](cng-key-storage-functions.md).

## <a name="key-types"></a>Tipos de clave

CNG admite los siguientes tipos de clave:

-   Diffie-Hellman claves públicas y privadas.
-   Algoritmo de firma digital (DSA, FIPS 186-2) claves públicas y privadas.
-   Claves rsa (PKCS \# 1) públicas y privadas.
-   Varias claves públicas y privadas heredadas (CryptoAPI).
-   Claves públicas y privadas de criptografía de curva elíptica.

## <a name="supported-algorithms"></a>Algoritmos admitidos

CNG admite los siguientes algoritmos clave.

| Algoritmo | Longitud de clave/hash (bits)             |
|-----------|------------------------------------|
| RSA       | De 512 a 16384, en incrementos de 64 bits |
| Dh        | De 512 a 16384, en incrementos de 64 bits |
| DSA       | De 512 a 1024, en incrementos de 64 bits  |
| ECDSA     | P-256, P-384, P-521 (curvas NIST)  |
| ECDH      | P-256, P-384, P-521 (curvas NIST)  |
| MD2       | 128                                |
| MD4       | 128                                |
| MD5       | 128                                |
| SHA-1     | 160                                |
| SHA-256   | 256                                |
| SHA-384   | 384                                |
| SHA-512   | 512                                |



 

## <a name="key-directories-and-files"></a>Directorios y archivos clave

Los CSP de CryptoAPI heredados de Microsoft almacenan claves privadas en los directorios siguientes.

| Tipo de clave                | Directorios                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Usuario privado            | %APPDATA% \\ \\ SID de usuario \\ RSA \\ *de* Microsoft Crypto\\<br/>%APPDATA% SID de usuario \\ \\ de Microsoft Crypto \\ DSS \\ \\<br/>                                                   |
| Sistema local privado    | %ALLUSERSPROFILE% \\ Datos de aplicación Microsoft Crypto RSA \\ \\ \\ \\ S-1-5-18\\<br/>%ALLUSERSPROFILE% \\ Datos de aplicación Microsoft Crypto \\ \\ \\ DSS \\ S-1-5-18\\<br/>   |
| Servicio local privado   | %ALLUSERSPROFILE% \\ Datos de aplicación Microsoft Crypto RSA \\ \\ \\ \\ S-1-5-19\\<br/>%ALLUSERSPROFILE% \\ Datos de aplicación Microsoft Crypto \\ \\ \\ DSS \\ S-1-5-19\\<br/>   |
| Servicio de red privado | %ALLUSERSPROFILE% \\ Datos de aplicación Microsoft Crypto RSA \\ \\ \\ \\ S-1-5-20\\<br/>%ALLUSERSPROFILE% \\ Datos de aplicación Microsoft Crypto \\ \\ \\ DSS \\ S-1-5-20\\<br/>   |
| Privado compartido          | %ALLUSERSPROFILE% \\ Datos de aplicación Microsoft Crypto RSA \\ \\ \\ \\ MachineKeys<br/>%ALLUSERSPROFILE% \\ Datos de aplicación Microsoft Crypto \\ \\ \\ DSS \\ MachineKeys<br/> |



 

CNG almacena las claves privadas en los directorios siguientes.

| Tipo de clave                | Directorio                                                          |
|-------------------------|--------------------------------------------------------------------|
| Usuario privado            | %APPDATA% Claves \\ \\ criptográficas de Microsoft \\                                 |
| Sistema local privado    | %ALLUSERSPROFILE% \\ Application Data Microsoft Crypto \\ \\ \\ SystemKeys |
| Servicio local privado   | %WINDIR% \\ ServiceProfiles \\ LocalService                            |
| Servicio de red privado | %WINDIR% \\ ServiceProfiles \\ NetworkService                          |
| Privado compartido          | %ALLUSERSPROFILE% Datos de aplicación Claves \\ \\ \\ criptográficos de Microsoft \\       |



 

Estas son algunas de las diferencias entre los contenedores de claves CryptoAPI y CNG.

-   CNG usa nombres de archivo diferentes para los archivos de clave que los archivos de clave creados por el Rsaenh.dll y Dssenh.dll LOSPS heredados. Los archivos de clave heredados también tienen la extensión .key, pero los archivos de clave CNG no tienen la extensión .key.
-   CNG es totalmente compatible con los nombres de contenedor de claves Unicode; CNG usa un hash del nombre del contenedor Unicode, mientras que CryptoAPI usa un hash del nombre del contenedor ANSI.
-   CNG es más flexible con respecto a los pares de claves RSA. Por ejemplo, CNG admite exponentes públicos de más de 32 bits de longitud y admite claves en las que p y q tienen longitudes diferentes.
-   En CryptoAPI, el archivo contenedor de claves se almacena en un directorio cuyo nombre es el equivalente textual del SID del usuario. Este ya no es el caso de CNG, que elimina la dificultad de mover usuarios de un dominio a otro sin perder todas sus claves privadas.
-   Los nombres de clave y KSP de CNG se limitan a los caracteres Unicode **MAX \_ PATH.** El CSP de CryptoAPI y los nombres de clave se limitan a **los caracteres ANSI MAX \_ PATH.**
-   CNG ofrece la funcionalidad de propiedades de clave definidas por el usuario. Los usuarios pueden crear y asociar propiedades personalizadas con claves y almacenarlas con claves persistentes.

Al conservar una clave, CNG puede crear dos archivos. El primer archivo contiene la clave privada en el nuevo formato CNG y siempre se crea. Este archivo no es utilizable por los CSP de CryptoAPI heredados. El segundo archivo contiene la misma clave privada en el contenedor de claves CryptoAPI heredado. El segundo archivo se ajusta al formato y la ubicación que usa Rsaenh.dll. La creación del segundo archivo solo se produce si se especifica la marca **NCRYPT \_ WRITE KEY TO \_ \_ \_ LEGACY STORE \_ \_ FLAG** cuando se llama a la función [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) para finalizar una clave RSA. Esta característica no es compatible con las claves DSA y DH.

Cuando una aplicación intenta abrir una clave persistente existente, CNG intenta abrir primero el archivo CNG nativo. Si este archivo no existe, CNG intenta encontrar una clave correspondiente en el contenedor de claves CryptoAPI heredado.

Al mover o copiar claves CryptoAPI de una máquina de origen a una máquina de destino con Windows Herramienta de migración de estado de usuario (USMT), CNG no podrá acceder a las claves de la máquina de destino. Para acceder a estas claves migradas, debe usar CryptoAPI.

 

 





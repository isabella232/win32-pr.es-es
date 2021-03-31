---
description: CNG proporciona un modelo para el almacenamiento de claves privadas que permite adaptarse a las demandas actuales y futuras de la creación de aplicaciones que usan características de criptografía como el cifrado de claves públicas o privadas, así como las demandas del almacenamiento de material de clave.
ms.assetid: 95e5750f-fdc5-41f3-a4ce-9593a7081e95
title: Almacenamiento y recuperación de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5abfd6319353440c580d53990075a71613a1eba9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361150"
---
# <a name="key-storage-and-retrieval"></a>Almacenamiento y recuperación de claves

-   [Arquitectura de almacenamiento de claves](#key-storage-architecture)
-   [Tipos de clave](#key-types)
-   [Algoritmos admitidos](#supported-algorithms)
-   [Archivos y directorios clave](#key-directories-and-files)

## <a name="key-storage-architecture"></a>Arquitectura de almacenamiento de claves

CNG proporciona un modelo para el almacenamiento de claves privadas que permite adaptarse a las demandas actuales y futuras de la creación de aplicaciones que usan características de criptografía como el cifrado de claves públicas o privadas, así como las demandas del almacenamiento de material de clave. El enrutador de almacenamiento de claves es la rutina central de este modelo y se implementa en Ncrypt.dll. Una aplicación tiene acceso a los proveedores de almacenamiento de claves (KSP) en el sistema a través del enrutador de almacenamiento de claves, que oculta los detalles, como el aislamiento de claves, tanto de la aplicación como del propio proveedor de almacenamiento. En la ilustración siguiente se muestra el diseño y la función de la arquitectura de aislamiento de claves CNG.

![proveedor de almacenamiento de claves CNG](images/cng-key-storage-provider.png)

Para cumplir los requisitos de criterios comunes (CC), las claves de larga duración deben estar aisladas para que nunca estén presentes en el proceso de la aplicación. CNG actualmente admite el almacenamiento de claves privadas asimétricas mediante el KSP software de Microsoft que se incluye con Windows Server 2008 y Windows Vista, y se instala de manera predeterminada.

El aislamiento de claves está habilitado de forma predeterminada en Windows Server 2008 y Windows Vista. La característica de aislamiento de claves no está disponible en las plataformas anteriores a ellas. Además, los KSP de terceros no se cargan en el servicio de aislamiento de claves (proceso LSA). Solo se carga el KSP de Microsoft en el servicio de aislamiento de claves.

El proceso de LSA se utiliza como el proceso de aislamiento de claves para maximizar el rendimiento. Todo el acceso a las claves privadas se realiza a través del enrutador de almacenamiento de claves, que expone un conjunto completo de funciones para administrar y usar las claves privadas.

CNG almacena la parte pública de la clave almacenada de forma independiente de la parte privada. La parte pública de un par de claves también se mantiene en el servicio de aislamiento de claves y se tiene acceso a ella mediante la llamada a procedimiento remoto local (LRPC). El enrutador de almacenamiento de claves usa LRPC cuando llama al proceso de aislamiento de claves. Todo el acceso a las claves privadas se realiza a través del enrutador de clave privada y se audita mediante CNG.

Tal y como se ha descrito anteriormente, se puede admitir una amplia gama de dispositivos de almacenamiento de hardware. En cada caso, la interfaz para todos estos dispositivos de almacenamiento es idéntica. Incluye funciones para realizar varias operaciones de clave privada, así como funciones que pertenecen al almacenamiento y la administración de claves.

CNG proporciona un conjunto de API que se usan para crear, almacenar y recuperar claves criptográficas. Para obtener una lista de estas API, consulte [funciones de almacenamiento de claves CNG](cng-key-storage-functions.md).

## <a name="key-types"></a>Tipos de clave

CNG admite los siguientes tipos de clave:

-   Diffie-Hellman claves públicas y privadas.
-   Claves públicas y privadas del algoritmo de firma digital (DSA, FIPS 186-2).
-   \#Claves públicas y privadas RSA (PKCS 1).
-   Varias claves públicas y privadas heredadas (CryptoAPI).
-   Claves públicas y privadas de criptografía de curva elíptica.

## <a name="supported-algorithms"></a>Algoritmos admitidos

CNG admite los siguientes algoritmos de clave.

| Algoritmo | Longitud de clave/hash (bits)             |
|-----------|------------------------------------|
| RSA       | de 512 a 16384, en incrementos de 64 bits |
| DH        | de 512 a 16384, en incrementos de 64 bits |
| DSA       | de 512 a 1024, en incrementos de 64 bits  |
| ECDSA     | P-256, P-384, P-521 (curvas NIST)  |
| ECDH      | P-256, P-384, P-521 (curvas NIST)  |
| MD2       | 128                                |
| MD4       | 128                                |
| MD5       | 128                                |
| SHA-1     | 160                                |
| SHA-256   | 256                                |
| SHA-384   | 384                                |
| SHA-512   | 512                                |



 

## <a name="key-directories-and-files"></a>Archivos y directorios clave

Las claves privadas de los CSP de CryptoAPI heredadas de Microsoft se almacenan en los siguientes directorios.

| Tipo de clave                | Directorios                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Usuario privado            | % APPDATA% \\ \\ SID de \\ \\ *usuario* de RSA de Microsoft Crypto\\<br/>% APPDATA% \\ SID de usuario de Microsoft \\ Crypto \\ DSS \\ \\<br/>                                                   |
| Privado del sistema local    | % ALLUSERSPROFILE% de \\ datos de aplicación \\ Microsoft \\ Crypto \\ RSA \\ S-1-5-18\\<br/>% ALLUSERSPROFILE% \\ datos de aplicación \\ Microsoft \\ Crypto \\ DSS \\ S-1-5-18\\<br/>   |
| Servicio local privado   | % ALLUSERSPROFILE% de \\ datos de aplicación \\ Microsoft \\ Crypto \\ RSA \\ S-1-5-19\\<br/>% ALLUSERSPROFILE% \\ datos de aplicación \\ Microsoft \\ Crypto \\ DSS \\ S-1-5-19\\<br/>   |
| Servicio de red privado | % ALLUSERSPROFILE% de \\ datos de aplicación \\ Microsoft \\ Crypto \\ RSA \\ S-1-5-20\\<br/>% ALLUSERSPROFILE% \\ datos de aplicación \\ Microsoft \\ Crypto \\ DSS \\ S-1-5-20\\<br/>   |
| Privado compartido          | % ALLUSERSPROFILE% \\ datos de aplicación \\ Microsoft \\ Crypto \\ RSA \\ MachineKeys<br/>% ALLUSERSPROFILE% \\ datos de aplicación \\ Microsoft \\ Crypto \\ DSS \\ MachineKeys<br/> |



 

CNG almacena las claves privadas en los directorios siguientes.

| Tipo de clave                | Directorio                                                          |
|-------------------------|--------------------------------------------------------------------|
| Usuario privado            | % APPDATA% \\ \\ claves criptográficas de Microsoft \\                                 |
| Privado del sistema local    | % ALLUSERSPROFILE% \\ datos de aplicación \\ Microsoft \\ Crypto \\ SystemKeys |
| Servicio local privado   | % WINDIR% \\ ServiceProfiles \\ LocalService                            |
| Servicio de red privado | % WINDIR% \\ ServiceProfiles \\ NetworkService                          |
| Privado compartido          | % ALLUSERSPROFILE% de \\ datos de aplicaciones \\ Microsoft \\ Crypto \\ Keys       |



 

A continuación se muestran algunas de las diferencias entre los contenedores de claves de CryptoAPI y CNG.

-   CNG usa nombres de archivo diferentes para los archivos de clave que los archivos de clave creados por el Rsaenh.dll y Dssenh.dll CSP heredados. Los archivos de clave heredados también tienen la extensión. Key, pero los archivos de clave CNG no tienen la extensión. Key.
-   CNG es totalmente compatible con los nombres de contenedor de claves Unicode; CNG usa un hash del nombre del contenedor Unicode, mientras que CryptoAPI usa un hash del nombre del contenedor ANSI.
-   CNG es más flexible con respecto a los pares de claves RSA. Por ejemplo, CNG admite exponentes públicos mayores de 32 bits de longitud y admite claves en las que p y q tienen longitudes diferentes.
-   En CryptoAPI, el archivo de contenedor de claves se almacena en un directorio cuyo nombre es el equivalente textual del SID del usuario. Esto ya no es así en CNG, lo que elimina la dificultad de mover usuarios de un dominio a otro sin perder todas sus claves privadas.
-   Los nombres de clave y KSP de CNG se limitan a caracteres Unicode de **\_ ruta de acceso máxima** . Los nombres de clave y CSP de CryptoAPI se limitan a caracteres ANSI de **\_ ruta de acceso máxima** .
-   CNG ofrece la funcionalidad de las propiedades de clave definidas por el usuario. Los usuarios pueden crear y asociar propiedades personalizadas con claves y hacer que se almacenen con claves persistentes.

Cuando se conserva una clave, CNG puede crear dos archivos. El primer archivo contiene la clave privada en el nuevo formato CNG y siempre se crea. Los CSP de CryptoAPI heredados no pueden usar este archivo. El segundo archivo contiene la misma clave privada en el contenedor de claves CryptoAPI heredado. El segundo archivo se ajusta al formato y la ubicación que usa Rsaenh.dll. La creación del segundo archivo solo se produce si se especifica la marca de **marcador de escritura de NCRYPT \_ en el \_ \_ \_ \_ almacén \_ heredado** cuando se llama a la función [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) para finalizar una clave RSA. Esta característica no se admite para las claves DSA y DH.

Cuando una aplicación intenta abrir una clave persistente existente, CNG intenta abrir primero el archivo CNG nativo. Si este archivo no existe, CNG intenta encontrar una clave coincidente en el contenedor de claves CryptoAPI heredado.

Cuando se mueven o copian las claves de CryptoAPI de una máquina de origen a un equipo de destino con Herramienta de migración de estado de usuario de Windows (USMT), CNG no podrá tener acceso a las claves en el equipo de destino. Para tener acceso a estas claves migradas, debe usar la CryptoAPI.

 

 





---
description: Un almacén del sistema es una colección que consta de uno o varios almacenes físicos relacionados.
ms.assetid: 41fe9366-4c17-43bb-91d6-934c7aa87a2d
title: Ubicaciones del almacén del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0863ffde8be5db67459908b1ec26ec73da029744
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160707"
---
# <a name="system-store-locations"></a>Ubicaciones del almacén del sistema

Un almacén del sistema es una colección que consta de uno o varios almacenes físicos relacionados. Para cada almacén del sistema, hay almacenes del mismo nivel físicos predefinidos. Después de abrir un almacén del sistema como MY en CERT SYSTEM STORE CURRENT USER, el proveedor de almacén llama a \_ \_ \_ \_ [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) para abrir cada uno de los almacenes físicos de la colección de almacenes del sistema. En el proceso abierto, cada uno de estos almacenes físicos se agrega a la colección de almacenes del sistema mediante [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection). Todos los certificados de esos almacenes físicos están disponibles a través de la colección de almacenes del sistema lógico.

Para cada ubicación del almacén del sistema, los almacenes de sistemas predefinidos son:

-   MY
-   Root
-   Confianza
-   CA

En CERT \_ SYSTEM \_ STORE CURRENT \_ \_ USER, también hay un almacén UserDS predefinido. Se planea una tienda de tarjetas inteligentes para esta ubicación.

Estos son los almacenes del sistema seguidos de otros comentarios:

-   [USUARIO \_ ACTUAL DEL ALMACÉN DEL SISTEMA DE \_ \_ \_ CERT](#cert_system_store_current_user)
-   [MÁQUINA \_ LOCAL DEL ALMACÉN DEL SISTEMA \_ \_ \_ CERT](#cert_system_store_local_machine)
-   [SERVICIO \_ ACTUAL DEL ALMACÉN DEL SISTEMA \_ \_ \_ CERT](#cert_system_store_current_service)
-   [SERVICIOS DE \_ ALMACÉN \_ DEL SISTEMA \_ CERT](#cert_system_store_services)
-   [USUARIOS DEL \_ ALMACÉN DEL \_ SISTEMA CERT \_](#cert_system_store_users)
-   [DIRECTIVA \_ DE GRUPO DE USUARIOS ACTUAL DEL SISTEMA DE \_ \_ \_ \_ CERTIFICADOS](#cert_system_current_user_group_policy)
-   [CERT SYSTEM LOCAL MACHINE GROUP POLICY (DIRECTIVA DE \_ GRUPO DE MÁQUINAS LOCALES DEL SISTEMA DE \_ \_ \_ \_ CERTIFICADOS)](#cert_system_local_machine_group_policy)
-   [CERT \_ SYSTEM \_ STORE \_ LOCAL \_ MACHINE \_ ENTERPRISE](#cert_system_store_local_machine_enterprise)
-   [Comentarios:](#remarks)

### <a name="cert_system_store_current_user"></a>USUARIO \_ ACTUAL DEL ALMACÉN DEL SISTEMA DE \_ \_ \_ CERT

Los \_ almacenes del sistema CERT SYSTEM STORE CURRENT USER se encuentran en la siguiente ubicación del \_ \_ \_ Registro:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         SystemCertificates
```

Los almacenes físicos predefinidos asociados a esos almacenes del sistema son los siguientes.



| Almacén del sistema | Almacén físico                                           |
|--------------|----------------------------------------------------------|
| MY           | . Predeterminado                                                 |
| Root         | . Default.LocalMachine<br/> . Smartcard<br/>   |
| Confianza        | . Default.GroupPolicy<br/> . LocalMachine<br/> |
| CA           | . Default.GroupPolicy<br/> . LocalMachine<br/> |
| UserDS       | . Usercertificate                                         |



 

### <a name="cert_system_store_local_machine"></a>MÁQUINA \_ LOCAL DEL ALMACÉN DEL SISTEMA \_ \_ \_ CERT

Los \_ almacenes del sistema CERT SYSTEM STORE LOCAL MACHINE se encuentran en la siguiente ubicación del \_ \_ \_ Registro:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         SystemCertificates
```

Los almacenes físicos predefinidos están asociados a esos almacenes del sistema como se muestra a continuación.



| Almacén del sistema | Almacén físico                                                                                    |
|--------------|---------------------------------------------------------------------------------------------------|
| MY           | . Predeterminado                                                                                          |
| Root         | . Default.AuthRoot<br/> . GroupPolicy<br/> . Enterprise<br/> . Smartcard<br/> |
| Confianza        | . Default.GroupPolicy<br/> . Enterprise<br/>                                            |
| CA           | . Default.GroupPolicy<br/> . Enterprise <br/>                                           |



 

### <a name="cert_system_store_current_service"></a>SERVICIO \_ ACTUAL DEL ALMACÉN DEL SISTEMA \_ \_ \_ CERT

Los \_ almacenes del sistema CERT SYSTEM STORE CURRENT SERVICE se encuentran en la siguiente ubicación del \_ \_ \_ Registro:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

Los almacenes físicos predefinidos asociados a esos almacenes del sistema son los siguientes.



| Almacén del sistema | Almacén físico                   |
|--------------|----------------------------------|
| MY           | . Predeterminado                         |
| Root         | . Default.LocalMachine<br/> |
| Confianza        | . Default.LocalMachine<br/> |
| CA           | . Default.LocalMachine<br/> |



 

### <a name="cert_system_store_services"></a>SERVICIOS DE \_ ALMACÉN \_ DEL SISTEMA \_ CERT

Los \_ almacenes del sistema CERT SYSTEM STORE SERVICES se encuentran en la siguiente ubicación del \_ \_ Registro:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

Los almacenes físicos predefinidos asociados a esos almacenes del sistema son los siguientes.



| Almacén del sistema       | Almacén físico                   |
|--------------------|----------------------------------|
| ServiceName \\ MY    | . Predeterminado                         |
| Raíz \\ de ServiceName  | . Default.LocalMachine<br/> |
| Confianza \\ de ServiceName | . Default.LocalMachine<br/> |
| Entidad de certificación ServiceName \\    | . Default.LocalMachine<br/> |



 

### <a name="cert_system_store_users"></a>USUARIOS DEL \_ ALMACÉN DEL \_ SISTEMA CERT \_

Los \_ almacenes del sistema CERT SYSTEM STORE USERS se encuentran en la siguiente ubicación del \_ \_ Registro:

```
HKEY_USERS
   UserName
      Software
         Microsoft
            SystemCertificates
```

Los almacenes físicos predefinidos asociados a esos almacenes del sistema son los siguientes.



| Almacén del sistema  | Almacén físico                   |
|---------------|----------------------------------|
| userid \\ MY    | . Default.LocalMachine<br/> |
| userid \\ Root  | . Default.LocalMachine<br/> |
| userid \\ Trust | . Default.LocalMachine<br/> |
| userid \\ CA    | . Default.LocalMachine<br/> |



 

### <a name="cert_system_current_user_group_policy"></a>DIRECTIVA \_ DE GRUPO DE USUARIOS ACTUAL DEL SISTEMA DE \_ \_ \_ \_ CERTIFICADOS

Los almacenes \_ del sistema CERT SYSTEM CURRENT USER GROUP POLICY se encuentran en la siguiente ubicación del \_ \_ \_ \_ Registro:

```
HKEY_CURRENT_USER
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_local_machine_group_policy"></a>DIRECTIVA \_ DE GRUPO DE MÁQUINAS LOCALES DEL SISTEMA DE \_ \_ \_ \_ CERTIFICADOS

Los almacenes \_ del sistema CERT SYSTEM LOCAL MACHINE GROUP POLICY se encuentran en la siguiente ubicación del \_ \_ \_ \_ Registro:

```
HKEY_LOCAL_MACHINE
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_store_local_machine_enterprise"></a>CERT \_ SYSTEM \_ STORE \_ LOCAL \_ MACHINE \_ ENTERPRISE

CERT SYSTEM STORE LOCAL MACHINE ENTERPRISE contiene certificados compartidos entre dominios de la \_ \_ empresa y \_ \_ \_ descargados desde el directorio global de la empresa. Para sincronizar el almacén empresarial del cliente, el directorio empresarial se sondea cada ocho horas y los certificados se descargan automáticamente en segundo plano.

Los almacenes físicos predefinidos asociados a estos almacenes del sistema son los siguientes.



| Almacén del sistema | Almacén físico |
|--------------|----------------|
| MY           | . Predeterminado       |
| Root         | . Predeterminado       |
| Confianza        | . Predeterminado       |
| CA           | . Predeterminado       |



 

### <a name="remarks"></a>Observaciones

Se pueden asociar almacenes físicos adicionales a un almacén del sistema mediante [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).

Los almacenes CERT SYSTEM STORE SERVICE y CERT SYSTEM STORE USERS se abren antefijiendo el nombre del almacén en la cadena que se pasa a pvPara con el servicio o nombre de usuario, como \_ \_ \_ \_ \_ \_ *ServiceName*  \\ **Trust** o **. Mi** \\ **valor predeterminado** es . La ubicación CERT SYSTEM STORE SERVICES o CERT SYSTEM STORE USERS puede abrir el mismo almacén en CERT SYSTEM CURRENT SERVICE o CERT SYSTEM STORE CURRENT USER mediante el identificador de seguridad \_ \_ \_ \_ textual \_ \_ \_ \_ \_ \_ \_ \_ \_ (SID) [](../secgloss/s-gly.md) del servicio o usuario actual.

Los almacenes de LA DIRECTIVA DE GRUPO DE USUARIOS DEL ALMACÉN DEL SISTEMA DE CERTIFICADOS y LA DIRECTIVA DE GRUPO DE MÁQUINAS LOCALES DEL SISTEMA DE CERT en una configuración de red se descargan en el equipo cliente desde la plantilla de \_ \_ directiva de grupo \_ \_ \_ \_ \_ \_ \_ \_ (GPT) durante el inicio del equipo o el inicio de sesión del usuario. Estos almacenes se pueden actualizar en el equipo cliente después del inicio o el inicio de sesión cuando un administrador cambia el GPT en el servidor de dominio. La [**función CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) permite notificar a una aplicación cuando los almacenes de cualquiera de estas ubicaciones han cambiado.

Las siguientes ubicaciones del almacén del sistema se pueden abrir de forma remota:

-   CERT \_ SYSTEM \_ STORE \_ LOCAL \_ MACHINE
-   CERT \_ SYSTEM \_ STORE \_ LOCAL \_ MACHINE \_ GROUP \_ POLICY
-   CERT \_ SYSTEM \_ STORE \_ SERVICES
-   CERT \_ SYSTEM \_ STORE \_ USERS

Las ubicaciones del almacén del sistema se abren de forma remota antefijiendo el nombre del almacén en la cadena que se pasa a *pvPara* con el nombre del equipo. Algunos ejemplos de nombres de almacén del sistema remoto son:

-   *NombreDeEquipo* \\ **CA**
-   \\\\*NombreDeEquipo* \\ **CA**
-   *NombreDeEquipo* \\ *ServiceName* \\ **Confianza**
-   \\\\*NombreDeEquipo* \\ *ServiceName* \\ **Confianza**

 

 

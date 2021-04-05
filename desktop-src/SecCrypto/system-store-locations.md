---
description: Un almacén del sistema es una colección que consta de uno o varios almacenes físicos del mismo nivel.
ms.assetid: 41fe9366-4c17-43bb-91d6-934c7aa87a2d
title: Ubicaciones del almacén del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0863ffde8be5db67459908b1ec26ec73da029744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002081"
---
# <a name="system-store-locations"></a>Ubicaciones del almacén del sistema

Un almacén del sistema es una colección que consta de uno o varios almacenes físicos del mismo nivel. En cada almacén del sistema hay almacenes físicos predefinidos. Después de abrir un almacén del sistema como mi en CERT \_ System \_ Store \_ Current \_ User, el proveedor de almacén llama a [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) para abrir cada uno de los almacenes físicos en la colección de almacenes del sistema. En el proceso de apertura, cada uno de estos almacenes físicos se agrega a la colección de almacenes del sistema mediante [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection). Todos los certificados de esos almacenes físicos están disponibles a través de la colección de almacenes lógicos del sistema.

Para cada ubicación del almacén del sistema, los almacenes de sistemas predefinidos son:

-   MY
-   Root
-   Confianza
-   CA

En CERT \_ System \_ Store \_ \_ el usuario actual, también hay un almacén UserDS predefinido. Se planea una tienda de tarjetas inteligentes para esta ubicación.

Estos son los almacenes del sistema seguidos de comentarios adicionales:

-   [\_ \_ usuario actual del almacén del sistema \_ CERT \_](#cert_system_store_current_user)
-   [\_ \_ máquina local del almacén del sistema \_ CERT \_](#cert_system_store_local_machine)
-   [\_ \_ servicio actual del almacén del sistema \_ de certificados \_](#cert_system_store_current_service)
-   [\_servicios del \_ almacén del sistema de certificados \_](#cert_system_store_services)
-   [\_usuarios del \_ almacén del sistema CERT \_](#cert_system_store_users)
-   [\_Directiva de \_ \_ grupo de usuario actual del \_ sistema \_ de certificados](#cert_system_current_user_group_policy)
-   [\_Directiva de \_ \_ Grupo del equipo local \_ \_ del sistema de certificados](#cert_system_local_machine_group_policy)
-   [certificado de la \_ \_ \_ máquina local del almacén \_ del sistema CERT \_](#cert_system_store_local_machine_enterprise)
-   [Comentarios:](#remarks)

### <a name="cert_system_store_current_user"></a>\_ \_ usuario actual del almacén del sistema \_ CERT \_

\_ \_ \_ Los almacenes del sistema del usuario actual del almacén del sistema \_ de certificados se encuentran en la siguiente ubicación del registro:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         SystemCertificates
```

Los almacenes físicos predefinidos asociados a esos almacenes del sistema son los siguientes.



| Almacén del sistema | Almacén físico                                           |
|--------------|----------------------------------------------------------|
| MY           | . Predeterminada                                                 |
| Root         | . Default. LocalMachine<br/> . Tarjeta<br/>   |
| Confianza        | . Default. GroupPolicy<br/> . Almacén<br/> |
| CA           | . Default. GroupPolicy<br/> . Almacén<br/> |
| UserDS       | . UserCertificate                                         |



 

### <a name="cert_system_store_local_machine"></a>\_ \_ máquina local del almacén del sistema \_ CERT \_

\_ \_ \_ Los almacenes del sistema del equipo local del almacén del sistema \_ de certificados se encuentran en la siguiente ubicación del registro:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         SystemCertificates
```

Los almacenes físicos predefinidos se asocian a los almacenes del sistema como se indica a continuación.



| Almacén del sistema | Almacén físico                                                                                    |
|--------------|---------------------------------------------------------------------------------------------------|
| MY           | . Predeterminada                                                                                          |
| Root         | . Default. AuthRoot<br/> . GroupPolicy<br/> . Entidades<br/> . Tarjeta<br/> |
| Confianza        | . Default. GroupPolicy<br/> . Entidades<br/>                                            |
| CA           | . Default. GroupPolicy<br/> . Entidades <br/>                                           |



 

### <a name="cert_system_store_current_service"></a>\_ \_ servicio actual del almacén del sistema \_ de certificados \_

\_ \_ \_ \_ Los almacenes del sistema del servicio del almacén del sistema de certificados se encuentran en la siguiente ubicación del registro:

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
| MY           | . Predeterminada                         |
| Root         | . Default. LocalMachine<br/> |
| Confianza        | . Default. LocalMachine<br/> |
| CA           | . Default. LocalMachine<br/> |



 

### <a name="cert_system_store_services"></a>\_servicios del \_ almacén del sistema de certificados \_

\_ \_ Los almacenes del sistema de certificados del almacén del sistema \_ se encuentran en la siguiente ubicación del registro:

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
| ServiceName \\ mi    | . Predeterminada                         |
| ServiceName \\ raíz  | . Default. LocalMachine<br/> |
| ServiceName \\ confianza | . Default. LocalMachine<br/> |
| \\CA ServiceName    | . Default. LocalMachine<br/> |



 

### <a name="cert_system_store_users"></a>\_usuarios del \_ almacén del sistema CERT \_

\_ \_ \_ Los almacenes del sistema del almacén del sistema de certificados se encuentran en la siguiente ubicación del registro:

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
| userid \\ My    | . Default. LocalMachine<br/> |
| userid \\ raíz  | . Default. LocalMachine<br/> |
| userid \\ confianza | . Default. LocalMachine<br/> |
| userid \\ CA    | . Default. LocalMachine<br/> |



 

### <a name="cert_system_current_user_group_policy"></a>\_Directiva de \_ \_ grupo de usuario actual del \_ sistema \_ de certificados

\_ \_ \_ \_ \_ Los almacenes del sistema de la Directiva de grupo del usuario actual del sistema de certificados se encuentran en la siguiente ubicación del registro:

```
HKEY_CURRENT_USER
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_local_machine_group_policy"></a>\_Directiva de \_ \_ Grupo del equipo local \_ \_ del sistema de certificados

\_ \_ \_ \_ \_ Los almacenes del sistema de la Directiva de grupo del equipo local del sistema de certificados se encuentran en la siguiente ubicación del registro:

```
HKEY_LOCAL_MACHINE
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_store_local_machine_enterprise"></a>certificado de la \_ \_ \_ máquina local del almacén \_ del sistema CERT \_

\_Almacén del sistema de certificados: la \_ \_ \_ máquina local \_ contiene los certificados compartidos entre dominios de la empresa y descargados del directorio global de la empresa. Para sincronizar el almacén empresarial del cliente, el directorio empresarial se sondea cada ocho horas y los certificados se descargan automáticamente en segundo plano.

Los almacenes físicos predefinidos asociados a estos almacenes del sistema son los siguientes.



| Almacén del sistema | Almacén físico |
|--------------|----------------|
| MY           | . Predeterminada       |
| Root         | . Predeterminada       |
| Confianza        | . Predeterminada       |
| CA           | . Predeterminada       |



 

### <a name="remarks"></a>Observaciones

Se pueden asociar almacenes físicos adicionales a un almacén del sistema mediante [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).

\_ \_ Los almacenes de certificados \_ de servicio de almacén de sistema y certificado \_ de almacén del sistema \_ de certificados \_ se abren prefijando el nombre del almacén en la cadena que se pasa a *pvPara* con el nombre de servicio o de usuario como *ServiceName* \\ **Trust** o **.** \\ **Mi**. La ubicación de los usuarios de los servicios del almacén del sistema de certificados \_ \_ o del \_ \_ almacén del sistema \_ de certificados \_ puede abrir el mismo almacén en el \_ servicio actual del sistema de certificados \_ o el \_ \_ usuario actual del almacén del sistema de certificados mediante \_ \_ \_ el [*identificador de seguridad*](../secgloss/s-gly.md) de texto (SID) del servicio o usuario actual.

Los almacenes de \_ la Directiva de grupo de usuarios del almacén del sistema de certificados \_ \_ \_ \_ y \_ \_ \_ la Directiva de grupo del equipo local del sistema de certificados \_ \_ en una configuración de red se descargan en el equipo cliente desde la plantilla de directiva de grupo (GPT) durante el inicio del equipo o el inicio de sesión Estos almacenes se pueden actualizar en el equipo cliente después del inicio o el inicio de sesión cuando un administrador cambia la GPT en el servidor de dominio. La función [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) permite a una aplicación recibir una notificación cuando los almacenes en cualquiera de estas ubicaciones han cambiado.

Las siguientes ubicaciones del almacén del sistema se pueden abrir de forma remota:

-   \_ \_ máquina local del almacén del sistema \_ CERT \_
-   \_Directiva de \_ \_ Grupo del \_ equipo local del \_ almacén \_ del sistema de certificados
-   \_servicios del \_ almacén del sistema de certificados \_
-   \_usuarios del \_ almacén del sistema CERT \_

Las ubicaciones del almacén del sistema se abren de forma remota mediante el prefijo del nombre del almacén en la cadena que se pasa a *pvPara* con el nombre del equipo. Ejemplos de nombres de almacén del sistema remoto:

-   *Nombre del equipo* \\ **Entidad de certificación**
-   \\\\*Nombre del equipo* \\ **Entidad de certificación**
-   *Nombre del equipo* \\ *ServiceName* \\ **Confianza** de
-   \\\\*Nombre del equipo* \\ *ServiceName* \\ **Confianza** de

 

 

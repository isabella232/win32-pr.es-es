---
title: atributo MS-DS-REPL-Authentication-Mode
description: El atributo MS-DS-REPL-Authentication-Mode se usa para especificar el método de autenticación que se utiliza para autenticar a los asociados de replicación.
ms.assetid: b7e77b40-7aa7-4990-93fd-c8068e35fcf9
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-REPL-Authentication-Mode
- Esquema de AD del atributo msDS-ReplAuthenticationMode
topic_type:
- apiref
api_name:
- ms-DS-Repl-Authentication-Mode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b88c7e3223b946b56962b710b036ee6e0c36dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494020"
---
# <a name="ms-ds-repl-authentication-mode-attribute"></a>atributo MS-DS-REPL-Authentication-Mode

El atributo **MS-DS-REPL-Authentication-Mode** se usa para especificar el método de autenticación que se utiliza para autenticar a los asociados de replicación. Este atributo se aplica a la partición de configuración de una instancia de ADAM.

Los valores siguientes son los valores posibles para este atributo.

| Value        | Método de autenticación                          | Descripción                                                                                                                                                                    |
|--------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0<br/> | Paso negociado<br/>             | Todas las instancias de ADAM del conjunto de configuración usan el mismo nombre de cuenta y la misma contraseña que la cuenta de servicio de ADAM.<br/>                                                 |
| 1<br/> | Negotiated<br/>                          | Primero se intenta la autenticación Kerberos (utilizando SPN). Si se produce un error en Kerberos, se intenta la autenticación NTLM. Si se produce un error en NTLM, las instancias de ADAM no se replicarán.<br/> |
| 2<br/> | Autenticación mutua con Kerberos<br/> | Autenticación con Kerberos, que usa nombres principales de servicio (SPN) obligatoriamente. Si se produce un error en la autenticación Kerberos, no se replicarán las instancias de ADAM.<br/>                |



 

La tabla siguiente contiene los identificadores de programación para los valores de este atributo.

| Value        | Identifier (desde ntdsapi. h)                                               |
|--------------|---------------------------------------------------------------------------|
| 0<br/> | **modo de autenticación de REPL de ADAM \_ \_ \_ \_ negociar \_ paso \_ a través**<br/> |
| 1<br/> | **modo de autenticación de REPL de ADAM \_ \_ \_ \_ Negotiate**<br/>                |
| 2<br/> | **modo de autenticación de replicación de ADAM, se \_ \_ \_ \_ \_ requiere autenticación mutua \_**<br/>   |



 



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | MS-DS-REPL-autenticación-modo       |
| Nombre para mostrar de LDAP | msDS-ReplAuthenticationMode          |
| Tamaño              | \-                                   |
| Actualizar privilegio  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1861              |
| System-ID-GUID    | 6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50 |
| Sintaxis            | [**Enumeración**](s-enumeration.md) |



## <a name="implementations"></a>Implementaciones

-   [**ADAM**](#adam)

## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|-----------------------------------------------------|
| Identificador de vínculo                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | False                                               |
| Tiene un único valor       | True                                                |
| Está indexado             | False                                               |
| En el catálogo global      | False                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Clases usadas en        | [**Configuración**](c-configuration.md)<br/> |



 

 






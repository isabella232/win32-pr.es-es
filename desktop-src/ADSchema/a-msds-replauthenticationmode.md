---
title: Atributo ms-DS-Repl-Authentication-Mode
description: El atributo ms-DS-Repl-Authentication-Mode se usa para especificar qué método de autenticación se usa para autenticar los asociados de replicación.
ms.assetid: b7e77b40-7aa7-4990-93fd-c8068e35fcf9
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo ms-DS-Repl-Authentication-Mode
- Esquema de AD del atributo msDS-ReplAuthenticationMode
topic_type:
- apiref
api_name:
- ms-DS-Repl-Authentication-Mode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff624a9b7a1d1f678c748f79d3193b0b4b287026de1a669896c3e25d69f27ab0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803545"
---
# <a name="ms-ds-repl-authentication-mode-attribute"></a>Atributo ms-DS-Repl-Authentication-Mode

El **atributo ms-DS-Repl-Authentication-Mode** se usa para especificar qué método de autenticación se usa para autenticar los asociados de replicación. Este atributo se aplica a la partición de configuración de una instancia de ADAM.

Los valores siguientes son los valores posibles para este atributo.

| Valor        | Método de autenticación                          | Descripción                                                                                                                                                                    |
|--------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0<br/> | Paso negociado<br/>             | Todas las instancias de ADAM del conjunto de configuración usan un nombre de cuenta y una contraseña idénticos que la cuenta de servicio de ADAM.<br/>                                                 |
| 1<br/> | Negotiated<br/>                          | Primero se intenta la autenticación Kerberos (utilizando SPN). Si se produce un error en Kerberos, se intenta la autenticación NTLM. Si se produce un error en NTLM, las instancias de ADAM no se replicarán.<br/> |
| 2<br/> | Autenticación mutua con Kerberos<br/> | Autenticación con Kerberos, que usa nombres principales de servicio (SPN) obligatoriamente. Si se produce un error en la autenticación Kerberos, las instancias de ADAM no se replicarán.<br/>                |



 

La tabla siguiente contiene los identificadores de programación para los valores de este atributo.

| Value        | Identificador (de Ntdsapi.h)                                               |
|--------------|---------------------------------------------------------------------------|
| 0<br/> | **MODO DE AUTENTICACIÓN DE ADAM \_ REPL \_ NEGOTIATE PASS \_ \_ \_ \_ THROUGH**<br/> |
| 1<br/> | **NEGOCIACIÓN \_ DEL MODO DE \_ \_ AUTENTICACIÓN DE \_ ADAM REPL**<br/>                |
| 2<br/> | **SE \_ REQUIERE AUTENTICACIÓN MUTUA EN \_ MODO \_ DE \_ \_ \_ AUTENTICACIÓN DE ADAM REPL**<br/>   |



 



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | ms-DS-Repl-Authentication-Mode       |
| Ldap-Display-Name | msDS-ReplAuthenticationMode          |
| Size              | \-                                   |
| Actualizar privilegios  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1861              |
| System-Id-Guid    | 6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50 |
| Syntax            | [**Enumeración**](s-enumeration.md) |



## <a name="implementations"></a>Implementaciones

-   [**Adán**](#adam)

## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|-----------------------------------------------------|
| Id. de vínculo                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | Falso                                               |
| Es de un solo valor       | Verdadero                                                |
| Está indexado             | Falso                                               |
| En el catálogo global      | Falso                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Clases usadas en        | [**Configuración**](c-configuration.md)<br/> |



 

 






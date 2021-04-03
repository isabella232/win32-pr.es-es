---
title: Conjunto de propiedades User-Account-Restrictions
description: Conjunto de propiedades que contiene los atributos de usuario que describen las restricciones de la cuenta.
ms.assetid: 5616fede-12b1-41bd-b445-11c0e1ff66db
ms.tgt_platform: multiple
keywords:
- Conjunto de propiedades User-Account-Restrictions Set AD Schema
topic_type:
- apiref
api_name:
- User-Account-Restrictions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c3c39c80c83f321c654e675ccd87950cfd4bcf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997233"
---
# <a name="user-account-restrictions-property-set"></a>Conjunto de propiedades User-Account-Restrictions

Conjunto de propiedades que contiene los atributos de usuario que describen las restricciones de la cuenta.



| Entrada | Value |
|--------------|--------------------------------------|
| CN           | Restricciones de cuenta de usuario            |
| Display-Name | Restricciones de cuenta                 |
| Rights-GUID  | 4c164200-20c0-11d0-a768-00aa006e0529 |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**User**](c-user.md)<br/> [**Computer**](c-computer.md)<br/>                                                                                                                                                   |
| Localización: ID. de presentación | 9                                                                                                                                                                                                                             |
| Miembros del conjunto de propiedades    | [**Cuenta-expira**](a-accountexpires.md)<br/> [**PWD: último conjunto**](a-pwdlastset.md)<br/> [**Control de cuentas de usuario**](a-useraccountcontrol.md)<br/> [**User-Parameters**](a-userparameters.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**User**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                              |
| Localización: ID. de presentación | 9                                                                                                                                                                                                                                                                                                                            |
| Miembros del conjunto de propiedades    | [**Cuenta-expira**](a-accountexpires.md)<br/> [**MS-DS-User-Account-control-calculado**](a-msds-user-account-control-computed.md)<br/> [**PWD: último conjunto**](a-pwdlastset.md)<br/> [**Control de cuentas de usuario**](a-useraccountcontrol.md)<br/> [**User-Parameters**](a-userparameters.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | \-                                                                                                                                                                                                    |
| Localización: ID. de presentación | 9                                                                                                                                                                                                     |
| Miembros del conjunto de propiedades    | [**Cuenta-expira**](a-accountexpires.md)<br/> [**MS-DS-User-Account-control-calculado**](a-msds-user-account-control-computed.md)<br/> [**PWD: último conjunto**](a-pwdlastset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**User**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                              |
| Localización: ID. de presentación | 9                                                                                                                                                                                                                                                                                                                            |
| Miembros del conjunto de propiedades    | [**Cuenta-expira**](a-accountexpires.md)<br/> [**MS-DS-User-Account-control-calculado**](a-msds-user-account-control-computed.md)<br/> [**PWD: último conjunto**](a-pwdlastset.md)<br/> [**Control de cuentas de usuario**](a-useraccountcontrol.md)<br/> [**User-Parameters**](a-userparameters.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**User**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                                                                                                   |
| Localización: ID. de presentación | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Miembros del conjunto de propiedades    | [**Cuenta-expira**](a-accountexpires.md)<br/> [**MS-DS-User-Account-control-calculado**](a-msds-user-account-control-computed.md)<br/> [**MS-DS-usuario-contraseña-fecha de expiración calculada**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**PWD: último conjunto**](a-pwdlastset.md)<br/> [**Control de cuentas de usuario**](a-useraccountcontrol.md)<br/> [**User-Parameters**](a-userparameters.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**User**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**Cuenta de servicio de MS-DS-Managed**](c-msds-managedserviceaccount.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                  |
| Localización: ID. de presentación | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Miembros del conjunto de propiedades    | [**Cuenta-expira**](a-accountexpires.md)<br/> [**MS-DS-User-Account-control-calculado**](a-msds-user-account-control-computed.md)<br/> [**MS-DS-usuario-contraseña-fecha de expiración calculada**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**PWD: último conjunto**](a-pwdlastset.md)<br/> [**Control de cuentas de usuario**](a-useraccountcontrol.md)<br/> [**User-Parameters**](a-userparameters.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**User**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**Cuenta de servicio de MS-DS-Managed**](c-msds-managedserviceaccount.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                  |
| Localización: ID. de presentación | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Miembros del conjunto de propiedades    | [**Cuenta-expira**](a-accountexpires.md)<br/> [**MS-DS-User-Account-control-calculado**](a-msds-user-account-control-computed.md)<br/> [**MS-DS-usuario-contraseña-fecha de expiración calculada**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**PWD: último conjunto**](a-pwdlastset.md)<br/> [**Control de cuentas de usuario**](a-useraccountcontrol.md)<br/> [**User-Parameters**](a-userparameters.md)<br/> |



 

 






---
title: ACS-DSBM-atributo de prioridad
description: Este atributo contiene la prioridad de este administrador de ancho de banda de subred (SBM).
ms.assetid: 08dd49d2-a2fa-4707-8302-25566680b91d
ms.tgt_platform: multiple
keywords:
- ACS-DSBM-esquema de AD de atributo de prioridad
- aCSDSBMPriority esquema de AD de atributos
topic_type:
- apiref
api_name:
- ACS-DSBM-Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd32c9e9cca95dbd5f52569de0b61e886033d13
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151907"
---
# <a name="acs-dsbm-priority-attribute"></a>ACS-DSBM-atributo de prioridad

Este atributo contiene la prioridad de este administrador de ancho de banda de subred (SBM). Cuando es necesario elegir un nuevo administrador de ancho de banda de subred (DSBM), este valor se envía a otros SBMs del dominio como parte de un mensaje de uso de DSBM \_ . El SBM con la prioridad más alta se elige como el nuevo DSBM.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | ACS-DSBM-prioridad                    |
| Nombre para mostrar de LDAP | aCSDSBMPriority                      |
| Tamaño              | 4 bytes                              |
| Actualizar privilegio  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.776               |
| System-ID-GUID    | 1cb3559e-56d0-11d1-a9c6-0000f80367c1 |
| Sintaxis            | [**Enumeración**](s-enumeration.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|----------------------------------------------|
| Identificador de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Tiene un único valor       | True                                         |
| Está indexado             | False                                        |
| En el catálogo global      | False                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**ACS-subred**](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------------|
| Identificador de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Tiene un único valor       | True                                         |
| Está indexado             | False                                        |
| En el catálogo global      | False                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**ACS-subred**](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------|
| Identificador de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Tiene un único valor       | True                                         |
| Está indexado             | False                                        |
| En el catálogo global      | False                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**ACS-subred**](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------|
| Identificador de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Tiene un único valor       | True                                         |
| Está indexado             | False                                        |
| En el catálogo global      | False                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**ACS-subred**](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------|
| Identificador de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Tiene un único valor       | True                                         |
| Está indexado             | False                                        |
| En el catálogo global      | False                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**ACS-subred**](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------|
| Identificador de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Tiene un único valor       | True                                         |
| Está indexado             | False                                        |
| En el catálogo global      | False                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**ACS-subred**](c-acssubnet.md)<br/> |



 

 






---
title: Atributo ACS-ESTAM-Priority
description: Estos atributos contienen la prioridad de este Administrador de ancho de banda de subred (SBM).
ms.assetid: 08dd49d2-a2fa-4707-8302-25566680b91d
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo ACS-ESTAM-Priority
- Esquema de AD del atributo aCSDSBMPriority
topic_type:
- apiref
api_name:
- ACS-DSBM-Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e7a80c9c866b5c91f83f884ecaafe60e4596af4ca8d625791ed9264679c356
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637495"
---
# <a name="acs-dsbm-priority-attribute"></a>Atributo ACS-ESTAM-Priority

Estos atributos contienen la prioridad de este Administrador de ancho de banda de subred (SBM). Cuando es necesario elegir un nuevo Administrador de ancho de banda de subred designado (SEM) designado, este valor se envía a otros SMM del dominio como parte de un mensaje de aceptación de \_ ESTAM. El SBM con la prioridad más alta se elige como el nuevo DEMHM.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | ACS-UNAM-Prioridad                    |
| Ldap-Display-Name | aCSDSBMPriority                      |
| Size              | 4 bytes                              |
| Privilegio actualizar  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.776               |
| System-Id-Guid    | 1cb3559e-56d0-11d1-a9c6-0000f80367c1 |
| Syntax            | [**Enumeración**](s-enumeration.md) |



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
| Id. de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Es de un solo valor       | Verdadero                                         |
| Está indexado             | Falso                                        |
| En el catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**ACS-Subnet**](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------------|
| Id. de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Es de un solo valor       | Verdadero                                         |
| Está indexado             | Falso                                        |
| En el catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**ACS-Subnet**](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------|
| Id. de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Es de un solo valor       | Verdadero                                         |
| Está indexado             | Falso                                        |
| En el catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**ACS-Subnet**](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------|
| Id. de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Es de un solo valor       | Verdadero                                         |
| Está indexado             | Falso                                        |
| En el catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**ACS-Subnet**](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------|
| Id. de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Es de un solo valor       | Verdadero                                         |
| Está indexado             | Falso                                        |
| En el catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**ACS-Subnet**](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------|
| Id. de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Es de un solo valor       | Verdadero                                         |
| Está indexado             | Falso                                        |
| En el catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**ACS-Subnet**](c-acssubnet.md)<br/> |



 

 






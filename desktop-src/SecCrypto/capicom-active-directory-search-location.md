---
description: Indica la ubicación en la que se va a buscar un almacén Active Directory certificados.
ms.assetid: 56b9695e-7ab9-405b-9cae-d78c43071186
title: CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION enumeración (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 52f205717f3ba361c2c15dafc6e53f6cef3cd9d41cbbbf2ed243c60a74c2ca62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879445"
---
# <a name="capicom_active_directory_search_location-enumeration"></a>CAPICOM \_ ACTIVE DIRECTORY SEARCH LOCATION \_ \_ \_ (enumeración)

El **tipo de enumeración CAPICOM \_ ACTIVE DIRECTORY SEARCH \_ \_ \_ LOCATION** indica la ubicación en la que se va a buscar Active Directory [*almacén de certificados*](../secgloss/c-gly.md).

## <a name="members"></a>Miembros



| Miembro                               | Descripción                                  | Value |
|--------------------------------------|----------------------------------------------|-------|
| **CAPICOM \_ SEARCH \_ ANY**             | Busca en todas las ubicaciones disponibles.<br/> | 0     |
| **CATÁLOGO GLOBAL DE CAPICOM \_ SEARCH \_ \_** | Busca solo en el catálogo global.<br/> | 1     |
| **DOMINIO PREDETERMINADO DE CAPICOM \_ SEARCH \_ \_** | Busca solo el dominio predeterminado.<br/> | 2     |



## <a name="remarks"></a>Comentarios

La propiedad siguiente usa este tipo de enumeración:

-   [**Configuración. ActiveDirectorySearchLocation**](settings-activedirectorysearchlocation.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 

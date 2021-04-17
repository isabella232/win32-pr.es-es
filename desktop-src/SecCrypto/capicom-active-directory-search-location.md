---
description: Indica la ubicación en la que se buscará un almacén de certificados Active Directory.
ms.assetid: 56b9695e-7ab9-405b-9cae-d78c43071186
title: Enumeración CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION (CAPICOM. h)
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
ms.openlocfilehash: cd630bdc0c09a6bb57a9163ec972451011f3e826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670614"
---
# <a name="capicom_active_directory_search_location-enumeration"></a>CAPICOM \_ Active \_ Directory \_ Search \_ Location (enumeración)

El tipo de enumeración ubicación de **\_ búsqueda de Active \_ Directory \_ \_ de CAPICOM** indica la ubicación en la que se buscará un almacén de [*certificados*](../secgloss/c-gly.md)Active Directory.

## <a name="members"></a>Miembros



| Miembro                               | Descripción                                  | Value |
|--------------------------------------|----------------------------------------------|-------|
| **CAPICOM \_ Search \_ any**             | Busca en todas las ubicaciones disponibles.<br/> | 0     |
| **CAPICOM \_ Buscar en el \_ \_ catálogo global** | Busca solo en el catálogo global.<br/> | 1     |
| **\_ \_ dominio predeterminado de búsqueda de CAPICOM \_** | Busca solo en el dominio predeterminado.<br/> | 2     |



## <a name="remarks"></a>Observaciones

Este tipo de enumeración se usa en la siguiente propiedad:

-   [**Settings. ActiveDirectorySearchLocation**](settings-activedirectorysearchlocation.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 

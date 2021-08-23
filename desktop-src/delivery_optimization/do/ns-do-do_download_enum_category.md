---
title: DO_DOWNLOAD_ENUM_CATEGORY estructura
description: Usado por **IDOManager::EnumDownloads** para filtrar la enumeración de descargas por el valor de la propiedad específica.
keywords:
- DO_DOWNLOAD_ENUM_CATEGORY estructura
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_ENUM_CATEGORY
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 32bdc7ca9a84bfe87ff453d34c4ecff57a8dabf5f67b21cc0d54ba079efd1578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543775"
---
# <a name="do_download_enum_category-structure"></a>DO_DOWNLOAD_ENUM_CATEGORY estructura

**IDOManager::EnumDownloads** usa la estructura DO_DOWNLOAD_ENUM_CATEGORY para filtrar la enumeración de descargas por el valor de la propiedad específica. 

## <a name="syntax"></a>Sintaxis
```cpp
typedef struct _DO_DOWNLOAD_ENUM_CATEGORY
{
  DODownloadProperty Property;
  LPCWSTR Value;
} DO_DOWNLOAD_ENUM_CATEGORY;
```

## <a name="members"></a>Miembros

`Property`

Nombre de propiedad que se va a usar para la enumeración de descarga. Estas propiedades se admiten con fines de enumeración.
- **DODownloadProperty_Id**
- **DODownloadProperty_Uri**
- **DODownloadProperty_ContentId**
- **DODownloadProperty_DisplayName**
- **DODownloadProperty_LocalPath**

`Value`

Valor de la propiedad.

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | Do.h |

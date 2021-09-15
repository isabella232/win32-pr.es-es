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
ms.openlocfilehash: a78c94cd9d8854453517976300e12a031f65b8cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568053"
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

## <a name="members"></a>Members

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

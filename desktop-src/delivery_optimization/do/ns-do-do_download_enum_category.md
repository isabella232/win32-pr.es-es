---
title: Estructura de DO_DOWNLOAD_ENUM_CATEGORY
description: 'Lo usa **IDOManager:: EnumDownloads** para filtrar la enumeración downloads por el valor de la propiedad específica.'
keywords:
- Estructura de DO_DOWNLOAD_ENUM_CATEGORY
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
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "105720103"
---
# <a name="do_download_enum_category-structure"></a>Estructura de DO_DOWNLOAD_ENUM_CATEGORY

**IDOManager:: EnumDownloads** usa la estructura **DO_DOWNLOAD_ENUM_CATEGORY** para filtrar la enumeración downloads por el valor de la propiedad específica.

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

Nombre de propiedad que se va a utilizar para la enumeración de descarga. Estas propiedades se admiten para la enumeración.
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
| **Cliente mínimo compatible** | Solo aplicaciones Win32 de Windows 10, versión 1809 \[\] |
| **Servidor mínimo compatible** | Windows Server, versión 1809 \[ Win32 Applications Only\] |
| **Header** | Do. h |

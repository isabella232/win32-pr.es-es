---
title: Método IDOManager::EnumDownloads
description: Recupera un puntero de interfaz a un objeto enumerador que se usa para enumerar las descargas existentes.
keywords:
- Método IDOManager::EnumDownloads
topic_type:
- apiref
api_name:
- IDOManager.EnumDownloads
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5442196b95e654755b4f84fe85375afb8f5b9372ddae453ca4ddffb567882fda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543832"
---
# <a name="idomanagerenumdownloads-method"></a>Método IDOManager::EnumDownloads

Recupera un puntero de interfaz a un objeto enumerador que se usa para enumerar las descargas existentes.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT EnumDownloads(
  DO_DOWNLOAD_ENUM_CATEGORY *category, 
  IEnumUnknown **ppEnum
);
```

## <a name="parameters"></a>Parámetros

`category`

Opcional. Nombre de propiedad que se va a usar como categoría para enumerar. Al `nullptr` pasar se recuperarán todas las descargas existentes. Las siguientes propiedades se admiten como una categoría.

- **DODownloadProperty_Id**
- **DODownloadProperty_Uri**
- **DODownloadProperty_ContentId**
- **DODownloadProperty_DisplayName**
- **DODownloadProperty_LocalPath**

`ppEnum`

Dirección de un puntero de interfaz a **IEnumUnknown**, que se usa para enumerar las descargas existentes. El contenido del enumerador depende del valor de *la categoría*. Las descargas incluidas en la interfaz de enumeración son las que creó anteriormente el mismo autor de la llamada a esta función. 

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve **S_OK**. De lo contrario, devuelve un [**código de**](/windows/desktop/com/structure-of-com-error-codes) error [HRESULT](/windows/desktop/com/com-error-codes-10).

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | Do.h |

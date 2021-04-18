---
title: 'IDOManager:: EnumDownloads (método)'
description: Recupera un puntero de interfaz a un objeto de enumerador que se usa para enumerar las descargas existentes.
keywords:
- 'IDOManager:: EnumDownloads (método)'
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
ms.openlocfilehash: a1e7fed2955fdc1b5ac0c11cfebc34aa95517603
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "105720105"
---
# <a name="idomanagerenumdownloads-method"></a>IDOManager:: EnumDownloads (método)

Recupera un puntero de interfaz a un objeto de enumerador que se usa para enumerar las descargas existentes.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT EnumDownloads(
  DO_DOWNLOAD_ENUM_CATEGORY *category, 
  IEnumUnknown **ppEnum
);
```

## <a name="parameters"></a>Parámetros

`category`

Opcional. Nombre de la propiedad que se va a utilizar como categoría que se va a enumerar. Al pasar `nullptr` , se recuperarán todas las descargas existentes. Las siguientes propiedades se admiten como una categoría.

- **DODownloadProperty_Id**
- **DODownloadProperty_Uri**
- **DODownloadProperty_ContentId**
- **DODownloadProperty_DisplayName**
- **DODownloadProperty_LocalPath**

`ppEnum`

La dirección de un puntero de interfaz a **IEnumUnknown**, que se usa para enumerar las descargas existentes. El contenido del enumerador depende del valor de *Category*. Las descargas incluidas en la interfaz de enumeración son las que crearon previamente el mismo llamador en esta función. 

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve **S_OK**. De lo contrario, devuelve un [código de error](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Solo aplicaciones Win32 de Windows 10, versión 1809 \[\] |
| **Servidor mínimo compatible** | Windows Server, versión 1809 \[ Win32 Applications Only\] |
| **Header** | Do. h |

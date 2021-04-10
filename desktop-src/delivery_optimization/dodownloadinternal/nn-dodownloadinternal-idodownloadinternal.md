---
title: Interfaz IDODownloadInternal
description: Se usa para obtener o establecer las propiedades de descarga extendida.
keywords:
- Interfaz IDODownloadInternal
topic_type:
- apiref
api_name:
- IDODownloadInternal
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 89dcf0e397e9761c1b156a4ad4b245209cf50020
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149461"
---
# <a name="idodownloadinternal-interface"></a>Interfaz IDODownloadInternal

> [!IMPORTANT]
> La interfaz **IDODownloadInternal** está en desuso. En su lugar, use la interfaz [IDODownload](../do/nn-do-idodownload.md) .

La interfaz **IDODownloadInternal** se usa para obtener o establecer las propiedades de descarga extendida.

## <a name="methods"></a>Métodos

La interfaz **IDODownloadInternal** tiene estos métodos.

| Método | Descripción |
| ---- |:---- |
| [IDODownloadInternal::GetPropertyEx](./nf-dodownloadinternal-idodownloadinternal-getpropertyex.md) | Recupera un puntero a una **variante** que contiene un valor de propiedad de descarga extendida específico. |
| [IDODownloadInternal::SetPropertyEx](./nf-dodownloadinternal-idodownloadinternal-setpropertyex.md) | Establece una propiedad de descarga extendida. El método acepta un puntero a una **variante** que contiene un valor de propiedad específico que se va a aplicar a la descarga. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Solo aplicaciones Win32 de Windows 10, versión 1809 \[\] |
| **Servidor mínimo compatible** | Windows Server, versión 1809 \[ Win32 Applications Only\] |
| **Header** | DODownloadInternal. h |
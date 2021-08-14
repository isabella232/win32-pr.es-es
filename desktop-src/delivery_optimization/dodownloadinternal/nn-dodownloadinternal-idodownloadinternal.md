---
title: Interfaz IDODownloadInternal
description: Se usa para obtener o establecer propiedades de descarga extendidas.
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
ms.openlocfilehash: de9079f7b87822ce950bc4e6c3ece6457e62775c32f7c0d51e76959332298bb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755785"
---
# <a name="idodownloadinternal-interface"></a>Interfaz IDODownloadInternal

> [!IMPORTANT]
> La **interfaz IDODownloadInternal** está en desuso. En su lugar, use la [interfaz IDODownload.](../do/nn-do-idodownload.md)

La **interfaz IDODownloadInternal** se usa para obtener o establecer propiedades de descarga extendidas.

## <a name="methods"></a>Métodos

La **interfaz IDODownloadInternal** tiene estos métodos.

| Método | Descripción |
| ---- |:---- |
| [IDODownloadInternal::GetPropertyEx](./nf-dodownloadinternal-idodownloadinternal-getpropertyex.md) | Recupera un puntero a un **variant que** contiene un valor de propiedad de descarga extendido específico. |
| [IDODownloadInternal::SetPropertyEx](./nf-dodownloadinternal-idodownloadinternal-setpropertyex.md) | Establece una propiedad de descarga extendida. El método acepta un puntero a **un variant** que contiene un valor de propiedad específico que se aplicará a la descarga. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | DODownloadInternal.h |
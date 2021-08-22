---
title: Interfaz IDOManager
description: Se usa para crear una nueva descarga y para enumerar las descargas existentes.
keywords:
- Interfaz IDOManager
topic_type:
- apiref
api_name:
- IDOManager
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5fff72067c69345a9852718c377b179d16f398c0eb3b84c73ca82c3af1b08a71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047093"
---
# <a name="idomanager-interface"></a>Interfaz IDOManager

La **interfaz IDOManager** se usa para crear una nueva descarga y enumerar las descargas existentes.

## <a name="methods"></a>Métodos

La **interfaz IDOManager** tiene estos métodos.

| Método | Descripción |
| ---- |:---- |
| [IDOManager::CreateDownload](./nf-do-idomanager-createdownload.md) | Crea una nueva descarga. |
| [IDOManager::EnumDownloads](./nf-do-idomanager-enumdownloads.md) | Recupera un puntero de interfaz a un objeto enumerador que se usa para enumerar las descargas existentes. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | Do.h |
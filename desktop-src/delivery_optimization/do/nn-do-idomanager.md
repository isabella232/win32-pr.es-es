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
ms.openlocfilehash: a8755615e4d2f0fd074117438f8f305dce0cb681
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105720168"
---
# <a name="idomanager-interface"></a>Interfaz IDOManager

La interfaz **IDOManager** se usa para crear una nueva descarga y enumerar las descargas existentes.

## <a name="methods"></a>Métodos

La interfaz **IDOManager** tiene estos métodos.

| Método | Descripción |
| ---- |:---- |
| [IDOManager::CreateDownload](./nf-do-idomanager-createdownload.md) | Crea una nueva descarga. |
| [IDOManager::EnumDownloads](./nf-do-idomanager-enumdownloads.md) | Recupera un puntero de interfaz a un objeto de enumerador que se usa para enumerar las descargas existentes. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Solo aplicaciones Win32 de Windows 10, versión 1809 \[\] |
| **Servidor mínimo compatible** | Windows Server, versión 1809 \[ Win32 Applications Only\] |
| **Header** | Do. h |
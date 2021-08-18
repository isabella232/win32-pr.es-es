---
title: Interfaz IDODownload
description: Se usa para iniciar y administrar una descarga.
keywords:
- Interfaz IDODownload
topic_type:
- apiref
api_name:
- IDODownload
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 356d6ae2e01f91eae94d9d2ff01a39dd49708eb73a7287d8c176b4231654a74a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543822"
---
# <a name="idodownload-interface"></a>Interfaz IDODownload

La **interfaz IDODownload** se usa para iniciar y administrar una descarga.

## <a name="methods"></a>Métodos

La **interfaz IDODownload** tiene estos métodos.

| Método | Descripción |
| ---- |:---- |
| [IDODownload::Abort](./nf-do-idomanager-createdownload.md) | Anula la descarga. |
| [IDODownload::Finalize](./nf-do-idodownload-finalize.md) | Finalizará la descarga. |
| [IDODownload::GetProperty](./nf-do-idodownload-getproperty.md) | Recupera un puntero a un **variant que** contiene una propiedad de descarga específica. |
| [IDODownload::GetStatus](./nf-do-idodownload-getstatus.md) | Recupera un puntero a una **estructura DO_DOWNLOAD_STATUS** que refleja el estado actual de la descarga. |
| [IDODownload::P ause](./nf-do-idodownload-pause.md) | Pausa la descarga. |
| [IDODownload::SetProperty](./nf-do-idodownload-setproperty.md) | Establece una propiedad de descarga. |
| [IDODownload::Start](./nf-do-idodownload-start.md) | Inicia o reanuda una descarga. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | Do.h |
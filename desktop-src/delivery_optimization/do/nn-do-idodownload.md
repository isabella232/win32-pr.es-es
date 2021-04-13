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
ms.openlocfilehash: ec2f74ce7daae6f612297d21e15e6993fcd78382
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359016"
---
# <a name="idodownload-interface"></a>Interfaz IDODownload

La interfaz **IDODownload** se usa para iniciar y administrar una descarga.

## <a name="methods"></a>Métodos

La interfaz **IDODownload** tiene estos métodos.

| Método | Descripción |
| ---- |:---- |
| [IDODownload:: ABORT](./nf-do-idomanager-createdownload.md) | Anula la descarga. |
| [IDODownload:: Finalize](./nf-do-idodownload-finalize.md) | Finaliza la descarga. |
| [IDODownload:: GetProperty](./nf-do-idodownload-getproperty.md) | Recupera un puntero a un **valor de tipo Variant** que contiene una propiedad de descarga específica. |
| [IDODownload:: GetStatus](./nf-do-idodownload-getstatus.md) | Recupera un puntero a una estructura de **DO_DOWNLOAD_STATUS** que refleja el estado actual de la descarga. |
| [IDODownload::P ause](./nf-do-idodownload-pause.md) | Pausa la descarga. |
| [IDODownload:: SetProperty](./nf-do-idodownload-setproperty.md) | Establece una propiedad de descarga. |
| [IDODownload:: Start](./nf-do-idodownload-start.md) | Inicia o reanuda una descarga. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Solo aplicaciones Win32 de Windows 10, versión 1809 \[\] |
| **Servidor mínimo compatible** | Windows Server, versión 1809 \[ Win32 Applications Only\] |
| **Header** | Do. h |
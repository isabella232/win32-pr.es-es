---
title: Interfaz IDODownloadStatusCallback
description: Se usa para recibir notificaciones sobre una descarga.
keywords:
- Interfaz IDODownloadStatusCallback
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0917b73939535854469a1fe02ea89acc904cf055
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420767"
---
# <a name="idodownloadstatuscallback-interface"></a>Interfaz IDODownloadStatusCallback

La interfaz **IDODownloadStatusCallback** se usa para recibir notificaciones sobre una descarga.

## <a name="methods"></a>Métodos

La interfaz **IDODownloadStatusCallback** tiene estos métodos.

| Método | Descripción |
| ---- |:---- |
| [IDODownloadStatusCallback::OnStatusChanged](./nf-do-idodownloadstatuscallback-onstatuschanged.md) | Llama a la implementación de este método cada vez que cambia el estado de la descarga. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Solo aplicaciones Win32 de Windows 10, versión 1809 \[\] |
| **Servidor mínimo compatible** | Windows Server, versión 1809 \[ Win32 Applications Only\] |
| **Header** | Do. h |
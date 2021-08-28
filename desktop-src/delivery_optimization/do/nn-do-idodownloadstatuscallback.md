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
ms.openlocfilehash: d91ff44e3b4f4247983ec81d53257347c8bcfa523f85855dcd0d37074f4b38fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498955"
---
# <a name="idodownloadstatuscallback-interface"></a>Interfaz IDODownloadStatusCallback

La **interfaz IDODownloadStatusCallback** se usa para recibir notificaciones sobre una descarga.

## <a name="methods"></a>Métodos

La **interfaz IDODownloadStatusCallback** tiene estos métodos.

| Método | Descripción |
| ---- |:---- |
| [IDODownloadStatusCallback::OnStatusChanged](./nf-do-idodownloadstatuscallback-onstatuschanged.md) | DO llama a la implementación de este método cada vez que cambia un estado de descarga. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | Do.h |
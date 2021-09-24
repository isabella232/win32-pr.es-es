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
ms.openlocfilehash: a6db896bf8d70e795b16512d22027c7ab6a02e91
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128521342"
---
# <a name="idodownloadstatuscallback-interface"></a>Interfaz IDODownloadStatusCallback

La **interfaz IDODownloadStatusCallback** se usa para recibir notificaciones sobre una descarga.

## <a name="methods"></a>Métodos

La **interfaz IDODownloadStatusCallback** tiene estos métodos.

| Método | Descripción |
| ---- |:---- |
| [IDODownloadStatusCallback::OnStatusChanged](./nf-do-idodownloadstatuscallback-onstatuschanged.md) | Optimización de distribución llama a la implementación de este método cada vez que cambia un estado de descarga. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | Do.h |
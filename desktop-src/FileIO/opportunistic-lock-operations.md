---
description: Si una aplicación solicita bloqueos oportunistas, todos los archivos para los que solicita bloqueos deben abrirse para la entrada y salida superpuestas (asincrónicas) mediante la función CreateFile con la marca FILE \_ FLAG \_ OVERLAPPED.
ms.assetid: 1595c03e-9f6d-456c-8164-fafba06bbd79
title: Operaciones de bloqueo oportunista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefd9b292747e89f5ebafd94cb8aa0e38833e8cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069876"
---
# <a name="opportunistic-lock-operations"></a>Operaciones de bloqueo oportunista

Si una aplicación solicita bloqueos oportunistas, todos los archivos para los que solicita bloqueos deben abrirse para la entrada y salida superpuestas (asincrónicas) mediante la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con la marca **FILE FLAG \_ \_ OVERLAPPED.** Después de abrir los archivos para la operación superpuesta, puede usar la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con uno de los siguientes códigos de control para trabajar con los bloqueos oportunistas de esos archivos:

<dl>

[**FSCTL \_ OPBATCH \_ ACK \_ CLOSE \_ PENDING**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[**FSCTL \_ OPLOCK \_ BREAK \_ ACK NO \_ \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[**CONFIRMACIÓN DE \_ INTERRUPCIÓN DEL BLOQUEO DE OPERACIÓN \_ DE FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[**NOTIFICACIÓN DE \_ INTERRUPCIÓN DEL BLOQUEO \_ DE OPERACIÓN \_ DE FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[**FSCTL \_ REQUEST \_ BATCH \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[**FSCTL \_ REQUEST \_ FILTER \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[**FSCTL \_ REQUEST \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[**FSCTL \_ REQUEST \_ OPLOCK LEVEL \_ \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[**FSCTL \_ REQUEST \_ OPLOCK LEVEL \_ \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

 

 

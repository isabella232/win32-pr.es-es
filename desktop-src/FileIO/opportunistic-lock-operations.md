---
description: Si una aplicación solicita bloqueos oportunistas, todos los archivos para los que solicita bloqueos deben abrirse para la entrada y salida superpuestas (asincrónicas) mediante la función CreateFile con la marca de la marca de archivo \_ \_ superpuesta.
ms.assetid: 1595c03e-9f6d-456c-8164-fafba06bbd79
title: Operaciones de bloqueo oportunista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefd9b292747e89f5ebafd94cb8aa0e38833e8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545542"
---
# <a name="opportunistic-lock-operations"></a>Operaciones de bloqueo oportunista

Si una aplicación solicita bloqueos oportunistas, todos los archivos para los que solicita bloqueos deben abrirse para la entrada y salida superpuestas (asincrónicas) mediante la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con la marca de la **marca de archivo \_ \_ superpuesta** . Una vez abiertos los archivos para la operación superpuesta, puede usar la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con uno de los siguientes códigos de control para trabajar con los bloqueos oportunistas de los archivos:

<dl>

[**el \_ cierre de ACK OPBATCH de FSCTL está \_ \_ \_ pendiente**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[**\_Confirmación de interrupción de bloqueo oportunista \_ \_ \_ no \_ 2 de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[**\_confirmación de interrupción de bloqueo oportunista de FSCTL \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[**\_notificación de interrupción de bloqueo oportunista de FSCTL \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[**\_ \_ bloqueo oportunista de batch de solicitud de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[**\_ \_ bloqueo oportunista de filtro de solicitud de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[**\_bloqueo oportunista de solicitud de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[**\_ \_ \_ Nivel 1 de bloqueo oportunista de solicitud de FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[**\_Nivel 2 de solicitud de \_ bloqueo oportunista de \_ FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

 

 

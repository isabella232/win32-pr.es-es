---
title: Estructuras y uniones de BITS
description: Las Servicio de transferencia inteligente en segundo plano (BITS) usan las estructuras siguientes.
ms.assetid: a1b8b4a1-77d6-46ac-96d5-6a0c99cfc643
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 199d5648ba8205d0417304350a104b2e16a607e4d7f1bdce4dfe9ecec34f98dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702035"
---
# <a name="bits-structures-and-unions"></a>Estructuras y uniones de BITS

Las Servicio de transferencia inteligente en segundo plano (BITS) [usan](bits-interfaces.md) las estructuras siguientes.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**BG_AUTH_CREDENTIALS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials) | Identifica el destino (proxy o servidor), el esquema de autenticación y las credenciales del usuario que se usarán para las solicitudes de autenticación de usuario. La estructura se pasa al [método IBackgroundCopyJob2::SetCredentials](/windows/win32/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials). |
| [**BG_AUTH_CREDENTIALS_UNION**](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials_union) | Identifica las credenciales que se usarán para el esquema de autenticación especificado en [la BG_AUTH_CREDENTIALS estructura](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials). |
| [**BG_BASIC_CREDENTIALS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_basic_credentials) | Identifica el nombre de usuario y la contraseña que se autenticarán. |
| [**BG_FILE_INFO**](/windows/win32/api/bits/ns-bits-bg_file_info) | Proporciona los nombres locales y remotos del archivo que se transferirá. |
| [**BG_FILE_PROGRESS**](/windows/win32/api/bits/ns-bits-bg_file_progress) | Proporciona información de progreso relacionada con el archivo, como el número de bytes transferidos. |
| [**BG_FILE_RANGE**](/windows/win32/api/bits2_0/ns-bits2_0-bg_file_range) | Identifica un intervalo de bytes que se van a descargar de un archivo. |
| [**BG_JOB_PROGRESS**](/windows/win32/api/bits/ns-bits-bg_job_progress) | Proporciona información de progreso relacionada con el trabajo, como el número de bytes y archivos transferidos. Para los trabajos de carga, el progreso se aplica al archivo de carga, no al archivo de respuesta. Para ver el progreso del archivo de respuesta, vea [la BG_JOB_REPLY_PROGRESS estructura](/windows/win32/api/bits1_5/ns-bits1_5-bg_job_reply_progress). |
| [**BG_JOB_REPLY_PROGRESS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_job_reply_progress) | Proporciona información de progreso relacionada con la parte de respuesta de un trabajo de carga y respuesta. |
| [**BG_JOB_TIMES**](/windows/win32/api/bits/ns-bits-bg_job_times) | Proporciona marcas de tiempo relacionadas con el trabajo. |
| [**BITS_FILE_PROPERTY_VALUE unión**](/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value) | Proporciona el valor de propiedad de un archivo BITS. |
| [**BITS_JOB_PROPERTY_VALUE**](/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value) | Proporciona el valor de propiedad del trabajo bits basado en el valor de la [enumeración BITS_JOB_PROPERTY_ID bits](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id). |

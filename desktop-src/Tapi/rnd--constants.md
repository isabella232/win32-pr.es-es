---
description: Las siguientes constantes se pueden devolver como errores.
ms.assetid: 185bd906-c276-4075-9c23-eb112da2a7ca
title: RND_ constantes (Rnderr.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ed1b55b0ed18215fb17e27504c309c67b0cea3351acea6cffadc4b3ff31c9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773375"
---
# <a name="rnd_-constants"></a>Constantes \_ de RND

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

Las siguientes constantes se pueden devolver como errores.

<dl> <dt>

<span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**HORA DE \_ RND NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

 0xe0000200
</dt> <dt>



El valor de hora especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**NOMBRE DE \_ SERVIDOR NULL \_ DE \_ RND**
</dt> <dd> <dl> <dt>

 0xe0000201
</dt> <dt>



El nombre del servidor **es NULL,** probablemente porque [**ITConferenceBlob::Init**](itconferenceblob-init.md) no se ha ejecutado o no se ha ejecutado correctamente.


</dt> </dl> </dd> <dt>

<span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**RND \_ YA \_ CONECTADO**
</dt> <dd> <dl> <dt>

 0xe0000202
</dt> <dt>



Se [**llamó al método ITDirectory::Conectar,**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) pero ya existe una conexión.


</dt> </dl> </dd> <dt>

<span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**RND \_ NO \_ CONECTADO**
</dt> <dd> <dl> <dt>

 0xe0000203
</dt> <dt>



El [**método ITDirectory::Conectar**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) no se ha llamado o no se ha podido.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                               |
| Header<br/>       | <dl> <dt>Rnderr.h</dt> </dl> |



 

 





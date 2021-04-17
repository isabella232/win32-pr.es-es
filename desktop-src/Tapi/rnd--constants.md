---
description: Las constantes siguientes pueden devolverse como errores.
ms.assetid: 185bd906-c276-4075-9c23-eb112da2a7ca
title: Constantes de RND_ (Rnderr. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a89b6747fb9fef775bbf40fac472081567ff1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690314"
---
# <a name="rnd_-constants"></a>RND ( \_ constantes)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

Las constantes siguientes pueden devolverse como errores.

<dl> <dt>

<span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**RND \_ hora no válida \_**
</dt> <dd> <dl> <dt>

 0xe0000200
</dt> <dt>



El valor de hora especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**RND \_ \_ nombre de servidor null \_**
</dt> <dd> <dl> <dt>

 0xe0000201
</dt> <dt>



El nombre del servidor es **null**, probablemente porque [**ITConferenceBlob:: init**](itconferenceblob-init.md) no se ha ejecutado o no se ha realizado correctamente.


</dt> </dl> </dd> <dt>

<span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**RND \_ ya está \_ conectado**
</dt> <dd> <dl> <dt>

 0xe0000202
</dt> <dt>



Se llamó al método [**ITDirectory:: Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) , pero ya existe una conexión.


</dt> </dl> </dd> <dt>

<span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**RND \_ no \_ conectado**
</dt> <dd> <dl> <dt>

 0xe0000203
</dt> <dt>



No se ha llamado al método [**ITDirectory:: Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) o se produjo un error.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                               |
| Encabezado<br/>       | <dl> <dt>Rnderr. h</dt> </dl> |



 

 





---
description: Define los valores que determinan cómo capturar la credencial de una cuenta de servicio administrada de grupo (gMSA).
ms.assetid: 90891448-22F6-497A-A612-3DAB8622C325
title: Enumeración CRED_FETCH (Secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRED_FETCH
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 6a7c30f29826b017bc7a3badd796955ec31a1ca7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002472"
---
# <a name="cred_fetch-enumeration"></a>Enumeración de recopilación de CREDENCIALes \_

Define los valores que determinan cómo capturar la credencial de una cuenta de servicio administrada de grupo (gMSA).

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _CRED_FETCH { 
  CredFetchDefault  = 0,
  CredFetchDPAPI    = 1,
  CredFetchForced   = 2
} CRED_FETCH;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span>**CredFetchDefault**
</dt> <dd>

Significa que el sistema operativo debe intentar primero recuperar la contraseña de la caché local. Si es el momento de capturar la contraseña, el sistema operativo debe ponerse en contacto con un controlador de dominio para la contraseña. Si se produce un error, devuelva cualquier contraseña almacenada en caché con el valor de estado correcto.

</dd> <dt>

<span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span>**CredFetchDPAPI**
</dt> <dd>

Devuelve la credencial DPAPI local al autor de la llamada. Los [*proveedores de compatibilidad para seguridad*](/windows/desktop/SecGloss/s-gly) (SSP) no suelen requerir el uso de esta enumeración.

</dd> <dt>

<span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span>**CredFetchForced**
</dt> <dd>

Obliga al sistema operativo a intentar leer la contraseña del controlador de dominio. Durante el tiempo de sustitución de contraseña, la contraseña puede haber cambiado en el controlador de dominio y en otros hosts miembros, pero el host miembro gMSA reconoce la contraseña como todavía válida. Esto puede ocurrir debido a problemas de sesgo del reloj entre distintos controladores de dominio. Cuando se especifica este valor, el sistema operativo determina si puede haber un posible cambio de contraseña debido al sesgo del reloj y, en caso afirmativo, recupera la contraseña. De lo contrario, se devuelve la credencial almacenada en caché. Si no hay ninguna credencial almacenada en caché, el sistema operativo intenta obtener una del controlador de dominio.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Secpkg. h</dt> </dl> |



 


---
title: Estructura WMDMRIGHTS
description: La estructura WMDMRIGHTS describe los derechos de uso de contenido.
ms.assetid: 1be9167b-0d20-4a17-a42b-9696ada2b539
keywords:
- Estructura WMDMRIGHTS windows Media Administrador de dispositivos
- Puntero de estructura PWMDMRIGHTS ventanas Multimedia Administrador de dispositivos
topic_type:
- apiref
api_name:
- WMDMRIGHTS
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b54713add3bef1c51d18fea3f66ac4b3e2e8ff1a066bcd83781f0f522d5a4be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583988"
---
# <a name="wmdmrights-structure"></a>Estructura WMDMRIGHTS

La **estructura WMDMRIGHTS** describe los derechos de uso de contenido.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct __WMDMRIGHTS {
  UINT         cbSize;
  DWORD        dwContentType;
  DWORD        fuFlags;
  DWORD        fuRights;
  DWORD        dwAppSec;
  DWORD        dwPlaybackCount;
  WMDMDATETIME ExpirationDate;
} WMDMRIGHTS, *PWMDMRIGHTS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tamaño de la estructura, en bytes.

</dd> <dt>

**dwContentType**
</dt> <dd>

**DWORD que** contiene el tipo de contenido.

</dd> <dt>

**fuFlags**
</dt> <dd>

Campo de bits que especifica las opciones de derechos en uso para el contenido.



| Valor                        | Descripción                                  |
|------------------------------|----------------------------------------------|
| WMDM \_ RIGHTS \_ PLAYBACKCOUNT  | Número de veces que se puede reproducir el archivo. |
| FECHA DE \_ EXPIRACIÓN DE DERECHOS DE WMDM \_ | Fecha de expiración del archivo.                 |
| WMDM \_ RIGHTS \_ FREESERIALIDS  | Identificador de serie gratuito del archivo.          |
| Grupo \_ GROUPID DE DERECHOS DE WMDM \_  | Identificador del archivo.                      |
| DERECHOS WMDM \_ \_ DENOMINADOSERIALIDS | Identificador de serie con nombre del archivo.         |



 

</dd> <dt>

**fuRights**
</dt> <dd>

Campo de bits que contiene los bits de derechos del contenido.



| Valor                                     | Descripción                                   |
|-------------------------------------------|-----------------------------------------------|
| WMDM \_ RIGHTS PLAY EN \_ \_ \_ PC                | El contenido se puede reproducir en un equipo personal. |
| COPIA DE \_ DERECHOS \_ WMDM \_ EN UN DISPOSITIVO QUE NO ES \_ \_ \_ SDMI | El contenido se puede copiar en un dispositivo que no sea SDMI.   |
| COPIA DE DERECHOS DE WMDM \_ \_ EN \_ \_ CD                | El contenido se puede copiar en un CD.                |
| COPIA DE DERECHOS DE WMDM \_ \_ EN EL DISPOSITIVO \_ \_ \_ SDMI      | El contenido se puede copiar en un dispositivo SDMI.      |



 

</dd> <dt>

**dwAppSec**
</dt> <dd>

Matriz de bytes que especifica el nivel mínimo de seguridad de la aplicación.

</dd> <dt>

**dwPlaybackCount**
</dt> <dd>

**DWORD** que contiene el número de veces restantes que se puede representar el contenido.

</dd> <dt>

**ExpirationDate**
</dt> <dd>

[**Estructura WMDMDATETIME**](wmdmdatetime.md) que contiene la fecha y hora de expiración del contenido. Si la licencia no tiene fecha de expiración, el **miembro wYear** se establece en 0xFFFF y se omiten todos los demás miembros de **WMDMDATETIME.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMDSPStorage::GetRights**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getrights)
</dt> <dt>

[**IWMDMStorage::GetRights**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getrights)
</dt> <dt>

[**WMDMDATETIME**](wmdmdatetime.md)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 






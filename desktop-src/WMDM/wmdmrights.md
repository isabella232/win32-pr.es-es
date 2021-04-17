---
title: Estructura WMDMRIGHTS
description: La estructura WMDMRIGHTS describe los derechos de uso de contenido.
ms.assetid: 1be9167b-0d20-4a17-a42b-9696ada2b539
keywords:
- Estructura WMDMRIGHTS Administrador de dispositivos Windows Media
- Puntero de estructura PWMDMRIGHTS Administrador de dispositivos de Windows Media
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
ms.openlocfilehash: ff8bc3bcd61efc64d32daa3179b77a9aaa518d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698689"
---
# <a name="wmdmrights-structure"></a>Estructura WMDMRIGHTS

La estructura **WMDMRIGHTS** describe los derechos de uso de contenido.

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

**DWORD** que contiene el tipo de contenido.

</dd> <dt>

**fuFlags**
</dt> <dd>

Campo de bits que especifica las opciones de derechos que se usan para el contenido.



| Value                        | Descripción                                  |
|------------------------------|----------------------------------------------|
| derechos de WMDM \_ \_ PLAYBACKCOUNT  | Número de veces que se puede reproducir el archivo. |
| \_EXPIRATIONDATE Rights de WMDM \_ | Fecha de expiración del archivo.                 |
| derechos de WMDM \_ \_ FREESERIALIDS  | Identificador de serie libre del archivo.          |
| Grupo del GROUPID de \_ derechos de WMDM \_  | Identificador del archivo.                      |
| derechos de WMDM \_ \_ NAMEDSERIALIDS | Identificador de serie con nombre del archivo.         |



 

</dd> <dt>

**fuRights**
</dt> <dd>

Campo de bits que contiene los bits de derechos para el contenido.



| Value                                     | Descripción                                   |
|-------------------------------------------|-----------------------------------------------|
| \_ \_ juego de derechos \_ de WMDM en \_ PC                | El contenido se puede reproducir en un equipo personal. |
| \_ \_ copia de derechos \_ de WMDM en un \_ dispositivo que no es de \_ SDMI \_ | El contenido se puede copiar en un dispositivo que no es de SDMI.   |
| \_ \_ copia de derechos \_ de WMDM en \_ CD                | El contenido se puede copiar en un CD.                |
| \_ \_ copia de derechos \_ de WMDM en el \_ dispositivo de SDMI \_      | El contenido se puede copiar en un dispositivo de SDMI.      |



 

</dd> <dt>

**dwAppSec**
</dt> <dd>

Matriz de bytes que especifica el nivel mínimo de seguridad de la aplicación.

</dd> <dt>

**dwPlaybackCount**
</dt> <dd>

**DWORD** que contiene el número de veces que se puede representar el contenido.

</dd> <dt>

**ExpirationDate**
</dt> <dd>

Estructura [**WMDMDATETIME**](wmdmdatetime.md) que contiene la fecha y hora de expiración del contenido. Si la licencia no tiene fecha de expiración, el miembro **wYear** se establece en 0xFFFF y se omiten todos los demás miembros de **WMDMDATETIME** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMDSPStorage::GetRights**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getrights)
</dt> <dt>

[**IWMDMStorage::GetRights**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getrights)
</dt> <dt>

[**WMDMDATETIME**](wmdmdatetime.md)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 






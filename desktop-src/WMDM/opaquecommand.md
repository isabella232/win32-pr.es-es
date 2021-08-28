---
title: ESTRUCTURA OPAQUECOMMAND
description: La estructura OPAQUECOMMAND contiene datos para los comandos que se pasan a través de Windows Media Administrador de dispositivos a un dispositivo, pero que no están diseñados para ser actuados por Windows Media Administrador de dispositivos.
ms.assetid: 5b39cf07-2816-4615-a754-e3f0c57bf4ce
keywords:
- Estructura OPAQUECOMMAND windows Media Administrador de dispositivos
- estructura windows Media Administrador de dispositivos
topic_type:
- apiref
api_name:
- OPAQUECOMMAND
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76d3f0b94146262c480e7e510497111bf82f0c020001717cb0000ee4a88df440
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904015"
---
# <a name="opaquecommand-structure"></a>ESTRUCTURA OPAQUECOMMAND

La **estructura OPAQUECOMMAND** contiene datos para los comandos que se pasan a través de Windows Media Administrador de dispositivos a un dispositivo, pero que no están diseñados para ser actuados por Windows Media Administrador de dispositivos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct OPAQUECOMMAND {
  GUID  guidCommand;
  DWORD dwDataLen;
  BYTE  *pData;
  BYTE  abMAC[20];
} ;
```



## <a name="members"></a>Miembros

<dl> <dt>

**guidCommand**
</dt> <dd>

**GUID que** representa el comando solicitado.

</dd> <dt>

**dwDataLen**
</dt> <dd>

Longitud de los datos a los que *apunta pData,* en bytes.

</dd> <dt>

**pData**
</dt> <dd>

Datos necesarios para ejecutar el comando o datos devueltos por el comando.

</dd> <dt>

**abMAC \[ 20\]**
</dt> <dd>

Este código de autenticación de mensajes (MAC) debe incluir el miembro **guidCommand,** los datos a los que *apunta pdwDataLen* y los datos a los que *apunta pData,* si los hay. Si *pData* **es NULL,** no debe incluirse en el equipo MAC. WMDM \_ MAC LENGTH se define como \_ 20.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMDSPDevice::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-sendopaquecommand)
</dt> <dt>

[**IMDSPStorage::SendOpaqueCommands**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-sendopaquecommand)
</dt> <dt>

[**IWMDMDevice::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-sendopaquecommand)
</dt> <dt>

[**IWMDMStorage::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 






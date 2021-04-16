---
title: Estructura OPAQUECOMMAND
description: La estructura OPAQUECOMMAND contiene los datos de los comandos que se pasan a través de Windows Media Administrador de dispositivos a un dispositivo, pero que no están diseñados para ser actuados por Windows Media Administrador de dispositivos.
ms.assetid: 5b39cf07-2816-4615-a754-e3f0c57bf4ce
keywords:
- Estructura OPAQUECOMMAND Administrador de dispositivos Windows Media
- estructura Administrador de dispositivos Windows Media
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
ms.openlocfilehash: 672147cb99336f95a1ced88a3cc6b8df977aec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699732"
---
# <a name="opaquecommand-structure"></a>Estructura OPAQUECOMMAND

La estructura **OPAQUECOMMAND** contiene los datos de los comandos que se pasan a través de windows media administrador de dispositivos a un dispositivo, pero que no están diseñados para ser actuados por windows media administrador de dispositivos.

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

**GUID** que representa el comando solicitado.

</dd> <dt>

**dwDataLen**
</dt> <dd>

Longitud de los datos a los que se redirige *pdata* , en bytes.

</dd> <dt>

**pData**
</dt> <dd>

Datos necesarios para ejecutar el comando o los datos devueltos por el comando.

</dd> <dt>

**abMAC \[ 20\]**
</dt> <dd>

Este código de autenticación de mensajes (MAC) debe incluir el miembro **guidCommand** , los datos a los que apunta *pdwDataLen* y los datos a los que se señala *pdata* , si los hay. Si *pdata* es **null**, no se debe incluir en el equipo Mac. La \_ \_ longitud de Mac de WMDM se define como 20.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



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

 

 






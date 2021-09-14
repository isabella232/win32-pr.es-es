---
title: Estructura OPAQUECOMMAND
description: La estructura OPAQUECOMMAND contiene datos para los comandos que se pasan a través de Windows Media Administrador de dispositivos a un dispositivo, pero que no están diseñados para que actúen Windows media Administrador de dispositivos.
ms.assetid: 5b39cf07-2816-4615-a754-e3f0c57bf4ce
keywords:
- Estructura OPAQUECOMMAND windows Media Administrador de dispositivos
- ventanas de estructura Ventanas multimedia Administrador de dispositivos
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967811"
---
# <a name="opaquecommand-structure"></a>Estructura OPAQUECOMMAND

La **estructura OPAQUECOMMAND** contiene datos para los comandos que se pasan a través de Windows Media Administrador de dispositivos a un dispositivo, pero que no están diseñados para que intervendrán Windows Media Administrador de dispositivos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct OPAQUECOMMAND {
  GUID  guidCommand;
  DWORD dwDataLen;
  BYTE  *pData;
  BYTE  abMAC[20];
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**guidCommand**
</dt> <dd>

**GUID** que representa el comando solicitado.

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

Este código de autenticación de mensajes (MAC) debe incluir el miembro **guidCommand,** los datos a los que *apunta pdwDataLen* y los datos a los que *apunta pData,* si los hay. Si *pData* es **NULL,** no debe incluirse en el EQUIPO MAC. WMDM \_ MAC LENGTH se define como \_ 20.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

 






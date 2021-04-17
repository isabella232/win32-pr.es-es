---
description: 'Contiene la respuesta a una llamada al método IDirect3DAuthenticatedChannel9:: configure.'
ms.assetid: 6f33d3f7-a883-4aca-a058-b656d745f2b1
title: D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6c7a029bd73069795b83b0b2a330835782192683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360106"
---
# <a name="d3dauthenticatedchannel_configure_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ configurar la \_ estructura de salida

Contiene la respuesta a una llamada al método [**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
  HRESULT  ReturnCode;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**omac**
</dt> <dd>

Una estructura [**D3D \_ OMAC**](d3d-omac.md) que contiene un código de autentificación de mensajes (Mac) (Mac) de los datos. El controlador utiliza una clave CBC MAC (OMAC) basada en AES para calcular este valor para el bloque de datos que aparece después de este miembro de estructura.

</dd> <dt>

**ConfigureType**
</dt> <dd>

GUID que especifica el comando. Para obtener una lista de valores, vea [comandos Content Protection](content-protection-commands.md).

</dd> <dt>

**hChannel**
</dt> <dd>

Identificador del canal autenticado.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Número de secuencia del comando.

</dd> <dt>

**ReturnCode**
</dt> <dd>

Código de resultado para el comando.

</dd> </dl>

## <a name="remarks"></a>Observaciones

En el caso de los miembros **ConfigureType**, **hChannel** y **SequenceNumber** , el controlador usa los mismos valores que la aplicación proporcionada en D3DAUTHENTICATEDCHANNEL configurar la estructura de [**\_ \_ entrada**](d3dauthenticatedchannel-configure-input.md) . La aplicación debe comprobar que estos valores coinciden.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de vídeo de Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




